---
title: EU-Telefonnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1c90ca41-1681-46bf-8ad6-6bf4cec5c426
description: Verhinderung von Datenverlust (DLP) in die Office 365-Sicherheit &amp; Compliance Center enthält viele Arten von vertraulichen Informationen, die Sie in Ihrer DLP-Richtlinien verwendet werden. In diesem Thema wird den Typ der Telefonnummer EU-vertrauliche Informationen.
ms.openlocfilehash: 9dd878e3385312982f9f3a4927205e3ebb27aabb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529524"
---
# <a name="eu-phone-number"></a><span data-ttu-id="48927-104">EU-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="48927-104">EU Phone Number</span></span>

<span data-ttu-id="48927-p102">Verhinderung von Datenverlust (DLP) in die Office 365-Sicherheit &amp; Compliance Center enthält viele Arten von vertraulichen Informationen, die Sie in Ihrer DLP-Richtlinien verwendet werden. In diesem Thema wird den Typ der Telefonnummer EU-vertrauliche Informationen.</span><span class="sxs-lookup"><span data-stu-id="48927-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU Phone Number sensitive information type.</span></span> 
  
## <a name="austria"></a><span data-ttu-id="48927-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="48927-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="48927-108">Format</span><span class="sxs-lookup"><span data-stu-id="48927-108">Format</span></span>

<span data-ttu-id="48927-109">Keine standard Länge</span><span class="sxs-lookup"><span data-stu-id="48927-109">No standard length</span></span>
  
### <a name="pattern"></a><span data-ttu-id="48927-110">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-110">Pattern</span></span>

- <span data-ttu-id="48927-111">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-111">Digits</span></span> 
    
- <span data-ttu-id="48927-112">Nur Mobiltelefone beginnen mit der Ziffer "6"</span><span class="sxs-lookup"><span data-stu-id="48927-112">Only mobile phone numbers begin with the digit "6"</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-113">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-113">Checksum</span></span>

<span data-ttu-id="48927-114">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-114">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-115">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-115">Definition</span></span>

<span data-ttu-id="48927-116">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-117">Der reguläre Ausdruck `Regex_austria_eu_telephone_number_1` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-117">The regular expression  `Regex_austria_eu_telephone_number_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-118">Ein Schlüsselwort aus `Keywords_austria_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-118">A keyword from  `Keywords_austria_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-119">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-119">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-120">Der reguläre Ausdruck `Regex_austria_eu_telephone_number_2` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-120">The regular expression  `Regex_austria_eu_telephone_number_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-121">Ein Schlüsselwort aus `Keywords_austria_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-121">A keyword from  `Keywords_austria_eu_telephone_number` is found.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_telephone_number_1" />
          <Match idRef="Keywords_austria_eu_telephone_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_telephone_number_2" />
          <Match idRef="Keywords_austria_eu_telephone_number" />
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_austria_eu_formatted_telephone_number_1" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_austria_eu_formatted_telephone_number_2" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a><span data-ttu-id="48927-122">Belgien</span><span class="sxs-lookup"><span data-stu-id="48927-122">Belgium</span></span>

### <a name="definition"></a><span data-ttu-id="48927-123">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-123">Definition</span></span>

<span data-ttu-id="48927-124">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-125">Der reguläre Ausdruck `Regex_belgium_eu_telephone_number_1` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-125">The regular expression  `Regex_belgium_eu_telephone_number_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-126">Ein Schlüsselwort aus `Keywords_belgium_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-126">A keyword from  `Keywords_belgium_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-127">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-127">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-128">Der reguläre Ausdruck `Regex_belgium_eu_telephone_number_2` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-128">The regular expression  `Regex_belgium_eu_telephone_number_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-129">Ein Schlüsselwort aus `Keywords_belgium_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-129">A keyword from  `Keywords_belgium_eu_telephone_number` is found.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_telephone_number_1" />
          <Match idRef="Keywords_belgium_eu_telephone_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_telephone_number_2" />
          <Match idRef="Keywords_belgium_eu_telephone_number" />
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_belgium_eu_formatted_telephone_number_1" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_belgium_eu_formatted_telephone_number_2" />
          </Pattern></Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="48927-130">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="48927-130">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-131">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-131">Pattern</span></span>

- <span data-ttu-id="48927-132">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-132">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-133">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-133">Checksum</span></span>

<span data-ttu-id="48927-134">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-134">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-135">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-135">Definition</span></span>

<span data-ttu-id="48927-136">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-137">Der reguläre Ausdruck `Regex_bulgaria_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-137">The regular expression  `Regex_bulgaria_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-138">Ein Schlüsselwort aus `Keywords_bulgaria_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-138">A keyword from  `Keywords_bulgaria_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-139">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-139">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-140">Der reguläre Ausdruck `Regex_bulgaria_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-140">The regular expression  `Regex_bulgaria_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_telephone_number" />
          <Match idRef="Keywords_bulgaria_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_bulgaria_eu_formatted_telephone_number" />
          </Pattern>
          
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="48927-141">Kroatien</span><span class="sxs-lookup"><span data-stu-id="48927-141">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-142">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-142">Pattern</span></span>

- <span data-ttu-id="48927-143">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-143">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-144">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-144">Checksum</span></span>

<span data-ttu-id="48927-145">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-145">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-146">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-146">Definition</span></span>

<span data-ttu-id="48927-147">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-148">Der reguläre Ausdruck `Regex_croatia_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-148">The regular expression  `Regex_croatia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-149">Ein Schlüsselwort aus `Keywords_croatia_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-149">A keyword from  `Keywords_croatia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-150">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-150">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-151">Der reguläre Ausdruck `Regex_croatia_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-151">The regular expression  `Regex_croatia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_telephone_number" />
          <Match idRef="Keywords_croatia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_croatia_eu_formatted_telephone_number" />
          </Pattern>
         </Entity>
```

## <a name="cyprus"></a><span data-ttu-id="48927-152">Zypern</span><span class="sxs-lookup"><span data-stu-id="48927-152">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-153">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-153">Pattern</span></span>

- <span data-ttu-id="48927-154">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-154">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-155">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-155">Checksum</span></span>

<span data-ttu-id="48927-156">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-156">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-157">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-157">Definition</span></span>

<span data-ttu-id="48927-158">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-159">Der reguläre Ausdruck `Regex_cyprus_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-159">The regular expression  `Regex_cyprus_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-160">Ein Schlüsselwort aus `Keywords_cyprus_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-160">A keyword from  `Keywords_cyprus_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-161">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-161">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-162">Der reguläre Ausdruck `Regex_cyprus_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-162">The regular expression  `Regex_cyprus_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_telephone_number" />
          <Match idRef="Keywords_cyprus_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_cyprus_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="48927-163">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="48927-163">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-164">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-164">Pattern</span></span>

- <span data-ttu-id="48927-165">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-165">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-166">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-166">Checksum</span></span>

<span data-ttu-id="48927-167">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-167">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-168">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-168">Definition</span></span>

<span data-ttu-id="48927-169">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-169">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-170">Der reguläre Ausdruck `Regex_czech_republic_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-170">The regular expression  `Regex_czech_republic_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-171">Ein Schlüsselwort aus `Keywords_czech_republic_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-171">A keyword from  `Keywords_czech_republic_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-172">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-172">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-173">Der reguläre Ausdruck `Regex_czech_republic_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-173">The regular expression  `Regex_czech_republic_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_telephone_number" />
          <Match idRef="Keywords_czech_republic_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_czech_republic_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="denmark"></a><span data-ttu-id="48927-174">Dänemark</span><span class="sxs-lookup"><span data-stu-id="48927-174">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-175">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-175">Pattern</span></span>

- <span data-ttu-id="48927-176">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-176">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-177">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-177">Checksum</span></span>

<span data-ttu-id="48927-178">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-178">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-179">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-179">Definition</span></span>

<span data-ttu-id="48927-180">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-180">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-181">Der reguläre Ausdruck `Regex_denmark_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-181">The regular expression  `Regex_denmark_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-182">Ein Schlüsselwort aus `Keywords_denmark_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-182">A keyword from  `Keywords_denmark_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-183">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-184">Der reguläre Ausdruck `Regex_denmark_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-184">The regular expression  `Regex_denmark_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_telephone_number" />
          <Match idRef="Keywords_denmark_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_denmark_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="estonia"></a><span data-ttu-id="48927-185">Estland</span><span class="sxs-lookup"><span data-stu-id="48927-185">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-186">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-186">Pattern</span></span>

- <span data-ttu-id="48927-187">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-187">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-188">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-188">Checksum</span></span>

<span data-ttu-id="48927-189">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-189">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-190">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-190">Definition</span></span>

<span data-ttu-id="48927-191">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-191">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-192">Der reguläre Ausdruck `Regex_estonia_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-192">The regular expression  `Regex_estonia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-193">Ein Schlüsselwort aus `Keywords_estonia_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-193">A keyword from  `Keywords_estonia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-194">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-195">Der reguläre Ausdruck `Regex_estonia_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-195">The regular expression  `Regex_estonia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_telephone_number" />
          <Match idRef="Keywords_estonia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_estonia_eu_formatted_telephone_number" />
          </Pattern>
       </Entity>
```

## <a name="finland"></a><span data-ttu-id="48927-196">Finnland</span><span class="sxs-lookup"><span data-stu-id="48927-196">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-197">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-197">Pattern</span></span>

- <span data-ttu-id="48927-198">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-198">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-199">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-199">Checksum</span></span>

<span data-ttu-id="48927-200">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-200">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-201">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-201">Definition</span></span>

<span data-ttu-id="48927-202">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-203">Der reguläre Ausdruck `Regex_finland_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-203">The regular expression  `Regex_finland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-204">Ein Schlüsselwort aus `Keywords_finland_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-204">A keyword from  `Keywords_finland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-205">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-205">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-206">Der reguläre Ausdruck `Regex_finland_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-206">The regular expression  `Regex_finland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_telephone_number" />
          <Match idRef="Keywords_finland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_finland_eu_formatted_telephone_number" />
             </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="48927-207">Frankreich</span><span class="sxs-lookup"><span data-stu-id="48927-207">France</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-208">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-208">Pattern</span></span>

- <span data-ttu-id="48927-209">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-209">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-210">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-210">Checksum</span></span>

<span data-ttu-id="48927-211">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-211">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-212">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-212">Definition</span></span>

<span data-ttu-id="48927-213">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-213">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-214">Der reguläre Ausdruck `Regex_france_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-214">The regular expression  `Regex_france_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-215">Ein Schlüsselwort aus `Keywords_france_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-215">A keyword from  `Keywords_france_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-216">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-217">Der reguläre Ausdruck `Regex_france_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-217">The regular expression  `Regex_france_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_telephone_number" />
          <Match idRef="Keywords_france_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_france_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="germany"></a><span data-ttu-id="48927-218">Deutschland</span><span class="sxs-lookup"><span data-stu-id="48927-218">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-219">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-219">Pattern</span></span>

- <span data-ttu-id="48927-220">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-220">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-221">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-221">Checksum</span></span>

<span data-ttu-id="48927-222">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-222">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-223">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-223">Definition</span></span>

<span data-ttu-id="48927-224">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-224">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-225">Der reguläre Ausdruck `Regex_germany_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-225">The regular expression  `Regex_germany_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-226">Ein Schlüsselwort aus `Keywords_germany_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-226">A keyword from  `Keywords_germany_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-227">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-227">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-228">Der reguläre Ausdruck `Regex_germany_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-228">The regular expression  `Regex_germany_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_telephone_number" />
          <Match idRef="Keywords_germany_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_germany_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="greece"></a><span data-ttu-id="48927-229">Griechenland</span><span class="sxs-lookup"><span data-stu-id="48927-229">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-230">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-230">Pattern</span></span>

- <span data-ttu-id="48927-231">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-231">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-232">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-232">Checksum</span></span>

<span data-ttu-id="48927-233">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-233">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-234">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-234">Definition</span></span>

<span data-ttu-id="48927-235">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-235">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-236">Der reguläre Ausdruck `Regex_greece_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-236">The regular expression  `Regex_greece_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-237">Ein Schlüsselwort aus `Keywords_greece_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-237">A keyword from  `Keywords_greece_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-238">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-238">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-239">Der reguläre Ausdruck `Regex_greece_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-239">The regular expression  `Regex_greece_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_telephone_number" />
          <Match idRef="Keywords_greece_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_greece_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="hungary"></a><span data-ttu-id="48927-240">Ungarn</span><span class="sxs-lookup"><span data-stu-id="48927-240">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-241">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-241">Pattern</span></span>

- <span data-ttu-id="48927-242">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-242">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-243">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-243">Checksum</span></span>

<span data-ttu-id="48927-244">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-244">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-245">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-245">Definition</span></span>

<span data-ttu-id="48927-246">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-247">Der reguläre Ausdruck `Regex_hungary_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-247">The regular expression  `Regex_hungary_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-248">Ein Schlüsselwort aus `Keywords_hungary_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-248">A keyword from  `Keywords_hungary_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-249">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-250">Der reguläre Ausdruck `Regex_hungary_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-250">The regular expression  `Regex_hungary_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_telephone_number" />
          <Match idRef="Keywords_hungary_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_hungary_eu_formatted_telephone_number" />
          </Pattern>
       </Entity>
```

## <a name="ireland"></a><span data-ttu-id="48927-251">Irland</span><span class="sxs-lookup"><span data-stu-id="48927-251">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-252">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-252">Pattern</span></span>

- <span data-ttu-id="48927-253">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-253">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-254">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-254">Checksum</span></span>

<span data-ttu-id="48927-255">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-255">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-256">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-256">Definition</span></span>

<span data-ttu-id="48927-257">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-257">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-258">Der reguläre Ausdruck `Regex_ireland_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-258">The regular expression  `Regex_ireland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-259">Ein Schlüsselwort aus `Keywords_ireland_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-259">A keyword from  `Keywords_ireland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-260">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-260">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-261">Der reguläre Ausdruck `Regex_ireland_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-261">The regular expression  `Regex_ireland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_telephone_number" />
          <Match idRef="Keywords_ireland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_ireland_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="italy"></a><span data-ttu-id="48927-262">Italien</span><span class="sxs-lookup"><span data-stu-id="48927-262">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-263">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-263">Pattern</span></span>

- <span data-ttu-id="48927-264">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-264">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-265">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-265">Checksum</span></span>

<span data-ttu-id="48927-266">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-266">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-267">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-267">Definition</span></span>

<span data-ttu-id="48927-268">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-268">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-269">Der reguläre Ausdruck `Regex_italy_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-269">The regular expression  `Regex_italy_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-270">Ein Schlüsselwort aus `Keywords_italy_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-270">A keyword from  `Keywords_italy_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-271">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-272">Der reguläre Ausdruck `Regex_italy_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-272">The regular expression  `Regex_italy_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_telephone_number" />
          <Match idRef="Keywords_italy_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_italy_eu_formatted_telephone_number" />
          </Pattern>
         </Entity>
```

## <a name="latvia"></a><span data-ttu-id="48927-273">Lettland</span><span class="sxs-lookup"><span data-stu-id="48927-273">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-274">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-274">Pattern</span></span>

- <span data-ttu-id="48927-275">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-275">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-276">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-276">Checksum</span></span>

<span data-ttu-id="48927-277">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-277">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-278">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-278">Definition</span></span>

<span data-ttu-id="48927-279">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-279">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-280">Der reguläre Ausdruck `Regex_latvia_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-280">The regular expression  `Regex_latvia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-281">Ein Schlüsselwort aus `Keywords_latvia_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-281">A keyword from  `Keywords_latvia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-282">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-283">Der reguläre Ausdruck `Regex_latvia_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-283">The regular expression  `Regex_latvia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_telephone_number" />
          <Match idRef="Keywords_latvia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_latvia_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="lithuania"></a><span data-ttu-id="48927-284">Litauen</span><span class="sxs-lookup"><span data-stu-id="48927-284">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-285">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-285">Pattern</span></span>

- <span data-ttu-id="48927-286">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-286">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-287">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-287">Checksum</span></span>

<span data-ttu-id="48927-288">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-288">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-289">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-289">Definition</span></span>

<span data-ttu-id="48927-290">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-291">Der reguläre Ausdruck `Regex_lithuania_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-291">The regular expression  `Regex_lithuania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-292">Ein Schlüsselwort aus `Keywords_lithuania_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-292">A keyword from  `Keywords_lithuania_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-293">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-293">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-294">Der reguläre Ausdruck `Regex_lithuania_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-294">The regular expression  `Regex_lithuania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_telephone_number" />
          <Match idRef="Keywords_lithuania_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_lithuania_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="48927-295">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="48927-295">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-296">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-296">Pattern</span></span>

- <span data-ttu-id="48927-297">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-297">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-298">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-298">Checksum</span></span>

<span data-ttu-id="48927-299">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-299">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-300">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-300">Definition</span></span>

<span data-ttu-id="48927-301">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-301">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-302">Der reguläre Ausdruck `Regex_luxemburg_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-302">The regular expression  `Regex_luxemburg_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-303">Ein Schlüsselwort aus `Keywords_luxemburg_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-303">A keyword from  `Keywords_luxemburg_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-304">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-304">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-305">Der reguläre Ausdruck `Regex_luxemburg_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-305">The regular expression  `Regex_luxemburg_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_telephone_number" />
          <Match idRef="Keywords_luxemburg_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_luxemburg_eu_formatted_telephone_number" />
                  </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="48927-306">Malta</span><span class="sxs-lookup"><span data-stu-id="48927-306">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-307">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-307">Pattern</span></span>

- <span data-ttu-id="48927-308">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-308">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-309">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-309">Checksum</span></span>

<span data-ttu-id="48927-310">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-310">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-311">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-311">Definition</span></span>

<span data-ttu-id="48927-312">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-313">Der reguläre Ausdruck `Regex_malta_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-313">The regular expression  `Regex_malta_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-314">Ein Schlüsselwort aus `Keywords_malta_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-314">A keyword from  `Keywords_malta_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-315">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-315">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-316">Der reguläre Ausdruck `Regex_malta_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-316">The regular expression  `Regex_malta_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_telephone_number" />
          <Match idRef="Keywords_malta_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_malta_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="48927-317">Niederlande</span><span class="sxs-lookup"><span data-stu-id="48927-317">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-318">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-318">Pattern</span></span>

- <span data-ttu-id="48927-319">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-319">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-320">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-320">Checksum</span></span>

<span data-ttu-id="48927-321">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-321">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-322">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-322">Definition</span></span>

<span data-ttu-id="48927-323">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-323">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-324">Der reguläre Ausdruck `Regex_netherlands_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-324">The regular expression  `Regex_netherlands_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-325">Ein Schlüsselwort aus `Keywords_netherlands_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-325">A keyword from  `Keywords_netherlands_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-326">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-327">Der reguläre Ausdruck `Regex_netherlands_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-327">The regular expression  `Regex_netherlands_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_telephone_number" />
          <Match idRef="Keywords_netherlands_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_netherlands_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="48927-328">Polen</span><span class="sxs-lookup"><span data-stu-id="48927-328">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-329">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-329">Pattern</span></span>

- <span data-ttu-id="48927-330">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-330">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-331">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-331">Checksum</span></span>

<span data-ttu-id="48927-332">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-332">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-333">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-333">Definition</span></span>

<span data-ttu-id="48927-334">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-334">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-335">Der reguläre Ausdruck `Regex_poland_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-335">The regular expression  `Regex_poland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-336">Ein Schlüsselwort aus `Keywords_poland_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-336">A keyword from  `Keywords_poland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-337">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-337">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-338">Der reguläre Ausdruck `Regex_poland_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-338">The regular expression  `Regex_poland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_telephone_number" />
          <Match idRef="Keywords_poland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_poland_eu_formatted_telephone_number" />
             </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="48927-339">Portugal</span><span class="sxs-lookup"><span data-stu-id="48927-339">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-340">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-340">Pattern</span></span>

- <span data-ttu-id="48927-341">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-341">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-342">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-342">Checksum</span></span>

<span data-ttu-id="48927-343">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-343">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-344">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-344">Definition</span></span>

<span data-ttu-id="48927-345">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-345">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-346">Der reguläre Ausdruck `Regex_portugal_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-346">The regular expression  `Regex_portugal_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-347">Ein Schlüsselwort aus `Keywords_portugal_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-347">A keyword from  `Keywords_portugal_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-348">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-348">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-349">Der reguläre Ausdruck `Regex_portugal_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-349">The regular expression  `Regex_portugal_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_telephone_number" />
          <Match idRef="Keywords_portugal_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_portugal_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="romania"></a><span data-ttu-id="48927-350">Rumänien</span><span class="sxs-lookup"><span data-stu-id="48927-350">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-351">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-351">Pattern</span></span>

- <span data-ttu-id="48927-352">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-352">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-353">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-353">Checksum</span></span>

<span data-ttu-id="48927-354">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-354">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-355">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-355">Definition</span></span>

<span data-ttu-id="48927-356">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-356">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-357">Der reguläre Ausdruck `Regex_romania_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-357">The regular expression  `Regex_romania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-358">Ein Schlüsselwort aus `Keywords_romania_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-358">A keyword from  `Keywords_romania_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-359">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-359">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-360">Der reguläre Ausdruck `Regex_romania_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-360">The regular expression  `Regex_romania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_telephone_number" />
          <Match idRef="Keywords_romania_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_romania_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="48927-361">Slowakei</span><span class="sxs-lookup"><span data-stu-id="48927-361">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-362">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-362">Pattern</span></span>

- <span data-ttu-id="48927-363">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-363">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-364">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-364">Checksum</span></span>

<span data-ttu-id="48927-365">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-365">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-366">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-366">Definition</span></span>

<span data-ttu-id="48927-367">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-367">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-368">Der reguläre Ausdruck `Regex_slovakia_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-368">The regular expression  `Regex_slovakia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-369">Ein Schlüsselwort aus `Keywords_slovakia_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-369">A keyword from  `Keywords_slovakia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-370">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-370">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-371">Der reguläre Ausdruck `Regex_slovakia_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-371">The regular expression  `Regex_slovakia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_telephone_number" />
          <Match idRef="Keywords_slovakia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_slovakia_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="48927-372">Slowenien</span><span class="sxs-lookup"><span data-stu-id="48927-372">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-373">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-373">Pattern</span></span>

- <span data-ttu-id="48927-374">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-374">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-375">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-375">Checksum</span></span>

<span data-ttu-id="48927-376">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-377">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-377">Definition</span></span>

<span data-ttu-id="48927-378">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-379">Der reguläre Ausdruck `Regex_slovenia_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-379">The regular expression  `Regex_slovenia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-380">Ein Schlüsselwort aus `Keywords_slovenia_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-380">A keyword from  `Keywords_slovenia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-381">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-382">Der reguläre Ausdruck `Regex_slovenia_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-382">The regular expression  `Regex_slovenia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_telephone_number" />
          <Match idRef="Keywords_slovenia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_slovenia_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="spain"></a><span data-ttu-id="48927-383">Spanien</span><span class="sxs-lookup"><span data-stu-id="48927-383">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-384">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-384">Pattern</span></span>

- <span data-ttu-id="48927-385">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-385">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-386">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-386">Checksum</span></span>

<span data-ttu-id="48927-387">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-387">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-388">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-388">Definition</span></span>

<span data-ttu-id="48927-389">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-389">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-390">Der reguläre Ausdruck `Regex_spain_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-390">The regular expression  `Regex_spain_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-391">Ein Schlüsselwort aus `Keywords_spain_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-391">A keyword from  `Keywords_spain_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-392">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-392">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-393">Der reguläre Ausdruck `Regex_spain_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-393">The regular expression  `Regex_spain_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_telephone_number" />
          <Match idRef="Keywords_spain_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_spain_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="sweden"></a><span data-ttu-id="48927-394">Schweden</span><span class="sxs-lookup"><span data-stu-id="48927-394">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-395">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-395">Pattern</span></span>

- <span data-ttu-id="48927-396">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-396">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-397">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-397">Checksum</span></span>

<span data-ttu-id="48927-398">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-398">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-399">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-399">Definition</span></span>

<span data-ttu-id="48927-400">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-400">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-401">Der reguläre Ausdruck `Regex_sweden_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-401">The regular expression  `Regex_sweden_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-402">Ein Schlüsselwort aus `Keywords_sweden_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-402">A keyword from  `Keywords_sweden_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-403">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-403">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-404">Der reguläre Ausdruck `Regex_sweden_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-404">The regular expression  `Regex_sweden_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_telephone_number" />
          <Match idRef="Keywords_sweden_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_sweden_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="uk"></a><span data-ttu-id="48927-405">GROßBRITANNIEN</span><span class="sxs-lookup"><span data-stu-id="48927-405">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="48927-406">Muster</span><span class="sxs-lookup"><span data-stu-id="48927-406">Pattern</span></span>

- <span data-ttu-id="48927-407">Ziffern</span><span class="sxs-lookup"><span data-stu-id="48927-407">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="48927-408">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="48927-408">Checksum</span></span>

<span data-ttu-id="48927-409">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48927-409">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="48927-410">Definition</span><span class="sxs-lookup"><span data-stu-id="48927-410">Definition</span></span>

<span data-ttu-id="48927-411">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-412">Der reguläre Ausdruck `Regex_uk_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-412">The regular expression  `Regex_uk_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="48927-413">Ein Schlüsselwort aus `Keywords_uk_eu_telephone_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="48927-413">A keyword from  `Keywords_uk_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="48927-414">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="48927-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="48927-415">Der reguläre Ausdruck `Regex_uk_eu_telephone_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="48927-415">The regular expression  `Regex_uk_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_telephone_number" />
          <Match idRef="Keywords_uk_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_uk_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="48927-416">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48927-416">See also</span></span>

[<span data-ttu-id="48927-417">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="48927-417">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

