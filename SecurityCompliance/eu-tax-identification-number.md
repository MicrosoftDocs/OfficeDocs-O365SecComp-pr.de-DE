---
title: EU-Steueridentifikationsnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine DLP-Richtlinie (Data Loss Prevention) sucht, wenn der vertrauliche Informationstyp "EU-Steueridentifikationsnummer" erkannt wird. Dieser Typ vertraulicher Informationen definiert unterschiedliche Muster, Stichwörter und andere Beweise für jedes Land.
ms.openlocfilehash: adcd9be9b5f8775ad39010d771ff2ac214df1e17
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152957"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="0fd99-104">EU-Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-104">EU Tax Identification Number</span></span>

<span data-ttu-id="0fd99-105">In diesem Thema wird gezeigt, was eine DLP-Richtlinie (Data Loss Prevention) sucht, wenn Sie den Typ der vertraulichen Informationen für die EU-Steueridentifikationsnummer (TIN) erkennt.</span><span class="sxs-lookup"><span data-stu-id="0fd99-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="0fd99-106">Dieser Typ vertraulicher Informationen definiert unterschiedliche Muster, Stichwörter und andere Beweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="0fd99-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="0fd99-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="0fd99-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-108">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-108">Format</span></span>

<span data-ttu-id="0fd99-109">Neun Ziffern mit optionalem Bindestrich und Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="0fd99-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-110">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-110">Pattern</span></span>

<span data-ttu-id="0fd99-111">Neun Ziffern mit optionalem Bindestrich und Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="0fd99-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="0fd99-112">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-112">Two digits</span></span> 
    
- <span data-ttu-id="0fd99-113">Ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="0fd99-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="0fd99-114">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-114">Three digits</span></span>
    
- <span data-ttu-id="0fd99-115">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="0fd99-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="0fd99-116">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-117">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-117">Checksum</span></span>

<span data-ttu-id="0fd99-118">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-119">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-119">Definition</span></span>

<span data-ttu-id="0fd99-120">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-121">Die- `Func_austria_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-122">Ein Schlüsselwort `Keywords_austria_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-123">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-124">Die- `Func_austria_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-125">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="0fd99-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-127">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-127">tax number</span></span>
  
<span data-ttu-id="0fd99-128">number</span><span class="sxs-lookup"><span data-stu-id="0fd99-128">number</span></span>
  
<span data-ttu-id="0fd99-129">Steuerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-129">tax registration number</span></span>
  
<span data-ttu-id="0fd99-130">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-130">tax id</span></span>
  
<span data-ttu-id="0fd99-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-131">st.nr.</span></span>
  
<span data-ttu-id="0fd99-132">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="0fd99-133">Belgien</span><span class="sxs-lookup"><span data-stu-id="0fd99-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-134">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-134">Format</span></span>

<span data-ttu-id="0fd99-135">11 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-136">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-136">Pattern</span></span>

<span data-ttu-id="0fd99-137">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0fd99-137">11 digits:</span></span>
  
- <span data-ttu-id="0fd99-138">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-138">Two digits</span></span>
    
- <span data-ttu-id="0fd99-139">A "0" oder "1"</span><span class="sxs-lookup"><span data-stu-id="0fd99-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="0fd99-140">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="0fd99-140">One digit</span></span>
    
- <span data-ttu-id="0fd99-141">A "0" oder "1" oder "2" oder "3"</span><span class="sxs-lookup"><span data-stu-id="0fd99-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="0fd99-142">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-143">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-143">Checksum</span></span>

<span data-ttu-id="0fd99-144">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fd99-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-145">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-145">Definition</span></span>

<span data-ttu-id="0fd99-146">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-147">Der reguläre Ausdruck `Regex_belgium_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-148">Ein Schlüsselwort `Keywords_belgium_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fd99-149">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="0fd99-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-151">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-151">tax number</span></span>
  
<span data-ttu-id="0fd99-152">nationale Registrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-152">national registration number</span></span>
  
<span data-ttu-id="0fd99-153">Steuerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-153">tax registration number</span></span>
  
<span data-ttu-id="0fd99-154">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-154">tax id</span></span>
  
<span data-ttu-id="0fd99-155">NIF</span><span class="sxs-lookup"><span data-stu-id="0fd99-155">nif</span></span>
  
<span data-ttu-id="0fd99-156">NIF</span><span class="sxs-lookup"><span data-stu-id="0fd99-156">nif#</span></span>
  
<span data-ttu-id="0fd99-157">Numéro de Registre National</span><span class="sxs-lookup"><span data-stu-id="0fd99-157">numéro de registre national</span></span>
  
<span data-ttu-id="0fd99-158">Numéro d'identification Fiscale</span><span class="sxs-lookup"><span data-stu-id="0fd99-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="0fd99-159">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="0fd99-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-160">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-160">Format</span></span>

<span data-ttu-id="0fd99-161">Zehn Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-162">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-162">Pattern</span></span>

<span data-ttu-id="0fd99-163">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fd99-164">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-164">Checksum</span></span>

<span data-ttu-id="0fd99-165">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-166">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-166">Definition</span></span>

<span data-ttu-id="0fd99-167">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-168">Die- `Func_bulgaria_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-169">Ein Schlüsselwort `Keywords_bulgaria_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-170">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-171">Die- `Func_bulgaria_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-172">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="0fd99-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-174">BUCN</span><span class="sxs-lookup"><span data-stu-id="0fd99-174">bucn</span></span>
  
<span data-ttu-id="0fd99-175">einheitliche Zivil Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-175">uniform civil number</span></span>
  
<span data-ttu-id="0fd99-176">BUCN</span><span class="sxs-lookup"><span data-stu-id="0fd99-176">bucn#</span></span>
  
<span data-ttu-id="0fd99-177">uniformcivilnumber#</span><span class="sxs-lookup"><span data-stu-id="0fd99-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="0fd99-178">Uniform Civil ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-178">uniform civil id</span></span>
  
<span data-ttu-id="0fd99-179">Uniform Civil Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-179">uniform civil no</span></span>
  
<span data-ttu-id="0fd99-180">EGN</span><span class="sxs-lookup"><span data-stu-id="0fd99-180">egn</span></span>
  
<span data-ttu-id="0fd99-181">Bulgarische Uniform Civil Number</span><span class="sxs-lookup"><span data-stu-id="0fd99-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="0fd99-182">uniformcivilno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-182">uniformcivilno#</span></span>
  
<span data-ttu-id="0fd99-183">EGN</span><span class="sxs-lookup"><span data-stu-id="0fd99-183">egn#</span></span>
  
<span data-ttu-id="0fd99-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="0fd99-184">униформ граждански номер</span></span>
  
<span data-ttu-id="0fd99-185">униформ-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-185">униформ id</span></span>
  
<span data-ttu-id="0fd99-186">униформ-граждански-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-186">униформ граждански id</span></span>
  
<span data-ttu-id="0fd99-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="0fd99-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="0fd99-188">Kroatien</span><span class="sxs-lookup"><span data-stu-id="0fd99-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-189">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-189">Format</span></span>

<span data-ttu-id="0fd99-190">11 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-191">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-191">Pattern</span></span>

<span data-ttu-id="0fd99-192">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0fd99-192">11 digits:</span></span>
  
- <span data-ttu-id="0fd99-193">Zehn Ziffern, nach dem Zufallsprinzip ausgewählt</span><span class="sxs-lookup"><span data-stu-id="0fd99-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="0fd99-194">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0fd99-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-195">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-195">Checksum</span></span>

<span data-ttu-id="0fd99-196">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-197">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-197">Definition</span></span>

<span data-ttu-id="0fd99-198">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-199">Die- `Func_croatia_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-200">Ein Schlüsselwort `Keywords_croatia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-201">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-202">Die- `Func_croatia_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-203">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="0fd99-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-205">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-205">tax number</span></span>
  
<span data-ttu-id="0fd99-206">Steuer</span><span class="sxs-lookup"><span data-stu-id="0fd99-206">tax</span></span>
  
<span data-ttu-id="0fd99-207">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-207">tax id</span></span>
  
<span data-ttu-id="0fd99-208">oid</span><span class="sxs-lookup"><span data-stu-id="0fd99-208">oid</span></span>
  
<span data-ttu-id="0fd99-209">OID</span><span class="sxs-lookup"><span data-stu-id="0fd99-209">oid#</span></span>
  
<span data-ttu-id="0fd99-210">porezni Broj</span><span class="sxs-lookup"><span data-stu-id="0fd99-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="0fd99-211">Zypern</span><span class="sxs-lookup"><span data-stu-id="0fd99-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-212">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-212">Format</span></span>

<span data-ttu-id="0fd99-213">Acht Ziffern und ein Buchstabe im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-214">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-214">Pattern</span></span>

<span data-ttu-id="0fd99-215">Acht Ziffern und ein Buchstabe:</span><span class="sxs-lookup"><span data-stu-id="0fd99-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="0fd99-216">A "0"</span><span class="sxs-lookup"><span data-stu-id="0fd99-216">A "0"</span></span> 
    
- <span data-ttu-id="0fd99-217">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0fd99-217">Seven digits</span></span>
    
- <span data-ttu-id="0fd99-218">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0fd99-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-219">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-219">Checksum</span></span>

<span data-ttu-id="0fd99-220">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fd99-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-221">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-221">Definition</span></span>

<span data-ttu-id="0fd99-222">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-223">Die- `Func_cyprus_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-224">Ein Schlüsselwort `Keywords_cyprus_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-225">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-226">Die- `Func_cyprus_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-227">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="0fd99-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-229">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-229">tax number</span></span>
  
<span data-ttu-id="0fd99-230">Steuer</span><span class="sxs-lookup"><span data-stu-id="0fd99-230">tax</span></span>
  
<span data-ttu-id="0fd99-231">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-231">tax id</span></span>
  
<span data-ttu-id="0fd99-232">Steuer Identifikationscode</span><span class="sxs-lookup"><span data-stu-id="0fd99-232">tax identification code</span></span>
  
<span data-ttu-id="0fd99-233">TIC</span><span class="sxs-lookup"><span data-stu-id="0fd99-233">tic</span></span>
  
<span data-ttu-id="0fd99-234">TIC</span><span class="sxs-lookup"><span data-stu-id="0fd99-234">tic#</span></span>
  
<span data-ttu-id="0fd99-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0fd99-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="0fd99-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="0fd99-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="0fd99-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0fd99-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="0fd99-238">Tschechien</span><span class="sxs-lookup"><span data-stu-id="0fd99-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-239">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-239">Format</span></span>

<span data-ttu-id="0fd99-240">Neun oder zehn Ziffern mit einem optionalen Backslash</span><span class="sxs-lookup"><span data-stu-id="0fd99-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-241">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-241">Pattern</span></span>

<span data-ttu-id="0fd99-242">Neun oder zehn Ziffern mit einem optionalen backslashl:</span><span class="sxs-lookup"><span data-stu-id="0fd99-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="0fd99-243">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-243">Six digits</span></span> 
    
- <span data-ttu-id="0fd99-244">Ein Backslash (optional)</span><span class="sxs-lookup"><span data-stu-id="0fd99-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="0fd99-245">Drei oder vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-246">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-246">Checksum</span></span>

<span data-ttu-id="0fd99-247">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fd99-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-248">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-248">Definition</span></span>

<span data-ttu-id="0fd99-249">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-250">Der reguläre Ausdruck `Regex_czech_republic_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-251">Ein Schlüsselwort `Keywords_czech_republic_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fd99-252">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="0fd99-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-254">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-254">tax number</span></span>
  
<span data-ttu-id="0fd99-255">Steuer</span><span class="sxs-lookup"><span data-stu-id="0fd99-255">tax</span></span>
  
<span data-ttu-id="0fd99-256">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-256">tax id</span></span>
  
<span data-ttu-id="0fd99-257">persönliche Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-257">personal number</span></span>
  
<span data-ttu-id="0fd99-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="0fd99-258">daňové číslo</span></span>
  
<span data-ttu-id="0fd99-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="0fd99-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="0fd99-260">Dänemark</span><span class="sxs-lookup"><span data-stu-id="0fd99-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-261">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-261">Format</span></span>

<span data-ttu-id="0fd99-262">Zehn Ziffern mit einem Bindestrich</span><span class="sxs-lookup"><span data-stu-id="0fd99-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-263">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-263">Pattern</span></span>

<span data-ttu-id="0fd99-264">Zehn Ziffern mit einem Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="0fd99-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="0fd99-265">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="0fd99-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="0fd99-266">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="0fd99-266">A hyphen</span></span>
    
- <span data-ttu-id="0fd99-267">Vier Ziffern, die einer Sequenznummer entsprechen, wobei die erste Ziffer dem Jahrhundert der Geburt entspricht und die letzte Ziffer dem Geschlecht der Person entspricht (ungerade für männliche und sogar für weiblich)</span><span class="sxs-lookup"><span data-stu-id="0fd99-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-268">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-268">Checksum</span></span>

<span data-ttu-id="0fd99-269">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-270">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-270">Definition</span></span>

<span data-ttu-id="0fd99-271">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-272">Die- `Func_denmark_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-273">Ein Schlüsselwort `Keywords_denmark_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-274">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-275">Die- `Func_denmark_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-276">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="0fd99-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-278">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-278">tax number</span></span>
  
<span data-ttu-id="0fd99-279">Steuer</span><span class="sxs-lookup"><span data-stu-id="0fd99-279">tax</span></span>
  
<span data-ttu-id="0fd99-280">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-280">tax id</span></span>
  
<span data-ttu-id="0fd99-281">CPR-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-281">cpr number</span></span>
  
<span data-ttu-id="0fd99-282">CPR</span><span class="sxs-lookup"><span data-stu-id="0fd99-282">cpr#</span></span>
  
<span data-ttu-id="0fd99-283">Skate Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-283">skat nummer</span></span>
  
<span data-ttu-id="0fd99-284">Skat-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="0fd99-285">Estland</span><span class="sxs-lookup"><span data-stu-id="0fd99-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-286">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-286">Format</span></span>

<span data-ttu-id="0fd99-287">11 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-288">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-288">Pattern</span></span>

<span data-ttu-id="0fd99-289">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0fd99-289">11 digits:</span></span>
  
-  <span data-ttu-id="0fd99-290">Eine Ziffer, die dem Geschlecht und dem Jahrhundert der Geburt entspricht, wobei eine ungerade Zahl männlich ist und die gerade Zahl weiblich wie folgt angibt: 1, 2 für das 19. Jahrhundert; 3,4 für das 20. Jahrhundert; und 5, 6 für das 21. Jahrhundert</span><span class="sxs-lookup"><span data-stu-id="0fd99-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="0fd99-291">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="0fd99-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="0fd99-292">Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am gleichen Datum geboren wurden</span><span class="sxs-lookup"><span data-stu-id="0fd99-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="0fd99-293">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0fd99-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-294">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-294">Checksum</span></span>

<span data-ttu-id="0fd99-295">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-296">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-296">Definition</span></span>

<span data-ttu-id="0fd99-297">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-298">Die- `Func_estonia_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-299">Ein Schlüsselwort `Keywords_estonia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-300">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-301">Die- `Func_estonia_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-302">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="0fd99-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-304">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-304">tax number</span></span>
  
<span data-ttu-id="0fd99-305">Steuer</span><span class="sxs-lookup"><span data-stu-id="0fd99-305">tax</span></span>
  
<span data-ttu-id="0fd99-306">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-306">tax id</span></span>
  
<span data-ttu-id="0fd99-307">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="0fd99-307">personal code</span></span>
  
<span data-ttu-id="0fd99-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="0fd99-308">maksunumber</span></span>
  
<span data-ttu-id="0fd99-309">maksu-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-309">maksu id</span></span>
  
<span data-ttu-id="0fd99-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="0fd99-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="0fd99-311">Finnland</span><span class="sxs-lookup"><span data-stu-id="0fd99-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-312">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-312">Format</span></span>

<span data-ttu-id="0fd99-313">Eine Kombination aus 11 Zeichen aus Ziffern, Buchstaben und Plus-und Minuszeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-314">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-314">Pattern</span></span>

<span data-ttu-id="0fd99-315">Eine Kombination aus 11 Zeichen aus Ziffern, Buchstaben und Plus-und Minuszeichen:</span><span class="sxs-lookup"><span data-stu-id="0fd99-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="0fd99-316">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-316">Six digits</span></span>
    
- <span data-ttu-id="0fd99-317">Eine der folgenden Optionen: ein Pluszeichen, ein Minuszeichen oder der Buchstabe "a" (Groß-/Kleinschreibung nicht beachtet), wobei das Pluszeichen zwischen 1800-1899 geboren wird, das Minuszeichen zwischen 1900-1999 und "a" geboren ist 2000 und nach</span><span class="sxs-lookup"><span data-stu-id="0fd99-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="0fd99-318">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-318">Three digits</span></span>
    
- <span data-ttu-id="0fd99-319">Ein Buchstabe oder eine Zahl</span><span class="sxs-lookup"><span data-stu-id="0fd99-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-320">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-320">Checksum</span></span>

<span data-ttu-id="0fd99-321">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-322">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-322">Definition</span></span>

<span data-ttu-id="0fd99-323">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-324">Die- `Func_finland_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-325">Ein Schlüsselwort `Keywords_finland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-326">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-327">Die- `Func_finland_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-328">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="0fd99-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-330">identification number</span><span class="sxs-lookup"><span data-stu-id="0fd99-330">identification number</span></span>
  
<span data-ttu-id="0fd99-331">persönliche ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-331">personal id</span></span>
  
<span data-ttu-id="0fd99-332">Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-332">identity number</span></span>
  
<span data-ttu-id="0fd99-333">Finnische Nationale ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-333">finnish national id number</span></span>
  
<span data-ttu-id="0fd99-334">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="0fd99-334">personalidnumber#</span></span>
  
<span data-ttu-id="0fd99-335">national identification number</span><span class="sxs-lookup"><span data-stu-id="0fd99-335">national identification number</span></span>
  
<span data-ttu-id="0fd99-336">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-336">id number</span></span>
  
<span data-ttu-id="0fd99-337">nationale ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-337">national id no.</span></span>
  
<span data-ttu-id="0fd99-338">nationale ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-338">national id number</span></span>
  
<span data-ttu-id="0fd99-339">ID Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-339">id no</span></span>
  
<span data-ttu-id="0fd99-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="0fd99-340">tunnistenumero</span></span>
  
<span data-ttu-id="0fd99-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="0fd99-341">henkilötunnus</span></span>
  
<span data-ttu-id="0fd99-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="0fd99-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="0fd99-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="0fd99-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="0fd99-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="0fd99-344">identiteetti numero</span></span>
  
<span data-ttu-id="0fd99-345">Suomen der Kok henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="0fd99-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="0fd99-346">henkilötunnusnumero#</span><span class="sxs-lookup"><span data-stu-id="0fd99-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="0fd99-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="0fd99-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="0fd99-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="0fd99-348">tunnusnumero</span></span>
  
<span data-ttu-id="0fd99-349">der Kok tunnus numero</span><span class="sxs-lookup"><span data-stu-id="0fd99-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="0fd99-350">Frankreich</span><span class="sxs-lookup"><span data-stu-id="0fd99-350">France</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-351">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-351">Format</span></span>

<span data-ttu-id="0fd99-352">13 Ziffern für einzelne Personen und neun Ziffern für Entitäten</span><span class="sxs-lookup"><span data-stu-id="0fd99-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-353">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-353">Pattern</span></span>

<span data-ttu-id="0fd99-354">13 Ziffern für einzelne Personen:</span><span class="sxs-lookup"><span data-stu-id="0fd99-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="0fd99-355">Eine Ziffer, die 0, 1, 2 oder 3 sein muss</span><span class="sxs-lookup"><span data-stu-id="0fd99-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="0fd99-356">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-356">12 digits</span></span>
    
<span data-ttu-id="0fd99-357">Neun Ziffern für Entitäten</span><span class="sxs-lookup"><span data-stu-id="0fd99-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fd99-358">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-358">Checksum</span></span>

<span data-ttu-id="0fd99-359">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fd99-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-360">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-360">Definition</span></span>

<span data-ttu-id="0fd99-361">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-362">Die- `Func_france_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-363">Ein Schlüsselwort `Keywords_france_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-364">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-365">Die- `Func_france_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-366">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="0fd99-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-368">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-368">tax identification number</span></span>
  
<span data-ttu-id="0fd99-369">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-369">tax number</span></span>
  
<span data-ttu-id="0fd99-370">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-370">tax id</span></span>
  
<span data-ttu-id="0fd99-371">Numéro d'identification Fiscale</span><span class="sxs-lookup"><span data-stu-id="0fd99-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="0fd99-372">Deutschland</span><span class="sxs-lookup"><span data-stu-id="0fd99-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-373">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-373">Format</span></span>

<span data-ttu-id="0fd99-374">11 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-375">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-375">Pattern</span></span>

<span data-ttu-id="0fd99-376">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0fd99-376">11 digits :</span></span>
  
-  <span data-ttu-id="0fd99-377">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-377">Ten digits</span></span> 
    
- <span data-ttu-id="0fd99-378">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0fd99-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-379">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-379">Checksum</span></span>

<span data-ttu-id="0fd99-380">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-381">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-381">Definition</span></span>

<span data-ttu-id="0fd99-382">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-383">Die- `Func_germany_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-384">Ein Schlüsselwort `Keywords_germany_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-385">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-386">Die- `Func_germany_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-387">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="0fd99-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-389">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-389">tax number</span></span>
  
<span data-ttu-id="0fd99-390">Steuer-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-390">tax no.</span></span>
  
<span data-ttu-id="0fd99-391">taxno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-391">taxno#</span></span>
  
<span data-ttu-id="0fd99-392">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="0fd99-392">taxnumber#</span></span>
  
<span data-ttu-id="0fd99-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0fd99-393">taxnumber</span></span>
  
<span data-ttu-id="0fd99-394">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-394">tax id</span></span>
  
<span data-ttu-id="0fd99-395">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-395">taxid#</span></span>
  
<span data-ttu-id="0fd99-396">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-396">tax identification number</span></span>
  
<span data-ttu-id="0fd99-397">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-397">tax identification no.</span></span>
  
<span data-ttu-id="0fd99-398">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-398">steuernummer</span></span>
  
<span data-ttu-id="0fd99-399">Ingo-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-399">steuer id</span></span>
  
<span data-ttu-id="0fd99-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="0fd99-401">Griechenland</span><span class="sxs-lookup"><span data-stu-id="0fd99-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-402">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-402">Format</span></span>

<span data-ttu-id="0fd99-403">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-404">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-404">Pattern</span></span>

<span data-ttu-id="0fd99-405">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fd99-406">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-406">Checksum</span></span>

<span data-ttu-id="0fd99-407">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fd99-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-408">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-408">Definition</span></span>

<span data-ttu-id="0fd99-409">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-410">Der reguläre Ausdruck `Regex_greece_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-411">Ein Schlüsselwort `Keywords_greece_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fd99-412">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="0fd99-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-414">AFM</span><span class="sxs-lookup"><span data-stu-id="0fd99-414">afm</span></span>
  
<span data-ttu-id="0fd99-415">Zinn</span><span class="sxs-lookup"><span data-stu-id="0fd99-415">tin</span></span>
  
<span data-ttu-id="0fd99-416">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-416">tax id no.</span></span>
  
<span data-ttu-id="0fd99-417">Steuernummer Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-417">tax id no</span></span>
  
<span data-ttu-id="0fd99-418">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-418">tax identification number</span></span>
  
<span data-ttu-id="0fd99-419">Steuerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-419">tax registry number</span></span>
  
<span data-ttu-id="0fd99-420">Steuerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-420">tax registry no.</span></span>
  
<span data-ttu-id="0fd99-421">AFM</span><span class="sxs-lookup"><span data-stu-id="0fd99-421">afm#</span></span>
  
<span data-ttu-id="0fd99-422">Zinn</span><span class="sxs-lookup"><span data-stu-id="0fd99-422">tin#</span></span>
  
<span data-ttu-id="0fd99-423">taxidno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-423">taxidno#</span></span>
  
<span data-ttu-id="0fd99-424">taxregistryno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-424">taxregistryno#</span></span>
  
<span data-ttu-id="0fd99-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0fd99-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="0fd99-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="0fd99-426">aφμ</span></span>
  
<span data-ttu-id="0fd99-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="0fd99-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="0fd99-428">φορολογικού μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="0fd99-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="0fd99-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0fd99-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="0fd99-430">Ungarn</span><span class="sxs-lookup"><span data-stu-id="0fd99-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-431">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-431">Format</span></span>

<span data-ttu-id="0fd99-432">Zehn Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-433">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-433">Pattern</span></span>

<span data-ttu-id="0fd99-434">Zehn Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0fd99-434">Ten digits:</span></span>
  
-  <span data-ttu-id="0fd99-435">Eine Ziffer, die "8" sein muss</span><span class="sxs-lookup"><span data-stu-id="0fd99-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="0fd99-436">Fünf Ziffern, die der Anzahl von Tagen zwischen dem Datum 01/01/1867 und dem Geburtsdatum der einzelnen Personen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="0fd99-437">Drei Ziffern, die der durch Zufall generierten Zahl entsprechen, um Personen zu unterscheiden, die am selben Tag geboren wurden</span><span class="sxs-lookup"><span data-stu-id="0fd99-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="0fd99-438">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0fd99-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-439">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-439">Checksum</span></span>

<span data-ttu-id="0fd99-440">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-441">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-441">Definition</span></span>

<span data-ttu-id="0fd99-442">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-443">Die- `Func_hungary_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-444">Ein Schlüsselwort `Keywords_hungary_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-445">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-446">Die- `Func_hungary_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-447">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="0fd99-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-449">ungarische Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="0fd99-450">Ungarisch Zinn</span><span class="sxs-lookup"><span data-stu-id="0fd99-450">hungarian tin</span></span>
  
<span data-ttu-id="0fd99-451">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-451">tax id number</span></span>
  
<span data-ttu-id="0fd99-452">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-452">vat number</span></span>
  
<span data-ttu-id="0fd99-453">Steuerbehörde Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-453">tax authority no</span></span>
  
<span data-ttu-id="0fd99-454">USt-ID-Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-454">tax id tax identity number</span></span>
  
<span data-ttu-id="0fd99-455">taxidnumber#</span><span class="sxs-lookup"><span data-stu-id="0fd99-455">taxidnumber#</span></span>
  
<span data-ttu-id="0fd99-456">Zinn</span><span class="sxs-lookup"><span data-stu-id="0fd99-456">tin#</span></span>
  
<span data-ttu-id="0fd99-457">hungatiantin#</span><span class="sxs-lookup"><span data-stu-id="0fd99-457">hungatiantin#</span></span>
  
<span data-ttu-id="0fd99-458">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-458">tax identification no</span></span>
  
<span data-ttu-id="0fd99-459">taxidno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-459">taxidno#</span></span>
  
<span data-ttu-id="0fd99-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="0fd99-460">adóazonosító szám</span></span>
  
<span data-ttu-id="0fd99-461">adószám</span><span class="sxs-lookup"><span data-stu-id="0fd99-461">adószám</span></span>
  
<span data-ttu-id="0fd99-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="0fd99-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="0fd99-463">Irland</span><span class="sxs-lookup"><span data-stu-id="0fd99-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-464">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-464">Format</span></span>

<span data-ttu-id="0fd99-465">Sieben Ziffern, gefolgt von einem Buchstaben ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-466">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-466">Pattern</span></span>

<span data-ttu-id="0fd99-467">Sieben Ziffern, gefolgt von einem Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="0fd99-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="0fd99-468">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0fd99-468">Seven digits</span></span> 
    
- <span data-ttu-id="0fd99-469">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0fd99-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-470">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-470">Checksum</span></span>

<span data-ttu-id="0fd99-471">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fd99-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-472">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-472">Definition</span></span>

<span data-ttu-id="0fd99-473">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-474">Die- `Func_ireland_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-475">Ein Schlüsselwort `Keywords_ireland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-476">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-477">Die- `Func_ireland_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-478">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="0fd99-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-480">öffentlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-480">public service no</span></span>
  
<span data-ttu-id="0fd99-481">persönlicher öffentlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-481">personal public service no</span></span>
  
<span data-ttu-id="0fd99-482">PPS Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-482">pps no</span></span>
  
<span data-ttu-id="0fd99-483">persönlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-483">personal service no</span></span>
  
<span data-ttu-id="0fd99-484">PPS-Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-484">pps service no</span></span>
  
<span data-ttu-id="0fd99-485">ppsno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-485">ppsno#</span></span>
  
<span data-ttu-id="0fd99-486">irische PPS Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-486">irish pps no</span></span>
  
<span data-ttu-id="0fd99-487">publicserviceno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-487">publicserviceno#</span></span>
  
<span data-ttu-id="0fd99-488">persönliche öffentliche Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-488">personal public service number</span></span>
  
<span data-ttu-id="0fd99-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="0fd99-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="0fd99-490">PPS-uimh</span><span class="sxs-lookup"><span data-stu-id="0fd99-490">pps uimh</span></span>
  
<span data-ttu-id="0fd99-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="0fd99-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="0fd99-492">Italien</span><span class="sxs-lookup"><span data-stu-id="0fd99-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-493">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-493">Format</span></span>

<span data-ttu-id="0fd99-494">16 Buchstaben und Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-495">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-495">Pattern</span></span>

<span data-ttu-id="0fd99-496">16 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0fd99-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="0fd99-497">Drei Buchstaben, die den ersten drei Konsonanten im Familiennamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="0fd99-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="0fd99-498">Drei Buchstaben, die den ersten, dritten und vierten Konsonanten im Vornamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="0fd99-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="0fd99-499">Zwei Ziffern, die den letzten Ziffern des Geburtsjahres entsprechen</span><span class="sxs-lookup"><span data-stu-id="0fd99-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="0fd99-500">Eine Ziffer, die dem Monat der Geburt entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben a bis E, H, L, M, P, R bis T werden verwendet (der Januar ist also a und Oktober ist r).</span><span class="sxs-lookup"><span data-stu-id="0fd99-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="0fd99-501">Zwei Ziffern, die dem Tag des Geburtsmonats entsprechen, in dem 40 dem Tag der Geburt hinzugefügt wird, damit weibliche Personen von Männern unterscheiden können</span><span class="sxs-lookup"><span data-stu-id="0fd99-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="0fd99-502">Vier Ziffern, die einer Ortskennzahl entsprechen, die für die Gemeinde spezifisch ist, in der die Person geboren wurde – landesweite Codes werden für fremde Länder verwendet</span><span class="sxs-lookup"><span data-stu-id="0fd99-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="0fd99-503">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0fd99-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-504">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-504">Checksum</span></span>

<span data-ttu-id="0fd99-505">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-506">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-506">Definition</span></span>

<span data-ttu-id="0fd99-507">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-508">Die- `Func_italy_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-509">Ein Schlüsselwort `Keywords_italy_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-510">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-511">Die- `Func_italy_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-512">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="0fd99-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-514">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-514">tax number</span></span>
  
<span data-ttu-id="0fd99-515">Steuer-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-515">tax no.</span></span>
  
<span data-ttu-id="0fd99-516">taxno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-516">taxno#</span></span>
  
<span data-ttu-id="0fd99-517">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="0fd99-517">taxnumber#</span></span>
  
<span data-ttu-id="0fd99-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0fd99-518">taxnumber</span></span>
  
<span data-ttu-id="0fd99-519">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-519">tax id</span></span>
  
<span data-ttu-id="0fd99-520">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-520">taxid#</span></span>
  
<span data-ttu-id="0fd99-521">Geschäftscode</span><span class="sxs-lookup"><span data-stu-id="0fd99-521">fiscal code</span></span>
  
<span data-ttu-id="0fd99-522">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="0fd99-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="0fd99-523">Lettland</span><span class="sxs-lookup"><span data-stu-id="0fd99-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-524">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-524">Format</span></span>

<span data-ttu-id="0fd99-525">11 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-526">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-526">Pattern</span></span>

<span data-ttu-id="0fd99-527">11 Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="0fd99-528">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="0fd99-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="0fd99-529">Eine Ziffer, die dem Jahrhundert der Geburt entspricht, wobei "0" dem 19. Jahrhundert entspricht, "1" entspricht dem 20. Jahrhundert, und "2" entspricht dem 21. Jahrhundert</span><span class="sxs-lookup"><span data-stu-id="0fd99-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="0fd99-530">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-531">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-531">Checksum</span></span>

<span data-ttu-id="0fd99-532">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-533">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-533">Definition</span></span>

<span data-ttu-id="0fd99-534">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-535">Die- `Func_latvia_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-536">Ein Schlüsselwort `Keywords_latvia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-537">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-538">Die- `Func_latvia_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-539">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="0fd99-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-541">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-541">tax number</span></span>
  
<span data-ttu-id="0fd99-542">Steuer-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-542">tax no.</span></span>
  
<span data-ttu-id="0fd99-543">taxno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-543">taxno#</span></span>
  
<span data-ttu-id="0fd99-544">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="0fd99-544">taxnumber#</span></span>
  
<span data-ttu-id="0fd99-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0fd99-545">taxnumber</span></span>
  
<span data-ttu-id="0fd99-546">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-546">tax id</span></span>
  
<span data-ttu-id="0fd99-547">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-547">taxid#</span></span>
  
<span data-ttu-id="0fd99-548">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-548">tax identification number</span></span>
  
<span data-ttu-id="0fd99-549">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-549">tax identification no.</span></span>
  
<span data-ttu-id="0fd99-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="0fd99-550">nodokļa numurs</span></span>
  
<span data-ttu-id="0fd99-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="0fd99-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="0fd99-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="0fd99-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="0fd99-553">Litauen</span><span class="sxs-lookup"><span data-stu-id="0fd99-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-554">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-554">Format</span></span>

<span data-ttu-id="0fd99-555">11 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-556">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-556">Pattern</span></span>

<span data-ttu-id="0fd99-557">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fd99-558">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-558">Checksum</span></span>

<span data-ttu-id="0fd99-559">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fd99-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-560">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-560">Definition</span></span>

<span data-ttu-id="0fd99-561">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-562">Die- `Func_lithuania_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-563">Ein Schlüsselwort `Keywords_lithuania_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-564">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-565">Die- `Func_lithuania_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-566">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="0fd99-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-568">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-568">tax number</span></span>
  
<span data-ttu-id="0fd99-569">Steuer-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-569">tax no.</span></span>
  
<span data-ttu-id="0fd99-570">Steuernummer #</span><span class="sxs-lookup"><span data-stu-id="0fd99-570">tax no#</span></span>
  
<span data-ttu-id="0fd99-571">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="0fd99-571">taxnumber#</span></span>
  
<span data-ttu-id="0fd99-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0fd99-572">taxnumber</span></span>
  
<span data-ttu-id="0fd99-573">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-573">tax id</span></span>
  
<span data-ttu-id="0fd99-574">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-574">taxid#</span></span>
  
<span data-ttu-id="0fd99-575">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-575">tax identification number</span></span>
  
<span data-ttu-id="0fd99-576">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-576">tax identification no.</span></span>
  
<span data-ttu-id="0fd99-577">mokesčių-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-577">mokesčių id</span></span>
  
<span data-ttu-id="0fd99-578">mokesčių Numeris</span><span class="sxs-lookup"><span data-stu-id="0fd99-578">mokesčių numeris</span></span>
  
<span data-ttu-id="0fd99-579">mokesčių identifikavimas Numeris</span><span class="sxs-lookup"><span data-stu-id="0fd99-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="0fd99-580">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="0fd99-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-581">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-581">Format</span></span>

<span data-ttu-id="0fd99-582">13 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-583">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-583">Pattern</span></span>

<span data-ttu-id="0fd99-584">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0fd99-584">13 digits:</span></span>
  
-  <span data-ttu-id="0fd99-585">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-585">11 digits</span></span> 
    
- <span data-ttu-id="0fd99-586">Zwei Prüfziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-587">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-587">Checksum</span></span>

<span data-ttu-id="0fd99-588">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-589">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-589">Definition</span></span>

<span data-ttu-id="0fd99-590">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-591">Die- `Func_luxemburg_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-592">Ein Schlüsselwort `Keywords_luxemburg_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-593">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-594">Die- `Func_luxemburg_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-595">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="0fd99-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-597">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-597">tax number</span></span>
  
<span data-ttu-id="0fd99-598">Steuer-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-598">tax no.</span></span>
  
<span data-ttu-id="0fd99-599">taxno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-599">taxno#</span></span>
  
<span data-ttu-id="0fd99-600">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="0fd99-600">taxnumber#</span></span>
  
<span data-ttu-id="0fd99-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0fd99-601">taxnumber</span></span>
  
<span data-ttu-id="0fd99-602">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-602">tax id</span></span>
  
<span data-ttu-id="0fd99-603">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-603">taxid#</span></span>
  
<span data-ttu-id="0fd99-604">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-604">tax identification number</span></span>
  
<span data-ttu-id="0fd99-605">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-605">tax identification no.</span></span>
  
<span data-ttu-id="0fd99-606">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-606">steuernummer</span></span>
  
<span data-ttu-id="0fd99-607">Ingo-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-607">steuer id</span></span>
  
<span data-ttu-id="0fd99-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="0fd99-609">Malta</span><span class="sxs-lookup"><span data-stu-id="0fd99-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-610">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-610">Format</span></span>

<span data-ttu-id="0fd99-611">Für maltesische Staatsangehörige: 7 Ziffern und ein Buchstabe im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="0fd99-612">Nicht-maltesische Staatsangehörige und maltesische Entitäten: 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-613">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-613">Pattern</span></span>

<span data-ttu-id="0fd99-614">Maltesische Staatsangehörige: 7 Ziffern und ein Buchstaben</span><span class="sxs-lookup"><span data-stu-id="0fd99-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="0fd99-615">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0fd99-615">Seven digits</span></span> 
    
- <span data-ttu-id="0fd99-616">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0fd99-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="0fd99-617">Nicht-maltesische Staatsangehörige und maltesische Entitäten: 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="0fd99-618">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="0fd99-619">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-619">Checksum</span></span>

<span data-ttu-id="0fd99-620">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fd99-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-621">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-621">Definition</span></span>

<span data-ttu-id="0fd99-622">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-623">Die- `Func_malta_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-624">Ein Schlüsselwort `Keywords_malta_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-625">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-626">Die- `Func_malta_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-627">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="0fd99-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-629">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-629">tax number</span></span>
  
<span data-ttu-id="0fd99-630">Steuer-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-630">tax no.</span></span>
  
<span data-ttu-id="0fd99-631">taxno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-631">taxno#</span></span>
  
<span data-ttu-id="0fd99-632">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="0fd99-632">taxnumber#</span></span>
  
<span data-ttu-id="0fd99-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0fd99-633">taxnumber</span></span>
  
<span data-ttu-id="0fd99-634">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-634">tax id</span></span>
  
<span data-ttu-id="0fd99-635">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-635">taxid#</span></span>
  
<span data-ttu-id="0fd99-636">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-636">tax identification number</span></span>
  
<span data-ttu-id="0fd99-637">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-637">tax identification no.</span></span>
  
<span data-ttu-id="0fd99-638">numru tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="0fd99-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="0fd99-639">ID tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="0fd99-639">id tat-taxxa</span></span>
  
<span data-ttu-id="0fd99-640">numru ta ' identifikazzjoni tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="0fd99-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="0fd99-641">Niederlande</span><span class="sxs-lookup"><span data-stu-id="0fd99-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-642">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-642">Format</span></span>

<span data-ttu-id="0fd99-643">Neun Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-644">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-644">Pattern</span></span>

<span data-ttu-id="0fd99-645">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="0fd99-646">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-646">Checksum</span></span>

<span data-ttu-id="0fd99-647">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-648">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-648">Definition</span></span>

<span data-ttu-id="0fd99-649">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-650">Die- `Func_netherlands_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-651">Ein Schlüsselwort `Keywords_netherlands_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-652">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-653">Die- `Func_netherlands_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-654">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="0fd99-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-656">niederländische Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="0fd99-657">niederländische Steueridentifikation</span><span class="sxs-lookup"><span data-stu-id="0fd99-657">netherlands tax identification</span></span>
  
<span data-ttu-id="0fd99-658">niederländische Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="0fd99-659">niederländische Steueridentifikation</span><span class="sxs-lookup"><span data-stu-id="0fd99-659">netherland's tax identification</span></span>
  
<span data-ttu-id="0fd99-660">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-660">tax identification number</span></span>
  
<span data-ttu-id="0fd99-661">niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-661">dutch tax id</span></span>
  
<span data-ttu-id="0fd99-662">niederländische Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-662">dutch tax identification number</span></span>
  
<span data-ttu-id="0fd99-663">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-663">tax id</span></span>
  
<span data-ttu-id="0fd99-664">Steuer-ID #</span><span class="sxs-lookup"><span data-stu-id="0fd99-664">tax id#</span></span>
  
<span data-ttu-id="0fd99-665">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-665">tax number</span></span>
  
<span data-ttu-id="0fd99-666">Steuernummer #</span><span class="sxs-lookup"><span data-stu-id="0fd99-666">tax no#</span></span>
  
<span data-ttu-id="0fd99-667">Steuer</span><span class="sxs-lookup"><span data-stu-id="0fd99-667">tax#</span></span>
  
<span data-ttu-id="0fd99-668">Zinn</span><span class="sxs-lookup"><span data-stu-id="0fd99-668">tin</span></span>
  
<span data-ttu-id="0fd99-669">Zinn</span><span class="sxs-lookup"><span data-stu-id="0fd99-669">tin#</span></span>
  
<span data-ttu-id="0fd99-670">Niederlande Tin</span><span class="sxs-lookup"><span data-stu-id="0fd99-670">netherlands tin</span></span>
  
<span data-ttu-id="0fd99-671">niederländische Zinn</span><span class="sxs-lookup"><span data-stu-id="0fd99-671">netherland's tin</span></span>
  
<span data-ttu-id="0fd99-672">Nederlands belasten identificatienummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="0fd99-673">identificatienummer van belasten</span><span class="sxs-lookup"><span data-stu-id="0fd99-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="0fd99-674">identificatienummer-Belastungen</span><span class="sxs-lookup"><span data-stu-id="0fd99-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="0fd99-675">Nederlands belasten identificatie</span><span class="sxs-lookup"><span data-stu-id="0fd99-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="0fd99-676">Nederlands Belasting ID Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="0fd99-677">Nederlands belastingnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="0fd99-678">BTW Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-678">btw nummer</span></span>
  
<span data-ttu-id="0fd99-679">Nederlandse belasten von identificatie</span><span class="sxs-lookup"><span data-stu-id="0fd99-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="0fd99-680">Polen</span><span class="sxs-lookup"><span data-stu-id="0fd99-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-681">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-681">Format</span></span>

<span data-ttu-id="0fd99-682">Elf Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-683">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-683">Pattern</span></span>

<span data-ttu-id="0fd99-684">Elf Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fd99-685">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-685">Checksum</span></span>

<span data-ttu-id="0fd99-686">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-687">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-687">Definition</span></span>

<span data-ttu-id="0fd99-688">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-689">Die- `Func_poland_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-690">Ein Schlüsselwort `Keywords_poland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-691">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-692">Die- `Func_poland_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-693">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="0fd99-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-695">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-695">tax number</span></span>
  
<span data-ttu-id="0fd99-696">Steuer-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-696">tax no.</span></span>
  
<span data-ttu-id="0fd99-697">taxno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-697">taxno#</span></span>
  
<span data-ttu-id="0fd99-698">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="0fd99-698">taxnumber#</span></span>
  
<span data-ttu-id="0fd99-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0fd99-699">taxnumber</span></span>
  
<span data-ttu-id="0fd99-700">NIP</span><span class="sxs-lookup"><span data-stu-id="0fd99-700">nip</span></span>
  
<span data-ttu-id="0fd99-701">NIP</span><span class="sxs-lookup"><span data-stu-id="0fd99-701">nip#</span></span>
  
<span data-ttu-id="0fd99-702">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-702">tax id</span></span>
  
<span data-ttu-id="0fd99-703">Steuer-ID #</span><span class="sxs-lookup"><span data-stu-id="0fd99-703">tax id#</span></span>
  
<span data-ttu-id="0fd99-704">NIP-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-704">nip id</span></span>
  
<span data-ttu-id="0fd99-705">NIP-ID #</span><span class="sxs-lookup"><span data-stu-id="0fd99-705">nip id#</span></span>
  
<span data-ttu-id="0fd99-706">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-706">tax identification number</span></span>
  
<span data-ttu-id="0fd99-707">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-707">tax identification no.</span></span>
  
<span data-ttu-id="0fd99-708">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-708">vat number</span></span>
  
<span data-ttu-id="0fd99-709">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-709">vat no.</span></span>
  
<span data-ttu-id="0fd99-710">vatno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-710">vatno#</span></span>
  
<span data-ttu-id="0fd99-711">USt-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-711">vat id</span></span>
  
<span data-ttu-id="0fd99-712">USt-ID #</span><span class="sxs-lookup"><span data-stu-id="0fd99-712">vat id#</span></span>
  
<span data-ttu-id="0fd99-713">Numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="0fd99-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="0fd99-714">Polski Numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="0fd99-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="0fd99-715">numeridentyfikacjipodatkowej#</span><span class="sxs-lookup"><span data-stu-id="0fd99-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="0fd99-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="0fd99-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-717">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-717">Format</span></span>

<span data-ttu-id="0fd99-718">Neun Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-719">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-719">Pattern</span></span>

<span data-ttu-id="0fd99-720">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fd99-721">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-721">Checksum</span></span>

<span data-ttu-id="0fd99-722">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-723">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-723">Definition</span></span>

<span data-ttu-id="0fd99-724">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-725">Die- `Func_portugal_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-726">Ein Schlüsselwort `Keywords_portugal_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-727">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-728">Die- `Func_portugal_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-729">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="0fd99-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-731">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-731">tax number</span></span>
  
<span data-ttu-id="0fd99-732">Steuer-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-732">tax no.</span></span>
  
<span data-ttu-id="0fd99-733">taxno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-733">taxno#</span></span>
  
<span data-ttu-id="0fd99-734">taxnumber#</span><span class="sxs-lookup"><span data-stu-id="0fd99-734">taxnumber#</span></span>
  
<span data-ttu-id="0fd99-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0fd99-735">taxnumber</span></span>
  
<span data-ttu-id="0fd99-736">NIF</span><span class="sxs-lookup"><span data-stu-id="0fd99-736">nif</span></span>
  
<span data-ttu-id="0fd99-737">NIF</span><span class="sxs-lookup"><span data-stu-id="0fd99-737">nif#</span></span>
  
<span data-ttu-id="0fd99-738">numerisch-Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="0fd99-738">numero fiscal</span></span>
  
<span data-ttu-id="0fd99-739">número de identificação Fiscal</span><span class="sxs-lookup"><span data-stu-id="0fd99-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="0fd99-740">Rumänien</span><span class="sxs-lookup"><span data-stu-id="0fd99-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-741">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-741">Format</span></span>

<span data-ttu-id="0fd99-742">13 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-743">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-743">Pattern</span></span>

<span data-ttu-id="0fd99-744">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fd99-745">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-745">Checksum</span></span>

<span data-ttu-id="0fd99-746">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fd99-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-747">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-747">Definition</span></span>

<span data-ttu-id="0fd99-748">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-749">Der reguläre Ausdruck `Regex_romania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-750">Ein Schlüsselwort `Keywords_romania_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fd99-751">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="0fd99-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-753">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-753">tax id</span></span>
  
<span data-ttu-id="0fd99-754">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-754">tax id number</span></span>
  
<span data-ttu-id="0fd99-755">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-755">tax file no</span></span>
  
<span data-ttu-id="0fd99-756">tax file number</span><span class="sxs-lookup"><span data-stu-id="0fd99-756">tax file number</span></span>
  
<span data-ttu-id="0fd99-757">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-757">tax no</span></span>
  
<span data-ttu-id="0fd99-758">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-758">tax number</span></span>
  
<span data-ttu-id="0fd99-759">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-759">taxid#</span></span>
  
<span data-ttu-id="0fd99-760">taxno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-760">taxno#</span></span>
  
<span data-ttu-id="0fd99-761">ID-UL taxei</span><span class="sxs-lookup"><span data-stu-id="0fd99-761">id-ul taxei</span></span>
  
<span data-ttu-id="0fd99-762">numărul de identificare fiscală</span><span class="sxs-lookup"><span data-stu-id="0fd99-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="0fd99-763">Slowakei</span><span class="sxs-lookup"><span data-stu-id="0fd99-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-764">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-764">Format</span></span>

<span data-ttu-id="0fd99-765">10 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-766">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-766">Pattern</span></span>

<span data-ttu-id="0fd99-767">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fd99-768">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-768">Checksum</span></span>

<span data-ttu-id="0fd99-769">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0fd99-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-770">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-770">Definition</span></span>

<span data-ttu-id="0fd99-771">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-772">Der reguläre Ausdruck `Regex_slovakia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-773">Ein Schlüsselwort `Keywords_slovakia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fd99-774">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="0fd99-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-776">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-776">tax id</span></span>
  
<span data-ttu-id="0fd99-777">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-777">tax id number</span></span>
  
<span data-ttu-id="0fd99-778">Tin-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-778">tin id</span></span>
  
<span data-ttu-id="0fd99-779">Tin Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-779">tin no</span></span>
  
<span data-ttu-id="0fd99-780">Slowakische Tin-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-780">slovakian tin id</span></span>
  
<span data-ttu-id="0fd99-781">Zinn</span><span class="sxs-lookup"><span data-stu-id="0fd99-781">tin</span></span>
  
<span data-ttu-id="0fd99-782">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-782">tax file no</span></span>
  
<span data-ttu-id="0fd99-783">tax file number</span><span class="sxs-lookup"><span data-stu-id="0fd99-783">tax file number</span></span>
  
<span data-ttu-id="0fd99-784">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-784">tax no</span></span>
  
<span data-ttu-id="0fd99-785">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-785">tax number</span></span>
  
<span data-ttu-id="0fd99-786">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-786">taxid#</span></span>
  
<span data-ttu-id="0fd99-787">taxno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-787">taxno#</span></span>
  
<span data-ttu-id="0fd99-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="0fd99-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="0fd99-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="0fd99-789">daňové číslo</span></span>
  
<span data-ttu-id="0fd99-790">Daňové číslo SÚBORU</span><span class="sxs-lookup"><span data-stu-id="0fd99-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="0fd99-791">Slowenien</span><span class="sxs-lookup"><span data-stu-id="0fd99-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-792">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-792">Format</span></span>

<span data-ttu-id="0fd99-793">Acht Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-794">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-794">Pattern</span></span>

<span data-ttu-id="0fd99-795">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fd99-796">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-796">Checksum</span></span>

<span data-ttu-id="0fd99-797">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-798">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-798">Definition</span></span>

<span data-ttu-id="0fd99-799">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-800">Die- `Func_slovenia_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-801">Ein Schlüsselwort `Keywords_slovenia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-802">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-803">Die- `Func_slovenia_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-804">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="0fd99-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-806">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-806">tax id</span></span>
  
<span data-ttu-id="0fd99-807">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-807">tax id number</span></span>
  
<span data-ttu-id="0fd99-808">Tin-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-808">tin id</span></span>
  
<span data-ttu-id="0fd99-809">Tin Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-809">tin no</span></span>
  
<span data-ttu-id="0fd99-810">slowenische Tin-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-810">slovenian tin id</span></span>
  
<span data-ttu-id="0fd99-811">Zinn</span><span class="sxs-lookup"><span data-stu-id="0fd99-811">tin</span></span>
  
<span data-ttu-id="0fd99-812">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-812">tax file no</span></span>
  
<span data-ttu-id="0fd99-813">tax file number</span><span class="sxs-lookup"><span data-stu-id="0fd99-813">tax file number</span></span>
  
<span data-ttu-id="0fd99-814">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-814">tax no</span></span>
  
<span data-ttu-id="0fd99-815">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-815">tax number</span></span>
  
<span data-ttu-id="0fd99-816">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-816">taxid#</span></span>
  
<span data-ttu-id="0fd99-817">taxno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-817">taxno#</span></span>
  
<span data-ttu-id="0fd99-818">identifikacijska številka beim Davka</span><span class="sxs-lookup"><span data-stu-id="0fd99-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="0fd99-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="0fd99-819">davčna številka</span></span>
  
<span data-ttu-id="0fd99-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="0fd99-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="0fd99-821">Spanien</span><span class="sxs-lookup"><span data-stu-id="0fd99-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-822">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-822">Format</span></span>

<span data-ttu-id="0fd99-823">Sieben oder acht Ziffern und ein oder zwei Buchstaben im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-824">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-824">Pattern</span></span>

<span data-ttu-id="0fd99-825">Spanisch natürliche Personen mit einem nationalen spanischen Identitätsausweis:</span><span class="sxs-lookup"><span data-stu-id="0fd99-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="0fd99-826">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-826">Eight digits</span></span> 
    
- <span data-ttu-id="0fd99-827">Ein Großbuchstabe (Unterscheidung nach Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0fd99-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="0fd99-828">Nicht-residente Spanier ohne einen nationalen Identitätsausweis in Spanien</span><span class="sxs-lookup"><span data-stu-id="0fd99-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="0fd99-829">Ein Großbuchstabe "L" (Unterscheidung nach Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0fd99-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="0fd99-830">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0fd99-830">Seven digits</span></span>
    
- <span data-ttu-id="0fd99-831">Ein Großbuchstabe (Unterscheidung nach Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0fd99-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="0fd99-832">Ansässige Spanier unter 14 Jahren ohne einen nationalen spanischen Identitätsausweis:</span><span class="sxs-lookup"><span data-stu-id="0fd99-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="0fd99-833">Ein Großbuchstabe "K" (Unterscheidung nach Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0fd99-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="0fd99-834">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0fd99-834">Seven digits</span></span> 
    
- <span data-ttu-id="0fd99-835">Ein Großbuchstabe (Unterscheidung nach Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0fd99-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="0fd99-836">Ausländer mit Identifikationsnummer eines Ausländers</span><span class="sxs-lookup"><span data-stu-id="0fd99-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="0fd99-837">Ein Großbuchstabe mit "X", "Y" oder "Z" (Groß-/Kleinschreibung wird beachtet)</span><span class="sxs-lookup"><span data-stu-id="0fd99-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="0fd99-838">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0fd99-838">Seven digits</span></span>
    
- <span data-ttu-id="0fd99-839">Ein Großbuchstabe (Unterscheidung nach Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0fd99-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="0fd99-840">Ausländer ohne Identifikationsnummer eines Ausländers</span><span class="sxs-lookup"><span data-stu-id="0fd99-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="0fd99-841">Ein Großbuchstabe, der "M" ist (Groß-/Kleinschreibung beachten)</span><span class="sxs-lookup"><span data-stu-id="0fd99-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="0fd99-842">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0fd99-842">Seven digits</span></span>
    
- <span data-ttu-id="0fd99-843">Ein Großbuchstabe (Unterscheidung nach Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0fd99-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="0fd99-844">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-844">Checksum</span></span>

<span data-ttu-id="0fd99-845">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-846">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-846">Definition</span></span>

<span data-ttu-id="0fd99-847">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-848">Die- `Func_spain_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-849">Ein Schlüsselwort `Keywords_spain_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-850">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-851">Die- `Func_spain_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-852">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="0fd99-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-854">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-854">tax id</span></span>
  
<span data-ttu-id="0fd99-855">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-855">tax id number</span></span>
  
<span data-ttu-id="0fd99-856">CIF-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-856">cif id</span></span>
  
<span data-ttu-id="0fd99-857">CIF Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-857">cif no</span></span>
  
<span data-ttu-id="0fd99-858">spanische CIF-ID</span><span class="sxs-lookup"><span data-stu-id="0fd99-858">spanish cif id</span></span>
  
<span data-ttu-id="0fd99-859">CIF</span><span class="sxs-lookup"><span data-stu-id="0fd99-859">cif</span></span>
  
<span data-ttu-id="0fd99-860">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-860">tax file no</span></span>
  
<span data-ttu-id="0fd99-861">spanische CIF-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-861">spanish cif number</span></span>
  
<span data-ttu-id="0fd99-862">tax file number</span><span class="sxs-lookup"><span data-stu-id="0fd99-862">tax file number</span></span>
  
<span data-ttu-id="0fd99-863">Spanisch CIF Nein</span><span class="sxs-lookup"><span data-stu-id="0fd99-863">spanish cif no</span></span>
  
<span data-ttu-id="0fd99-864">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-864">tax no</span></span>
  
<span data-ttu-id="0fd99-865">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-865">tax number</span></span>
  
<span data-ttu-id="0fd99-866">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-866">taxid#</span></span>
  
<span data-ttu-id="0fd99-867">taxno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-867">taxno#</span></span>
  
<span data-ttu-id="0fd99-868">cifid#</span><span class="sxs-lookup"><span data-stu-id="0fd99-868">cifid#</span></span>
  
<span data-ttu-id="0fd99-869">spanishcifid#</span><span class="sxs-lookup"><span data-stu-id="0fd99-869">spanishcifid#</span></span>
  
<span data-ttu-id="0fd99-870">spanishcifno#</span><span class="sxs-lookup"><span data-stu-id="0fd99-870">spanishcifno#</span></span>
  
<span data-ttu-id="0fd99-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="0fd99-871">número de contribuyente</span></span>
  
<span data-ttu-id="0fd99-872">número de Impuesto Corporativo</span><span class="sxs-lookup"><span data-stu-id="0fd99-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="0fd99-873">número de Identificación Fiscal</span><span class="sxs-lookup"><span data-stu-id="0fd99-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="0fd99-874">CIF-número</span><span class="sxs-lookup"><span data-stu-id="0fd99-874">cif número</span></span>
  
<span data-ttu-id="0fd99-875">cifnúmero#</span><span class="sxs-lookup"><span data-stu-id="0fd99-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="0fd99-876">Schweden</span><span class="sxs-lookup"><span data-stu-id="0fd99-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-877">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-877">Format</span></span>

<span data-ttu-id="0fd99-878">Zehn Ziffern und ein Symbol im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-879">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-879">Pattern</span></span>

<span data-ttu-id="0fd99-880">Zehn Ziffern und ein Symbol:</span><span class="sxs-lookup"><span data-stu-id="0fd99-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="0fd99-881">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="0fd99-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="0fd99-882">Pluszeichen, Minuszeichen oder Backslash</span><span class="sxs-lookup"><span data-stu-id="0fd99-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="0fd99-883">Drei Ziffern, die die Identifikationsnummer eindeutig machen:</span><span class="sxs-lookup"><span data-stu-id="0fd99-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="0fd99-884">Für Zahlen, die vor 1990 ausgegeben wurden, identifizieren die siebte und die achte Ziffer den Geburts Kreis oder den in der fremde geborenen Personen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="0fd99-885">Die Ziffer in der neunten Position gibt das Geschlecht entweder ungerade für männliche oder sogar für weiblich an.</span><span class="sxs-lookup"><span data-stu-id="0fd99-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="0fd99-886">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0fd99-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fd99-887">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-887">Checksum</span></span>

<span data-ttu-id="0fd99-888">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-889">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-889">Definition</span></span>

<span data-ttu-id="0fd99-890">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-891">Die- `Func_sweden_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-892">Ein Schlüsselwort `Keywords_sweden_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fd99-893">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-894">Die- `Func_sweden_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fd99-895">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="0fd99-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-897">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-897">tax id</span></span>
  
<span data-ttu-id="0fd99-898">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-898">tax id no.</span></span>
  
<span data-ttu-id="0fd99-899">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-899">tax id number</span></span>
  
<span data-ttu-id="0fd99-900">tax identification</span><span class="sxs-lookup"><span data-stu-id="0fd99-900">tax identification</span></span>
  
<span data-ttu-id="0fd99-901">Steueridentifikation #</span><span class="sxs-lookup"><span data-stu-id="0fd99-901">tax identification#</span></span>
  
<span data-ttu-id="0fd99-902">Steuer-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-902">tax no.</span></span>
  
<span data-ttu-id="0fd99-903">Steuer</span><span class="sxs-lookup"><span data-stu-id="0fd99-903">tax#</span></span>
  
<span data-ttu-id="0fd99-904">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-904">taxid#</span></span>
  
<span data-ttu-id="0fd99-905">Steuerdatei</span><span class="sxs-lookup"><span data-stu-id="0fd99-905">tax file</span></span>
  
<span data-ttu-id="0fd99-906">Steuerdatei-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-906">tax file no.</span></span>
  
<span data-ttu-id="0fd99-907">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-907">personal id number</span></span>
  
<span data-ttu-id="0fd99-908">Skate ID Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-908">skatt id nummer</span></span>
  
<span data-ttu-id="0fd99-909">skatt Identifikation</span><span class="sxs-lookup"><span data-stu-id="0fd99-909">skatt identifikation</span></span>
  
<span data-ttu-id="0fd99-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="0fd99-911">UK</span><span class="sxs-lookup"><span data-stu-id="0fd99-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="0fd99-912">Format</span><span class="sxs-lookup"><span data-stu-id="0fd99-912">Format</span></span>

<span data-ttu-id="0fd99-913">Unique Steuerzahler Referenz (UTR): 10 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0fd99-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="0fd99-914">Nationale Versicherungsnummer (Nino): Weitere Informationen finden Sie im Abschnitt "U.K.</span><span class="sxs-lookup"><span data-stu-id="0fd99-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="0fd99-915">Nationale Versicherungsnummer (Nino) "in [dem, wonach die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0fd99-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fd99-916">Muster</span><span class="sxs-lookup"><span data-stu-id="0fd99-916">Pattern</span></span>

<span data-ttu-id="0fd99-917">Unique Steuerzahler Referenz (UTR): 10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0fd99-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="0fd99-918">Nationale Versicherungsnummer (Nino): Weitere Informationen finden Sie im Abschnitt "U.K.</span><span class="sxs-lookup"><span data-stu-id="0fd99-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="0fd99-919">Nationale Versicherungsnummer (Nino) "in [dem, wonach die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0fd99-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fd99-920">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0fd99-920">Checksum</span></span>

<span data-ttu-id="0fd99-921">Ja</span><span class="sxs-lookup"><span data-stu-id="0fd99-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fd99-922">Definition</span><span class="sxs-lookup"><span data-stu-id="0fd99-922">Definition</span></span>

<span data-ttu-id="0fd99-923">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0fd99-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fd99-924">Die- `Func_uk_eu_tax_file_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0fd99-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fd99-925">Ein Schlüsselwort `Keywords_uk_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0fd99-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fd99-926">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0fd99-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="0fd99-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0fd99-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="0fd99-928">tax id</span><span class="sxs-lookup"><span data-stu-id="0fd99-928">tax id</span></span>
  
<span data-ttu-id="0fd99-929">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-929">tax id no.</span></span>
  
<span data-ttu-id="0fd99-930">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0fd99-930">tax id number</span></span>
  
<span data-ttu-id="0fd99-931">tax identification</span><span class="sxs-lookup"><span data-stu-id="0fd99-931">tax identification</span></span>
  
<span data-ttu-id="0fd99-932">Steueridentifikation #</span><span class="sxs-lookup"><span data-stu-id="0fd99-932">tax identification#</span></span>
  
<span data-ttu-id="0fd99-933">Steuer-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-933">tax no.</span></span>
  
<span data-ttu-id="0fd99-934">Steuer</span><span class="sxs-lookup"><span data-stu-id="0fd99-934">tax#</span></span>
  
<span data-ttu-id="0fd99-935">per Taxi #</span><span class="sxs-lookup"><span data-stu-id="0fd99-935">taxid#</span></span>
  
<span data-ttu-id="0fd99-936">Steuerdatei</span><span class="sxs-lookup"><span data-stu-id="0fd99-936">tax file</span></span>
  
<span data-ttu-id="0fd99-937">Steuerdatei-Nr.</span><span class="sxs-lookup"><span data-stu-id="0fd99-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0fd99-938">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fd99-938">See also</span></span>

[<span data-ttu-id="0fd99-939">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="0fd99-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

