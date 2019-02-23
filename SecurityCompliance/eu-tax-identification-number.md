---
title: USt-ID-Nummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Steuernummer erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: f851cce4be70fd41c24a7876d97c452f0a738eda
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213825"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="63116-104">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-104">EU Tax Identification Number</span></span>

<span data-ttu-id="63116-p102">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie bei der Erkennung des vertraulichen Informationstyps "TIN" (EU Tax Identification Number) sucht. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="63116-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="63116-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="63116-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="63116-108">Format</span><span class="sxs-lookup"><span data-stu-id="63116-108">Format</span></span>

<span data-ttu-id="63116-109">Neun Ziffern mit optionalem Bindestrich und Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="63116-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-110">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-110">Pattern</span></span>

<span data-ttu-id="63116-111">Neun Ziffern mit optionalem Bindestrich und Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="63116-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="63116-112">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-112">Two digits</span></span> 
    
- <span data-ttu-id="63116-113">Ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="63116-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="63116-114">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-114">Three digits</span></span>
    
- <span data-ttu-id="63116-115">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="63116-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="63116-116">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-117">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-117">Checksum</span></span>

<span data-ttu-id="63116-118">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-119">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-119">Definition</span></span>

<span data-ttu-id="63116-120">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-121">Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-122">Ein Schlüsselwort `Keywords_austria_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-123">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-124">Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-125">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="63116-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="63116-127">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-127">tax number</span></span>
  
<span data-ttu-id="63116-128">Anzahl</span><span class="sxs-lookup"><span data-stu-id="63116-128">number</span></span>
  
<span data-ttu-id="63116-129">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-129">tax registration number</span></span>
  
<span data-ttu-id="63116-130">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-130">tax id</span></span>
  
<span data-ttu-id="63116-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-131">st.nr.</span></span>
  
<span data-ttu-id="63116-132">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="63116-133">Belgien</span><span class="sxs-lookup"><span data-stu-id="63116-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="63116-134">Format</span><span class="sxs-lookup"><span data-stu-id="63116-134">Format</span></span>

<span data-ttu-id="63116-135">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-136">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-136">Pattern</span></span>

<span data-ttu-id="63116-137">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="63116-137">11 digits:</span></span>
  
- <span data-ttu-id="63116-138">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-138">Two digits</span></span>
    
- <span data-ttu-id="63116-139">"0" oder "1"</span><span class="sxs-lookup"><span data-stu-id="63116-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="63116-140">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="63116-140">One digit</span></span>
    
- <span data-ttu-id="63116-141">"0" oder "1" oder "2" oder "3"</span><span class="sxs-lookup"><span data-stu-id="63116-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="63116-142">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-143">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-143">Checksum</span></span>

<span data-ttu-id="63116-144">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="63116-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-145">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-145">Definition</span></span>

<span data-ttu-id="63116-146">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-147">Der reguläre Ausdruck `Regex_belgium_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-148">Ein Schlüsselwort `Keywords_belgium_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="63116-149">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="63116-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="63116-151">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-151">tax number</span></span>
  
<span data-ttu-id="63116-152">nationale Registrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="63116-152">national registration number</span></span>
  
<span data-ttu-id="63116-153">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-153">tax registration number</span></span>
  
<span data-ttu-id="63116-154">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-154">tax id</span></span>
  
<span data-ttu-id="63116-155">NIF</span><span class="sxs-lookup"><span data-stu-id="63116-155">nif</span></span>
  
<span data-ttu-id="63116-156">NIF</span><span class="sxs-lookup"><span data-stu-id="63116-156">nif#</span></span>
  
<span data-ttu-id="63116-157">Numéro de Registre National</span><span class="sxs-lookup"><span data-stu-id="63116-157">numéro de registre national</span></span>
  
<span data-ttu-id="63116-158">Numéro d'identification Fiscale</span><span class="sxs-lookup"><span data-stu-id="63116-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="63116-159">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="63116-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="63116-160">Format</span><span class="sxs-lookup"><span data-stu-id="63116-160">Format</span></span>

<span data-ttu-id="63116-161">Zehn Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-162">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-162">Pattern</span></span>

<span data-ttu-id="63116-163">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="63116-164">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-164">Checksum</span></span>

<span data-ttu-id="63116-165">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-166">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-166">Definition</span></span>

<span data-ttu-id="63116-167">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-168">Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-169">Ein Schlüsselwort `Keywords_bulgaria_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-170">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-171">Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-172">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="63116-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="63116-174">BUCN</span><span class="sxs-lookup"><span data-stu-id="63116-174">bucn</span></span>
  
<span data-ttu-id="63116-175">einheitliche Zivil Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-175">uniform civil number</span></span>
  
<span data-ttu-id="63116-176">BUCN</span><span class="sxs-lookup"><span data-stu-id="63116-176">bucn#</span></span>
  
<span data-ttu-id="63116-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="63116-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="63116-178">einheitliche Civil ID</span><span class="sxs-lookup"><span data-stu-id="63116-178">uniform civil id</span></span>
  
<span data-ttu-id="63116-179">einheitliches ziviles Nein</span><span class="sxs-lookup"><span data-stu-id="63116-179">uniform civil no</span></span>
  
<span data-ttu-id="63116-180">EGN</span><span class="sxs-lookup"><span data-stu-id="63116-180">egn</span></span>
  
<span data-ttu-id="63116-181">Bulgarische einheitliche Zivil Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="63116-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="63116-182">uniformcivilno#</span></span>
  
<span data-ttu-id="63116-183">EGN</span><span class="sxs-lookup"><span data-stu-id="63116-183">egn#</span></span>
  
<span data-ttu-id="63116-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="63116-184">униформ граждански номер</span></span>
  
<span data-ttu-id="63116-185">униформ-ID</span><span class="sxs-lookup"><span data-stu-id="63116-185">униформ id</span></span>
  
<span data-ttu-id="63116-186">униформ-граждански-ID</span><span class="sxs-lookup"><span data-stu-id="63116-186">униформ граждански id</span></span>
  
<span data-ttu-id="63116-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="63116-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="63116-188">Kroatien</span><span class="sxs-lookup"><span data-stu-id="63116-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="63116-189">Format</span><span class="sxs-lookup"><span data-stu-id="63116-189">Format</span></span>

<span data-ttu-id="63116-190">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-191">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-191">Pattern</span></span>

<span data-ttu-id="63116-192">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="63116-192">11 digits:</span></span>
  
- <span data-ttu-id="63116-193">Zehn Ziffern, zufällig gewählt</span><span class="sxs-lookup"><span data-stu-id="63116-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="63116-194">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="63116-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-195">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-195">Checksum</span></span>

<span data-ttu-id="63116-196">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-197">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-197">Definition</span></span>

<span data-ttu-id="63116-198">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-199">Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-200">Ein Schlüsselwort `Keywords_croatia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-201">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-202">Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-203">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="63116-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="63116-205">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-205">tax number</span></span>
  
<span data-ttu-id="63116-206">Steuer</span><span class="sxs-lookup"><span data-stu-id="63116-206">tax</span></span>
  
<span data-ttu-id="63116-207">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-207">tax id</span></span>
  
<span data-ttu-id="63116-208">OID</span><span class="sxs-lookup"><span data-stu-id="63116-208">oid</span></span>
  
<span data-ttu-id="63116-209">OID</span><span class="sxs-lookup"><span data-stu-id="63116-209">oid#</span></span>
  
<span data-ttu-id="63116-210">porezni Broj</span><span class="sxs-lookup"><span data-stu-id="63116-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="63116-211">Zypern</span><span class="sxs-lookup"><span data-stu-id="63116-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="63116-212">Format</span><span class="sxs-lookup"><span data-stu-id="63116-212">Format</span></span>

<span data-ttu-id="63116-213">Acht Ziffern und ein Buchstabe im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="63116-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-214">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-214">Pattern</span></span>

<span data-ttu-id="63116-215">Acht Ziffern und ein Buchstabe:</span><span class="sxs-lookup"><span data-stu-id="63116-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="63116-216">Ein "0"</span><span class="sxs-lookup"><span data-stu-id="63116-216">A "0"</span></span> 
    
- <span data-ttu-id="63116-217">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="63116-217">Seven digits</span></span>
    
- <span data-ttu-id="63116-218">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="63116-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-219">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-219">Checksum</span></span>

<span data-ttu-id="63116-220">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="63116-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-221">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-221">Definition</span></span>

<span data-ttu-id="63116-222">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-223">Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-224">Ein Schlüsselwort `Keywords_cyprus_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-225">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-226">Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-227">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="63116-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="63116-229">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-229">tax number</span></span>
  
<span data-ttu-id="63116-230">Steuer</span><span class="sxs-lookup"><span data-stu-id="63116-230">tax</span></span>
  
<span data-ttu-id="63116-231">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-231">tax id</span></span>
  
<span data-ttu-id="63116-232">USt-ID-Code</span><span class="sxs-lookup"><span data-stu-id="63116-232">tax identification code</span></span>
  
<span data-ttu-id="63116-233">TIC</span><span class="sxs-lookup"><span data-stu-id="63116-233">tic</span></span>
  
<span data-ttu-id="63116-234">TIC</span><span class="sxs-lookup"><span data-stu-id="63116-234">tic#</span></span>
  
<span data-ttu-id="63116-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="63116-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="63116-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="63116-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="63116-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="63116-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="63116-238">Tschechien</span><span class="sxs-lookup"><span data-stu-id="63116-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="63116-239">Format</span><span class="sxs-lookup"><span data-stu-id="63116-239">Format</span></span>

<span data-ttu-id="63116-240">Neun oder zehn Ziffern mit optionalem Backslash</span><span class="sxs-lookup"><span data-stu-id="63116-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-241">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-241">Pattern</span></span>

<span data-ttu-id="63116-242">Neun oder zehn Ziffern mit einem optionalen umgekehrten Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="63116-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="63116-243">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-243">Six digits</span></span> 
    
- <span data-ttu-id="63116-244">Ein umgekehrter Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="63116-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="63116-245">Drei oder vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-246">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-246">Checksum</span></span>

<span data-ttu-id="63116-247">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="63116-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-248">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-248">Definition</span></span>

<span data-ttu-id="63116-249">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-250">Der reguläre Ausdruck `Regex_czech_republic_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-251">Ein Schlüsselwort `Keywords_czech_republic_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="63116-252">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="63116-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="63116-254">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-254">tax number</span></span>
  
<span data-ttu-id="63116-255">Steuer</span><span class="sxs-lookup"><span data-stu-id="63116-255">tax</span></span>
  
<span data-ttu-id="63116-256">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-256">tax id</span></span>
  
<span data-ttu-id="63116-257">persönliche Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-257">personal number</span></span>
  
<span data-ttu-id="63116-258">Daňové číslo</span><span class="sxs-lookup"><span data-stu-id="63116-258">daňové číslo</span></span>
  
<span data-ttu-id="63116-259">Osobní číslo</span><span class="sxs-lookup"><span data-stu-id="63116-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="63116-260">Dänemark</span><span class="sxs-lookup"><span data-stu-id="63116-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="63116-261">Format</span><span class="sxs-lookup"><span data-stu-id="63116-261">Format</span></span>

<span data-ttu-id="63116-262">Zehn Ziffern mit einem Bindestrich</span><span class="sxs-lookup"><span data-stu-id="63116-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-263">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-263">Pattern</span></span>

<span data-ttu-id="63116-264">Zehn Ziffern, die einen Bindestrich enthalten:</span><span class="sxs-lookup"><span data-stu-id="63116-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="63116-265">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="63116-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="63116-266">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="63116-266">A hyphen</span></span>
    
- <span data-ttu-id="63116-267">Vier Ziffern, die einer Sequenznummer entsprechen, wobei die erste Ziffer dem Jahrhundert der Geburt entspricht und die letzte Ziffer dem Geschlecht des einzelnen entspricht (ungerade für männlich und sogar für weiblich)</span><span class="sxs-lookup"><span data-stu-id="63116-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-268">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-268">Checksum</span></span>

<span data-ttu-id="63116-269">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-270">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-270">Definition</span></span>

<span data-ttu-id="63116-271">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-272">Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-273">Ein Schlüsselwort `Keywords_denmark_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-274">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-275">Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-276">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="63116-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="63116-278">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-278">tax number</span></span>
  
<span data-ttu-id="63116-279">Steuer</span><span class="sxs-lookup"><span data-stu-id="63116-279">tax</span></span>
  
<span data-ttu-id="63116-280">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-280">tax id</span></span>
  
<span data-ttu-id="63116-281">CPR-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-281">cpr number</span></span>
  
<span data-ttu-id="63116-282">CPR</span><span class="sxs-lookup"><span data-stu-id="63116-282">cpr#</span></span>
  
<span data-ttu-id="63116-283">Skate Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-283">skat nummer</span></span>
  
<span data-ttu-id="63116-284">Skat-ID</span><span class="sxs-lookup"><span data-stu-id="63116-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="63116-285">Estland</span><span class="sxs-lookup"><span data-stu-id="63116-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="63116-286">Format</span><span class="sxs-lookup"><span data-stu-id="63116-286">Format</span></span>

<span data-ttu-id="63116-287">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-288">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-288">Pattern</span></span>

<span data-ttu-id="63116-289">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="63116-289">11 digits:</span></span>
  
-  <span data-ttu-id="63116-290">Eine Ziffer, die dem Geschlecht und dem Jahrhundert der Geburt entspricht, wobei eine ungerade Zahl männliche und die gerade Zahl angibt, wie folgt: 1,2 für das 19. Jahrhundert; 3, 4 für das 20. Jahrhundert; und 5, 6 für das 21. Jahrhundert</span><span class="sxs-lookup"><span data-stu-id="63116-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="63116-291">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="63116-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="63116-292">Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am selben Datum geboren wurden</span><span class="sxs-lookup"><span data-stu-id="63116-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="63116-293">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="63116-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-294">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-294">Checksum</span></span>

<span data-ttu-id="63116-295">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-296">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-296">Definition</span></span>

<span data-ttu-id="63116-297">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-298">Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-299">Ein Schlüsselwort `Keywords_estonia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-300">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-301">Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-302">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="63116-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="63116-304">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-304">tax number</span></span>
  
<span data-ttu-id="63116-305">Steuer</span><span class="sxs-lookup"><span data-stu-id="63116-305">tax</span></span>
  
<span data-ttu-id="63116-306">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-306">tax id</span></span>
  
<span data-ttu-id="63116-307">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="63116-307">personal code</span></span>
  
<span data-ttu-id="63116-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="63116-308">maksunumber</span></span>
  
<span data-ttu-id="63116-309">maksu-ID</span><span class="sxs-lookup"><span data-stu-id="63116-309">maksu id</span></span>
  
<span data-ttu-id="63116-310">Isikukood</span><span class="sxs-lookup"><span data-stu-id="63116-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="63116-311">Finnland</span><span class="sxs-lookup"><span data-stu-id="63116-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="63116-312">Format</span><span class="sxs-lookup"><span data-stu-id="63116-312">Format</span></span>

<span data-ttu-id="63116-313">Eine 11-stellige Kombination aus Ziffern, Buchstaben und Plus-und Minuszeichen</span><span class="sxs-lookup"><span data-stu-id="63116-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-314">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-314">Pattern</span></span>

<span data-ttu-id="63116-315">Eine 11-stellige Kombination aus Ziffern, Buchstaben und Plus-und Minuszeichen:</span><span class="sxs-lookup"><span data-stu-id="63116-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="63116-316">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-316">Six digits</span></span>
    
- <span data-ttu-id="63116-317">Eine der folgenden Optionen: ein Pluszeichen, ein Minuszeichen oder der Buchstabe "A" (ohne Beachtung der Groß-/Kleinschreibung), wobei das Pluszeichen zwischen 1800-1899, das Minuszeichen zwischen 1900-1999 und "A" als geboren 2000 und nach</span><span class="sxs-lookup"><span data-stu-id="63116-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="63116-318">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-318">Three digits</span></span>
    
- <span data-ttu-id="63116-319">Ein Buchstaben oder eine Zahl</span><span class="sxs-lookup"><span data-stu-id="63116-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-320">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-320">Checksum</span></span>

<span data-ttu-id="63116-321">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-322">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-322">Definition</span></span>

<span data-ttu-id="63116-323">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-324">Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-325">Ein Schlüsselwort `Keywords_finland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-326">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-327">Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-328">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="63116-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="63116-330">identification number
</span><span class="sxs-lookup"><span data-stu-id="63116-330">identification number</span></span>
  
<span data-ttu-id="63116-331">persönliche ID</span><span class="sxs-lookup"><span data-stu-id="63116-331">personal id</span></span>
  
<span data-ttu-id="63116-332">Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="63116-332">identity number</span></span>
  
<span data-ttu-id="63116-333">nationale finnische ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-333">finnish national id number</span></span>
  
<span data-ttu-id="63116-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="63116-334">personalidnumber#</span></span>
  
<span data-ttu-id="63116-335">nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="63116-335">national identification number</span></span>
  
<span data-ttu-id="63116-336">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-336">id number</span></span>
  
<span data-ttu-id="63116-337">nationale ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-337">national id no.</span></span>
  
<span data-ttu-id="63116-338">nationale ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-338">national id number</span></span>
  
<span data-ttu-id="63116-339">ID Nein</span><span class="sxs-lookup"><span data-stu-id="63116-339">id no</span></span>
  
<span data-ttu-id="63116-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="63116-340">tunnistenumero</span></span>
  
<span data-ttu-id="63116-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="63116-341">henkilötunnus</span></span>
  
<span data-ttu-id="63116-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="63116-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="63116-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="63116-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="63116-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="63116-344">identiteetti numero</span></span>
  
<span data-ttu-id="63116-345">Suomen der Kok henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="63116-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="63116-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="63116-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="63116-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="63116-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="63116-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="63116-348">tunnusnumero</span></span>
  
<span data-ttu-id="63116-349">der Kok tunnus numero</span><span class="sxs-lookup"><span data-stu-id="63116-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="63116-350">Frankreich</span><span class="sxs-lookup"><span data-stu-id="63116-350">France</span></span>

### <a name="format"></a><span data-ttu-id="63116-351">Format</span><span class="sxs-lookup"><span data-stu-id="63116-351">Format</span></span>

<span data-ttu-id="63116-352">13 Ziffern für Einzelpersonen und neun Ziffern für Entitäten</span><span class="sxs-lookup"><span data-stu-id="63116-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-353">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-353">Pattern</span></span>

<span data-ttu-id="63116-354">13 Ziffern für Einzelpersonen:</span><span class="sxs-lookup"><span data-stu-id="63116-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="63116-355">Eine Ziffer, die 0, 1, 2 oder 3 sein muss</span><span class="sxs-lookup"><span data-stu-id="63116-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="63116-356">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-356">12 digits</span></span>
    
<span data-ttu-id="63116-357">Neun Ziffern für Entitäten</span><span class="sxs-lookup"><span data-stu-id="63116-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="63116-358">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-358">Checksum</span></span>

<span data-ttu-id="63116-359">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="63116-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-360">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-360">Definition</span></span>

<span data-ttu-id="63116-361">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-362">Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-363">Ein Schlüsselwort `Keywords_france_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-364">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-365">Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-366">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="63116-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="63116-368">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-368">tax identification number</span></span>
  
<span data-ttu-id="63116-369">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-369">tax number</span></span>
  
<span data-ttu-id="63116-370">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-370">tax id</span></span>
  
<span data-ttu-id="63116-371">Numéro d'identification Fiscale</span><span class="sxs-lookup"><span data-stu-id="63116-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="63116-372">Deutschland</span><span class="sxs-lookup"><span data-stu-id="63116-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="63116-373">Format</span><span class="sxs-lookup"><span data-stu-id="63116-373">Format</span></span>

<span data-ttu-id="63116-374">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-375">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-375">Pattern</span></span>

<span data-ttu-id="63116-376">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="63116-376">11 digits :</span></span>
  
-  <span data-ttu-id="63116-377">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-377">Ten digits</span></span> 
    
- <span data-ttu-id="63116-378">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="63116-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-379">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-379">Checksum</span></span>

<span data-ttu-id="63116-380">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-381">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-381">Definition</span></span>

<span data-ttu-id="63116-382">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-383">Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-384">Ein Schlüsselwort `Keywords_germany_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-385">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-386">Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-387">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="63116-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="63116-389">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-389">tax number</span></span>
  
<span data-ttu-id="63116-390">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-390">tax no.</span></span>
  
<span data-ttu-id="63116-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="63116-391">taxno#</span></span>
  
<span data-ttu-id="63116-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="63116-392">taxnumber#</span></span>
  
<span data-ttu-id="63116-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="63116-393">taxnumber</span></span>
  
<span data-ttu-id="63116-394">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-394">tax id</span></span>
  
<span data-ttu-id="63116-395">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-395">taxid#</span></span>
  
<span data-ttu-id="63116-396">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-396">tax identification number</span></span>
  
<span data-ttu-id="63116-397">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-397">tax identification no.</span></span>
  
<span data-ttu-id="63116-398">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-398">steuernummer</span></span>
  
<span data-ttu-id="63116-399">Ingo-ID</span><span class="sxs-lookup"><span data-stu-id="63116-399">steuer id</span></span>
  
<span data-ttu-id="63116-400">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="63116-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="63116-401">Griechenland</span><span class="sxs-lookup"><span data-stu-id="63116-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="63116-402">Format</span><span class="sxs-lookup"><span data-stu-id="63116-402">Format</span></span>

<span data-ttu-id="63116-403">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-404">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-404">Pattern</span></span>

<span data-ttu-id="63116-405">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="63116-406">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-406">Checksum</span></span>

<span data-ttu-id="63116-407">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="63116-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-408">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-408">Definition</span></span>

<span data-ttu-id="63116-409">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-410">Der reguläre Ausdruck `Regex_greece_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-411">Ein Schlüsselwort `Keywords_greece_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="63116-412">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="63116-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="63116-414">AFM</span><span class="sxs-lookup"><span data-stu-id="63116-414">afm</span></span>
  
<span data-ttu-id="63116-415">tin
</span><span class="sxs-lookup"><span data-stu-id="63116-415">tin</span></span>
  
<span data-ttu-id="63116-416">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-416">tax id no.</span></span>
  
<span data-ttu-id="63116-417">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-417">tax id no</span></span>
  
<span data-ttu-id="63116-418">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-418">tax identification number</span></span>
  
<span data-ttu-id="63116-419">Steuerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="63116-419">tax registry number</span></span>
  
<span data-ttu-id="63116-420">Steuerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="63116-420">tax registry no.</span></span>
  
<span data-ttu-id="63116-421">AFM</span><span class="sxs-lookup"><span data-stu-id="63116-421">afm#</span></span>
  
<span data-ttu-id="63116-422">Zinn</span><span class="sxs-lookup"><span data-stu-id="63116-422">tin#</span></span>
  
<span data-ttu-id="63116-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="63116-423">taxidno#</span></span>
  
<span data-ttu-id="63116-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="63116-424">taxregistryno#</span></span>
  
<span data-ttu-id="63116-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="63116-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="63116-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="63116-426">aφμ</span></span>
  
<span data-ttu-id="63116-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="63116-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="63116-428">φορολογικού μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="63116-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="63116-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="63116-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="63116-430">Ungarn</span><span class="sxs-lookup"><span data-stu-id="63116-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="63116-431">Format</span><span class="sxs-lookup"><span data-stu-id="63116-431">Format</span></span>

<span data-ttu-id="63116-432">Zehn Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-433">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-433">Pattern</span></span>

<span data-ttu-id="63116-434">Zehn Ziffern:</span><span class="sxs-lookup"><span data-stu-id="63116-434">Ten digits:</span></span>
  
-  <span data-ttu-id="63116-435">Eine Ziffer, die "8" sein muss</span><span class="sxs-lookup"><span data-stu-id="63116-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="63116-436">Fünf Ziffern, die der Anzahl von Tagen zwischen dem Datum 01/01/1867 und dem Geburtsdatum des einzelnen entsprechen</span><span class="sxs-lookup"><span data-stu-id="63116-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="63116-437">Drei Ziffern, die der Zahl entsprechen, die von Wahrscheinlichkeit zur Unterscheidung von Individuen generiert wurde, die am selben Tag geboren wurden</span><span class="sxs-lookup"><span data-stu-id="63116-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="63116-438">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="63116-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-439">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-439">Checksum</span></span>

<span data-ttu-id="63116-440">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-441">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-441">Definition</span></span>

<span data-ttu-id="63116-442">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-443">Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-444">Ein Schlüsselwort `Keywords_hungary_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-445">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-446">Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-447">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="63116-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="63116-449">ungarische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="63116-450">ungarische Dose</span><span class="sxs-lookup"><span data-stu-id="63116-450">hungarian tin</span></span>
  
<span data-ttu-id="63116-451">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-451">tax id number</span></span>
  
<span data-ttu-id="63116-452">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="63116-452">vat number</span></span>
  
<span data-ttu-id="63116-453">Finanzamt Nein</span><span class="sxs-lookup"><span data-stu-id="63116-453">tax authority no</span></span>
  
<span data-ttu-id="63116-454">USt-ID-Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-454">tax id tax identity number</span></span>
  
<span data-ttu-id="63116-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="63116-455">taxidnumber#</span></span>
  
<span data-ttu-id="63116-456">Zinn</span><span class="sxs-lookup"><span data-stu-id="63116-456">tin#</span></span>
  
<span data-ttu-id="63116-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="63116-457">hungatiantin#</span></span>
  
<span data-ttu-id="63116-458">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-458">tax identification no</span></span>
  
<span data-ttu-id="63116-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="63116-459">taxidno#</span></span>
  
<span data-ttu-id="63116-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="63116-460">adóazonosító szám</span></span>
  
<span data-ttu-id="63116-461">adószám</span><span class="sxs-lookup"><span data-stu-id="63116-461">adószám</span></span>
  
<span data-ttu-id="63116-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="63116-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="63116-463">Irland</span><span class="sxs-lookup"><span data-stu-id="63116-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="63116-464">Format</span><span class="sxs-lookup"><span data-stu-id="63116-464">Format</span></span>

<span data-ttu-id="63116-465">Sieben Ziffern, gefolgt von einem Buchstaben ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="63116-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-466">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-466">Pattern</span></span>

<span data-ttu-id="63116-467">Sieben Ziffern gefolgt von einem Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="63116-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="63116-468">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="63116-468">Seven digits</span></span> 
    
- <span data-ttu-id="63116-469">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="63116-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-470">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-470">Checksum</span></span>

<span data-ttu-id="63116-471">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="63116-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-472">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-472">Definition</span></span>

<span data-ttu-id="63116-473">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-474">Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-475">Ein Schlüsselwort `Keywords_ireland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-476">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-477">Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-478">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="63116-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="63116-480">öffentlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="63116-480">public service no</span></span>
  
<span data-ttu-id="63116-481">persönlicher öffentlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="63116-481">personal public service no</span></span>
  
<span data-ttu-id="63116-482">PPS Nein</span><span class="sxs-lookup"><span data-stu-id="63116-482">pps no</span></span>
  
<span data-ttu-id="63116-483">persönlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="63116-483">personal service no</span></span>
  
<span data-ttu-id="63116-484">PPS-Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="63116-484">pps service no</span></span>
  
<span data-ttu-id="63116-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="63116-485">ppsno#</span></span>
  
<span data-ttu-id="63116-486">Irisch PPS Nein</span><span class="sxs-lookup"><span data-stu-id="63116-486">irish pps no</span></span>
  
<span data-ttu-id="63116-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="63116-487">publicserviceno#</span></span>
  
<span data-ttu-id="63116-488">persönliche öffentliche Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="63116-488">personal public service number</span></span>
  
<span data-ttu-id="63116-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="63116-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="63116-490">PPS-uimh</span><span class="sxs-lookup"><span data-stu-id="63116-490">pps uimh</span></span>
  
<span data-ttu-id="63116-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="63116-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="63116-492">Italien</span><span class="sxs-lookup"><span data-stu-id="63116-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="63116-493">Format</span><span class="sxs-lookup"><span data-stu-id="63116-493">Format</span></span>

<span data-ttu-id="63116-494">16 Buchstaben und Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="63116-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-495">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-495">Pattern</span></span>

<span data-ttu-id="63116-496">16 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="63116-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="63116-497">Drei Buchstaben, die den ersten drei Konsonanten im Familiennamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="63116-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="63116-498">Drei Buchstaben, die dem ersten, dritten und vierten Konsonanten im Vornamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="63116-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="63116-499">Zwei Ziffern, die den letzten Ziffern des Geburtsjahrs entsprechen</span><span class="sxs-lookup"><span data-stu-id="63116-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="63116-500">Eine Ziffer, die dem Geburtsmonat entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben A bis E, H, L, M, P, R bis T werden verwendet (also Januar ist A und Oktober ist R)</span><span class="sxs-lookup"><span data-stu-id="63116-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="63116-501">Zwei Ziffern, die dem Tag des Geburtsmonats entsprechen, wobei 40 zum Geburtstag hinzugefügt wird, damit Frauen von Männern unterschieden werden.</span><span class="sxs-lookup"><span data-stu-id="63116-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="63116-502">Vier Ziffern, die einer Ortskennzahl für die Gemeinde entsprechen, in der die Person geboren wurde – landesweite Codes werden für fremde Länder verwendet</span><span class="sxs-lookup"><span data-stu-id="63116-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="63116-503">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="63116-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-504">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-504">Checksum</span></span>

<span data-ttu-id="63116-505">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-506">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-506">Definition</span></span>

<span data-ttu-id="63116-507">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-508">Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-509">Ein Schlüsselwort `Keywords_italy_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-510">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-511">Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-512">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="63116-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="63116-514">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-514">tax number</span></span>
  
<span data-ttu-id="63116-515">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-515">tax no.</span></span>
  
<span data-ttu-id="63116-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="63116-516">taxno#</span></span>
  
<span data-ttu-id="63116-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="63116-517">taxnumber#</span></span>
  
<span data-ttu-id="63116-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="63116-518">taxnumber</span></span>
  
<span data-ttu-id="63116-519">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-519">tax id</span></span>
  
<span data-ttu-id="63116-520">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-520">taxid#</span></span>
  
<span data-ttu-id="63116-521">Fiskal Code</span><span class="sxs-lookup"><span data-stu-id="63116-521">fiscal code</span></span>
  
<span data-ttu-id="63116-522">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="63116-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="63116-523">Lettland</span><span class="sxs-lookup"><span data-stu-id="63116-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="63116-524">Format</span><span class="sxs-lookup"><span data-stu-id="63116-524">Format</span></span>

<span data-ttu-id="63116-525">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-526">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-526">Pattern</span></span>

<span data-ttu-id="63116-527">11 Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="63116-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="63116-528">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="63116-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="63116-529">Eine Ziffer, die dem Jahrhundert der Geburt entspricht, wobei "0" dem 19. Jahrhundert entspricht, "1" entspricht dem 20. Jahrhundert, und "2" entspricht dem 21. Jahrhundert</span><span class="sxs-lookup"><span data-stu-id="63116-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="63116-530">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-531">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-531">Checksum</span></span>

<span data-ttu-id="63116-532">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-533">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-533">Definition</span></span>

<span data-ttu-id="63116-534">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-535">Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-536">Ein Schlüsselwort `Keywords_latvia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-537">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-538">Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-539">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="63116-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="63116-541">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-541">tax number</span></span>
  
<span data-ttu-id="63116-542">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-542">tax no.</span></span>
  
<span data-ttu-id="63116-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="63116-543">taxno#</span></span>
  
<span data-ttu-id="63116-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="63116-544">taxnumber#</span></span>
  
<span data-ttu-id="63116-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="63116-545">taxnumber</span></span>
  
<span data-ttu-id="63116-546">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-546">tax id</span></span>
  
<span data-ttu-id="63116-547">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-547">taxid#</span></span>
  
<span data-ttu-id="63116-548">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-548">tax identification number</span></span>
  
<span data-ttu-id="63116-549">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-549">tax identification no.</span></span>
  
<span data-ttu-id="63116-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="63116-550">nodokļa numurs</span></span>
  
<span data-ttu-id="63116-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="63116-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="63116-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="63116-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="63116-553">Litauen</span><span class="sxs-lookup"><span data-stu-id="63116-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="63116-554">Format</span><span class="sxs-lookup"><span data-stu-id="63116-554">Format</span></span>

<span data-ttu-id="63116-555">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-556">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-556">Pattern</span></span>

<span data-ttu-id="63116-557">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="63116-558">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-558">Checksum</span></span>

<span data-ttu-id="63116-559">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="63116-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-560">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-560">Definition</span></span>

<span data-ttu-id="63116-561">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-562">Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-563">Ein Schlüsselwort `Keywords_lithuania_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-564">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-565">Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-566">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="63116-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="63116-568">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-568">tax number</span></span>
  
<span data-ttu-id="63116-569">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-569">tax no.</span></span>
  
<span data-ttu-id="63116-570">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-570">tax no#</span></span>
  
<span data-ttu-id="63116-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="63116-571">taxnumber#</span></span>
  
<span data-ttu-id="63116-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="63116-572">taxnumber</span></span>
  
<span data-ttu-id="63116-573">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-573">tax id</span></span>
  
<span data-ttu-id="63116-574">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-574">taxid#</span></span>
  
<span data-ttu-id="63116-575">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-575">tax identification number</span></span>
  
<span data-ttu-id="63116-576">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-576">tax identification no.</span></span>
  
<span data-ttu-id="63116-577">mokesčių-ID</span><span class="sxs-lookup"><span data-stu-id="63116-577">mokesčių id</span></span>
  
<span data-ttu-id="63116-578">mokesčių Numeris</span><span class="sxs-lookup"><span data-stu-id="63116-578">mokesčių numeris</span></span>
  
<span data-ttu-id="63116-579">mokesčių identifikavimas Numeris</span><span class="sxs-lookup"><span data-stu-id="63116-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="63116-580">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="63116-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="63116-581">Format</span><span class="sxs-lookup"><span data-stu-id="63116-581">Format</span></span>

<span data-ttu-id="63116-582">13 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-583">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-583">Pattern</span></span>

<span data-ttu-id="63116-584">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="63116-584">13 digits:</span></span>
  
-  <span data-ttu-id="63116-585">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-585">11 digits</span></span> 
    
- <span data-ttu-id="63116-586">Zwei Prüfziffern</span><span class="sxs-lookup"><span data-stu-id="63116-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-587">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-587">Checksum</span></span>

<span data-ttu-id="63116-588">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-589">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-589">Definition</span></span>

<span data-ttu-id="63116-590">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-591">Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-592">Ein Schlüsselwort `Keywords_luxemburg_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-593">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-594">Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-595">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="63116-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="63116-597">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-597">tax number</span></span>
  
<span data-ttu-id="63116-598">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-598">tax no.</span></span>
  
<span data-ttu-id="63116-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="63116-599">taxno#</span></span>
  
<span data-ttu-id="63116-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="63116-600">taxnumber#</span></span>
  
<span data-ttu-id="63116-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="63116-601">taxnumber</span></span>
  
<span data-ttu-id="63116-602">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-602">tax id</span></span>
  
<span data-ttu-id="63116-603">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-603">taxid#</span></span>
  
<span data-ttu-id="63116-604">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-604">tax identification number</span></span>
  
<span data-ttu-id="63116-605">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-605">tax identification no.</span></span>
  
<span data-ttu-id="63116-606">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-606">steuernummer</span></span>
  
<span data-ttu-id="63116-607">Ingo-ID</span><span class="sxs-lookup"><span data-stu-id="63116-607">steuer id</span></span>
  
<span data-ttu-id="63116-608">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="63116-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="63116-609">Malta</span><span class="sxs-lookup"><span data-stu-id="63116-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="63116-610">Format</span><span class="sxs-lookup"><span data-stu-id="63116-610">Format</span></span>

<span data-ttu-id="63116-611">Für maltesische Staatsangehörige: 7 Ziffern und ein Buchstabe im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="63116-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="63116-612">Nicht maltesische Staatsangehörige und maltesische Entitäten: 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-613">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-613">Pattern</span></span>

<span data-ttu-id="63116-614">Maltesische Staatsangehörige: 7 Ziffern und ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="63116-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="63116-615">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="63116-615">Seven digits</span></span> 
    
- <span data-ttu-id="63116-616">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="63116-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="63116-617">Nicht maltesische Staatsangehörige und maltesische Entitäten: 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="63116-618">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="63116-619">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-619">Checksum</span></span>

<span data-ttu-id="63116-620">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="63116-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-621">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-621">Definition</span></span>

<span data-ttu-id="63116-622">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-623">Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-624">Ein Schlüsselwort `Keywords_malta_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-625">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-626">Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-627">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="63116-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="63116-629">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-629">tax number</span></span>
  
<span data-ttu-id="63116-630">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-630">tax no.</span></span>
  
<span data-ttu-id="63116-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="63116-631">taxno#</span></span>
  
<span data-ttu-id="63116-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="63116-632">taxnumber#</span></span>
  
<span data-ttu-id="63116-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="63116-633">taxnumber</span></span>
  
<span data-ttu-id="63116-634">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-634">tax id</span></span>
  
<span data-ttu-id="63116-635">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-635">taxid#</span></span>
  
<span data-ttu-id="63116-636">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-636">tax identification number</span></span>
  
<span data-ttu-id="63116-637">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-637">tax identification no.</span></span>
  
<span data-ttu-id="63116-638">numru tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="63116-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="63116-639">ID tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="63116-639">id tat-taxxa</span></span>
  
<span data-ttu-id="63116-640">numru ta ' identifikazzjoni tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="63116-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="63116-641">Niederlande</span><span class="sxs-lookup"><span data-stu-id="63116-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="63116-642">Format</span><span class="sxs-lookup"><span data-stu-id="63116-642">Format</span></span>

<span data-ttu-id="63116-643">Neun Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-644">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-644">Pattern</span></span>

<span data-ttu-id="63116-645">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="63116-646">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-646">Checksum</span></span>

<span data-ttu-id="63116-647">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-648">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-648">Definition</span></span>

<span data-ttu-id="63116-649">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-650">Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-651">Ein Schlüsselwort `Keywords_netherlands_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-652">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-653">Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-654">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="63116-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="63116-656">niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="63116-657">niederländische Steueridentifikation</span><span class="sxs-lookup"><span data-stu-id="63116-657">netherlands tax identification</span></span>
  
<span data-ttu-id="63116-658">USt-ID-Nummer Niederlande</span><span class="sxs-lookup"><span data-stu-id="63116-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="63116-659">niederländische Steueridentifikation</span><span class="sxs-lookup"><span data-stu-id="63116-659">netherland's tax identification</span></span>
  
<span data-ttu-id="63116-660">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-660">tax identification number</span></span>
  
<span data-ttu-id="63116-661">niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-661">dutch tax id</span></span>
  
<span data-ttu-id="63116-662">niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-662">dutch tax identification number</span></span>
  
<span data-ttu-id="63116-663">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-663">tax id</span></span>
  
<span data-ttu-id="63116-664">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-664">tax id#</span></span>
  
<span data-ttu-id="63116-665">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-665">tax number</span></span>
  
<span data-ttu-id="63116-666">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-666">tax no#</span></span>
  
<span data-ttu-id="63116-667">Steuer</span><span class="sxs-lookup"><span data-stu-id="63116-667">tax#</span></span>
  
<span data-ttu-id="63116-668">tin
</span><span class="sxs-lookup"><span data-stu-id="63116-668">tin</span></span>
  
<span data-ttu-id="63116-669">Zinn</span><span class="sxs-lookup"><span data-stu-id="63116-669">tin#</span></span>
  
<span data-ttu-id="63116-670">Niederlande Zinn</span><span class="sxs-lookup"><span data-stu-id="63116-670">netherlands tin</span></span>
  
<span data-ttu-id="63116-671">Zinn der Niederlande</span><span class="sxs-lookup"><span data-stu-id="63116-671">netherland's tin</span></span>
  
<span data-ttu-id="63116-672">Nederlands identificatienummer</span><span class="sxs-lookup"><span data-stu-id="63116-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="63116-673">identificatienummer van belastend</span><span class="sxs-lookup"><span data-stu-id="63116-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="63116-674">identificatienummer-Belastungen</span><span class="sxs-lookup"><span data-stu-id="63116-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="63116-675">Nederlands identificatie</span><span class="sxs-lookup"><span data-stu-id="63116-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="63116-676">Nederlands-Nummer-ID</span><span class="sxs-lookup"><span data-stu-id="63116-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="63116-677">Nederlands belastingnummer</span><span class="sxs-lookup"><span data-stu-id="63116-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="63116-678">BTW Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-678">btw nummer</span></span>
  
<span data-ttu-id="63116-679">Nederlandse identificatie</span><span class="sxs-lookup"><span data-stu-id="63116-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="63116-680">Polen</span><span class="sxs-lookup"><span data-stu-id="63116-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="63116-681">Format</span><span class="sxs-lookup"><span data-stu-id="63116-681">Format</span></span>

<span data-ttu-id="63116-682">Elf Ziffern ohne Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="63116-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-683">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-683">Pattern</span></span>

<span data-ttu-id="63116-684">Elf Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="63116-685">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-685">Checksum</span></span>

<span data-ttu-id="63116-686">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-687">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-687">Definition</span></span>

<span data-ttu-id="63116-688">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-689">Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-690">Ein Schlüsselwort `Keywords_poland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-691">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-692">Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-693">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="63116-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="63116-695">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-695">tax number</span></span>
  
<span data-ttu-id="63116-696">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-696">tax no.</span></span>
  
<span data-ttu-id="63116-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="63116-697">taxno#</span></span>
  
<span data-ttu-id="63116-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="63116-698">taxnumber#</span></span>
  
<span data-ttu-id="63116-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="63116-699">taxnumber</span></span>
  
<span data-ttu-id="63116-700">NIP</span><span class="sxs-lookup"><span data-stu-id="63116-700">nip</span></span>
  
<span data-ttu-id="63116-701">NIP</span><span class="sxs-lookup"><span data-stu-id="63116-701">nip#</span></span>
  
<span data-ttu-id="63116-702">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-702">tax id</span></span>
  
<span data-ttu-id="63116-703">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-703">tax id#</span></span>
  
<span data-ttu-id="63116-704">NIP-ID</span><span class="sxs-lookup"><span data-stu-id="63116-704">nip id</span></span>
  
<span data-ttu-id="63116-705">NIP-ID #</span><span class="sxs-lookup"><span data-stu-id="63116-705">nip id#</span></span>
  
<span data-ttu-id="63116-706">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-706">tax identification number</span></span>
  
<span data-ttu-id="63116-707">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-707">tax identification no.</span></span>
  
<span data-ttu-id="63116-708">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="63116-708">vat number</span></span>
  
<span data-ttu-id="63116-709">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="63116-709">vat no.</span></span>
  
<span data-ttu-id="63116-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="63116-710">vatno#</span></span>
  
<span data-ttu-id="63116-711">USt-ID</span><span class="sxs-lookup"><span data-stu-id="63116-711">vat id</span></span>
  
<span data-ttu-id="63116-712">USt-ID #</span><span class="sxs-lookup"><span data-stu-id="63116-712">vat id#</span></span>
  
<span data-ttu-id="63116-713">Numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="63116-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="63116-714">Polski Numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="63116-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="63116-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="63116-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="63116-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="63116-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="63116-717">Format</span><span class="sxs-lookup"><span data-stu-id="63116-717">Format</span></span>

<span data-ttu-id="63116-718">Neun Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-719">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-719">Pattern</span></span>

<span data-ttu-id="63116-720">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="63116-721">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-721">Checksum</span></span>

<span data-ttu-id="63116-722">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-723">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-723">Definition</span></span>

<span data-ttu-id="63116-724">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-725">Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-726">Ein Schlüsselwort `Keywords_portugal_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-727">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-728">Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-729">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="63116-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="63116-731">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-731">tax number</span></span>
  
<span data-ttu-id="63116-732">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-732">tax no.</span></span>
  
<span data-ttu-id="63116-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="63116-733">taxno#</span></span>
  
<span data-ttu-id="63116-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="63116-734">taxnumber#</span></span>
  
<span data-ttu-id="63116-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="63116-735">taxnumber</span></span>
  
<span data-ttu-id="63116-736">NIF</span><span class="sxs-lookup"><span data-stu-id="63116-736">nif</span></span>
  
<span data-ttu-id="63116-737">NIF</span><span class="sxs-lookup"><span data-stu-id="63116-737">nif#</span></span>
  
<span data-ttu-id="63116-738">Numero Fiscal</span><span class="sxs-lookup"><span data-stu-id="63116-738">numero fiscal</span></span>
  
<span data-ttu-id="63116-739">número de identificação Fiscal</span><span class="sxs-lookup"><span data-stu-id="63116-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="63116-740">Rumänien</span><span class="sxs-lookup"><span data-stu-id="63116-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="63116-741">Format</span><span class="sxs-lookup"><span data-stu-id="63116-741">Format</span></span>

<span data-ttu-id="63116-742">13 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-743">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-743">Pattern</span></span>

<span data-ttu-id="63116-744">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="63116-745">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-745">Checksum</span></span>

<span data-ttu-id="63116-746">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="63116-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-747">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-747">Definition</span></span>

<span data-ttu-id="63116-748">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-749">Der reguläre Ausdruck `Regex_romania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-750">Ein Schlüsselwort `Keywords_romania_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="63116-751">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="63116-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="63116-753">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-753">tax id</span></span>
  
<span data-ttu-id="63116-754">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-754">tax id number</span></span>
  
<span data-ttu-id="63116-755">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="63116-755">tax file no</span></span>
  
<span data-ttu-id="63116-756">

tax file number</span><span class="sxs-lookup"><span data-stu-id="63116-756">tax file number</span></span>
  
<span data-ttu-id="63116-757">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-757">tax no</span></span>
  
<span data-ttu-id="63116-758">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-758">tax number</span></span>
  
<span data-ttu-id="63116-759">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-759">taxid#</span></span>
  
<span data-ttu-id="63116-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="63116-760">taxno#</span></span>
  
<span data-ttu-id="63116-761">ID – UL-taxei</span><span class="sxs-lookup"><span data-stu-id="63116-761">id-ul taxei</span></span>
  
<span data-ttu-id="63116-762">numărul de identificare fiscală</span><span class="sxs-lookup"><span data-stu-id="63116-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="63116-763">Slowakei</span><span class="sxs-lookup"><span data-stu-id="63116-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="63116-764">Format</span><span class="sxs-lookup"><span data-stu-id="63116-764">Format</span></span>

<span data-ttu-id="63116-765">10 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-766">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-766">Pattern</span></span>

<span data-ttu-id="63116-767">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="63116-768">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-768">Checksum</span></span>

<span data-ttu-id="63116-769">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="63116-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-770">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-770">Definition</span></span>

<span data-ttu-id="63116-771">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-772">Der reguläre Ausdruck `Regex_slovakia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-773">Ein Schlüsselwort `Keywords_slovakia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="63116-774">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="63116-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="63116-776">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-776">tax id</span></span>
  
<span data-ttu-id="63116-777">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-777">tax id number</span></span>
  
<span data-ttu-id="63116-778">Tin-ID</span><span class="sxs-lookup"><span data-stu-id="63116-778">tin id</span></span>
  
<span data-ttu-id="63116-779">Tin Nein</span><span class="sxs-lookup"><span data-stu-id="63116-779">tin no</span></span>
  
<span data-ttu-id="63116-780">Slowakische Tin-ID</span><span class="sxs-lookup"><span data-stu-id="63116-780">slovakian tin id</span></span>
  
<span data-ttu-id="63116-781">tin
</span><span class="sxs-lookup"><span data-stu-id="63116-781">tin</span></span>
  
<span data-ttu-id="63116-782">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="63116-782">tax file no</span></span>
  
<span data-ttu-id="63116-783">

tax file number</span><span class="sxs-lookup"><span data-stu-id="63116-783">tax file number</span></span>
  
<span data-ttu-id="63116-784">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-784">tax no</span></span>
  
<span data-ttu-id="63116-785">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-785">tax number</span></span>
  
<span data-ttu-id="63116-786">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-786">taxid#</span></span>
  
<span data-ttu-id="63116-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="63116-787">taxno#</span></span>
  
<span data-ttu-id="63116-788">Daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="63116-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="63116-789">Daňové číslo</span><span class="sxs-lookup"><span data-stu-id="63116-789">daňové číslo</span></span>
  
<span data-ttu-id="63116-790">Daňové číslo SÚBORU</span><span class="sxs-lookup"><span data-stu-id="63116-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="63116-791">Slowenien</span><span class="sxs-lookup"><span data-stu-id="63116-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="63116-792">Format</span><span class="sxs-lookup"><span data-stu-id="63116-792">Format</span></span>

<span data-ttu-id="63116-793">Acht Ziffern ohne Leerzeichen oder Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-794">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-794">Pattern</span></span>

<span data-ttu-id="63116-795">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="63116-796">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-796">Checksum</span></span>

<span data-ttu-id="63116-797">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-798">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-798">Definition</span></span>

<span data-ttu-id="63116-799">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-800">Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-801">Ein Schlüsselwort `Keywords_slovenia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-802">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-803">Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-804">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="63116-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="63116-806">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-806">tax id</span></span>
  
<span data-ttu-id="63116-807">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-807">tax id number</span></span>
  
<span data-ttu-id="63116-808">Tin-ID</span><span class="sxs-lookup"><span data-stu-id="63116-808">tin id</span></span>
  
<span data-ttu-id="63116-809">Tin Nein</span><span class="sxs-lookup"><span data-stu-id="63116-809">tin no</span></span>
  
<span data-ttu-id="63116-810">slowenische Tin-ID</span><span class="sxs-lookup"><span data-stu-id="63116-810">slovenian tin id</span></span>
  
<span data-ttu-id="63116-811">tin
</span><span class="sxs-lookup"><span data-stu-id="63116-811">tin</span></span>
  
<span data-ttu-id="63116-812">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="63116-812">tax file no</span></span>
  
<span data-ttu-id="63116-813">

tax file number</span><span class="sxs-lookup"><span data-stu-id="63116-813">tax file number</span></span>
  
<span data-ttu-id="63116-814">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-814">tax no</span></span>
  
<span data-ttu-id="63116-815">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-815">tax number</span></span>
  
<span data-ttu-id="63116-816">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-816">taxid#</span></span>
  
<span data-ttu-id="63116-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="63116-817">taxno#</span></span>
  
<span data-ttu-id="63116-818">identifikacijska številka beim Davka</span><span class="sxs-lookup"><span data-stu-id="63116-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="63116-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="63116-819">davčna številka</span></span>
  
<span data-ttu-id="63116-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="63116-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="63116-821">Spanien</span><span class="sxs-lookup"><span data-stu-id="63116-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="63116-822">Format</span><span class="sxs-lookup"><span data-stu-id="63116-822">Format</span></span>

<span data-ttu-id="63116-823">Sieben oder acht Ziffern und ein oder zwei Buchstaben im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="63116-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-824">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-824">Pattern</span></span>

<span data-ttu-id="63116-825">Spanische natürliche Personen mit einem nationalen spanischen Identitätsausweis:</span><span class="sxs-lookup"><span data-stu-id="63116-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="63116-826">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-826">Eight digits</span></span> 
    
- <span data-ttu-id="63116-827">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="63116-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="63116-828">Nicht residente Spanier ohne nationalen Personalausweis</span><span class="sxs-lookup"><span data-stu-id="63116-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="63116-829">Ein Großbuchstabe "L" (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="63116-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="63116-830">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="63116-830">Seven digits</span></span>
    
- <span data-ttu-id="63116-831">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="63116-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="63116-832">Residente Spanier unter 14 Jahren ohne National Ausweis für Spanien:</span><span class="sxs-lookup"><span data-stu-id="63116-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="63116-833">Ein Großbuchstabe "K" (Groß-/Kleinschreibung beachten)</span><span class="sxs-lookup"><span data-stu-id="63116-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="63116-834">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="63116-834">Seven digits</span></span> 
    
- <span data-ttu-id="63116-835">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="63116-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="63116-836">Ausländer mit der IdentifikationsNummer eines ausLänders</span><span class="sxs-lookup"><span data-stu-id="63116-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="63116-837">Ein Großbuchstabe, der "X", "Y" oder "Z" ist (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="63116-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="63116-838">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="63116-838">Seven digits</span></span>
    
- <span data-ttu-id="63116-839">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="63116-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="63116-840">Ausländer ohne IdentifikationsNummer eines ausLänders</span><span class="sxs-lookup"><span data-stu-id="63116-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="63116-841">Ein Großbuchstabe, der "M" (Groß-/Kleinschreibung beachtet) ist</span><span class="sxs-lookup"><span data-stu-id="63116-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="63116-842">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="63116-842">Seven digits</span></span>
    
- <span data-ttu-id="63116-843">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="63116-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="63116-844">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-844">Checksum</span></span>

<span data-ttu-id="63116-845">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-846">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-846">Definition</span></span>

<span data-ttu-id="63116-847">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-848">Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-849">Ein Schlüsselwort `Keywords_spain_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-850">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-851">Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-852">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="63116-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="63116-854">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-854">tax id</span></span>
  
<span data-ttu-id="63116-855">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-855">tax id number</span></span>
  
<span data-ttu-id="63116-856">CIF-ID</span><span class="sxs-lookup"><span data-stu-id="63116-856">cif id</span></span>
  
<span data-ttu-id="63116-857">CIF Nein</span><span class="sxs-lookup"><span data-stu-id="63116-857">cif no</span></span>
  
<span data-ttu-id="63116-858">spanische CIF-ID</span><span class="sxs-lookup"><span data-stu-id="63116-858">spanish cif id</span></span>
  
<span data-ttu-id="63116-859">CIF</span><span class="sxs-lookup"><span data-stu-id="63116-859">cif</span></span>
  
<span data-ttu-id="63116-860">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="63116-860">tax file no</span></span>
  
<span data-ttu-id="63116-861">spanische CIF-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-861">spanish cif number</span></span>
  
<span data-ttu-id="63116-862">

tax file number</span><span class="sxs-lookup"><span data-stu-id="63116-862">tax file number</span></span>
  
<span data-ttu-id="63116-863">Spanisch (CIF) Nein</span><span class="sxs-lookup"><span data-stu-id="63116-863">spanish cif no</span></span>
  
<span data-ttu-id="63116-864">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-864">tax no</span></span>
  
<span data-ttu-id="63116-865">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-865">tax number</span></span>
  
<span data-ttu-id="63116-866">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-866">taxid#</span></span>
  
<span data-ttu-id="63116-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="63116-867">taxno#</span></span>
  
<span data-ttu-id="63116-868">CIFID #</span><span class="sxs-lookup"><span data-stu-id="63116-868">cifid#</span></span>
  
<span data-ttu-id="63116-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="63116-869">spanishcifid#</span></span>
  
<span data-ttu-id="63116-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="63116-870">spanishcifno#</span></span>
  
<span data-ttu-id="63116-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="63116-871">número de contribuyente</span></span>
  
<span data-ttu-id="63116-872">número de Impuesto Corporativo</span><span class="sxs-lookup"><span data-stu-id="63116-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="63116-873">número de Identificación Fiscal</span><span class="sxs-lookup"><span data-stu-id="63116-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="63116-874">CIF-número</span><span class="sxs-lookup"><span data-stu-id="63116-874">cif número</span></span>
  
<span data-ttu-id="63116-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="63116-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="63116-876">Schweden</span><span class="sxs-lookup"><span data-stu-id="63116-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="63116-877">Format</span><span class="sxs-lookup"><span data-stu-id="63116-877">Format</span></span>

<span data-ttu-id="63116-878">Zehn Ziffern und ein Symbol im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="63116-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-879">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-879">Pattern</span></span>

<span data-ttu-id="63116-880">Zehn Ziffern und ein Symbol:</span><span class="sxs-lookup"><span data-stu-id="63116-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="63116-881">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="63116-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="63116-882">Ein Pluszeichen, Minuszeichen oder umgekehrter Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="63116-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="63116-883">Drei Ziffern, die die Identifizierungsnummer eindeutig machen, wobei:</span><span class="sxs-lookup"><span data-stu-id="63116-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="63116-884">Für Zahlen, die vor 1990 ausgegeben wurden, kennzeichnen die siebte und die achte Ziffer den Geburtsort oder die im Ausland geborenen Personen.</span><span class="sxs-lookup"><span data-stu-id="63116-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="63116-885">Die Ziffer in der neunten Position gibt an, dass Geschlecht entweder ungerade für männlich oder sogar für weiblich ist.</span><span class="sxs-lookup"><span data-stu-id="63116-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="63116-886">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="63116-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="63116-887">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-887">Checksum</span></span>

<span data-ttu-id="63116-888">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-889">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-889">Definition</span></span>

<span data-ttu-id="63116-890">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-891">Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-892">Ein Schlüsselwort `Keywords_sweden_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="63116-893">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-894">Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="63116-895">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="63116-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="63116-897">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-897">tax id</span></span>
  
<span data-ttu-id="63116-898">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-898">tax id no.</span></span>
  
<span data-ttu-id="63116-899">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-899">tax id number</span></span>
  
<span data-ttu-id="63116-900">tax identification
</span><span class="sxs-lookup"><span data-stu-id="63116-900">tax identification</span></span>
  
<span data-ttu-id="63116-901">USt-Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="63116-901">tax identification#</span></span>
  
<span data-ttu-id="63116-902">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-902">tax no.</span></span>
  
<span data-ttu-id="63116-903">Steuer</span><span class="sxs-lookup"><span data-stu-id="63116-903">tax#</span></span>
  
<span data-ttu-id="63116-904">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-904">taxid#</span></span>
  
<span data-ttu-id="63116-905">Steuerdatei</span><span class="sxs-lookup"><span data-stu-id="63116-905">tax file</span></span>
  
<span data-ttu-id="63116-906">Steuerdatei Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-906">tax file no.</span></span>
  
<span data-ttu-id="63116-907">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-907">personal id number</span></span>
  
<span data-ttu-id="63116-908">Skate ID Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-908">skatt id nummer</span></span>
  
<span data-ttu-id="63116-909">Skate Identifikation</span><span class="sxs-lookup"><span data-stu-id="63116-909">skatt identifikation</span></span>
  
<span data-ttu-id="63116-910">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="63116-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="63116-911">UK</span><span class="sxs-lookup"><span data-stu-id="63116-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="63116-912">Format</span><span class="sxs-lookup"><span data-stu-id="63116-912">Format</span></span>

<span data-ttu-id="63116-913">Eindeutige Steuerzahler-Referenz (UTR): 10 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="63116-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="63116-p103">National Insurance Number (NINO): Weitere Informationen finden Sie im Abschnitt "UK National Insurance Number (NINO)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="63116-p103">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="63116-916">Muster</span><span class="sxs-lookup"><span data-stu-id="63116-916">Pattern</span></span>

<span data-ttu-id="63116-917">Eindeutige Steuerzahler-Referenz (UTR): 10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="63116-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="63116-p104">National Insurance Number (NINO): Weitere Informationen finden Sie im Abschnitt "UK National Insurance Number (NINO)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="63116-p104">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="63116-920">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="63116-920">Checksum</span></span>

<span data-ttu-id="63116-921">Ja</span><span class="sxs-lookup"><span data-stu-id="63116-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="63116-922">Definition</span><span class="sxs-lookup"><span data-stu-id="63116-922">Definition</span></span>

<span data-ttu-id="63116-923">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="63116-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="63116-924">Die Funktion `Func_uk_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63116-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="63116-925">Ein Schlüsselwort `Keywords_uk_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="63116-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="63116-926">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="63116-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="63116-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="63116-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="63116-928">tax id
</span><span class="sxs-lookup"><span data-stu-id="63116-928">tax id</span></span>
  
<span data-ttu-id="63116-929">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-929">tax id no.</span></span>
  
<span data-ttu-id="63116-930">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="63116-930">tax id number</span></span>
  
<span data-ttu-id="63116-931">tax identification
</span><span class="sxs-lookup"><span data-stu-id="63116-931">tax identification</span></span>
  
<span data-ttu-id="63116-932">USt-Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="63116-932">tax identification#</span></span>
  
<span data-ttu-id="63116-933">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="63116-933">tax no.</span></span>
  
<span data-ttu-id="63116-934">Steuer</span><span class="sxs-lookup"><span data-stu-id="63116-934">tax#</span></span>
  
<span data-ttu-id="63116-935">getaxit #</span><span class="sxs-lookup"><span data-stu-id="63116-935">taxid#</span></span>
  
<span data-ttu-id="63116-936">Steuerdatei</span><span class="sxs-lookup"><span data-stu-id="63116-936">tax file</span></span>
  
<span data-ttu-id="63116-937">Steuerdatei Nr.</span><span class="sxs-lookup"><span data-stu-id="63116-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63116-938">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63116-938">See also</span></span>

[<span data-ttu-id="63116-939">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="63116-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

