---
title: EU Mobiltelefonnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 555e7675-2ae8-42d1-9b8e-2c8f8cd21337
description: Verhinderung von Datenverlust (DLP) in die Office 365-Sicherheit &amp; Compliance Center enthält viele Arten von vertraulichen Informationen, die Sie in Ihrer DLP-Richtlinien verwendet werden. In diesem Thema wird den Typ der EU Mobiltelefonnummer vertraulichen Informationen.
ms.openlocfilehash: d0818759dae8ed86cc9aef6f7fad48cbd2acf24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529356"
---
# <a name="eu-mobile-phone-number"></a><span data-ttu-id="17f6a-104">EU Mobiltelefonnummer</span><span class="sxs-lookup"><span data-stu-id="17f6a-104">EU Mobile Phone Number</span></span>

<span data-ttu-id="17f6a-p102">Verhinderung von Datenverlust (DLP) in die Office 365-Sicherheit &amp; Compliance Center enthält viele Arten von vertraulichen Informationen, die Sie in Ihrer DLP-Richtlinien verwendet werden. In diesem Thema wird den Typ der EU Mobiltelefonnummer vertraulichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="17f6a-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU Mobile Phone Number sensitive information type.</span></span> 
  
## <a name="austria"></a><span data-ttu-id="17f6a-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="17f6a-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="17f6a-108">Format</span><span class="sxs-lookup"><span data-stu-id="17f6a-108">Format</span></span>

<span data-ttu-id="17f6a-109">Ziffern ohne standard Längen</span><span class="sxs-lookup"><span data-stu-id="17f6a-109">Digits without standard lengths</span></span>
  
### <a name="pattern"></a><span data-ttu-id="17f6a-110">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-110">Pattern</span></span>

-  <span data-ttu-id="17f6a-111">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-111">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="17f6a-112">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-112">Definition</span></span>

<span data-ttu-id="17f6a-113">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-113">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-114">Der reguläre Ausdruck `Regex_austria_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-114">The regular expression  `Regex_austria_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-115">Der reguläre Ausdruck `Regex_austria_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-115">The regular expression  `Regex_austria_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-116">Ein Schlüsselwort aus `Keywords_austria_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-116">A keyword from  `Keywords_austria_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_mobile_number"/>
          <Match idRef="Keywords_austria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_austria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a><span data-ttu-id="17f6a-117">Belgien</span><span class="sxs-lookup"><span data-stu-id="17f6a-117">Belgium</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-118">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-118">Pattern</span></span>

-  <span data-ttu-id="17f6a-119">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-119">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="17f6a-120">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-120">Definition</span></span>

<span data-ttu-id="17f6a-121">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-122">Der reguläre Ausdruck `Regex_belgium_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-122">The regular expression  `Regex_belgium_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-123">Der reguläre Ausdruck `Regex_belgium_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-123">The regular expression  `Regex_belgium_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-124">Ein Schlüsselwort aus `Keywords_belgium_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-124">A keyword from  `Keywords_belgium_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_mobile_number"/>
          <Match idRef="Keywords_belgium_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_belgium_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="17f6a-125">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="17f6a-125">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-126">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-126">Pattern</span></span>

-  <span data-ttu-id="17f6a-127">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-127">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="17f6a-128">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-128">Definition</span></span>

<span data-ttu-id="17f6a-129">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-129">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-130">Der reguläre Ausdruck `Regex_bulgaria_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-130">The regular expression  `Regex_bulgaria_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-131">Der reguläre Ausdruck `Regex_bulgaria_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-131">The regular expression  `Regex_bulgaria_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-132">Ein Schlüsselwort aus `Keywords_bulgaria_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-132">A keyword from  `Keywords_bulgaria_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_mobile_number"/>
          <Match idRef="Keywords_bulgaria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_bulgaria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="17f6a-133">Kroatien</span><span class="sxs-lookup"><span data-stu-id="17f6a-133">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-134">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-134">Pattern</span></span>

-  <span data-ttu-id="17f6a-135">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-135">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="17f6a-136">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-136">Definition</span></span>

<span data-ttu-id="17f6a-137">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-138">Der reguläre Ausdruck `Regex_croatia_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-138">The regular expression  `Regex_croatia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-139">Der reguläre Ausdruck `Regex_croatia_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-139">The regular expression  `Regex_croatia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-140">Ein Schlüsselwort aus `Keywords_croatia_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-140">A keyword from  `Keywords_croatia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_mobile_number"/>
          <Match idRef="Keywords_croatia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_croatia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="cyprus"></a><span data-ttu-id="17f6a-141">Zypern</span><span class="sxs-lookup"><span data-stu-id="17f6a-141">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-142">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-142">Pattern</span></span>

-  <span data-ttu-id="17f6a-143">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-143">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-144">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-144">Checksum</span></span>

<span data-ttu-id="17f6a-145">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-145">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-146">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-146">Definition</span></span>

<span data-ttu-id="17f6a-147">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-148">Der reguläre Ausdruck `Regex_cyprus_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-148">The regular expression  `Regex_cyprus_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-149">Der reguläre Ausdruck `Regex_cyprus_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-149">The regular expression  `Regex_cyprus_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-150">Ein Schlüsselwort aus `Keywords_cyprus_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-150">A keyword from  `Keywords_cyprus_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_mobile_number"/>
          <Match idRef="Keywords_cyprus_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_cyprus_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="17f6a-151">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="17f6a-151">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-152">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-152">Pattern</span></span>

-  <span data-ttu-id="17f6a-153">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-153">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-154">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-154">Checksum</span></span>

<span data-ttu-id="17f6a-155">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-155">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-156">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-156">Definition</span></span>

<span data-ttu-id="17f6a-157">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-157">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-158">Der reguläre Ausdruck `Regex_czech_republic_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-158">The regular expression  `Regex_czech_republic_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-159">Der reguläre Ausdruck `Regex_czech_republic_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-159">The regular expression  `Regex_czech_republic_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-160">Ein Schlüsselwort aus `Keywords_czech_republic_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-160">A keyword from  `Keywords_czech_republic_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_mobile_number"/>
          <Match idRef="Keywords_czech_republic_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_czech_republic_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="denmark"></a><span data-ttu-id="17f6a-161">Dänemark</span><span class="sxs-lookup"><span data-stu-id="17f6a-161">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-162">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-162">Pattern</span></span>

-  <span data-ttu-id="17f6a-163">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-163">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-164">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-164">Checksum</span></span>

<span data-ttu-id="17f6a-165">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-165">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-166">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-166">Definition</span></span>

<span data-ttu-id="17f6a-167">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-167">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-168">Der reguläre Ausdruck `Regex_denmark_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-168">The regular expression  `Regex_denmark_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-169">Der reguläre Ausdruck `Regex_denmark_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-169">The regular expression  `Regex_denmark_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-170">Ein Schlüsselwort aus `Keywords_denmark_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-170">A keyword from  `Keywords_denmark_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_mobile_number"/>
          <Match idRef="Keywords_denmark_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_denmark_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="estonia"></a><span data-ttu-id="17f6a-171">Estland</span><span class="sxs-lookup"><span data-stu-id="17f6a-171">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-172">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-172">Pattern</span></span>

-  <span data-ttu-id="17f6a-173">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-173">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-174">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-174">Checksum</span></span>

<span data-ttu-id="17f6a-175">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-175">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-176">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-176">Definition</span></span>

<span data-ttu-id="17f6a-177">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-177">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-178">Der reguläre Ausdruck `Regex_estonia_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-178">The regular expression  `Regex_estonia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-179">Der reguläre Ausdruck `Regex_estonia_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-179">The regular expression  `Regex_estonia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-180">Ein Schlüsselwort aus `Keywords_estonia_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-180">A keyword from  `Keywords_estonia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_mobile_number"/>
          <Match idRef="Keywords_estonia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_estonia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="finland"></a><span data-ttu-id="17f6a-181">Finnland</span><span class="sxs-lookup"><span data-stu-id="17f6a-181">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-182">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-182">Pattern</span></span>

-  <span data-ttu-id="17f6a-183">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-183">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-184">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-184">Checksum</span></span>

<span data-ttu-id="17f6a-185">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-185">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-186">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-186">Definition</span></span>

<span data-ttu-id="17f6a-187">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-187">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-188">Der reguläre Ausdruck `Regex_finland_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-188">The regular expression  `Regex_finland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-189">Der reguläre Ausdruck `Regex_finland_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-189">The regular expression  `Regex_finland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-190">Ein Schlüsselwort aus `Keywords_finland_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-190">A keyword from  `Keywords_finland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_mobile_number"/>
          <Match idRef="Keywords_finland_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_finland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="17f6a-191">Frankreich</span><span class="sxs-lookup"><span data-stu-id="17f6a-191">France</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-192">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-192">Pattern</span></span>

-  <span data-ttu-id="17f6a-193">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-193">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-194">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-194">Checksum</span></span>

<span data-ttu-id="17f6a-195">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-195">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-196">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-196">Definition</span></span>

<span data-ttu-id="17f6a-197">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-197">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-198">Der reguläre Ausdruck `Regex_france_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-198">The regular expression  `Regex_france_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-199">Der reguläre Ausdruck `Regex_france_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-199">The regular expression  `Regex_france_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-200">Ein Schlüsselwort aus `Keywords_france_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-200">A keyword from  `Keywords_france_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_mobile_number"/>
          <Match idRef="Keywords_france_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_france_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="germany"></a><span data-ttu-id="17f6a-201">Deutschland</span><span class="sxs-lookup"><span data-stu-id="17f6a-201">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-202">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-202">Pattern</span></span>

-  <span data-ttu-id="17f6a-203">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-203">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-204">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-204">Checksum</span></span>

<span data-ttu-id="17f6a-205">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-205">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-206">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-206">Definition</span></span>

<span data-ttu-id="17f6a-207">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-207">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-208">Der reguläre Ausdruck `Regex_germany_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-208">The regular expression  `Regex_germany_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-209">Der reguläre Ausdruck `Regex_germany_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-209">The regular expression  `Regex_germany_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-210">Ein Schlüsselwort aus `Keywords_germany_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-210">A keyword from  `Keywords_germany_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_mobile_number"/>
          <Match idRef="Keywords_germany_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_germany_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="greece"></a><span data-ttu-id="17f6a-211">Griechenland</span><span class="sxs-lookup"><span data-stu-id="17f6a-211">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-212">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-212">Pattern</span></span>

-  <span data-ttu-id="17f6a-213">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-213">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-214">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-214">Checksum</span></span>

<span data-ttu-id="17f6a-215">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-215">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-216">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-216">Definition</span></span>

<span data-ttu-id="17f6a-217">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-217">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-218">Der reguläre Ausdruck `Regex_greece_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-218">The regular expression  `Regex_greece_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-219">Der reguläre Ausdruck `Regex_greece_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-219">The regular expression  `Regex_greece_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-220">Ein Schlüsselwort aus `Keywords_greece_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-220">A keyword from  `Keywords_greece_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_mobile_number"/>
          <Match idRef="Keywords_greece_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_greece_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="hungary"></a><span data-ttu-id="17f6a-221">Ungarn</span><span class="sxs-lookup"><span data-stu-id="17f6a-221">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-222">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-222">Pattern</span></span>

-  <span data-ttu-id="17f6a-223">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-223">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-224">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-224">Checksum</span></span>

<span data-ttu-id="17f6a-225">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-225">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-226">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-226">Definition</span></span>

<span data-ttu-id="17f6a-227">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-227">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-228">Der reguläre Ausdruck `Regex_hungary_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-228">The regular expression  `Regex_hungary_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-229">Der reguläre Ausdruck `Regex_hungary_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-229">The regular expression  `Regex_hungary_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-230">Ein Schlüsselwort aus `Keywords_hungary_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-230">A keyword from  `Keywords_hungary_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_mobile_number"/>
          <Match idRef="Keywords_hungary_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_hungary_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="ireland"></a><span data-ttu-id="17f6a-231">Irland</span><span class="sxs-lookup"><span data-stu-id="17f6a-231">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-232">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-232">Pattern</span></span>

-  <span data-ttu-id="17f6a-233">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-233">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-234">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-234">Checksum</span></span>

<span data-ttu-id="17f6a-235">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-235">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-236">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-236">Definition</span></span>

<span data-ttu-id="17f6a-237">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-237">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-238">Der reguläre Ausdruck `Regex_ireland_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-238">The regular expression  `Regex_ireland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-239">Der reguläre Ausdruck `Regex_ireland_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-239">The regular expression  `Regex_ireland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-240">Ein Schlüsselwort aus `Keywords_ireland_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-240">A keyword from  `Keywords_ireland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_mobile_number"/>
          <Match idRef="Keywords_ireland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_ireland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="italy"></a><span data-ttu-id="17f6a-241">Italien</span><span class="sxs-lookup"><span data-stu-id="17f6a-241">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-242">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-242">Pattern</span></span>

-  <span data-ttu-id="17f6a-243">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-243">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-244">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-244">Checksum</span></span>

<span data-ttu-id="17f6a-245">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-245">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-246">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-246">Definition</span></span>

<span data-ttu-id="17f6a-247">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-248">Der reguläre Ausdruck `Regex_italy_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-248">The regular expression  `Regex_italy_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-249">Der reguläre Ausdruck `Regex_italy_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-249">The regular expression  `Regex_italy_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-250">Ein Schlüsselwort aus `Keywords_italy_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-250">A keyword from  `Keywords_italy_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_mobile_number"/>
          <Match idRef="Keywords_italy_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_italy_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="latvia"></a><span data-ttu-id="17f6a-251">Lettland</span><span class="sxs-lookup"><span data-stu-id="17f6a-251">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-252">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-252">Pattern</span></span>

-  <span data-ttu-id="17f6a-253">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-253">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-254">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-254">Checksum</span></span>

<span data-ttu-id="17f6a-255">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-255">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-256">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-256">Definition</span></span>

<span data-ttu-id="17f6a-257">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-257">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-258">Der reguläre Ausdruck `Regex_latvia_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-258">The regular expression  `Regex_latvia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-259">Der reguläre Ausdruck `Regex_latvia_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-259">The regular expression  `Regex_latvia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-260">Ein Schlüsselwort aus `Keywords_latvia_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-260">A keyword from  `Keywords_latvia_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_mobile_number"/>
          <Match idRef="Keywords_latvia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_latvia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="lithuania"></a><span data-ttu-id="17f6a-261">Litauen</span><span class="sxs-lookup"><span data-stu-id="17f6a-261">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-262">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-262">Pattern</span></span>

-  <span data-ttu-id="17f6a-263">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-263">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-264">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-264">Checksum</span></span>

<span data-ttu-id="17f6a-265">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-265">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-266">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-266">Definition</span></span>

<span data-ttu-id="17f6a-267">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-268">Der reguläre Ausdruck `Regex_lithuania_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-268">The regular expression  `Regex_lithuania_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-269">Der reguläre Ausdruck `Regex_lithuania_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-269">The regular expression  `Regex_lithuania_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-270">Ein Schlüsselwort aus `Keywords_lithuania_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-270">A keyword from  `Keywords_lithuania_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_mobile_number"/>
          <Match idRef="Keywords_lithuania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_lithuania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="17f6a-271">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="17f6a-271">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-272">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-272">Pattern</span></span>

-  <span data-ttu-id="17f6a-273">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-273">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-274">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-274">Checksum</span></span>

<span data-ttu-id="17f6a-275">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-275">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-276">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-276">Definition</span></span>

<span data-ttu-id="17f6a-277">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-277">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-278">Der reguläre Ausdruck `Regex_luxumburg_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-278">The regular expression  `Regex_luxumburg_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-279">Der reguläre Ausdruck `Regex_luxumburg_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-279">The regular expression  `Regex_luxumburg_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-280">Ein Schlüsselwort aus `Keywords_luxumburg_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-280">A keyword from  `Keywords_luxumburg_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxumburg_eu_mobile_number"/>
          <Match idRef="Keywords_luxumburg_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_luxumburg_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="17f6a-281">Malta</span><span class="sxs-lookup"><span data-stu-id="17f6a-281">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-282">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-282">Pattern</span></span>

-  <span data-ttu-id="17f6a-283">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-283">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-284">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-284">Checksum</span></span>

<span data-ttu-id="17f6a-285">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-285">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-286">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-286">Definition</span></span>

<span data-ttu-id="17f6a-287">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-288">Der reguläre Ausdruck `Regex_malta_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-288">The regular expression  `Regex_malta_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-289">Der reguläre Ausdruck `Regex_malta_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-289">The regular expression  `Regex_malta_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-290">Ein Schlüsselwort aus `Keywords_malta_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-290">A keyword from  `Keywords_malta_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_mobile_number"/>
          <Match idRef="Keywords_malta_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_malta_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="17f6a-291">Niederlande</span><span class="sxs-lookup"><span data-stu-id="17f6a-291">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-292">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-292">Pattern</span></span>

-  <span data-ttu-id="17f6a-293">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-293">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-294">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-294">Checksum</span></span>

<span data-ttu-id="17f6a-295">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-295">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-296">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-296">Definition</span></span>

<span data-ttu-id="17f6a-297">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-297">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-298">Der reguläre Ausdruck `Regex_netherlands_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-298">The regular expression  `Regex_netherlands_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-299">Der reguläre Ausdruck `Regex_netherlands_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-299">The regular expression  `Regex_netherlands_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-300">Ein Schlüsselwort aus `Keywords_netherlands_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-300">A keyword from  `Keywords_netherlands_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_mobile_number"/>
          <Match idRef="Keywords_netherlands_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_netherlands_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="17f6a-301">Polen</span><span class="sxs-lookup"><span data-stu-id="17f6a-301">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-302">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-302">Pattern</span></span>

-  <span data-ttu-id="17f6a-303">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-303">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-304">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-304">Checksum</span></span>

<span data-ttu-id="17f6a-305">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-305">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-306">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-306">Definition</span></span>

<span data-ttu-id="17f6a-307">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-308">Der reguläre Ausdruck `Regex_poland_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-308">The regular expression  `Regex_poland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-309">Der reguläre Ausdruck `Regex_poland_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-309">The regular expression  `Regex_poland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-310">Ein Schlüsselwort aus `Keywords_poland_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-310">A keyword from  `Keywords_poland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_mobile_number"/>
          <Match idRef="Keywords_poland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_poland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="17f6a-311">Portugal</span><span class="sxs-lookup"><span data-stu-id="17f6a-311">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-312">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-312">Pattern</span></span>

-  <span data-ttu-id="17f6a-313">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-313">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-314">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-314">Checksum</span></span>

<span data-ttu-id="17f6a-315">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-315">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-316">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-316">Definition</span></span>

<span data-ttu-id="17f6a-317">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-317">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-318">Der reguläre Ausdruck `Regex_portugal_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-318">The regular expression  `Regex_portugal_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-319">Der reguläre Ausdruck `Regex_portugal_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-319">The regular expression  `Regex_portugal_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-320">Ein Schlüsselwort aus `Keywords_portugal_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-320">A keyword from  `Keywords_portugal_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_mobile_number"/>
          <Match idRef="Keywords_portugal_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_portugal_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="romania"></a><span data-ttu-id="17f6a-321">Rumänien</span><span class="sxs-lookup"><span data-stu-id="17f6a-321">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-322">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-322">Pattern</span></span>

-  <span data-ttu-id="17f6a-323">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-323">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-324">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-324">Checksum</span></span>

<span data-ttu-id="17f6a-325">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-325">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-326">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-326">Definition</span></span>

<span data-ttu-id="17f6a-327">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-327">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-328">Der reguläre Ausdruck `Regex_romania_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-328">The regular expression  `Regex_romania_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-329">Der reguläre Ausdruck `Regex_romania_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-329">The regular expression  `Regex_romania_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-330">Ein Schlüsselwort aus `Keywords_romania_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-330">A keyword from  `Keywords_romania_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_mobile_number"/>
          <Match idRef="Keywords_romania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_romania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="17f6a-331">Slowakei</span><span class="sxs-lookup"><span data-stu-id="17f6a-331">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-332">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-332">Pattern</span></span>

-  <span data-ttu-id="17f6a-333">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-333">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-334">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-334">Checksum</span></span>

<span data-ttu-id="17f6a-335">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-335">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-336">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-336">Definition</span></span>

<span data-ttu-id="17f6a-337">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-337">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-338">Der reguläre Ausdruck `Regex_slovakia_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-338">The regular expression  `Regex_slovakia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-339">Der reguläre Ausdruck `Regex_slovakia_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-339">The regular expression  `Regex_slovakia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-340">Ein Schlüsselwort aus `Keywords_slovakia_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-340">A keyword from  `Keywords_slovakia_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_mobile_number"/>
          <Match idRef="Keywords_slovakia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovakia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="17f6a-341">Slowenien</span><span class="sxs-lookup"><span data-stu-id="17f6a-341">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-342">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-342">Pattern</span></span>

-  <span data-ttu-id="17f6a-343">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-343">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-344">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-344">Checksum</span></span>

<span data-ttu-id="17f6a-345">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-345">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-346">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-346">Definition</span></span>

<span data-ttu-id="17f6a-347">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-347">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-348">Der reguläre Ausdruck `Regex_slovenia_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-348">The regular expression  `Regex_slovenia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-349">Der reguläre Ausdruck `Regex_slovenia_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-349">The regular expression  `Regex_slovenia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-350">Ein Schlüsselwort aus `Keywords_slovenia_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-350">A keyword from  `Keywords_slovenia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_mobile_number"/>
          <Match idRef="Keywords_slovenia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovenia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="spain"></a><span data-ttu-id="17f6a-351">Spanien</span><span class="sxs-lookup"><span data-stu-id="17f6a-351">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-352">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-352">Pattern</span></span>

-  <span data-ttu-id="17f6a-353">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-353">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-354">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-354">Checksum</span></span>

<span data-ttu-id="17f6a-355">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-355">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-356">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-356">Definition</span></span>

<span data-ttu-id="17f6a-357">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-358">Der reguläre Ausdruck `Regex_spain_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-358">The regular expression  `Regex_spain_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-359">Der reguläre Ausdruck `Regex_spain_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-359">The regular expression  `Regex_spain_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-360">Ein Schlüsselwort aus `Keywords_spain_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-360">A keyword from  `Keywords_spain_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_mobile_number"/>
          <Match idRef="Keywords_spain_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_spain_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="sweden"></a><span data-ttu-id="17f6a-361">Schweden</span><span class="sxs-lookup"><span data-stu-id="17f6a-361">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-362">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-362">Pattern</span></span>

-  <span data-ttu-id="17f6a-363">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-363">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-364">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-364">Checksum</span></span>

<span data-ttu-id="17f6a-365">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-365">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-366">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-366">Definition</span></span>

<span data-ttu-id="17f6a-367">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-367">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-368">Der reguläre Ausdruck `Regex_sweden_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-368">The regular expression  `Regex_sweden_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-369">Der reguläre Ausdruck `Regex_sweden_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-369">The regular expression  `Regex_sweden_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-370">Ein Schlüsselwort aus `Keywords_sweden_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-370">A keyword from  `Keywords_sweden_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_mobile_number"/>
          <Match idRef="Keywords_sweden_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_sweden_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="uk"></a><span data-ttu-id="17f6a-371">GROßBRITANNIEN</span><span class="sxs-lookup"><span data-stu-id="17f6a-371">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="17f6a-372">Muster</span><span class="sxs-lookup"><span data-stu-id="17f6a-372">Pattern</span></span>

-  <span data-ttu-id="17f6a-373">Ziffern</span><span class="sxs-lookup"><span data-stu-id="17f6a-373">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="17f6a-374">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="17f6a-374">Checksum</span></span>

<span data-ttu-id="17f6a-375">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="17f6a-375">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="17f6a-376">Definition</span><span class="sxs-lookup"><span data-stu-id="17f6a-376">Definition</span></span>

<span data-ttu-id="17f6a-377">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="17f6a-377">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="17f6a-378">Der reguläre Ausdruck `Regex_uk_eu_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-378">The regular expression  `Regex_uk_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-379">Der reguläre Ausdruck `Regex_uk_eu_formatted_mobile_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="17f6a-379">The regular expression  `Regex_uk_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="17f6a-380">Ein Schlüsselwort aus `Keywords_uk_eu_mobile_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="17f6a-380">A keyword from  `Keywords_uk_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_mobile_number"/>
          <Match idRef="Keywords_uk_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_uk_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="17f6a-381">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17f6a-381">See also</span></span>

[<span data-ttu-id="17f6a-382">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="17f6a-382">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

