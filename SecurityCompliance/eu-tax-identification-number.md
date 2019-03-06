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
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410910"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="158c7-104">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-104">EU Tax Identification Number</span></span>

<span data-ttu-id="158c7-105">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie bei der Erkennung des vertraulichen Informationstyps "TIN" (EU Tax Identification Number) sucht.</span><span class="sxs-lookup"><span data-stu-id="158c7-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="158c7-106">Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="158c7-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="158c7-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="158c7-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="158c7-108">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-108">Format</span></span>

<span data-ttu-id="158c7-109">Neun Ziffern mit optionalem Bindestrich und Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="158c7-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-110">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-110">Pattern</span></span>

<span data-ttu-id="158c7-111">Neun Ziffern mit optionalem Bindestrich und Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="158c7-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="158c7-112">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-112">Two digits</span></span> 
    
- <span data-ttu-id="158c7-113">Ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="158c7-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="158c7-114">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-114">Three digits</span></span>
    
- <span data-ttu-id="158c7-115">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="158c7-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="158c7-116">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-117">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-117">Checksum</span></span>

<span data-ttu-id="158c7-118">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-119">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-119">Definition</span></span>

<span data-ttu-id="158c7-120">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-121">Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-122">Ein Schlüsselwort `Keywords_austria_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-123">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-124">Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-125">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="158c7-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-127">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-127">tax number</span></span>
  
<span data-ttu-id="158c7-128">number</span><span class="sxs-lookup"><span data-stu-id="158c7-128">number</span></span>
  
<span data-ttu-id="158c7-129">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-129">tax registration number</span></span>
  
<span data-ttu-id="158c7-130">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-130">tax id</span></span>
  
<span data-ttu-id="158c7-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-131">st.nr.</span></span>
  
<span data-ttu-id="158c7-132">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="158c7-133">Belgien</span><span class="sxs-lookup"><span data-stu-id="158c7-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="158c7-134">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-134">Format</span></span>

<span data-ttu-id="158c7-135">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-136">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-136">Pattern</span></span>

<span data-ttu-id="158c7-137">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="158c7-137">11 digits:</span></span>
  
- <span data-ttu-id="158c7-138">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-138">Two digits</span></span>
    
- <span data-ttu-id="158c7-139">"0" oder "1"</span><span class="sxs-lookup"><span data-stu-id="158c7-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="158c7-140">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="158c7-140">One digit</span></span>
    
- <span data-ttu-id="158c7-141">"0" oder "1" oder "2" oder "3"</span><span class="sxs-lookup"><span data-stu-id="158c7-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="158c7-142">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-143">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-143">Checksum</span></span>

<span data-ttu-id="158c7-144">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="158c7-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-145">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-145">Definition</span></span>

<span data-ttu-id="158c7-146">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-147">Der reguläre Ausdruck `Regex_belgium_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-148">Ein Schlüsselwort `Keywords_belgium_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="158c7-149">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="158c7-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-151">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-151">tax number</span></span>
  
<span data-ttu-id="158c7-152">nationale Registrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="158c7-152">national registration number</span></span>
  
<span data-ttu-id="158c7-153">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-153">tax registration number</span></span>
  
<span data-ttu-id="158c7-154">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-154">tax id</span></span>
  
<span data-ttu-id="158c7-155">NIF</span><span class="sxs-lookup"><span data-stu-id="158c7-155">nif</span></span>
  
<span data-ttu-id="158c7-156">NIF</span><span class="sxs-lookup"><span data-stu-id="158c7-156">nif#</span></span>
  
<span data-ttu-id="158c7-157">Numéro de Registre National</span><span class="sxs-lookup"><span data-stu-id="158c7-157">numéro de registre national</span></span>
  
<span data-ttu-id="158c7-158">Numéro d'identification Fiscale</span><span class="sxs-lookup"><span data-stu-id="158c7-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="158c7-159">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="158c7-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="158c7-160">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-160">Format</span></span>

<span data-ttu-id="158c7-161">Zehn Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-162">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-162">Pattern</span></span>

<span data-ttu-id="158c7-163">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="158c7-164">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-164">Checksum</span></span>

<span data-ttu-id="158c7-165">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-166">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-166">Definition</span></span>

<span data-ttu-id="158c7-167">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-168">Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-169">Ein Schlüsselwort `Keywords_bulgaria_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-170">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-171">Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-172">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="158c7-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-174">BUCN</span><span class="sxs-lookup"><span data-stu-id="158c7-174">bucn</span></span>
  
<span data-ttu-id="158c7-175">einheitliche Zivil Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-175">uniform civil number</span></span>
  
<span data-ttu-id="158c7-176">BUCN</span><span class="sxs-lookup"><span data-stu-id="158c7-176">bucn#</span></span>
  
<span data-ttu-id="158c7-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="158c7-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="158c7-178">einheitliche Civil ID</span><span class="sxs-lookup"><span data-stu-id="158c7-178">uniform civil id</span></span>
  
<span data-ttu-id="158c7-179">einheitliches ziviles Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-179">uniform civil no</span></span>
  
<span data-ttu-id="158c7-180">EGN</span><span class="sxs-lookup"><span data-stu-id="158c7-180">egn</span></span>
  
<span data-ttu-id="158c7-181">Bulgarische einheitliche Zivil Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="158c7-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="158c7-182">uniformcivilno#</span></span>
  
<span data-ttu-id="158c7-183">EGN</span><span class="sxs-lookup"><span data-stu-id="158c7-183">egn#</span></span>
  
<span data-ttu-id="158c7-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="158c7-184">униформ граждански номер</span></span>
  
<span data-ttu-id="158c7-185">униформ-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-185">униформ id</span></span>
  
<span data-ttu-id="158c7-186">униформ-граждански-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-186">униформ граждански id</span></span>
  
<span data-ttu-id="158c7-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="158c7-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="158c7-188">Kroatien</span><span class="sxs-lookup"><span data-stu-id="158c7-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="158c7-189">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-189">Format</span></span>

<span data-ttu-id="158c7-190">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-191">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-191">Pattern</span></span>

<span data-ttu-id="158c7-192">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="158c7-192">11 digits:</span></span>
  
- <span data-ttu-id="158c7-193">Zehn Ziffern, zufällig gewählt</span><span class="sxs-lookup"><span data-stu-id="158c7-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="158c7-194">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="158c7-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-195">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-195">Checksum</span></span>

<span data-ttu-id="158c7-196">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-197">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-197">Definition</span></span>

<span data-ttu-id="158c7-198">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-199">Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-200">Ein Schlüsselwort `Keywords_croatia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-201">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-202">Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-203">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="158c7-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-205">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-205">tax number</span></span>
  
<span data-ttu-id="158c7-206">Steuer</span><span class="sxs-lookup"><span data-stu-id="158c7-206">tax</span></span>
  
<span data-ttu-id="158c7-207">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-207">tax id</span></span>
  
<span data-ttu-id="158c7-208">oid</span><span class="sxs-lookup"><span data-stu-id="158c7-208">oid</span></span>
  
<span data-ttu-id="158c7-209">OID</span><span class="sxs-lookup"><span data-stu-id="158c7-209">oid#</span></span>
  
<span data-ttu-id="158c7-210">porezni Broj</span><span class="sxs-lookup"><span data-stu-id="158c7-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="158c7-211">Zypern</span><span class="sxs-lookup"><span data-stu-id="158c7-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="158c7-212">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-212">Format</span></span>

<span data-ttu-id="158c7-213">Acht Ziffern und ein Buchstabe im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-214">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-214">Pattern</span></span>

<span data-ttu-id="158c7-215">Acht Ziffern und ein Buchstabe:</span><span class="sxs-lookup"><span data-stu-id="158c7-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="158c7-216">Ein "0"</span><span class="sxs-lookup"><span data-stu-id="158c7-216">A "0"</span></span> 
    
- <span data-ttu-id="158c7-217">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="158c7-217">Seven digits</span></span>
    
- <span data-ttu-id="158c7-218">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="158c7-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-219">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-219">Checksum</span></span>

<span data-ttu-id="158c7-220">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="158c7-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-221">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-221">Definition</span></span>

<span data-ttu-id="158c7-222">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-223">Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-224">Ein Schlüsselwort `Keywords_cyprus_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-225">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-226">Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-227">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="158c7-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-229">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-229">tax number</span></span>
  
<span data-ttu-id="158c7-230">Steuer</span><span class="sxs-lookup"><span data-stu-id="158c7-230">tax</span></span>
  
<span data-ttu-id="158c7-231">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-231">tax id</span></span>
  
<span data-ttu-id="158c7-232">USt-ID-Code</span><span class="sxs-lookup"><span data-stu-id="158c7-232">tax identification code</span></span>
  
<span data-ttu-id="158c7-233">TIC</span><span class="sxs-lookup"><span data-stu-id="158c7-233">tic</span></span>
  
<span data-ttu-id="158c7-234">TIC</span><span class="sxs-lookup"><span data-stu-id="158c7-234">tic#</span></span>
  
<span data-ttu-id="158c7-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="158c7-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="158c7-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="158c7-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="158c7-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="158c7-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="158c7-238">Tschechien</span><span class="sxs-lookup"><span data-stu-id="158c7-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="158c7-239">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-239">Format</span></span>

<span data-ttu-id="158c7-240">Neun oder zehn Ziffern mit optionalem Backslash</span><span class="sxs-lookup"><span data-stu-id="158c7-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-241">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-241">Pattern</span></span>

<span data-ttu-id="158c7-242">Neun oder zehn Ziffern mit einem optionalen umgekehrten Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="158c7-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="158c7-243">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-243">Six digits</span></span> 
    
- <span data-ttu-id="158c7-244">Ein umgekehrter Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="158c7-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="158c7-245">Drei oder vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-246">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-246">Checksum</span></span>

<span data-ttu-id="158c7-247">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="158c7-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-248">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-248">Definition</span></span>

<span data-ttu-id="158c7-249">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-250">Der reguläre Ausdruck `Regex_czech_republic_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-251">Ein Schlüsselwort `Keywords_czech_republic_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="158c7-252">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="158c7-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-254">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-254">tax number</span></span>
  
<span data-ttu-id="158c7-255">Steuer</span><span class="sxs-lookup"><span data-stu-id="158c7-255">tax</span></span>
  
<span data-ttu-id="158c7-256">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-256">tax id</span></span>
  
<span data-ttu-id="158c7-257">persönliche Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-257">personal number</span></span>
  
<span data-ttu-id="158c7-258">Daňové číslo</span><span class="sxs-lookup"><span data-stu-id="158c7-258">daňové číslo</span></span>
  
<span data-ttu-id="158c7-259">Osobní číslo</span><span class="sxs-lookup"><span data-stu-id="158c7-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="158c7-260">Dänemark</span><span class="sxs-lookup"><span data-stu-id="158c7-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="158c7-261">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-261">Format</span></span>

<span data-ttu-id="158c7-262">Zehn Ziffern mit einem Bindestrich</span><span class="sxs-lookup"><span data-stu-id="158c7-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-263">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-263">Pattern</span></span>

<span data-ttu-id="158c7-264">Zehn Ziffern, die einen Bindestrich enthalten:</span><span class="sxs-lookup"><span data-stu-id="158c7-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="158c7-265">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="158c7-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="158c7-266">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="158c7-266">A hyphen</span></span>
    
- <span data-ttu-id="158c7-267">Vier Ziffern, die einer Sequenznummer entsprechen, wobei die erste Ziffer dem Jahrhundert der Geburt entspricht und die letzte Ziffer dem Geschlecht des einzelnen entspricht (ungerade für männlich und sogar für weiblich)</span><span class="sxs-lookup"><span data-stu-id="158c7-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-268">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-268">Checksum</span></span>

<span data-ttu-id="158c7-269">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-270">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-270">Definition</span></span>

<span data-ttu-id="158c7-271">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-272">Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-273">Ein Schlüsselwort `Keywords_denmark_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-274">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-275">Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-276">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="158c7-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-278">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-278">tax number</span></span>
  
<span data-ttu-id="158c7-279">Steuer</span><span class="sxs-lookup"><span data-stu-id="158c7-279">tax</span></span>
  
<span data-ttu-id="158c7-280">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-280">tax id</span></span>
  
<span data-ttu-id="158c7-281">CPR-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-281">cpr number</span></span>
  
<span data-ttu-id="158c7-282">CPR</span><span class="sxs-lookup"><span data-stu-id="158c7-282">cpr#</span></span>
  
<span data-ttu-id="158c7-283">Skate Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-283">skat nummer</span></span>
  
<span data-ttu-id="158c7-284">Skat-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="158c7-285">Estland</span><span class="sxs-lookup"><span data-stu-id="158c7-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="158c7-286">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-286">Format</span></span>

<span data-ttu-id="158c7-287">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-288">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-288">Pattern</span></span>

<span data-ttu-id="158c7-289">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="158c7-289">11 digits:</span></span>
  
-  <span data-ttu-id="158c7-290">Eine Ziffer, die dem Geschlecht und dem Jahrhundert der Geburt entspricht, wobei eine ungerade Zahl männliche und die gerade Zahl angibt, wie folgt: 1,2 für das 19. Jahrhundert; 3, 4 für das 20. Jahrhundert; und 5, 6 für das 21. Jahrhundert</span><span class="sxs-lookup"><span data-stu-id="158c7-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="158c7-291">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="158c7-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="158c7-292">Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am selben Datum geboren wurden</span><span class="sxs-lookup"><span data-stu-id="158c7-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="158c7-293">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="158c7-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-294">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-294">Checksum</span></span>

<span data-ttu-id="158c7-295">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-296">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-296">Definition</span></span>

<span data-ttu-id="158c7-297">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-298">Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-299">Ein Schlüsselwort `Keywords_estonia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-300">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-301">Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-302">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="158c7-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-304">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-304">tax number</span></span>
  
<span data-ttu-id="158c7-305">Steuer</span><span class="sxs-lookup"><span data-stu-id="158c7-305">tax</span></span>
  
<span data-ttu-id="158c7-306">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-306">tax id</span></span>
  
<span data-ttu-id="158c7-307">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="158c7-307">personal code</span></span>
  
<span data-ttu-id="158c7-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="158c7-308">maksunumber</span></span>
  
<span data-ttu-id="158c7-309">maksu-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-309">maksu id</span></span>
  
<span data-ttu-id="158c7-310">Isikukood</span><span class="sxs-lookup"><span data-stu-id="158c7-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="158c7-311">Finnland</span><span class="sxs-lookup"><span data-stu-id="158c7-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="158c7-312">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-312">Format</span></span>

<span data-ttu-id="158c7-313">Eine 11-stellige Kombination aus Ziffern, Buchstaben und Plus-und Minuszeichen</span><span class="sxs-lookup"><span data-stu-id="158c7-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-314">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-314">Pattern</span></span>

<span data-ttu-id="158c7-315">Eine 11-stellige Kombination aus Ziffern, Buchstaben und Plus-und Minuszeichen:</span><span class="sxs-lookup"><span data-stu-id="158c7-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="158c7-316">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-316">Six digits</span></span>
    
- <span data-ttu-id="158c7-317">Eine der folgenden Optionen: ein Pluszeichen, ein Minuszeichen oder der Buchstabe "A" (ohne Beachtung der Groß-/Kleinschreibung), wobei das Pluszeichen zwischen 1800-1899, das Minuszeichen zwischen 1900-1999 und "A" als geboren 2000 und nach</span><span class="sxs-lookup"><span data-stu-id="158c7-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="158c7-318">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-318">Three digits</span></span>
    
- <span data-ttu-id="158c7-319">Ein Buchstaben oder eine Zahl</span><span class="sxs-lookup"><span data-stu-id="158c7-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-320">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-320">Checksum</span></span>

<span data-ttu-id="158c7-321">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-322">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-322">Definition</span></span>

<span data-ttu-id="158c7-323">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-324">Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-325">Ein Schlüsselwort `Keywords_finland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-326">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-327">Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-328">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="158c7-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-330">identification number</span><span class="sxs-lookup"><span data-stu-id="158c7-330">identification number</span></span>
  
<span data-ttu-id="158c7-331">persönliche ID</span><span class="sxs-lookup"><span data-stu-id="158c7-331">personal id</span></span>
  
<span data-ttu-id="158c7-332">Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="158c7-332">identity number</span></span>
  
<span data-ttu-id="158c7-333">nationale finnische ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-333">finnish national id number</span></span>
  
<span data-ttu-id="158c7-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="158c7-334">personalidnumber#</span></span>
  
<span data-ttu-id="158c7-335">national identification number</span><span class="sxs-lookup"><span data-stu-id="158c7-335">national identification number</span></span>
  
<span data-ttu-id="158c7-336">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-336">id number</span></span>
  
<span data-ttu-id="158c7-337">nationale ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-337">national id no.</span></span>
  
<span data-ttu-id="158c7-338">nationale ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-338">national id number</span></span>
  
<span data-ttu-id="158c7-339">ID Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-339">id no</span></span>
  
<span data-ttu-id="158c7-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="158c7-340">tunnistenumero</span></span>
  
<span data-ttu-id="158c7-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="158c7-341">henkilötunnus</span></span>
  
<span data-ttu-id="158c7-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="158c7-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="158c7-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="158c7-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="158c7-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="158c7-344">identiteetti numero</span></span>
  
<span data-ttu-id="158c7-345">Suomen der Kok henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="158c7-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="158c7-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="158c7-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="158c7-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="158c7-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="158c7-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="158c7-348">tunnusnumero</span></span>
  
<span data-ttu-id="158c7-349">der Kok tunnus numero</span><span class="sxs-lookup"><span data-stu-id="158c7-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="158c7-350">Frankreich</span><span class="sxs-lookup"><span data-stu-id="158c7-350">France</span></span>

### <a name="format"></a><span data-ttu-id="158c7-351">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-351">Format</span></span>

<span data-ttu-id="158c7-352">13 Ziffern für Einzelpersonen und neun Ziffern für Entitäten</span><span class="sxs-lookup"><span data-stu-id="158c7-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-353">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-353">Pattern</span></span>

<span data-ttu-id="158c7-354">13 Ziffern für Einzelpersonen:</span><span class="sxs-lookup"><span data-stu-id="158c7-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="158c7-355">Eine Ziffer, die 0, 1, 2 oder 3 sein muss</span><span class="sxs-lookup"><span data-stu-id="158c7-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="158c7-356">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-356">12 digits</span></span>
    
<span data-ttu-id="158c7-357">Neun Ziffern für Entitäten</span><span class="sxs-lookup"><span data-stu-id="158c7-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="158c7-358">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-358">Checksum</span></span>

<span data-ttu-id="158c7-359">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="158c7-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-360">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-360">Definition</span></span>

<span data-ttu-id="158c7-361">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-362">Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-363">Ein Schlüsselwort `Keywords_france_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-364">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-365">Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-366">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="158c7-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-368">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-368">tax identification number</span></span>
  
<span data-ttu-id="158c7-369">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-369">tax number</span></span>
  
<span data-ttu-id="158c7-370">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-370">tax id</span></span>
  
<span data-ttu-id="158c7-371">Numéro d'identification Fiscale</span><span class="sxs-lookup"><span data-stu-id="158c7-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="158c7-372">Deutschland</span><span class="sxs-lookup"><span data-stu-id="158c7-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="158c7-373">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-373">Format</span></span>

<span data-ttu-id="158c7-374">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-375">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-375">Pattern</span></span>

<span data-ttu-id="158c7-376">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="158c7-376">11 digits :</span></span>
  
-  <span data-ttu-id="158c7-377">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-377">Ten digits</span></span> 
    
- <span data-ttu-id="158c7-378">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="158c7-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-379">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-379">Checksum</span></span>

<span data-ttu-id="158c7-380">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-381">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-381">Definition</span></span>

<span data-ttu-id="158c7-382">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-383">Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-384">Ein Schlüsselwort `Keywords_germany_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-385">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-386">Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-387">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="158c7-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-389">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-389">tax number</span></span>
  
<span data-ttu-id="158c7-390">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-390">tax no.</span></span>
  
<span data-ttu-id="158c7-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="158c7-391">taxno#</span></span>
  
<span data-ttu-id="158c7-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="158c7-392">taxnumber#</span></span>
  
<span data-ttu-id="158c7-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="158c7-393">taxnumber</span></span>
  
<span data-ttu-id="158c7-394">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-394">tax id</span></span>
  
<span data-ttu-id="158c7-395">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-395">taxid#</span></span>
  
<span data-ttu-id="158c7-396">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-396">tax identification number</span></span>
  
<span data-ttu-id="158c7-397">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-397">tax identification no.</span></span>
  
<span data-ttu-id="158c7-398">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-398">steuernummer</span></span>
  
<span data-ttu-id="158c7-399">Ingo-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-399">steuer id</span></span>
  
<span data-ttu-id="158c7-400">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="158c7-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="158c7-401">Griechenland</span><span class="sxs-lookup"><span data-stu-id="158c7-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="158c7-402">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-402">Format</span></span>

<span data-ttu-id="158c7-403">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-404">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-404">Pattern</span></span>

<span data-ttu-id="158c7-405">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="158c7-406">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-406">Checksum</span></span>

<span data-ttu-id="158c7-407">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="158c7-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-408">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-408">Definition</span></span>

<span data-ttu-id="158c7-409">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-410">Der reguläre Ausdruck `Regex_greece_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-411">Ein Schlüsselwort `Keywords_greece_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="158c7-412">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="158c7-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-414">AFM</span><span class="sxs-lookup"><span data-stu-id="158c7-414">afm</span></span>
  
<span data-ttu-id="158c7-415">Zinn</span><span class="sxs-lookup"><span data-stu-id="158c7-415">tin</span></span>
  
<span data-ttu-id="158c7-416">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-416">tax id no.</span></span>
  
<span data-ttu-id="158c7-417">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-417">tax id no</span></span>
  
<span data-ttu-id="158c7-418">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-418">tax identification number</span></span>
  
<span data-ttu-id="158c7-419">Steuerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="158c7-419">tax registry number</span></span>
  
<span data-ttu-id="158c7-420">Steuerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="158c7-420">tax registry no.</span></span>
  
<span data-ttu-id="158c7-421">AFM</span><span class="sxs-lookup"><span data-stu-id="158c7-421">afm#</span></span>
  
<span data-ttu-id="158c7-422">Zinn</span><span class="sxs-lookup"><span data-stu-id="158c7-422">tin#</span></span>
  
<span data-ttu-id="158c7-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="158c7-423">taxidno#</span></span>
  
<span data-ttu-id="158c7-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="158c7-424">taxregistryno#</span></span>
  
<span data-ttu-id="158c7-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="158c7-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="158c7-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="158c7-426">aφμ</span></span>
  
<span data-ttu-id="158c7-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="158c7-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="158c7-428">φορολογικού μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="158c7-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="158c7-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="158c7-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="158c7-430">Ungarn</span><span class="sxs-lookup"><span data-stu-id="158c7-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="158c7-431">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-431">Format</span></span>

<span data-ttu-id="158c7-432">Zehn Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-433">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-433">Pattern</span></span>

<span data-ttu-id="158c7-434">Zehn Ziffern:</span><span class="sxs-lookup"><span data-stu-id="158c7-434">Ten digits:</span></span>
  
-  <span data-ttu-id="158c7-435">Eine Ziffer, die "8" sein muss</span><span class="sxs-lookup"><span data-stu-id="158c7-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="158c7-436">Fünf Ziffern, die der Anzahl von Tagen zwischen dem Datum 01/01/1867 und dem Geburtsdatum des einzelnen entsprechen</span><span class="sxs-lookup"><span data-stu-id="158c7-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="158c7-437">Drei Ziffern, die der Zahl entsprechen, die von Wahrscheinlichkeit zur Unterscheidung von Individuen generiert wurde, die am selben Tag geboren wurden</span><span class="sxs-lookup"><span data-stu-id="158c7-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="158c7-438">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="158c7-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-439">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-439">Checksum</span></span>

<span data-ttu-id="158c7-440">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-441">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-441">Definition</span></span>

<span data-ttu-id="158c7-442">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-443">Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-444">Ein Schlüsselwort `Keywords_hungary_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-445">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-446">Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-447">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="158c7-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-449">ungarische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="158c7-450">ungarische Dose</span><span class="sxs-lookup"><span data-stu-id="158c7-450">hungarian tin</span></span>
  
<span data-ttu-id="158c7-451">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-451">tax id number</span></span>
  
<span data-ttu-id="158c7-452">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="158c7-452">vat number</span></span>
  
<span data-ttu-id="158c7-453">Finanzamt Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-453">tax authority no</span></span>
  
<span data-ttu-id="158c7-454">USt-ID-Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-454">tax id tax identity number</span></span>
  
<span data-ttu-id="158c7-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="158c7-455">taxidnumber#</span></span>
  
<span data-ttu-id="158c7-456">Zinn</span><span class="sxs-lookup"><span data-stu-id="158c7-456">tin#</span></span>
  
<span data-ttu-id="158c7-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="158c7-457">hungatiantin#</span></span>
  
<span data-ttu-id="158c7-458">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-458">tax identification no</span></span>
  
<span data-ttu-id="158c7-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="158c7-459">taxidno#</span></span>
  
<span data-ttu-id="158c7-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="158c7-460">adóazonosító szám</span></span>
  
<span data-ttu-id="158c7-461">adószám</span><span class="sxs-lookup"><span data-stu-id="158c7-461">adószám</span></span>
  
<span data-ttu-id="158c7-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="158c7-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="158c7-463">Irland</span><span class="sxs-lookup"><span data-stu-id="158c7-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="158c7-464">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-464">Format</span></span>

<span data-ttu-id="158c7-465">Sieben Ziffern, gefolgt von einem Buchstaben ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="158c7-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-466">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-466">Pattern</span></span>

<span data-ttu-id="158c7-467">Sieben Ziffern gefolgt von einem Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="158c7-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="158c7-468">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="158c7-468">Seven digits</span></span> 
    
- <span data-ttu-id="158c7-469">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="158c7-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-470">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-470">Checksum</span></span>

<span data-ttu-id="158c7-471">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="158c7-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-472">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-472">Definition</span></span>

<span data-ttu-id="158c7-473">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-474">Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-475">Ein Schlüsselwort `Keywords_ireland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-476">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-477">Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-478">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="158c7-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-480">öffentlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-480">public service no</span></span>
  
<span data-ttu-id="158c7-481">persönlicher öffentlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-481">personal public service no</span></span>
  
<span data-ttu-id="158c7-482">PPS Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-482">pps no</span></span>
  
<span data-ttu-id="158c7-483">persönlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-483">personal service no</span></span>
  
<span data-ttu-id="158c7-484">PPS-Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-484">pps service no</span></span>
  
<span data-ttu-id="158c7-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="158c7-485">ppsno#</span></span>
  
<span data-ttu-id="158c7-486">Irisch PPS Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-486">irish pps no</span></span>
  
<span data-ttu-id="158c7-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="158c7-487">publicserviceno#</span></span>
  
<span data-ttu-id="158c7-488">persönliche öffentliche Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="158c7-488">personal public service number</span></span>
  
<span data-ttu-id="158c7-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="158c7-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="158c7-490">PPS-uimh</span><span class="sxs-lookup"><span data-stu-id="158c7-490">pps uimh</span></span>
  
<span data-ttu-id="158c7-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="158c7-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="158c7-492">Italien</span><span class="sxs-lookup"><span data-stu-id="158c7-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="158c7-493">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-493">Format</span></span>

<span data-ttu-id="158c7-494">16 Buchstaben und Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-495">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-495">Pattern</span></span>

<span data-ttu-id="158c7-496">16 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="158c7-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="158c7-497">Drei Buchstaben, die den ersten drei Konsonanten im Familiennamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="158c7-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="158c7-498">Drei Buchstaben, die dem ersten, dritten und vierten Konsonanten im Vornamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="158c7-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="158c7-499">Zwei Ziffern, die den letzten Ziffern des Geburtsjahrs entsprechen</span><span class="sxs-lookup"><span data-stu-id="158c7-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="158c7-500">Eine Ziffer, die dem Geburtsmonat entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben A bis E, H, L, M, P, R bis T werden verwendet (also Januar ist A und Oktober ist R)</span><span class="sxs-lookup"><span data-stu-id="158c7-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="158c7-501">Zwei Ziffern, die dem Tag des Geburtsmonats entsprechen, wobei 40 zum Geburtstag hinzugefügt wird, damit Frauen von Männern unterschieden werden.</span><span class="sxs-lookup"><span data-stu-id="158c7-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="158c7-502">Vier Ziffern, die einer Ortskennzahl für die Gemeinde entsprechen, in der die Person geboren wurde – landesweite Codes werden für fremde Länder verwendet</span><span class="sxs-lookup"><span data-stu-id="158c7-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="158c7-503">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="158c7-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-504">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-504">Checksum</span></span>

<span data-ttu-id="158c7-505">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-506">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-506">Definition</span></span>

<span data-ttu-id="158c7-507">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-508">Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-509">Ein Schlüsselwort `Keywords_italy_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-510">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-511">Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-512">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="158c7-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-514">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-514">tax number</span></span>
  
<span data-ttu-id="158c7-515">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-515">tax no.</span></span>
  
<span data-ttu-id="158c7-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="158c7-516">taxno#</span></span>
  
<span data-ttu-id="158c7-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="158c7-517">taxnumber#</span></span>
  
<span data-ttu-id="158c7-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="158c7-518">taxnumber</span></span>
  
<span data-ttu-id="158c7-519">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-519">tax id</span></span>
  
<span data-ttu-id="158c7-520">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-520">taxid#</span></span>
  
<span data-ttu-id="158c7-521">Fiskal Code</span><span class="sxs-lookup"><span data-stu-id="158c7-521">fiscal code</span></span>
  
<span data-ttu-id="158c7-522">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="158c7-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="158c7-523">Lettland</span><span class="sxs-lookup"><span data-stu-id="158c7-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="158c7-524">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-524">Format</span></span>

<span data-ttu-id="158c7-525">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-526">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-526">Pattern</span></span>

<span data-ttu-id="158c7-527">11 Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="158c7-528">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="158c7-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="158c7-529">Eine Ziffer, die dem Jahrhundert der Geburt entspricht, wobei "0" dem 19. Jahrhundert entspricht, "1" entspricht dem 20. Jahrhundert, und "2" entspricht dem 21. Jahrhundert</span><span class="sxs-lookup"><span data-stu-id="158c7-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="158c7-530">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-531">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-531">Checksum</span></span>

<span data-ttu-id="158c7-532">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-533">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-533">Definition</span></span>

<span data-ttu-id="158c7-534">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-535">Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-536">Ein Schlüsselwort `Keywords_latvia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-537">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-538">Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-539">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="158c7-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-541">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-541">tax number</span></span>
  
<span data-ttu-id="158c7-542">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-542">tax no.</span></span>
  
<span data-ttu-id="158c7-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="158c7-543">taxno#</span></span>
  
<span data-ttu-id="158c7-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="158c7-544">taxnumber#</span></span>
  
<span data-ttu-id="158c7-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="158c7-545">taxnumber</span></span>
  
<span data-ttu-id="158c7-546">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-546">tax id</span></span>
  
<span data-ttu-id="158c7-547">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-547">taxid#</span></span>
  
<span data-ttu-id="158c7-548">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-548">tax identification number</span></span>
  
<span data-ttu-id="158c7-549">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-549">tax identification no.</span></span>
  
<span data-ttu-id="158c7-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="158c7-550">nodokļa numurs</span></span>
  
<span data-ttu-id="158c7-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="158c7-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="158c7-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="158c7-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="158c7-553">Litauen</span><span class="sxs-lookup"><span data-stu-id="158c7-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="158c7-554">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-554">Format</span></span>

<span data-ttu-id="158c7-555">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-556">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-556">Pattern</span></span>

<span data-ttu-id="158c7-557">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="158c7-558">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-558">Checksum</span></span>

<span data-ttu-id="158c7-559">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="158c7-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-560">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-560">Definition</span></span>

<span data-ttu-id="158c7-561">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-562">Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-563">Ein Schlüsselwort `Keywords_lithuania_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-564">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-565">Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-566">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="158c7-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-568">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-568">tax number</span></span>
  
<span data-ttu-id="158c7-569">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-569">tax no.</span></span>
  
<span data-ttu-id="158c7-570">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-570">tax no#</span></span>
  
<span data-ttu-id="158c7-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="158c7-571">taxnumber#</span></span>
  
<span data-ttu-id="158c7-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="158c7-572">taxnumber</span></span>
  
<span data-ttu-id="158c7-573">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-573">tax id</span></span>
  
<span data-ttu-id="158c7-574">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-574">taxid#</span></span>
  
<span data-ttu-id="158c7-575">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-575">tax identification number</span></span>
  
<span data-ttu-id="158c7-576">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-576">tax identification no.</span></span>
  
<span data-ttu-id="158c7-577">mokesčių-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-577">mokesčių id</span></span>
  
<span data-ttu-id="158c7-578">mokesčių Numeris</span><span class="sxs-lookup"><span data-stu-id="158c7-578">mokesčių numeris</span></span>
  
<span data-ttu-id="158c7-579">mokesčių identifikavimas Numeris</span><span class="sxs-lookup"><span data-stu-id="158c7-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="158c7-580">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="158c7-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="158c7-581">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-581">Format</span></span>

<span data-ttu-id="158c7-582">13 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-583">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-583">Pattern</span></span>

<span data-ttu-id="158c7-584">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="158c7-584">13 digits:</span></span>
  
-  <span data-ttu-id="158c7-585">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-585">11 digits</span></span> 
    
- <span data-ttu-id="158c7-586">Zwei Prüfziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-587">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-587">Checksum</span></span>

<span data-ttu-id="158c7-588">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-589">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-589">Definition</span></span>

<span data-ttu-id="158c7-590">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-591">Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-592">Ein Schlüsselwort `Keywords_luxemburg_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-593">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-594">Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-595">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="158c7-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-597">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-597">tax number</span></span>
  
<span data-ttu-id="158c7-598">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-598">tax no.</span></span>
  
<span data-ttu-id="158c7-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="158c7-599">taxno#</span></span>
  
<span data-ttu-id="158c7-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="158c7-600">taxnumber#</span></span>
  
<span data-ttu-id="158c7-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="158c7-601">taxnumber</span></span>
  
<span data-ttu-id="158c7-602">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-602">tax id</span></span>
  
<span data-ttu-id="158c7-603">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-603">taxid#</span></span>
  
<span data-ttu-id="158c7-604">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-604">tax identification number</span></span>
  
<span data-ttu-id="158c7-605">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-605">tax identification no.</span></span>
  
<span data-ttu-id="158c7-606">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-606">steuernummer</span></span>
  
<span data-ttu-id="158c7-607">Ingo-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-607">steuer id</span></span>
  
<span data-ttu-id="158c7-608">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="158c7-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="158c7-609">Malta</span><span class="sxs-lookup"><span data-stu-id="158c7-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="158c7-610">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-610">Format</span></span>

<span data-ttu-id="158c7-611">Für maltesische Staatsangehörige: 7 Ziffern und ein Buchstabe im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="158c7-612">Nicht maltesische Staatsangehörige und maltesische Entitäten: 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-613">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-613">Pattern</span></span>

<span data-ttu-id="158c7-614">Maltesische Staatsangehörige: 7 Ziffern und ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="158c7-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="158c7-615">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="158c7-615">Seven digits</span></span> 
    
- <span data-ttu-id="158c7-616">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="158c7-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="158c7-617">Nicht maltesische Staatsangehörige und maltesische Entitäten: 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="158c7-618">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="158c7-619">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-619">Checksum</span></span>

<span data-ttu-id="158c7-620">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="158c7-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-621">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-621">Definition</span></span>

<span data-ttu-id="158c7-622">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-623">Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-624">Ein Schlüsselwort `Keywords_malta_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-625">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-626">Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-627">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="158c7-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-629">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-629">tax number</span></span>
  
<span data-ttu-id="158c7-630">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-630">tax no.</span></span>
  
<span data-ttu-id="158c7-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="158c7-631">taxno#</span></span>
  
<span data-ttu-id="158c7-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="158c7-632">taxnumber#</span></span>
  
<span data-ttu-id="158c7-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="158c7-633">taxnumber</span></span>
  
<span data-ttu-id="158c7-634">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-634">tax id</span></span>
  
<span data-ttu-id="158c7-635">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-635">taxid#</span></span>
  
<span data-ttu-id="158c7-636">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-636">tax identification number</span></span>
  
<span data-ttu-id="158c7-637">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-637">tax identification no.</span></span>
  
<span data-ttu-id="158c7-638">numru tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="158c7-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="158c7-639">ID tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="158c7-639">id tat-taxxa</span></span>
  
<span data-ttu-id="158c7-640">numru ta ' identifikazzjoni tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="158c7-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="158c7-641">Niederlande</span><span class="sxs-lookup"><span data-stu-id="158c7-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="158c7-642">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-642">Format</span></span>

<span data-ttu-id="158c7-643">Neun Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-644">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-644">Pattern</span></span>

<span data-ttu-id="158c7-645">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="158c7-646">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-646">Checksum</span></span>

<span data-ttu-id="158c7-647">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-648">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-648">Definition</span></span>

<span data-ttu-id="158c7-649">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-650">Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-651">Ein Schlüsselwort `Keywords_netherlands_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-652">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-653">Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-654">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="158c7-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-656">niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="158c7-657">niederländische Steueridentifikation</span><span class="sxs-lookup"><span data-stu-id="158c7-657">netherlands tax identification</span></span>
  
<span data-ttu-id="158c7-658">USt-ID-Nummer Niederlande</span><span class="sxs-lookup"><span data-stu-id="158c7-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="158c7-659">niederländische Steueridentifikation</span><span class="sxs-lookup"><span data-stu-id="158c7-659">netherland's tax identification</span></span>
  
<span data-ttu-id="158c7-660">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-660">tax identification number</span></span>
  
<span data-ttu-id="158c7-661">niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-661">dutch tax id</span></span>
  
<span data-ttu-id="158c7-662">niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-662">dutch tax identification number</span></span>
  
<span data-ttu-id="158c7-663">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-663">tax id</span></span>
  
<span data-ttu-id="158c7-664">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-664">tax id#</span></span>
  
<span data-ttu-id="158c7-665">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-665">tax number</span></span>
  
<span data-ttu-id="158c7-666">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-666">tax no#</span></span>
  
<span data-ttu-id="158c7-667">Steuer</span><span class="sxs-lookup"><span data-stu-id="158c7-667">tax#</span></span>
  
<span data-ttu-id="158c7-668">Zinn</span><span class="sxs-lookup"><span data-stu-id="158c7-668">tin</span></span>
  
<span data-ttu-id="158c7-669">Zinn</span><span class="sxs-lookup"><span data-stu-id="158c7-669">tin#</span></span>
  
<span data-ttu-id="158c7-670">Niederlande Zinn</span><span class="sxs-lookup"><span data-stu-id="158c7-670">netherlands tin</span></span>
  
<span data-ttu-id="158c7-671">Zinn der Niederlande</span><span class="sxs-lookup"><span data-stu-id="158c7-671">netherland's tin</span></span>
  
<span data-ttu-id="158c7-672">Nederlands identificatienummer</span><span class="sxs-lookup"><span data-stu-id="158c7-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="158c7-673">identificatienummer van belastend</span><span class="sxs-lookup"><span data-stu-id="158c7-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="158c7-674">identificatienummer-Belastungen</span><span class="sxs-lookup"><span data-stu-id="158c7-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="158c7-675">Nederlands identificatie</span><span class="sxs-lookup"><span data-stu-id="158c7-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="158c7-676">Nederlands-Nummer-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="158c7-677">Nederlands belastingnummer</span><span class="sxs-lookup"><span data-stu-id="158c7-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="158c7-678">BTW Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-678">btw nummer</span></span>
  
<span data-ttu-id="158c7-679">Nederlandse identificatie</span><span class="sxs-lookup"><span data-stu-id="158c7-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="158c7-680">Polen</span><span class="sxs-lookup"><span data-stu-id="158c7-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="158c7-681">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-681">Format</span></span>

<span data-ttu-id="158c7-682">Elf Ziffern ohne Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="158c7-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-683">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-683">Pattern</span></span>

<span data-ttu-id="158c7-684">Elf Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="158c7-685">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-685">Checksum</span></span>

<span data-ttu-id="158c7-686">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-687">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-687">Definition</span></span>

<span data-ttu-id="158c7-688">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-689">Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-690">Ein Schlüsselwort `Keywords_poland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-691">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-692">Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-693">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="158c7-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-695">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-695">tax number</span></span>
  
<span data-ttu-id="158c7-696">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-696">tax no.</span></span>
  
<span data-ttu-id="158c7-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="158c7-697">taxno#</span></span>
  
<span data-ttu-id="158c7-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="158c7-698">taxnumber#</span></span>
  
<span data-ttu-id="158c7-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="158c7-699">taxnumber</span></span>
  
<span data-ttu-id="158c7-700">NIP</span><span class="sxs-lookup"><span data-stu-id="158c7-700">nip</span></span>
  
<span data-ttu-id="158c7-701">NIP</span><span class="sxs-lookup"><span data-stu-id="158c7-701">nip#</span></span>
  
<span data-ttu-id="158c7-702">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-702">tax id</span></span>
  
<span data-ttu-id="158c7-703">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-703">tax id#</span></span>
  
<span data-ttu-id="158c7-704">NIP-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-704">nip id</span></span>
  
<span data-ttu-id="158c7-705">NIP-ID #</span><span class="sxs-lookup"><span data-stu-id="158c7-705">nip id#</span></span>
  
<span data-ttu-id="158c7-706">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-706">tax identification number</span></span>
  
<span data-ttu-id="158c7-707">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-707">tax identification no.</span></span>
  
<span data-ttu-id="158c7-708">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="158c7-708">vat number</span></span>
  
<span data-ttu-id="158c7-709">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="158c7-709">vat no.</span></span>
  
<span data-ttu-id="158c7-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="158c7-710">vatno#</span></span>
  
<span data-ttu-id="158c7-711">USt-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-711">vat id</span></span>
  
<span data-ttu-id="158c7-712">USt-ID #</span><span class="sxs-lookup"><span data-stu-id="158c7-712">vat id#</span></span>
  
<span data-ttu-id="158c7-713">Numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="158c7-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="158c7-714">Polski Numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="158c7-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="158c7-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="158c7-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="158c7-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="158c7-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="158c7-717">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-717">Format</span></span>

<span data-ttu-id="158c7-718">Neun Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-719">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-719">Pattern</span></span>

<span data-ttu-id="158c7-720">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="158c7-721">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-721">Checksum</span></span>

<span data-ttu-id="158c7-722">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-723">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-723">Definition</span></span>

<span data-ttu-id="158c7-724">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-725">Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-726">Ein Schlüsselwort `Keywords_portugal_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-727">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-728">Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-729">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="158c7-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-731">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-731">tax number</span></span>
  
<span data-ttu-id="158c7-732">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-732">tax no.</span></span>
  
<span data-ttu-id="158c7-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="158c7-733">taxno#</span></span>
  
<span data-ttu-id="158c7-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="158c7-734">taxnumber#</span></span>
  
<span data-ttu-id="158c7-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="158c7-735">taxnumber</span></span>
  
<span data-ttu-id="158c7-736">NIF</span><span class="sxs-lookup"><span data-stu-id="158c7-736">nif</span></span>
  
<span data-ttu-id="158c7-737">NIF</span><span class="sxs-lookup"><span data-stu-id="158c7-737">nif#</span></span>
  
<span data-ttu-id="158c7-738">Numero Fiscal</span><span class="sxs-lookup"><span data-stu-id="158c7-738">numero fiscal</span></span>
  
<span data-ttu-id="158c7-739">número de identificação Fiscal</span><span class="sxs-lookup"><span data-stu-id="158c7-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="158c7-740">Rumänien</span><span class="sxs-lookup"><span data-stu-id="158c7-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="158c7-741">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-741">Format</span></span>

<span data-ttu-id="158c7-742">13 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-743">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-743">Pattern</span></span>

<span data-ttu-id="158c7-744">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="158c7-745">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-745">Checksum</span></span>

<span data-ttu-id="158c7-746">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="158c7-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-747">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-747">Definition</span></span>

<span data-ttu-id="158c7-748">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-749">Der reguläre Ausdruck `Regex_romania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-750">Ein Schlüsselwort `Keywords_romania_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="158c7-751">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="158c7-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-753">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-753">tax id</span></span>
  
<span data-ttu-id="158c7-754">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-754">tax id number</span></span>
  
<span data-ttu-id="158c7-755">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-755">tax file no</span></span>
  
<span data-ttu-id="158c7-756">tax file number</span><span class="sxs-lookup"><span data-stu-id="158c7-756">tax file number</span></span>
  
<span data-ttu-id="158c7-757">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-757">tax no</span></span>
  
<span data-ttu-id="158c7-758">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-758">tax number</span></span>
  
<span data-ttu-id="158c7-759">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-759">taxid#</span></span>
  
<span data-ttu-id="158c7-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="158c7-760">taxno#</span></span>
  
<span data-ttu-id="158c7-761">ID – UL-taxei</span><span class="sxs-lookup"><span data-stu-id="158c7-761">id-ul taxei</span></span>
  
<span data-ttu-id="158c7-762">numărul de identificare fiscală</span><span class="sxs-lookup"><span data-stu-id="158c7-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="158c7-763">Slowakei</span><span class="sxs-lookup"><span data-stu-id="158c7-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="158c7-764">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-764">Format</span></span>

<span data-ttu-id="158c7-765">10 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-766">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-766">Pattern</span></span>

<span data-ttu-id="158c7-767">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="158c7-768">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-768">Checksum</span></span>

<span data-ttu-id="158c7-769">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="158c7-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-770">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-770">Definition</span></span>

<span data-ttu-id="158c7-771">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-772">Der reguläre Ausdruck `Regex_slovakia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-773">Ein Schlüsselwort `Keywords_slovakia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="158c7-774">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="158c7-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-776">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-776">tax id</span></span>
  
<span data-ttu-id="158c7-777">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-777">tax id number</span></span>
  
<span data-ttu-id="158c7-778">Tin-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-778">tin id</span></span>
  
<span data-ttu-id="158c7-779">Tin Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-779">tin no</span></span>
  
<span data-ttu-id="158c7-780">Slowakische Tin-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-780">slovakian tin id</span></span>
  
<span data-ttu-id="158c7-781">Zinn</span><span class="sxs-lookup"><span data-stu-id="158c7-781">tin</span></span>
  
<span data-ttu-id="158c7-782">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-782">tax file no</span></span>
  
<span data-ttu-id="158c7-783">tax file number</span><span class="sxs-lookup"><span data-stu-id="158c7-783">tax file number</span></span>
  
<span data-ttu-id="158c7-784">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-784">tax no</span></span>
  
<span data-ttu-id="158c7-785">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-785">tax number</span></span>
  
<span data-ttu-id="158c7-786">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-786">taxid#</span></span>
  
<span data-ttu-id="158c7-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="158c7-787">taxno#</span></span>
  
<span data-ttu-id="158c7-788">Daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="158c7-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="158c7-789">Daňové číslo</span><span class="sxs-lookup"><span data-stu-id="158c7-789">daňové číslo</span></span>
  
<span data-ttu-id="158c7-790">Daňové číslo SÚBORU</span><span class="sxs-lookup"><span data-stu-id="158c7-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="158c7-791">Slowenien</span><span class="sxs-lookup"><span data-stu-id="158c7-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="158c7-792">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-792">Format</span></span>

<span data-ttu-id="158c7-793">Acht Ziffern ohne Leerzeichen oder Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-794">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-794">Pattern</span></span>

<span data-ttu-id="158c7-795">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="158c7-796">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-796">Checksum</span></span>

<span data-ttu-id="158c7-797">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-798">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-798">Definition</span></span>

<span data-ttu-id="158c7-799">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-800">Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-801">Ein Schlüsselwort `Keywords_slovenia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-802">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-803">Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-804">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="158c7-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-806">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-806">tax id</span></span>
  
<span data-ttu-id="158c7-807">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-807">tax id number</span></span>
  
<span data-ttu-id="158c7-808">Tin-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-808">tin id</span></span>
  
<span data-ttu-id="158c7-809">Tin Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-809">tin no</span></span>
  
<span data-ttu-id="158c7-810">slowenische Tin-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-810">slovenian tin id</span></span>
  
<span data-ttu-id="158c7-811">Zinn</span><span class="sxs-lookup"><span data-stu-id="158c7-811">tin</span></span>
  
<span data-ttu-id="158c7-812">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-812">tax file no</span></span>
  
<span data-ttu-id="158c7-813">tax file number</span><span class="sxs-lookup"><span data-stu-id="158c7-813">tax file number</span></span>
  
<span data-ttu-id="158c7-814">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-814">tax no</span></span>
  
<span data-ttu-id="158c7-815">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-815">tax number</span></span>
  
<span data-ttu-id="158c7-816">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-816">taxid#</span></span>
  
<span data-ttu-id="158c7-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="158c7-817">taxno#</span></span>
  
<span data-ttu-id="158c7-818">identifikacijska številka beim Davka</span><span class="sxs-lookup"><span data-stu-id="158c7-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="158c7-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="158c7-819">davčna številka</span></span>
  
<span data-ttu-id="158c7-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="158c7-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="158c7-821">Spanien</span><span class="sxs-lookup"><span data-stu-id="158c7-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="158c7-822">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-822">Format</span></span>

<span data-ttu-id="158c7-823">Sieben oder acht Ziffern und ein oder zwei Buchstaben im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-824">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-824">Pattern</span></span>

<span data-ttu-id="158c7-825">Spanische natürliche Personen mit einem nationalen spanischen Identitätsausweis:</span><span class="sxs-lookup"><span data-stu-id="158c7-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="158c7-826">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-826">Eight digits</span></span> 
    
- <span data-ttu-id="158c7-827">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="158c7-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="158c7-828">Nicht residente Spanier ohne nationalen Personalausweis</span><span class="sxs-lookup"><span data-stu-id="158c7-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="158c7-829">Ein Großbuchstabe "L" (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="158c7-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="158c7-830">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="158c7-830">Seven digits</span></span>
    
- <span data-ttu-id="158c7-831">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="158c7-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="158c7-832">Residente Spanier unter 14 Jahren ohne National Ausweis für Spanien:</span><span class="sxs-lookup"><span data-stu-id="158c7-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="158c7-833">Ein Großbuchstabe "K" (Groß-/Kleinschreibung beachten)</span><span class="sxs-lookup"><span data-stu-id="158c7-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="158c7-834">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="158c7-834">Seven digits</span></span> 
    
- <span data-ttu-id="158c7-835">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="158c7-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="158c7-836">Ausländer mit der IdentifikationsNummer eines ausLänders</span><span class="sxs-lookup"><span data-stu-id="158c7-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="158c7-837">Ein Großbuchstabe, der "X", "Y" oder "Z" ist (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="158c7-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="158c7-838">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="158c7-838">Seven digits</span></span>
    
- <span data-ttu-id="158c7-839">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="158c7-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="158c7-840">Ausländer ohne IdentifikationsNummer eines ausLänders</span><span class="sxs-lookup"><span data-stu-id="158c7-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="158c7-841">Ein Großbuchstabe, der "M" (Groß-/Kleinschreibung beachtet) ist</span><span class="sxs-lookup"><span data-stu-id="158c7-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="158c7-842">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="158c7-842">Seven digits</span></span>
    
- <span data-ttu-id="158c7-843">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="158c7-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="158c7-844">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-844">Checksum</span></span>

<span data-ttu-id="158c7-845">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-846">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-846">Definition</span></span>

<span data-ttu-id="158c7-847">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-848">Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-849">Ein Schlüsselwort `Keywords_spain_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-850">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-851">Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-852">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="158c7-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-854">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-854">tax id</span></span>
  
<span data-ttu-id="158c7-855">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-855">tax id number</span></span>
  
<span data-ttu-id="158c7-856">CIF-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-856">cif id</span></span>
  
<span data-ttu-id="158c7-857">CIF Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-857">cif no</span></span>
  
<span data-ttu-id="158c7-858">spanische CIF-ID</span><span class="sxs-lookup"><span data-stu-id="158c7-858">spanish cif id</span></span>
  
<span data-ttu-id="158c7-859">CIF</span><span class="sxs-lookup"><span data-stu-id="158c7-859">cif</span></span>
  
<span data-ttu-id="158c7-860">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-860">tax file no</span></span>
  
<span data-ttu-id="158c7-861">spanische CIF-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-861">spanish cif number</span></span>
  
<span data-ttu-id="158c7-862">tax file number</span><span class="sxs-lookup"><span data-stu-id="158c7-862">tax file number</span></span>
  
<span data-ttu-id="158c7-863">Spanisch (CIF) Nein</span><span class="sxs-lookup"><span data-stu-id="158c7-863">spanish cif no</span></span>
  
<span data-ttu-id="158c7-864">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-864">tax no</span></span>
  
<span data-ttu-id="158c7-865">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-865">tax number</span></span>
  
<span data-ttu-id="158c7-866">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-866">taxid#</span></span>
  
<span data-ttu-id="158c7-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="158c7-867">taxno#</span></span>
  
<span data-ttu-id="158c7-868">CIFID #</span><span class="sxs-lookup"><span data-stu-id="158c7-868">cifid#</span></span>
  
<span data-ttu-id="158c7-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="158c7-869">spanishcifid#</span></span>
  
<span data-ttu-id="158c7-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="158c7-870">spanishcifno#</span></span>
  
<span data-ttu-id="158c7-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="158c7-871">número de contribuyente</span></span>
  
<span data-ttu-id="158c7-872">número de Impuesto Corporativo</span><span class="sxs-lookup"><span data-stu-id="158c7-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="158c7-873">número de Identificación Fiscal</span><span class="sxs-lookup"><span data-stu-id="158c7-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="158c7-874">CIF-número</span><span class="sxs-lookup"><span data-stu-id="158c7-874">cif número</span></span>
  
<span data-ttu-id="158c7-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="158c7-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="158c7-876">Schweden</span><span class="sxs-lookup"><span data-stu-id="158c7-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="158c7-877">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-877">Format</span></span>

<span data-ttu-id="158c7-878">Zehn Ziffern und ein Symbol im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-879">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-879">Pattern</span></span>

<span data-ttu-id="158c7-880">Zehn Ziffern und ein Symbol:</span><span class="sxs-lookup"><span data-stu-id="158c7-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="158c7-881">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="158c7-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="158c7-882">Ein Pluszeichen, Minuszeichen oder umgekehrter Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="158c7-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="158c7-883">Drei Ziffern, die die Identifizierungsnummer eindeutig machen, wobei:</span><span class="sxs-lookup"><span data-stu-id="158c7-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="158c7-884">Für Zahlen, die vor 1990 ausgegeben wurden, kennzeichnen die siebte und die achte Ziffer den Geburtsort oder die im Ausland geborenen Personen.</span><span class="sxs-lookup"><span data-stu-id="158c7-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="158c7-885">Die Ziffer in der neunten Position gibt an, dass Geschlecht entweder ungerade für männlich oder sogar für weiblich ist.</span><span class="sxs-lookup"><span data-stu-id="158c7-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="158c7-886">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="158c7-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="158c7-887">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-887">Checksum</span></span>

<span data-ttu-id="158c7-888">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-889">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-889">Definition</span></span>

<span data-ttu-id="158c7-890">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-891">Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-892">Ein Schlüsselwort `Keywords_sweden_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="158c7-893">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-894">Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="158c7-895">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="158c7-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-897">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-897">tax id</span></span>
  
<span data-ttu-id="158c7-898">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-898">tax id no.</span></span>
  
<span data-ttu-id="158c7-899">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-899">tax id number</span></span>
  
<span data-ttu-id="158c7-900">tax identification</span><span class="sxs-lookup"><span data-stu-id="158c7-900">tax identification</span></span>
  
<span data-ttu-id="158c7-901">USt-Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="158c7-901">tax identification#</span></span>
  
<span data-ttu-id="158c7-902">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-902">tax no.</span></span>
  
<span data-ttu-id="158c7-903">Steuer</span><span class="sxs-lookup"><span data-stu-id="158c7-903">tax#</span></span>
  
<span data-ttu-id="158c7-904">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-904">taxid#</span></span>
  
<span data-ttu-id="158c7-905">Steuerdatei</span><span class="sxs-lookup"><span data-stu-id="158c7-905">tax file</span></span>
  
<span data-ttu-id="158c7-906">Steuerdatei Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-906">tax file no.</span></span>
  
<span data-ttu-id="158c7-907">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-907">personal id number</span></span>
  
<span data-ttu-id="158c7-908">Skate ID Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-908">skatt id nummer</span></span>
  
<span data-ttu-id="158c7-909">Skate Identifikation</span><span class="sxs-lookup"><span data-stu-id="158c7-909">skatt identifikation</span></span>
  
<span data-ttu-id="158c7-910">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="158c7-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="158c7-911">UK</span><span class="sxs-lookup"><span data-stu-id="158c7-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="158c7-912">Format</span><span class="sxs-lookup"><span data-stu-id="158c7-912">Format</span></span>

<span data-ttu-id="158c7-913">Eindeutige Steuerzahler-Referenz (UTR): 10 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="158c7-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="158c7-914">Nationale Versicherungsnummer (NINO): Weitere Informationen finden Sie im Abschnitt "U.K.</span><span class="sxs-lookup"><span data-stu-id="158c7-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="158c7-915">National Insurance Number (NINO) "in [dem, wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="158c7-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="158c7-916">Muster</span><span class="sxs-lookup"><span data-stu-id="158c7-916">Pattern</span></span>

<span data-ttu-id="158c7-917">Eindeutige Steuerzahler-Referenz (UTR): 10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="158c7-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="158c7-918">Nationale Versicherungsnummer (NINO): Weitere Informationen finden Sie im Abschnitt "U.K.</span><span class="sxs-lookup"><span data-stu-id="158c7-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="158c7-919">National Insurance Number (NINO) "in [dem, wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="158c7-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="158c7-920">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="158c7-920">Checksum</span></span>

<span data-ttu-id="158c7-921">Ja</span><span class="sxs-lookup"><span data-stu-id="158c7-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="158c7-922">Definition</span><span class="sxs-lookup"><span data-stu-id="158c7-922">Definition</span></span>

<span data-ttu-id="158c7-923">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="158c7-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="158c7-924">Die Funktion `Func_uk_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="158c7-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="158c7-925">Ein Schlüsselwort `Keywords_uk_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="158c7-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="158c7-926">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="158c7-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="158c7-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="158c7-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="158c7-928">tax id</span><span class="sxs-lookup"><span data-stu-id="158c7-928">tax id</span></span>
  
<span data-ttu-id="158c7-929">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-929">tax id no.</span></span>
  
<span data-ttu-id="158c7-930">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="158c7-930">tax id number</span></span>
  
<span data-ttu-id="158c7-931">tax identification</span><span class="sxs-lookup"><span data-stu-id="158c7-931">tax identification</span></span>
  
<span data-ttu-id="158c7-932">USt-Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="158c7-932">tax identification#</span></span>
  
<span data-ttu-id="158c7-933">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="158c7-933">tax no.</span></span>
  
<span data-ttu-id="158c7-934">Steuer</span><span class="sxs-lookup"><span data-stu-id="158c7-934">tax#</span></span>
  
<span data-ttu-id="158c7-935">getaxit #</span><span class="sxs-lookup"><span data-stu-id="158c7-935">taxid#</span></span>
  
<span data-ttu-id="158c7-936">Steuerdatei</span><span class="sxs-lookup"><span data-stu-id="158c7-936">tax file</span></span>
  
<span data-ttu-id="158c7-937">Steuerdatei Nr.</span><span class="sxs-lookup"><span data-stu-id="158c7-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="158c7-938">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="158c7-938">See also</span></span>

[<span data-ttu-id="158c7-939">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="158c7-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

