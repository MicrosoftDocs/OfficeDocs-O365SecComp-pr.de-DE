---
title: EU-Steuernummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: In diesem Thema wird eine Data Loss Prevention (DLP) Richtlinie sieht für bei der Entdeckung des Typs der EU Steuernummer vertraulichen Informationen. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 5192496b393d15fd6d063e09c9bfe1cb3dd7e2dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529425"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="8aba5-104">EU-Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-104">EU Tax Identification Number</span></span>

<span data-ttu-id="8aba5-p102">In diesem Thema dargestellt was eine Data Loss Prevention (DLP)-Richtlinie für den Typ der EU Tax Identification-Nummer (US) vertrauliche Daten erkannt. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="8aba5-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="8aba5-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="8aba5-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-108">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-108">Format</span></span>

<span data-ttu-id="8aba5-109">Neun Ziffern mit bedingter Trennstrich und Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="8aba5-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-110">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-110">Pattern</span></span>

<span data-ttu-id="8aba5-111">Neun Ziffern mit bedingter Trennstrich und Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="8aba5-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="8aba5-112">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-112">Two digits</span></span> 
    
- <span data-ttu-id="8aba5-113">Ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="8aba5-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="8aba5-114">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-114">Three digits</span></span>
    
- <span data-ttu-id="8aba5-115">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="8aba5-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="8aba5-116">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-117">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-117">Checksum</span></span>

<span data-ttu-id="8aba5-118">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-119">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-119">Definition</span></span>

<span data-ttu-id="8aba5-120">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-121">Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-122">Ein Schlüsselwort aus `Keywords_austria_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-123">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-124">Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-125">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="8aba5-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-127">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-127">tax number</span></span>
  
<span data-ttu-id="8aba5-128">Anzahl</span><span class="sxs-lookup"><span data-stu-id="8aba5-128">number</span></span>
  
<span data-ttu-id="8aba5-129">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-129">tax registration number</span></span>
  
<span data-ttu-id="8aba5-130">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-130">tax id</span></span>
  
<span data-ttu-id="8aba5-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="8aba5-131">st.nr.</span></span>
  
<span data-ttu-id="8aba5-132">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="8aba5-133">Belgien</span><span class="sxs-lookup"><span data-stu-id="8aba5-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-134">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-134">Format</span></span>

<span data-ttu-id="8aba5-135">11 Zahlen ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-136">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-136">Pattern</span></span>

<span data-ttu-id="8aba5-137">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="8aba5-137">11 digits:</span></span>
  
- <span data-ttu-id="8aba5-138">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-138">Two digits</span></span>
    
- <span data-ttu-id="8aba5-139">Eine "0" oder "1"</span><span class="sxs-lookup"><span data-stu-id="8aba5-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="8aba5-140">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="8aba5-140">One digit</span></span>
    
- <span data-ttu-id="8aba5-141">Eine "0" oder "1" oder "2" oder "3"</span><span class="sxs-lookup"><span data-stu-id="8aba5-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="8aba5-142">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-143">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-143">Checksum</span></span>

<span data-ttu-id="8aba5-144">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8aba5-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-145">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-145">Definition</span></span>

<span data-ttu-id="8aba5-146">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-147">Der reguläre Ausdruck `Regex_belgium_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-148">Ein Schlüsselwort aus `Keywords_belgium_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8aba5-149">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="8aba5-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-151">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-151">tax number</span></span>
  
<span data-ttu-id="8aba5-152">Nummer der Eintragung</span><span class="sxs-lookup"><span data-stu-id="8aba5-152">national registration number</span></span>
  
<span data-ttu-id="8aba5-153">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-153">tax registration number</span></span>
  
<span data-ttu-id="8aba5-154">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-154">tax id</span></span>
  
<span data-ttu-id="8aba5-155">if</span><span class="sxs-lookup"><span data-stu-id="8aba5-155">nif</span></span>
  
<span data-ttu-id="8aba5-156">if-</span><span class="sxs-lookup"><span data-stu-id="8aba5-156">nif#</span></span>
  
<span data-ttu-id="8aba5-157">Numéro de Registre national</span><span class="sxs-lookup"><span data-stu-id="8aba5-157">numéro de registre national</span></span>
  
<span data-ttu-id="8aba5-158">Numéro d ' Identification fiscale</span><span class="sxs-lookup"><span data-stu-id="8aba5-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="8aba5-159">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="8aba5-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-160">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-160">Format</span></span>

<span data-ttu-id="8aba5-161">Zehn Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-162">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-162">Pattern</span></span>

<span data-ttu-id="8aba5-163">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8aba5-164">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-164">Checksum</span></span>

<span data-ttu-id="8aba5-165">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-166">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-166">Definition</span></span>

<span data-ttu-id="8aba5-167">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-168">Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-169">Ein Schlüsselwort aus `Keywords_bulgaria_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-170">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-171">Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-172">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="8aba5-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-174">bucn</span><span class="sxs-lookup"><span data-stu-id="8aba5-174">bucn</span></span>
  
<span data-ttu-id="8aba5-175">Uniform der Anzahl</span><span class="sxs-lookup"><span data-stu-id="8aba5-175">uniform civil number</span></span>
  
<span data-ttu-id="8aba5-176">Bucn #</span><span class="sxs-lookup"><span data-stu-id="8aba5-176">bucn#</span></span>
  
<span data-ttu-id="8aba5-177">Uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="8aba5-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="8aba5-178">Uniform der id</span><span class="sxs-lookup"><span data-stu-id="8aba5-178">uniform civil id</span></span>
  
<span data-ttu-id="8aba5-179">Uniform der Nr.</span><span class="sxs-lookup"><span data-stu-id="8aba5-179">uniform civil no</span></span>
  
<span data-ttu-id="8aba5-180">egn</span><span class="sxs-lookup"><span data-stu-id="8aba5-180">egn</span></span>
  
<span data-ttu-id="8aba5-181">Bulgarisch uniform der Anzahl</span><span class="sxs-lookup"><span data-stu-id="8aba5-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="8aba5-182">Uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-182">uniformcivilno#</span></span>
  
<span data-ttu-id="8aba5-183">Egn #</span><span class="sxs-lookup"><span data-stu-id="8aba5-183">egn#</span></span>
  
<span data-ttu-id="8aba5-184">УНИФОРМ ГРАЖДАНСКИ НОМЕР</span><span class="sxs-lookup"><span data-stu-id="8aba5-184">униформ граждански номер</span></span>
  
<span data-ttu-id="8aba5-185">Униформ-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-185">униформ id</span></span>
  
<span data-ttu-id="8aba5-186">Униформ граждански-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-186">униформ граждански id</span></span>
  
<span data-ttu-id="8aba5-187">УНИФОРМ ГРАЖДАНСКИ НЕ</span><span class="sxs-lookup"><span data-stu-id="8aba5-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="8aba5-188">Kroatien</span><span class="sxs-lookup"><span data-stu-id="8aba5-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-189">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-189">Format</span></span>

<span data-ttu-id="8aba5-190">11 Zahlen ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-191">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-191">Pattern</span></span>

<span data-ttu-id="8aba5-192">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="8aba5-192">11 digits:</span></span>
  
- <span data-ttu-id="8aba5-193">Zehn Ziffern, zufällig ausgewählte</span><span class="sxs-lookup"><span data-stu-id="8aba5-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="8aba5-194">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8aba5-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-195">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-195">Checksum</span></span>

<span data-ttu-id="8aba5-196">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-197">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-197">Definition</span></span>

<span data-ttu-id="8aba5-198">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-199">Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-200">Ein Schlüsselwort aus `Keywords_croatia_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-201">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-202">Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-203">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="8aba5-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-205">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-205">tax number</span></span>
  
<span data-ttu-id="8aba5-206">tax</span><span class="sxs-lookup"><span data-stu-id="8aba5-206">tax</span></span>
  
<span data-ttu-id="8aba5-207">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-207">tax id</span></span>
  
<span data-ttu-id="8aba5-208">OID</span><span class="sxs-lookup"><span data-stu-id="8aba5-208">oid</span></span>
  
<span data-ttu-id="8aba5-209">OID-</span><span class="sxs-lookup"><span data-stu-id="8aba5-209">oid#</span></span>
  
<span data-ttu-id="8aba5-210">Porezni broj</span><span class="sxs-lookup"><span data-stu-id="8aba5-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="8aba5-211">Zypern</span><span class="sxs-lookup"><span data-stu-id="8aba5-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-212">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-212">Format</span></span>

<span data-ttu-id="8aba5-213">Acht Ziffern und einem Buchstaben in das angegebene Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-214">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-214">Pattern</span></span>

<span data-ttu-id="8aba5-215">Acht Ziffern und einem Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="8aba5-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="8aba5-216">EINE "0"</span><span class="sxs-lookup"><span data-stu-id="8aba5-216">A "0"</span></span> 
    
- <span data-ttu-id="8aba5-217">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="8aba5-217">Seven digits</span></span>
    
- <span data-ttu-id="8aba5-218">Ein Buchstabe (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8aba5-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-219">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-219">Checksum</span></span>

<span data-ttu-id="8aba5-220">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8aba5-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-221">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-221">Definition</span></span>

<span data-ttu-id="8aba5-222">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-223">Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-224">Ein Schlüsselwort aus `Keywords_cyprus_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-225">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-226">Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-227">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="8aba5-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-229">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-229">tax number</span></span>
  
<span data-ttu-id="8aba5-230">tax</span><span class="sxs-lookup"><span data-stu-id="8aba5-230">tax</span></span>
  
<span data-ttu-id="8aba5-231">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-231">tax id</span></span>
  
<span data-ttu-id="8aba5-232">Tax Kenncode</span><span class="sxs-lookup"><span data-stu-id="8aba5-232">tax identification code</span></span>
  
<span data-ttu-id="8aba5-233">Teilstrichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-233">tic</span></span>
  
<span data-ttu-id="8aba5-234">Teilstrichen #</span><span class="sxs-lookup"><span data-stu-id="8aba5-234">tic#</span></span>
  
<span data-ttu-id="8aba5-235">ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="8aba5-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="8aba5-236">ΦΟΡΟΛΟΓΙΚΉ ΤΑΥΤΌΤΗΤΑ</span><span class="sxs-lookup"><span data-stu-id="8aba5-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="8aba5-237">ΚΩΔΙΚΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="8aba5-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="8aba5-238">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="8aba5-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-239">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-239">Format</span></span>

<span data-ttu-id="8aba5-240">Neun oder zehn Ziffern und optional einen umgekehrten Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="8aba5-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-241">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-241">Pattern</span></span>

<span data-ttu-id="8aba5-242">Neun oder zehn Ziffern mit einem optionalen Backslashl:</span><span class="sxs-lookup"><span data-stu-id="8aba5-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="8aba5-243">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-243">Six digits</span></span> 
    
- <span data-ttu-id="8aba5-244">Einen umgekehrten Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="8aba5-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="8aba5-245">Drei oder vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-246">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-246">Checksum</span></span>

<span data-ttu-id="8aba5-247">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8aba5-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-248">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-248">Definition</span></span>

<span data-ttu-id="8aba5-249">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-250">Der reguläre Ausdruck `Regex_czech_republic_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-251">Ein Schlüsselwort aus `Keywords_czech_republic_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8aba5-252">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="8aba5-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-254">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-254">tax number</span></span>
  
<span data-ttu-id="8aba5-255">tax</span><span class="sxs-lookup"><span data-stu-id="8aba5-255">tax</span></span>
  
<span data-ttu-id="8aba5-256">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-256">tax id</span></span>
  
<span data-ttu-id="8aba5-257">persönliche Nummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-257">personal number</span></span>
  
<span data-ttu-id="8aba5-258">Daňové číslo</span><span class="sxs-lookup"><span data-stu-id="8aba5-258">daňové číslo</span></span>
  
<span data-ttu-id="8aba5-259">Osobní číslo</span><span class="sxs-lookup"><span data-stu-id="8aba5-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="8aba5-260">Dänemark</span><span class="sxs-lookup"><span data-stu-id="8aba5-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-261">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-261">Format</span></span>

<span data-ttu-id="8aba5-262">Zehn Ziffern, die einen Bindestrich enthält</span><span class="sxs-lookup"><span data-stu-id="8aba5-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-263">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-263">Pattern</span></span>

<span data-ttu-id="8aba5-264">Zehn Ziffern, die ein Hyphenl enthält:</span><span class="sxs-lookup"><span data-stu-id="8aba5-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="8aba5-265">Sechs Ziffern, die das Geburtsdatum (DDMMYY) entsprechen</span><span class="sxs-lookup"><span data-stu-id="8aba5-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="8aba5-266">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="8aba5-266">A hyphen</span></span>
    
- <span data-ttu-id="8aba5-267">Vier Ziffern, die ein, wobei die erste Ziffer der Century Geburtsdatum entspricht, Sequenznummer entsprechen und die letzte Ziffer entspricht der betroffenen Person Geschlecht (ungerade für Männlich und sogar weiblich)</span><span class="sxs-lookup"><span data-stu-id="8aba5-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-268">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-268">Checksum</span></span>

<span data-ttu-id="8aba5-269">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-270">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-270">Definition</span></span>

<span data-ttu-id="8aba5-271">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-272">Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-273">Ein Schlüsselwort aus `Keywords_denmark_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-274">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-275">Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-276">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="8aba5-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-278">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-278">tax number</span></span>
  
<span data-ttu-id="8aba5-279">tax</span><span class="sxs-lookup"><span data-stu-id="8aba5-279">tax</span></span>
  
<span data-ttu-id="8aba5-280">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-280">tax id</span></span>
  
<span data-ttu-id="8aba5-281">CPR Anzahl</span><span class="sxs-lookup"><span data-stu-id="8aba5-281">cpr number</span></span>
  
<span data-ttu-id="8aba5-282">CPR-</span><span class="sxs-lookup"><span data-stu-id="8aba5-282">cpr#</span></span>
  
<span data-ttu-id="8aba5-283">Skat nummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-283">skat nummer</span></span>
  
<span data-ttu-id="8aba5-284">Skat-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="8aba5-285">Estland</span><span class="sxs-lookup"><span data-stu-id="8aba5-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-286">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-286">Format</span></span>

<span data-ttu-id="8aba5-287">11 Zahlen ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-288">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-288">Pattern</span></span>

<span data-ttu-id="8aba5-289">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="8aba5-289">11 digits:</span></span>
  
-  <span data-ttu-id="8aba5-290">Eine Zahl, die Geschlecht und Century Geburtsdatum, in dem eine ungerade Anzahl gibt Männlich und die gerade Zahl Weiblich wie folgt, entspricht: 1, 2 für die 19. Century; 3, 4 für die allem; 5 und 6 für 2015</span><span class="sxs-lookup"><span data-stu-id="8aba5-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="8aba5-291">Sechs Ziffern, die Geburtsdatum (JJMMTT) entsprechen</span><span class="sxs-lookup"><span data-stu-id="8aba5-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="8aba5-292">Drei Ziffern, die eine fortlaufende Zahl, die Personen, die an demselben Tag geboren trennt entsprechen</span><span class="sxs-lookup"><span data-stu-id="8aba5-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="8aba5-293">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8aba5-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-294">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-294">Checksum</span></span>

<span data-ttu-id="8aba5-295">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-296">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-296">Definition</span></span>

<span data-ttu-id="8aba5-297">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-298">Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-299">Ein Schlüsselwort aus `Keywords_estonia_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-300">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-301">Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-302">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="8aba5-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-304">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-304">tax number</span></span>
  
<span data-ttu-id="8aba5-305">tax</span><span class="sxs-lookup"><span data-stu-id="8aba5-305">tax</span></span>
  
<span data-ttu-id="8aba5-306">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-306">tax id</span></span>
  
<span data-ttu-id="8aba5-307">Persönliche code</span><span class="sxs-lookup"><span data-stu-id="8aba5-307">personal code</span></span>
  
<span data-ttu-id="8aba5-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="8aba5-308">maksunumber</span></span>
  
<span data-ttu-id="8aba5-309">Maksu-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-309">maksu id</span></span>
  
<span data-ttu-id="8aba5-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="8aba5-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="8aba5-311">Finnland</span><span class="sxs-lookup"><span data-stu-id="8aba5-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-312">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-312">Format</span></span>

<span data-ttu-id="8aba5-313">Eine Kombination aus 11 Zeichen Ziffern, Buchstaben, und Plus- und Minuszeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-314">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-314">Pattern</span></span>

<span data-ttu-id="8aba5-315">Eine Kombination aus 11 Zeichen Ziffern, Buchstaben, und Plus- und Minuszeichen:</span><span class="sxs-lookup"><span data-stu-id="8aba5-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="8aba5-316">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-316">Six digits</span></span>
    
- <span data-ttu-id="8aba5-317">Einer der folgenden: ein Pluszeichen (+), ein Minuszeichen oder dem Buchstaben "A" (nicht Groß-/Kleinschreibung), in dem das Pluszeichen (+) bedeutet, dass, zwischen 1800-1899 geboren, Signieren das Minuszeichen bedeutet, dass zwischen geboren 1900-1999, und "A" bedeutet, dass geboren 2000 und nach</span><span class="sxs-lookup"><span data-stu-id="8aba5-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="8aba5-318">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-318">Three digits</span></span>
    
- <span data-ttu-id="8aba5-319">Einen Buchstaben oder eine Zahl</span><span class="sxs-lookup"><span data-stu-id="8aba5-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-320">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-320">Checksum</span></span>

<span data-ttu-id="8aba5-321">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-322">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-322">Definition</span></span>

<span data-ttu-id="8aba5-323">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-324">Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-325">Ein Schlüsselwort aus `Keywords_finland_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-326">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-327">Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-328">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="8aba5-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-330">identification number
</span><span class="sxs-lookup"><span data-stu-id="8aba5-330">identification number</span></span>
  
<span data-ttu-id="8aba5-331">Persönliche id</span><span class="sxs-lookup"><span data-stu-id="8aba5-331">personal id</span></span>
  
<span data-ttu-id="8aba5-332">Anzahl der Identität</span><span class="sxs-lookup"><span data-stu-id="8aba5-332">identity number</span></span>
  
<span data-ttu-id="8aba5-333">Anzahl der Finnland Personalausweis</span><span class="sxs-lookup"><span data-stu-id="8aba5-333">finnish national id number</span></span>
  
<span data-ttu-id="8aba5-334">Personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="8aba5-334">personalidnumber#</span></span>
  
<span data-ttu-id="8aba5-335">National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-335">national identification number</span></span>
  
<span data-ttu-id="8aba5-336">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-336">id number</span></span>
  
<span data-ttu-id="8aba5-337">Personalausweis keine.</span><span class="sxs-lookup"><span data-stu-id="8aba5-337">national id no.</span></span>
  
<span data-ttu-id="8aba5-338">Ausweis-Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-338">national id number</span></span>
  
<span data-ttu-id="8aba5-339">ID keine</span><span class="sxs-lookup"><span data-stu-id="8aba5-339">id no</span></span>
  
<span data-ttu-id="8aba5-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="8aba5-340">tunnistenumero</span></span>
  
<span data-ttu-id="8aba5-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="8aba5-341">henkilötunnus</span></span>
  
<span data-ttu-id="8aba5-342">Yksilöllinen Henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="8aba5-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="8aba5-343">Ainutlaatuinen Henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="8aba5-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="8aba5-344">Identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="8aba5-344">identiteetti numero</span></span>
  
<span data-ttu-id="8aba5-345">Suomen Kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="8aba5-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="8aba5-346">Henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="8aba5-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="8aba5-347">Kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="8aba5-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="8aba5-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="8aba5-348">tunnusnumero</span></span>
  
<span data-ttu-id="8aba5-349">Kansallinen Tunnus numero</span><span class="sxs-lookup"><span data-stu-id="8aba5-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="8aba5-350">Frankreich</span><span class="sxs-lookup"><span data-stu-id="8aba5-350">France</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-351">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-351">Format</span></span>

<span data-ttu-id="8aba5-352">13 Stellen für einzelne Benutzer und neun Ziffern für Entitäten</span><span class="sxs-lookup"><span data-stu-id="8aba5-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-353">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-353">Pattern</span></span>

<span data-ttu-id="8aba5-354">13 Stellen für einzelne Benutzer:</span><span class="sxs-lookup"><span data-stu-id="8aba5-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="8aba5-355">Eine Zahl, die 0, 1, 2 oder 3 sein müssen</span><span class="sxs-lookup"><span data-stu-id="8aba5-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="8aba5-356">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-356">12 digits</span></span>
    
<span data-ttu-id="8aba5-357">Neun Ziffern für Entitäten</span><span class="sxs-lookup"><span data-stu-id="8aba5-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8aba5-358">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-358">Checksum</span></span>

<span data-ttu-id="8aba5-359">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8aba5-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-360">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-360">Definition</span></span>

<span data-ttu-id="8aba5-361">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-362">Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-363">Ein Schlüsselwort aus `Keywords_france_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-364">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-365">Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-366">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="8aba5-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-368">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-368">tax identification number</span></span>
  
<span data-ttu-id="8aba5-369">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-369">tax number</span></span>
  
<span data-ttu-id="8aba5-370">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-370">tax id</span></span>
  
<span data-ttu-id="8aba5-371">Numéro d ' Identification fiscale</span><span class="sxs-lookup"><span data-stu-id="8aba5-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="8aba5-372">Deutschland</span><span class="sxs-lookup"><span data-stu-id="8aba5-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-373">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-373">Format</span></span>

<span data-ttu-id="8aba5-374">11 Zahlen ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-375">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-375">Pattern</span></span>

<span data-ttu-id="8aba5-376">11 Stellen:</span><span class="sxs-lookup"><span data-stu-id="8aba5-376">11 digits :</span></span>
  
-  <span data-ttu-id="8aba5-377">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-377">Ten digits</span></span> 
    
- <span data-ttu-id="8aba5-378">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8aba5-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-379">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-379">Checksum</span></span>

<span data-ttu-id="8aba5-380">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-381">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-381">Definition</span></span>

<span data-ttu-id="8aba5-382">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-383">Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-384">Ein Schlüsselwort aus `Keywords_germany_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-385">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-386">Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-387">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="8aba5-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-389">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-389">tax number</span></span>
  
<span data-ttu-id="8aba5-390">Steuern Sie Nein.</span><span class="sxs-lookup"><span data-stu-id="8aba5-390">tax no.</span></span>
  
<span data-ttu-id="8aba5-391">Taxno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-391">taxno#</span></span>
  
<span data-ttu-id="8aba5-392">Taxnumber #</span><span class="sxs-lookup"><span data-stu-id="8aba5-392">taxnumber#</span></span>
  
<span data-ttu-id="8aba5-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="8aba5-393">taxnumber</span></span>
  
<span data-ttu-id="8aba5-394">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-394">tax id</span></span>
  
<span data-ttu-id="8aba5-395">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-395">taxid#</span></span>
  
<span data-ttu-id="8aba5-396">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-396">tax identification number</span></span>
  
<span data-ttu-id="8aba5-397">Steuernummer nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-397">tax identification no.</span></span>
  
<span data-ttu-id="8aba5-398">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-398">steuernummer</span></span>
  
<span data-ttu-id="8aba5-399">Steuer-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-399">steuer id</span></span>
  
<span data-ttu-id="8aba5-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="8aba5-401">Griechenland</span><span class="sxs-lookup"><span data-stu-id="8aba5-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-402">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-402">Format</span></span>

<span data-ttu-id="8aba5-403">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-404">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-404">Pattern</span></span>

<span data-ttu-id="8aba5-405">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8aba5-406">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-406">Checksum</span></span>

<span data-ttu-id="8aba5-407">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8aba5-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-408">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-408">Definition</span></span>

<span data-ttu-id="8aba5-409">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-410">Der reguläre Ausdruck `Regex_greece_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-411">Ein Schlüsselwort aus `Keywords_greece_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8aba5-412">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="8aba5-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-414">AFM</span><span class="sxs-lookup"><span data-stu-id="8aba5-414">afm</span></span>
  
<span data-ttu-id="8aba5-415">tin
</span><span class="sxs-lookup"><span data-stu-id="8aba5-415">tin</span></span>
  
<span data-ttu-id="8aba5-416">Steuernummer nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-416">tax id no.</span></span>
  
<span data-ttu-id="8aba5-417">keine Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-417">tax id no</span></span>
  
<span data-ttu-id="8aba5-418">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-418">tax identification number</span></span>
  
<span data-ttu-id="8aba5-419">Registrierung Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-419">tax registry number</span></span>
  
<span data-ttu-id="8aba5-420">Steuern Sie Registrierung nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-420">tax registry no.</span></span>
  
<span data-ttu-id="8aba5-421">AFM #</span><span class="sxs-lookup"><span data-stu-id="8aba5-421">afm#</span></span>
  
<span data-ttu-id="8aba5-422">Steuernummer #</span><span class="sxs-lookup"><span data-stu-id="8aba5-422">tin#</span></span>
  
<span data-ttu-id="8aba5-423">Taxidno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-423">taxidno#</span></span>
  
<span data-ttu-id="8aba5-424">Taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-424">taxregistryno#</span></span>
  
<span data-ttu-id="8aba5-425">ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="8aba5-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="8aba5-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="8aba5-426">aφμ</span></span>
  
<span data-ttu-id="8aba5-427">Aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="8aba5-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="8aba5-428">ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ ΝΟ.</span><span class="sxs-lookup"><span data-stu-id="8aba5-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="8aba5-429">ΤΟΝ ΑΡΙΘΜΌ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="8aba5-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="8aba5-430">Ungarn</span><span class="sxs-lookup"><span data-stu-id="8aba5-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-431">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-431">Format</span></span>

<span data-ttu-id="8aba5-432">Zehn Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-433">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-433">Pattern</span></span>

<span data-ttu-id="8aba5-434">Zehn Ziffern:</span><span class="sxs-lookup"><span data-stu-id="8aba5-434">Ten digits:</span></span>
  
-  <span data-ttu-id="8aba5-435">Eine Zahl, die "8" sein müssen</span><span class="sxs-lookup"><span data-stu-id="8aba5-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="8aba5-436">Fünf Ziffern, die die Anzahl der Tage zwischen dem Datum entsprechen, 01/01/1867 und das Geburtsdatum der Person</span><span class="sxs-lookup"><span data-stu-id="8aba5-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="8aba5-437">Drei Ziffern, die die Anzahl an Personen, die an demselben Tag geboren unterscheiden zufällig generiert entsprechen</span><span class="sxs-lookup"><span data-stu-id="8aba5-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="8aba5-438">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8aba5-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-439">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-439">Checksum</span></span>

<span data-ttu-id="8aba5-440">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-441">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-441">Definition</span></span>

<span data-ttu-id="8aba5-442">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-443">Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-444">Ein Schlüsselwort aus `Keywords_hungary_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-445">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-446">Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-447">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="8aba5-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-449">Ungarisch Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="8aba5-450">Ungarisch Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-450">hungarian tin</span></span>
  
<span data-ttu-id="8aba5-451">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-451">tax id number</span></span>
  
<span data-ttu-id="8aba5-452">Anzahl der Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="8aba5-452">vat number</span></span>
  
<span data-ttu-id="8aba5-453">Behörde nicht steuern</span><span class="sxs-lookup"><span data-stu-id="8aba5-453">tax authority no</span></span>
  
<span data-ttu-id="8aba5-454">Tax Identität Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-454">tax id tax identity number</span></span>
  
<span data-ttu-id="8aba5-455">Taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="8aba5-455">taxidnumber#</span></span>
  
<span data-ttu-id="8aba5-456">Steuernummer #</span><span class="sxs-lookup"><span data-stu-id="8aba5-456">tin#</span></span>
  
<span data-ttu-id="8aba5-457">Hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="8aba5-457">hungatiantin#</span></span>
  
<span data-ttu-id="8aba5-458">keine Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-458">tax identification no</span></span>
  
<span data-ttu-id="8aba5-459">Taxidno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-459">taxidno#</span></span>
  
<span data-ttu-id="8aba5-460">Adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="8aba5-460">adóazonosító szám</span></span>
  
<span data-ttu-id="8aba5-461">adószám</span><span class="sxs-lookup"><span data-stu-id="8aba5-461">adószám</span></span>
  
<span data-ttu-id="8aba5-462">Adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="8aba5-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="8aba5-463">Irland</span><span class="sxs-lookup"><span data-stu-id="8aba5-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-464">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-464">Format</span></span>

<span data-ttu-id="8aba5-465">Sieben Ziffern, gefolgt von einem Buchstaben ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-466">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-466">Pattern</span></span>

<span data-ttu-id="8aba5-467">Sieben Ziffern, gefolgt von einem Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="8aba5-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="8aba5-468">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="8aba5-468">Seven digits</span></span> 
    
- <span data-ttu-id="8aba5-469">Ein Buchstabe (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8aba5-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-470">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-470">Checksum</span></span>

<span data-ttu-id="8aba5-471">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8aba5-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-472">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-472">Definition</span></span>

<span data-ttu-id="8aba5-473">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-474">Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-475">Ein Schlüsselwort aus `Keywords_ireland_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-476">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-477">Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-478">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="8aba5-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-480">öffentliche Dienstleistungen keine</span><span class="sxs-lookup"><span data-stu-id="8aba5-480">public service no</span></span>
  
<span data-ttu-id="8aba5-481">Persönliche öffentliche Dienstleistungen keine</span><span class="sxs-lookup"><span data-stu-id="8aba5-481">personal public service no</span></span>
  
<span data-ttu-id="8aba5-482">PPS keine</span><span class="sxs-lookup"><span data-stu-id="8aba5-482">pps no</span></span>
  
<span data-ttu-id="8aba5-483">Persönliche Nein service</span><span class="sxs-lookup"><span data-stu-id="8aba5-483">personal service no</span></span>
  
<span data-ttu-id="8aba5-484">PPS-service Nein</span><span class="sxs-lookup"><span data-stu-id="8aba5-484">pps service no</span></span>
  
<span data-ttu-id="8aba5-485">Ppsno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-485">ppsno#</span></span>
  
<span data-ttu-id="8aba5-486">Irland Pps keine</span><span class="sxs-lookup"><span data-stu-id="8aba5-486">irish pps no</span></span>
  
<span data-ttu-id="8aba5-487">Publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-487">publicserviceno#</span></span>
  
<span data-ttu-id="8aba5-488">Anzahl der persönlichen öffentliche Dienstleistungen</span><span class="sxs-lookup"><span data-stu-id="8aba5-488">personal public service number</span></span>
  
<span data-ttu-id="8aba5-489">Uimhir Phearsanta Seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="8aba5-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="8aba5-490">PPS-uimh</span><span class="sxs-lookup"><span data-stu-id="8aba5-490">pps uimh</span></span>
  
<span data-ttu-id="8aba5-491">Uimhir Aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="8aba5-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="8aba5-492">Italien</span><span class="sxs-lookup"><span data-stu-id="8aba5-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-493">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-493">Format</span></span>

<span data-ttu-id="8aba5-494">16 Buchstaben und Ziffern in dem angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-495">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-495">Pattern</span></span>

<span data-ttu-id="8aba5-496">16 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="8aba5-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="8aba5-497">Drei Buchstaben, die die ersten drei Doppelkonsonanten in der der Name der entsprechen</span><span class="sxs-lookup"><span data-stu-id="8aba5-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="8aba5-498">Drei Buchstaben, die die erste, dritte und vierte entsprechen, Doppelkonsonanten in den Vornamen</span><span class="sxs-lookup"><span data-stu-id="8aba5-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="8aba5-499">Zwei Ziffern, die auf die letzte Ziffern des Jahres Geburtsdatum entsprechen</span><span class="sxs-lookup"><span data-stu-id="8aba5-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="8aba5-500">Eine Ziffer, die den Monat Geburtsdatum entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben A bis E, H, L, M, P, R t verwendet werden (also Januar ist eine und Oktober R)</span><span class="sxs-lookup"><span data-stu-id="8aba5-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="8aba5-501">Zwei Ziffern, die den Tag des Monats Geburtsdatum entsprechen, in dem der Tag Geburtsdaten von bestimmten zur Unterscheidung von Männlich 40 hinzugefügt wird</span><span class="sxs-lookup"><span data-stu-id="8aba5-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="8aba5-502">Vier Ziffern, die speziell für die Gemeinde Ortskennzahl entsprechen, in die Person geboren wurde – Land geltende Codes für Ausland verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8aba5-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="8aba5-503">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8aba5-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-504">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-504">Checksum</span></span>

<span data-ttu-id="8aba5-505">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-506">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-506">Definition</span></span>

<span data-ttu-id="8aba5-507">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-508">Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-509">Ein Schlüsselwort aus `Keywords_italy_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-510">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-511">Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-512">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="8aba5-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-514">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-514">tax number</span></span>
  
<span data-ttu-id="8aba5-515">Steuern Sie Nein.</span><span class="sxs-lookup"><span data-stu-id="8aba5-515">tax no.</span></span>
  
<span data-ttu-id="8aba5-516">Taxno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-516">taxno#</span></span>
  
<span data-ttu-id="8aba5-517">Taxnumber #</span><span class="sxs-lookup"><span data-stu-id="8aba5-517">taxnumber#</span></span>
  
<span data-ttu-id="8aba5-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="8aba5-518">taxnumber</span></span>
  
<span data-ttu-id="8aba5-519">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-519">tax id</span></span>
  
<span data-ttu-id="8aba5-520">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-520">taxid#</span></span>
  
<span data-ttu-id="8aba5-521">Fiscal code</span><span class="sxs-lookup"><span data-stu-id="8aba5-521">fiscal code</span></span>
  
<span data-ttu-id="8aba5-522">Codice fiscale</span><span class="sxs-lookup"><span data-stu-id="8aba5-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="8aba5-523">Lettland</span><span class="sxs-lookup"><span data-stu-id="8aba5-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-524">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-524">Format</span></span>

<span data-ttu-id="8aba5-525">11 Zahlen ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-526">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-526">Pattern</span></span>

<span data-ttu-id="8aba5-527">11 Stellen in dem angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="8aba5-528">Sechs Ziffern, die das Geburtsdatum (DDMMYY) entsprechen</span><span class="sxs-lookup"><span data-stu-id="8aba5-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="8aba5-529">Eine Zahl, die die Century Geburtsdatum entspricht, in dem 19. Century entspricht "0", "1" entspricht allem und 2015 "2" entspricht</span><span class="sxs-lookup"><span data-stu-id="8aba5-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="8aba5-530">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-531">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-531">Checksum</span></span>

<span data-ttu-id="8aba5-532">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-533">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-533">Definition</span></span>

<span data-ttu-id="8aba5-534">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-535">Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-536">Ein Schlüsselwort aus `Keywords_latvia_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-537">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-538">Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-539">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="8aba5-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-541">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-541">tax number</span></span>
  
<span data-ttu-id="8aba5-542">Steuern Sie Nein.</span><span class="sxs-lookup"><span data-stu-id="8aba5-542">tax no.</span></span>
  
<span data-ttu-id="8aba5-543">Taxno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-543">taxno#</span></span>
  
<span data-ttu-id="8aba5-544">Taxnumber #</span><span class="sxs-lookup"><span data-stu-id="8aba5-544">taxnumber#</span></span>
  
<span data-ttu-id="8aba5-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="8aba5-545">taxnumber</span></span>
  
<span data-ttu-id="8aba5-546">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-546">tax id</span></span>
  
<span data-ttu-id="8aba5-547">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-547">taxid#</span></span>
  
<span data-ttu-id="8aba5-548">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-548">tax identification number</span></span>
  
<span data-ttu-id="8aba5-549">Steuernummer nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-549">tax identification no.</span></span>
  
<span data-ttu-id="8aba5-550">Nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="8aba5-550">nodokļa numurs</span></span>
  
<span data-ttu-id="8aba5-551">Nodokļu Identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="8aba5-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="8aba5-552">Nodokļu Identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="8aba5-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="8aba5-553">Litauen</span><span class="sxs-lookup"><span data-stu-id="8aba5-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-554">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-554">Format</span></span>

<span data-ttu-id="8aba5-555">11 Zahlen ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-556">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-556">Pattern</span></span>

<span data-ttu-id="8aba5-557">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8aba5-558">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-558">Checksum</span></span>

<span data-ttu-id="8aba5-559">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8aba5-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-560">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-560">Definition</span></span>

<span data-ttu-id="8aba5-561">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-562">Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-563">Ein Schlüsselwort aus `Keywords_lithuania_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-564">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-565">Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-566">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="8aba5-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-568">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-568">tax number</span></span>
  
<span data-ttu-id="8aba5-569">Steuern Sie Nein.</span><span class="sxs-lookup"><span data-stu-id="8aba5-569">tax no.</span></span>
  
<span data-ttu-id="8aba5-570">Steuerinformationen Nein #</span><span class="sxs-lookup"><span data-stu-id="8aba5-570">tax no#</span></span>
  
<span data-ttu-id="8aba5-571">Taxnumber #</span><span class="sxs-lookup"><span data-stu-id="8aba5-571">taxnumber#</span></span>
  
<span data-ttu-id="8aba5-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="8aba5-572">taxnumber</span></span>
  
<span data-ttu-id="8aba5-573">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-573">tax id</span></span>
  
<span data-ttu-id="8aba5-574">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-574">taxid#</span></span>
  
<span data-ttu-id="8aba5-575">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-575">tax identification number</span></span>
  
<span data-ttu-id="8aba5-576">Steuernummer nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-576">tax identification no.</span></span>
  
<span data-ttu-id="8aba5-577">Mokesčių-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-577">mokesčių id</span></span>
  
<span data-ttu-id="8aba5-578">Mokesčių numeris</span><span class="sxs-lookup"><span data-stu-id="8aba5-578">mokesčių numeris</span></span>
  
<span data-ttu-id="8aba5-579">Mokesčių Identifikavimas numeris</span><span class="sxs-lookup"><span data-stu-id="8aba5-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="8aba5-580">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="8aba5-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-581">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-581">Format</span></span>

<span data-ttu-id="8aba5-582">13 Stellen ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-583">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-583">Pattern</span></span>

<span data-ttu-id="8aba5-584">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="8aba5-584">13 digits:</span></span>
  
-  <span data-ttu-id="8aba5-585">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-585">11 digits</span></span> 
    
- <span data-ttu-id="8aba5-586">Zwei Prüfziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-587">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-587">Checksum</span></span>

<span data-ttu-id="8aba5-588">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-589">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-589">Definition</span></span>

<span data-ttu-id="8aba5-590">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-591">Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-592">Ein Schlüsselwort aus `Keywords_luxemburg_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-593">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-594">Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-595">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="8aba5-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-597">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-597">tax number</span></span>
  
<span data-ttu-id="8aba5-598">Steuern Sie Nein.</span><span class="sxs-lookup"><span data-stu-id="8aba5-598">tax no.</span></span>
  
<span data-ttu-id="8aba5-599">Taxno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-599">taxno#</span></span>
  
<span data-ttu-id="8aba5-600">Taxnumber #</span><span class="sxs-lookup"><span data-stu-id="8aba5-600">taxnumber#</span></span>
  
<span data-ttu-id="8aba5-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="8aba5-601">taxnumber</span></span>
  
<span data-ttu-id="8aba5-602">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-602">tax id</span></span>
  
<span data-ttu-id="8aba5-603">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-603">taxid#</span></span>
  
<span data-ttu-id="8aba5-604">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-604">tax identification number</span></span>
  
<span data-ttu-id="8aba5-605">Steuernummer nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-605">tax identification no.</span></span>
  
<span data-ttu-id="8aba5-606">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-606">steuernummer</span></span>
  
<span data-ttu-id="8aba5-607">Steuer-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-607">steuer id</span></span>
  
<span data-ttu-id="8aba5-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="8aba5-609">Malta</span><span class="sxs-lookup"><span data-stu-id="8aba5-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-610">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-610">Format</span></span>

<span data-ttu-id="8aba5-611">Maltesisch Staatsangehörigen: 7 Ziffern und einem Buchstaben in das angegebene Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="8aba5-612">Nicht-Maltesisch Staatsangehörigen und Maltesisch Entitäten: 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-613">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-613">Pattern</span></span>

<span data-ttu-id="8aba5-614">Maltesisch Staatsangehörigen: 7 Ziffern und einem Buchstaben</span><span class="sxs-lookup"><span data-stu-id="8aba5-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="8aba5-615">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="8aba5-615">Seven digits</span></span> 
    
- <span data-ttu-id="8aba5-616">Ein Buchstabe (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8aba5-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="8aba5-617">Nicht-Maltesisch Staatsangehörigen und Maltesisch Entitäten: 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="8aba5-618">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="8aba5-619">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-619">Checksum</span></span>

<span data-ttu-id="8aba5-620">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8aba5-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-621">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-621">Definition</span></span>

<span data-ttu-id="8aba5-622">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-623">Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-624">Ein Schlüsselwort aus `Keywords_malta_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-625">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-626">Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-627">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="8aba5-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-629">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-629">tax number</span></span>
  
<span data-ttu-id="8aba5-630">Steuern Sie Nein.</span><span class="sxs-lookup"><span data-stu-id="8aba5-630">tax no.</span></span>
  
<span data-ttu-id="8aba5-631">Taxno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-631">taxno#</span></span>
  
<span data-ttu-id="8aba5-632">Taxnumber #</span><span class="sxs-lookup"><span data-stu-id="8aba5-632">taxnumber#</span></span>
  
<span data-ttu-id="8aba5-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="8aba5-633">taxnumber</span></span>
  
<span data-ttu-id="8aba5-634">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-634">tax id</span></span>
  
<span data-ttu-id="8aba5-635">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-635">taxid#</span></span>
  
<span data-ttu-id="8aba5-636">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-636">tax identification number</span></span>
  
<span data-ttu-id="8aba5-637">Steuernummer nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-637">tax identification no.</span></span>
  
<span data-ttu-id="8aba5-638">Numru Tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="8aba5-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="8aba5-639">ID Tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="8aba5-639">id tat-taxxa</span></span>
  
<span data-ttu-id="8aba5-640">Numru ta ' Identifikazzjoni Tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="8aba5-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="8aba5-641">Niederlande</span><span class="sxs-lookup"><span data-stu-id="8aba5-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-642">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-642">Format</span></span>

<span data-ttu-id="8aba5-643">Neun Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-644">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-644">Pattern</span></span>

<span data-ttu-id="8aba5-645">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="8aba5-646">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-646">Checksum</span></span>

<span data-ttu-id="8aba5-647">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-648">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-648">Definition</span></span>

<span data-ttu-id="8aba5-649">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-650">Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-651">Ein Schlüsselwort aus `Keywords_netherlands_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-652">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-653">Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-654">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="8aba5-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-656">Niederlande Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="8aba5-657">Niederlande Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-657">netherlands tax identification</span></span>
  
<span data-ttu-id="8aba5-658">der niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="8aba5-659">der niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-659">netherland's tax identification</span></span>
  
<span data-ttu-id="8aba5-660">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-660">tax identification number</span></span>
  
<span data-ttu-id="8aba5-661">Niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-661">dutch tax id</span></span>
  
<span data-ttu-id="8aba5-662">Niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-662">dutch tax identification number</span></span>
  
<span data-ttu-id="8aba5-663">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-663">tax id</span></span>
  
<span data-ttu-id="8aba5-664">Nr.</span><span class="sxs-lookup"><span data-stu-id="8aba5-664">tax id#</span></span>
  
<span data-ttu-id="8aba5-665">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-665">tax number</span></span>
  
<span data-ttu-id="8aba5-666">Steuerinformationen Nein #</span><span class="sxs-lookup"><span data-stu-id="8aba5-666">tax no#</span></span>
  
<span data-ttu-id="8aba5-667">Tax #</span><span class="sxs-lookup"><span data-stu-id="8aba5-667">tax#</span></span>
  
<span data-ttu-id="8aba5-668">tin
</span><span class="sxs-lookup"><span data-stu-id="8aba5-668">tin</span></span>
  
<span data-ttu-id="8aba5-669">Steuernummer #</span><span class="sxs-lookup"><span data-stu-id="8aba5-669">tin#</span></span>
  
<span data-ttu-id="8aba5-670">Niederlande Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-670">netherlands tin</span></span>
  
<span data-ttu-id="8aba5-671">der niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-671">netherland's tin</span></span>
  
<span data-ttu-id="8aba5-672">Niederlande Belasting identificatienummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="8aba5-673">Identificatienummer van belasting</span><span class="sxs-lookup"><span data-stu-id="8aba5-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="8aba5-674">Identificatienummer belasting</span><span class="sxs-lookup"><span data-stu-id="8aba5-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="8aba5-675">Niederlande Belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="8aba5-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="8aba5-676">Niederlande Belasting-Id-nummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="8aba5-677">Niederlande belastingnummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="8aba5-678">btw Nummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-678">btw nummer</span></span>
  
<span data-ttu-id="8aba5-679">Nederlandse Belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="8aba5-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="8aba5-680">Polen</span><span class="sxs-lookup"><span data-stu-id="8aba5-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-681">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-681">Format</span></span>

<span data-ttu-id="8aba5-682">Elf Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-683">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-683">Pattern</span></span>

<span data-ttu-id="8aba5-684">Elf Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8aba5-685">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-685">Checksum</span></span>

<span data-ttu-id="8aba5-686">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-687">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-687">Definition</span></span>

<span data-ttu-id="8aba5-688">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-689">Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-690">Ein Schlüsselwort aus `Keywords_poland_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-691">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-692">Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-693">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="8aba5-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-695">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-695">tax number</span></span>
  
<span data-ttu-id="8aba5-696">Steuern Sie Nein.</span><span class="sxs-lookup"><span data-stu-id="8aba5-696">tax no.</span></span>
  
<span data-ttu-id="8aba5-697">Taxno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-697">taxno#</span></span>
  
<span data-ttu-id="8aba5-698">Taxnumber #</span><span class="sxs-lookup"><span data-stu-id="8aba5-698">taxnumber#</span></span>
  
<span data-ttu-id="8aba5-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="8aba5-699">taxnumber</span></span>
  
<span data-ttu-id="8aba5-700">Aktivieren der</span><span class="sxs-lookup"><span data-stu-id="8aba5-700">nip</span></span>
  
<span data-ttu-id="8aba5-701">Aktivieren der #</span><span class="sxs-lookup"><span data-stu-id="8aba5-701">nip#</span></span>
  
<span data-ttu-id="8aba5-702">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-702">tax id</span></span>
  
<span data-ttu-id="8aba5-703">Nr.</span><span class="sxs-lookup"><span data-stu-id="8aba5-703">tax id#</span></span>
  
<span data-ttu-id="8aba5-704">Aktivieren der id</span><span class="sxs-lookup"><span data-stu-id="8aba5-704">nip id</span></span>
  
<span data-ttu-id="8aba5-705">Aktivieren der ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-705">nip id#</span></span>
  
<span data-ttu-id="8aba5-706">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-706">tax identification number</span></span>
  
<span data-ttu-id="8aba5-707">Steuernummer nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-707">tax identification no.</span></span>
  
<span data-ttu-id="8aba5-708">Anzahl der Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="8aba5-708">vat number</span></span>
  
<span data-ttu-id="8aba5-709">Umsatzsteuer.</span><span class="sxs-lookup"><span data-stu-id="8aba5-709">vat no.</span></span>
  
<span data-ttu-id="8aba5-710">Vatno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-710">vatno#</span></span>
  
<span data-ttu-id="8aba5-711">ber</span><span class="sxs-lookup"><span data-stu-id="8aba5-711">vat id</span></span>
  
<span data-ttu-id="8aba5-712">Mehrwertsteuer-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-712">vat id#</span></span>
  
<span data-ttu-id="8aba5-713">Anzahl Identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="8aba5-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="8aba5-714">Polski Anzahl Identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="8aba5-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="8aba5-715">Numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="8aba5-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="8aba5-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="8aba5-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-717">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-717">Format</span></span>

<span data-ttu-id="8aba5-718">Neun Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-719">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-719">Pattern</span></span>

<span data-ttu-id="8aba5-720">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8aba5-721">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-721">Checksum</span></span>

<span data-ttu-id="8aba5-722">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-723">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-723">Definition</span></span>

<span data-ttu-id="8aba5-724">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-725">Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-726">Ein Schlüsselwort aus `Keywords_portugal_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-727">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-728">Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-729">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="8aba5-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-731">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-731">tax number</span></span>
  
<span data-ttu-id="8aba5-732">Steuern Sie Nein.</span><span class="sxs-lookup"><span data-stu-id="8aba5-732">tax no.</span></span>
  
<span data-ttu-id="8aba5-733">Taxno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-733">taxno#</span></span>
  
<span data-ttu-id="8aba5-734">Taxnumber #</span><span class="sxs-lookup"><span data-stu-id="8aba5-734">taxnumber#</span></span>
  
<span data-ttu-id="8aba5-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="8aba5-735">taxnumber</span></span>
  
<span data-ttu-id="8aba5-736">if</span><span class="sxs-lookup"><span data-stu-id="8aba5-736">nif</span></span>
  
<span data-ttu-id="8aba5-737">if-</span><span class="sxs-lookup"><span data-stu-id="8aba5-737">nif#</span></span>
  
<span data-ttu-id="8aba5-738">Numero Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="8aba5-738">numero fiscal</span></span>
  
<span data-ttu-id="8aba5-739">Número de Identificação Geschäftszeiträume</span><span class="sxs-lookup"><span data-stu-id="8aba5-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="8aba5-740">Rumänien</span><span class="sxs-lookup"><span data-stu-id="8aba5-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-741">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-741">Format</span></span>

<span data-ttu-id="8aba5-742">13 Stellen ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-743">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-743">Pattern</span></span>

<span data-ttu-id="8aba5-744">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8aba5-745">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-745">Checksum</span></span>

<span data-ttu-id="8aba5-746">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8aba5-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-747">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-747">Definition</span></span>

<span data-ttu-id="8aba5-748">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-749">Der reguläre Ausdruck `Regex_romania_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-750">Ein Schlüsselwort aus `Keywords_romania_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8aba5-751">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="8aba5-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-753">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-753">tax id</span></span>
  
<span data-ttu-id="8aba5-754">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-754">tax id number</span></span>
  
<span data-ttu-id="8aba5-755">Datei nicht steuern</span><span class="sxs-lookup"><span data-stu-id="8aba5-755">tax file no</span></span>
  
<span data-ttu-id="8aba5-756">

tax file number</span><span class="sxs-lookup"><span data-stu-id="8aba5-756">tax file number</span></span>
  
<span data-ttu-id="8aba5-757">Nein Steuerinformationen</span><span class="sxs-lookup"><span data-stu-id="8aba5-757">tax no</span></span>
  
<span data-ttu-id="8aba5-758">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-758">tax number</span></span>
  
<span data-ttu-id="8aba5-759">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-759">taxid#</span></span>
  
<span data-ttu-id="8aba5-760">Taxno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-760">taxno#</span></span>
  
<span data-ttu-id="8aba5-761">ID-Ul taxei</span><span class="sxs-lookup"><span data-stu-id="8aba5-761">id-ul taxei</span></span>
  
<span data-ttu-id="8aba5-762">Numărul de Identificare fiscală</span><span class="sxs-lookup"><span data-stu-id="8aba5-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="8aba5-763">Slowakei</span><span class="sxs-lookup"><span data-stu-id="8aba5-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-764">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-764">Format</span></span>

<span data-ttu-id="8aba5-765">10 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-766">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-766">Pattern</span></span>

<span data-ttu-id="8aba5-767">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8aba5-768">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-768">Checksum</span></span>

<span data-ttu-id="8aba5-769">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8aba5-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-770">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-770">Definition</span></span>

<span data-ttu-id="8aba5-771">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-772">Der reguläre Ausdruck `Regex_slovakia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-773">Ein Schlüsselwort aus `Keywords_slovakia_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8aba5-774">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="8aba5-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-776">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-776">tax id</span></span>
  
<span data-ttu-id="8aba5-777">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-777">tax id number</span></span>
  
<span data-ttu-id="8aba5-778">Steuernummer-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-778">tin id</span></span>
  
<span data-ttu-id="8aba5-779">Steuernummer Nr.</span><span class="sxs-lookup"><span data-stu-id="8aba5-779">tin no</span></span>
  
<span data-ttu-id="8aba5-780">Slowakische Steuernummer-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-780">slovakian tin id</span></span>
  
<span data-ttu-id="8aba5-781">tin
</span><span class="sxs-lookup"><span data-stu-id="8aba5-781">tin</span></span>
  
<span data-ttu-id="8aba5-782">Datei nicht steuern</span><span class="sxs-lookup"><span data-stu-id="8aba5-782">tax file no</span></span>
  
<span data-ttu-id="8aba5-783">

tax file number</span><span class="sxs-lookup"><span data-stu-id="8aba5-783">tax file number</span></span>
  
<span data-ttu-id="8aba5-784">Nein Steuerinformationen</span><span class="sxs-lookup"><span data-stu-id="8aba5-784">tax no</span></span>
  
<span data-ttu-id="8aba5-785">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-785">tax number</span></span>
  
<span data-ttu-id="8aba5-786">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-786">taxid#</span></span>
  
<span data-ttu-id="8aba5-787">Taxno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-787">taxno#</span></span>
  
<span data-ttu-id="8aba5-788">Daňové Identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="8aba5-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="8aba5-789">Daňové číslo</span><span class="sxs-lookup"><span data-stu-id="8aba5-789">daňové číslo</span></span>
  
<span data-ttu-id="8aba5-790">Daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="8aba5-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="8aba5-791">Slowenien</span><span class="sxs-lookup"><span data-stu-id="8aba5-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-792">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-792">Format</span></span>

<span data-ttu-id="8aba5-793">Acht Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-794">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-794">Pattern</span></span>

<span data-ttu-id="8aba5-795">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8aba5-796">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-796">Checksum</span></span>

<span data-ttu-id="8aba5-797">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-798">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-798">Definition</span></span>

<span data-ttu-id="8aba5-799">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-800">Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-801">Ein Schlüsselwort aus `Keywords_slovenia_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-802">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-803">Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-804">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="8aba5-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-806">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-806">tax id</span></span>
  
<span data-ttu-id="8aba5-807">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-807">tax id number</span></span>
  
<span data-ttu-id="8aba5-808">Steuernummer-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-808">tin id</span></span>
  
<span data-ttu-id="8aba5-809">Steuernummer Nr.</span><span class="sxs-lookup"><span data-stu-id="8aba5-809">tin no</span></span>
  
<span data-ttu-id="8aba5-810">Slowenisch Steuernummer-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-810">slovenian tin id</span></span>
  
<span data-ttu-id="8aba5-811">tin
</span><span class="sxs-lookup"><span data-stu-id="8aba5-811">tin</span></span>
  
<span data-ttu-id="8aba5-812">Datei nicht steuern</span><span class="sxs-lookup"><span data-stu-id="8aba5-812">tax file no</span></span>
  
<span data-ttu-id="8aba5-813">

tax file number</span><span class="sxs-lookup"><span data-stu-id="8aba5-813">tax file number</span></span>
  
<span data-ttu-id="8aba5-814">Nein Steuerinformationen</span><span class="sxs-lookup"><span data-stu-id="8aba5-814">tax no</span></span>
  
<span data-ttu-id="8aba5-815">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-815">tax number</span></span>
  
<span data-ttu-id="8aba5-816">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-816">taxid#</span></span>
  
<span data-ttu-id="8aba5-817">Taxno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-817">taxno#</span></span>
  
<span data-ttu-id="8aba5-818">Identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="8aba5-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="8aba5-819">Davčna številka</span><span class="sxs-lookup"><span data-stu-id="8aba5-819">davčna številka</span></span>
  
<span data-ttu-id="8aba5-820">Številka Davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="8aba5-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="8aba5-821">Spanien</span><span class="sxs-lookup"><span data-stu-id="8aba5-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-822">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-822">Format</span></span>

<span data-ttu-id="8aba5-823">Sieben oder acht Ziffern und ein oder zwei Buchstaben in das angegebene Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-824">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-824">Pattern</span></span>

<span data-ttu-id="8aba5-825">Spanische natürliche Personen mit einer Spanien National Identität Karte:</span><span class="sxs-lookup"><span data-stu-id="8aba5-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="8aba5-826">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-826">Eight digits</span></span> 
    
- <span data-ttu-id="8aba5-827">Einen Großbuchstaben (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8aba5-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="8aba5-828">Nicht Spaniards ohne eine Spanien National-Personalausweis</span><span class="sxs-lookup"><span data-stu-id="8aba5-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="8aba5-829">Einen Großbuchstaben "L" (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8aba5-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="8aba5-830">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="8aba5-830">Seven digits</span></span>
    
- <span data-ttu-id="8aba5-831">Einen Großbuchstaben (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8aba5-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="8aba5-832">Berater Spaniards unter 14 Jahre ohne eine Spanien National Personalausweis:</span><span class="sxs-lookup"><span data-stu-id="8aba5-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="8aba5-833">Ein Großbuchstabe "K" (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8aba5-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="8aba5-834">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="8aba5-834">Seven digits</span></span> 
    
- <span data-ttu-id="8aba5-835">Einen Großbuchstaben (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8aba5-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="8aba5-836">Foreigners mit einer Foreigner-ID</span><span class="sxs-lookup"><span data-stu-id="8aba5-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="8aba5-837">Einen Großbuchstaben Buchstabe d. h., "X", "Y" oder "Z" (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8aba5-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="8aba5-838">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="8aba5-838">Seven digits</span></span>
    
- <span data-ttu-id="8aba5-839">Einen Großbuchstaben (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8aba5-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="8aba5-840">Foreigners ohne eine Foreigner-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="8aba5-841">Einen Großbuchstaben, das "M" (Groß-/Kleinschreibung) ist.</span><span class="sxs-lookup"><span data-stu-id="8aba5-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="8aba5-842">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="8aba5-842">Seven digits</span></span>
    
- <span data-ttu-id="8aba5-843">Einen Großbuchstaben (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8aba5-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="8aba5-844">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-844">Checksum</span></span>

<span data-ttu-id="8aba5-845">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-846">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-846">Definition</span></span>

<span data-ttu-id="8aba5-847">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-848">Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-849">Ein Schlüsselwort aus `Keywords_spain_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-850">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-851">Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-852">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="8aba5-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-854">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-854">tax id</span></span>
  
<span data-ttu-id="8aba5-855">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-855">tax id number</span></span>
  
<span data-ttu-id="8aba5-856">Cif-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-856">cif id</span></span>
  
<span data-ttu-id="8aba5-857">Cif keine</span><span class="sxs-lookup"><span data-stu-id="8aba5-857">cif no</span></span>
  
<span data-ttu-id="8aba5-858">Spanische Cif-id</span><span class="sxs-lookup"><span data-stu-id="8aba5-858">spanish cif id</span></span>
  
<span data-ttu-id="8aba5-859">cif</span><span class="sxs-lookup"><span data-stu-id="8aba5-859">cif</span></span>
  
<span data-ttu-id="8aba5-860">Datei nicht steuern</span><span class="sxs-lookup"><span data-stu-id="8aba5-860">tax file no</span></span>
  
<span data-ttu-id="8aba5-861">Spanische Cif-Anzahl</span><span class="sxs-lookup"><span data-stu-id="8aba5-861">spanish cif number</span></span>
  
<span data-ttu-id="8aba5-862">

tax file number</span><span class="sxs-lookup"><span data-stu-id="8aba5-862">tax file number</span></span>
  
<span data-ttu-id="8aba5-863">Spanische Cif keine</span><span class="sxs-lookup"><span data-stu-id="8aba5-863">spanish cif no</span></span>
  
<span data-ttu-id="8aba5-864">Nein Steuerinformationen</span><span class="sxs-lookup"><span data-stu-id="8aba5-864">tax no</span></span>
  
<span data-ttu-id="8aba5-865">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-865">tax number</span></span>
  
<span data-ttu-id="8aba5-866">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-866">taxid#</span></span>
  
<span data-ttu-id="8aba5-867">Taxno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-867">taxno#</span></span>
  
<span data-ttu-id="8aba5-868">CIFID #</span><span class="sxs-lookup"><span data-stu-id="8aba5-868">cifid#</span></span>
  
<span data-ttu-id="8aba5-869">Spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-869">spanishcifid#</span></span>
  
<span data-ttu-id="8aba5-870">Spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="8aba5-870">spanishcifno#</span></span>
  
<span data-ttu-id="8aba5-871">Número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="8aba5-871">número de contribuyente</span></span>
  
<span data-ttu-id="8aba5-872">Número de Impuesto corporativo</span><span class="sxs-lookup"><span data-stu-id="8aba5-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="8aba5-873">Número de Identificación Geschäftszeiträume</span><span class="sxs-lookup"><span data-stu-id="8aba5-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="8aba5-874">Cif-número</span><span class="sxs-lookup"><span data-stu-id="8aba5-874">cif número</span></span>
  
<span data-ttu-id="8aba5-875">Cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="8aba5-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="8aba5-876">Schweden</span><span class="sxs-lookup"><span data-stu-id="8aba5-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-877">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-877">Format</span></span>

<span data-ttu-id="8aba5-878">Zehn Ziffern und ein Symbol in das angegebene Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-879">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-879">Pattern</span></span>

<span data-ttu-id="8aba5-880">Zehn Ziffern und ein Symbol:</span><span class="sxs-lookup"><span data-stu-id="8aba5-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="8aba5-881">Sechs Ziffern, die das Geburtsdatum (JJMMTT) entsprechen</span><span class="sxs-lookup"><span data-stu-id="8aba5-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="8aba5-882">Ein Pluszeichen (+), Minuszeichen oder umgekehrter Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="8aba5-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="8aba5-883">Drei Ziffern, aus die die Kennung zusammensetzt Nummer eindeutige Where wählen:</span><span class="sxs-lookup"><span data-stu-id="8aba5-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="8aba5-884">Zahlen, die vor dem 1990 ausgestellt wurden identifizieren Sie die siebte und die achte Ziffer den Kanton des Geburtsdatum oder foreign-born Personen</span><span class="sxs-lookup"><span data-stu-id="8aba5-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="8aba5-885">Die Ziffer in der neunten Position gibt Geschlecht nach entweder ungerade für männlich oder sogar Weiblich</span><span class="sxs-lookup"><span data-stu-id="8aba5-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="8aba5-886">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8aba5-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8aba5-887">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-887">Checksum</span></span>

<span data-ttu-id="8aba5-888">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-889">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-889">Definition</span></span>

<span data-ttu-id="8aba5-890">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-891">Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-892">Ein Schlüsselwort aus `Keywords_sweden_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="8aba5-893">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-894">Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8aba5-895">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="8aba5-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-897">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-897">tax id</span></span>
  
<span data-ttu-id="8aba5-898">Steuernummer nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-898">tax id no.</span></span>
  
<span data-ttu-id="8aba5-899">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-899">tax id number</span></span>
  
<span data-ttu-id="8aba5-900">tax identification
</span><span class="sxs-lookup"><span data-stu-id="8aba5-900">tax identification</span></span>
  
<span data-ttu-id="8aba5-901">Tax Identification #</span><span class="sxs-lookup"><span data-stu-id="8aba5-901">tax identification#</span></span>
  
<span data-ttu-id="8aba5-902">Steuern Sie Nein.</span><span class="sxs-lookup"><span data-stu-id="8aba5-902">tax no.</span></span>
  
<span data-ttu-id="8aba5-903">Tax #</span><span class="sxs-lookup"><span data-stu-id="8aba5-903">tax#</span></span>
  
<span data-ttu-id="8aba5-904">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-904">taxid#</span></span>
  
<span data-ttu-id="8aba5-905">Tax-Datei</span><span class="sxs-lookup"><span data-stu-id="8aba5-905">tax file</span></span>
  
<span data-ttu-id="8aba5-906">Steuern Sie Datei nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-906">tax file no.</span></span>
  
<span data-ttu-id="8aba5-907">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-907">personal id number</span></span>
  
<span data-ttu-id="8aba5-908">Skatt-Id-nummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-908">skatt id nummer</span></span>
  
<span data-ttu-id="8aba5-909">Skatt identifikation</span><span class="sxs-lookup"><span data-stu-id="8aba5-909">skatt identifikation</span></span>
  
<span data-ttu-id="8aba5-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="8aba5-911">GROßBRITANNIEN</span><span class="sxs-lookup"><span data-stu-id="8aba5-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="8aba5-912">Format</span><span class="sxs-lookup"><span data-stu-id="8aba5-912">Format</span></span>

<span data-ttu-id="8aba5-913">Eindeutige Steuernummer-Referenz (UTR): 10 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8aba5-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="8aba5-p103">Sozialversicherungsnummer (NINO): Weitere Informationen hierzu finden Sie im Abschnitt "Großbritannien National Insurance Anzahl (NINO)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8aba5-p103">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8aba5-916">Muster</span><span class="sxs-lookup"><span data-stu-id="8aba5-916">Pattern</span></span>

<span data-ttu-id="8aba5-917">Eindeutige Steuernummer-Referenz (UTR): 10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8aba5-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="8aba5-p104">Sozialversicherungsnummer (NINO): Weitere Informationen hierzu finden Sie im Abschnitt "Großbritannien National Insurance Anzahl (NINO)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8aba5-p104">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8aba5-920">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8aba5-920">Checksum</span></span>

<span data-ttu-id="8aba5-921">Ja</span><span class="sxs-lookup"><span data-stu-id="8aba5-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8aba5-922">Definition</span><span class="sxs-lookup"><span data-stu-id="8aba5-922">Definition</span></span>

<span data-ttu-id="8aba5-923">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8aba5-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8aba5-924">Die Funktion `Func_uk_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8aba5-925">Ein Schlüsselwort aus `Keywords_uk_eu_tax_file_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8aba5-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8aba5-926">Keywords</span><span class="sxs-lookup"><span data-stu-id="8aba5-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="8aba5-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="8aba5-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="8aba5-928">tax id
</span><span class="sxs-lookup"><span data-stu-id="8aba5-928">tax id</span></span>
  
<span data-ttu-id="8aba5-929">Steuernummer nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-929">tax id no.</span></span>
  
<span data-ttu-id="8aba5-930">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="8aba5-930">tax id number</span></span>
  
<span data-ttu-id="8aba5-931">tax identification
</span><span class="sxs-lookup"><span data-stu-id="8aba5-931">tax identification</span></span>
  
<span data-ttu-id="8aba5-932">Tax Identification #</span><span class="sxs-lookup"><span data-stu-id="8aba5-932">tax identification#</span></span>
  
<span data-ttu-id="8aba5-933">Steuern Sie Nein.</span><span class="sxs-lookup"><span data-stu-id="8aba5-933">tax no.</span></span>
  
<span data-ttu-id="8aba5-934">Tax #</span><span class="sxs-lookup"><span data-stu-id="8aba5-934">tax#</span></span>
  
<span data-ttu-id="8aba5-935">Taxid #</span><span class="sxs-lookup"><span data-stu-id="8aba5-935">taxid#</span></span>
  
<span data-ttu-id="8aba5-936">Tax-Datei</span><span class="sxs-lookup"><span data-stu-id="8aba5-936">tax file</span></span>
  
<span data-ttu-id="8aba5-937">Steuern Sie Datei nicht.</span><span class="sxs-lookup"><span data-stu-id="8aba5-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8aba5-938">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8aba5-938">See also</span></span>

[<span data-ttu-id="8aba5-939">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="8aba5-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

