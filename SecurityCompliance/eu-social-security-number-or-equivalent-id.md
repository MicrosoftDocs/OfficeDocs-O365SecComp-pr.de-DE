---
title: EU-sozialVersicherungsNummer oder entsprechende ID
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn die EU-sozialVersicherungsNummer oder der entsprechende ID-vertrauliche Informationstyp erkannt wird. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: c0c808eafa52209c79f3b4e8a2113f587fd8a771
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410800"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="5b81a-104">EU-sozialVersicherungsNummer oder entsprechende ID</span><span class="sxs-lookup"><span data-stu-id="5b81a-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="5b81a-105">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn die EU-sozialVersicherungsNummer (SSN) oder der entsprechende ID-vertrauliche Informationstyp erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="5b81a-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type.</span></span> <span data-ttu-id="5b81a-106">Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="5b81a-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="5b81a-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="5b81a-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="5b81a-108">Format</span><span class="sxs-lookup"><span data-stu-id="5b81a-108">Format</span></span>

<span data-ttu-id="5b81a-109">10 Ziffern im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="5b81a-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5b81a-110">Muster</span><span class="sxs-lookup"><span data-stu-id="5b81a-110">Pattern</span></span>

<span data-ttu-id="5b81a-111">10 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="5b81a-111">10 digits:</span></span>
  
-  <span data-ttu-id="5b81a-112">Drei Ziffern, die einer Seriennummer entsprechen</span><span class="sxs-lookup"><span data-stu-id="5b81a-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="5b81a-113">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="5b81a-113">One check digit</span></span>
    
- <span data-ttu-id="5b81a-114">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="5b81a-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5b81a-115">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="5b81a-115">Checksum</span></span>

<span data-ttu-id="5b81a-116">Ja</span><span class="sxs-lookup"><span data-stu-id="5b81a-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5b81a-117">Definition</span><span class="sxs-lookup"><span data-stu-id="5b81a-117">Definition</span></span>

<span data-ttu-id="5b81a-118">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-119">Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5b81a-120">Ein Schlüsselwort `Keywords_austria_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="5b81a-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5b81a-121">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-122">Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_austria_eu_ssn_or_equivalent" />
        </Pattern>
<Pattern confidenceLevel="75">
            <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5b81a-123">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="5b81a-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="5b81a-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5b81a-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5b81a-125">Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-125">social security no</span></span>
  
<span data-ttu-id="5b81a-126">social security number</span><span class="sxs-lookup"><span data-stu-id="5b81a-126">social security number</span></span>
  
<span data-ttu-id="5b81a-127">social security code</span><span class="sxs-lookup"><span data-stu-id="5b81a-127">social security code</span></span>
  
<span data-ttu-id="5b81a-128">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-128">insurance number</span></span>
  
<span data-ttu-id="5b81a-129">Austrian SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-129">austrian ssn</span></span>
  
<span data-ttu-id="5b81a-130">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-130">ssn#</span></span>
  
<span data-ttu-id="5b81a-131">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-131">ssn</span></span>
  
<span data-ttu-id="5b81a-132">versicherungscode</span><span class="sxs-lookup"><span data-stu-id="5b81a-132">insurance code</span></span>
  
<span data-ttu-id="5b81a-133">versicherungscode #</span><span class="sxs-lookup"><span data-stu-id="5b81a-133">insurance code#</span></span>
  
<span data-ttu-id="5b81a-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="5b81a-134">socialsecurityno#</span></span>
  
<span data-ttu-id="5b81a-135">Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="5b81a-136">soziale Sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="5b81a-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="5b81a-137">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="5b81a-138">Belgien</span><span class="sxs-lookup"><span data-stu-id="5b81a-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="5b81a-139">Format</span><span class="sxs-lookup"><span data-stu-id="5b81a-139">Format</span></span>

<span data-ttu-id="5b81a-140">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="5b81a-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5b81a-141">Muster</span><span class="sxs-lookup"><span data-stu-id="5b81a-141">Pattern</span></span>

<span data-ttu-id="5b81a-142">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="5b81a-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5b81a-143">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="5b81a-143">Checksum</span></span>

<span data-ttu-id="5b81a-144">Ja</span><span class="sxs-lookup"><span data-stu-id="5b81a-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5b81a-145">Definition</span><span class="sxs-lookup"><span data-stu-id="5b81a-145">Definition</span></span>

<span data-ttu-id="5b81a-146">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-147">Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5b81a-148">Ein Schlüsselwort `Keywords_belgium_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="5b81a-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5b81a-149">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-150">Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_belgium_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5b81a-151">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="5b81a-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="5b81a-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5b81a-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5b81a-153">belgische nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-153">belgian national number</span></span>
  
<span data-ttu-id="5b81a-154">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-154">national number</span></span>
  
<span data-ttu-id="5b81a-155">social security number</span><span class="sxs-lookup"><span data-stu-id="5b81a-155">social security number</span></span>
  
<span data-ttu-id="5b81a-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="5b81a-156">nationalnumber#</span></span>
  
<span data-ttu-id="5b81a-157">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-157">ssn#</span></span>
  
<span data-ttu-id="5b81a-158">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-158">ssn</span></span>
  
<span data-ttu-id="5b81a-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="5b81a-159">nationalnumber</span></span>
  
<span data-ttu-id="5b81a-160">BNN</span><span class="sxs-lookup"><span data-stu-id="5b81a-160">bnn#</span></span>
  
<span data-ttu-id="5b81a-161">BNN</span><span class="sxs-lookup"><span data-stu-id="5b81a-161">bnn</span></span>
  
<span data-ttu-id="5b81a-162">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-162">personal id number</span></span>
  
<span data-ttu-id="5b81a-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="5b81a-163">personalidnumber#</span></span>
  
<span data-ttu-id="5b81a-164">Numéro National</span><span class="sxs-lookup"><span data-stu-id="5b81a-164">numéro national</span></span>
  
<span data-ttu-id="5b81a-165">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="5b81a-165">numéro de sécurité</span></span>
  
<span data-ttu-id="5b81a-166">Numéro d'assuré</span><span class="sxs-lookup"><span data-stu-id="5b81a-166">numéro d'assuré</span></span>
  
<span data-ttu-id="5b81a-167">identifizierbare nationale</span><span class="sxs-lookup"><span data-stu-id="5b81a-167">identifiant national</span></span>
  
<span data-ttu-id="5b81a-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="5b81a-168">identifiantnational#</span></span>
  
<span data-ttu-id="5b81a-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="5b81a-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="5b81a-170">Kroatien</span><span class="sxs-lookup"><span data-stu-id="5b81a-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="5b81a-171">Format</span><span class="sxs-lookup"><span data-stu-id="5b81a-171">Format</span></span>

<span data-ttu-id="5b81a-172">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="5b81a-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5b81a-173">Muster</span><span class="sxs-lookup"><span data-stu-id="5b81a-173">Pattern</span></span>

 <span data-ttu-id="5b81a-174">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="5b81a-174">11 digits:</span></span> 
  
-  <span data-ttu-id="5b81a-175">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="5b81a-175">Ten digits</span></span> 
    
- <span data-ttu-id="5b81a-176">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="5b81a-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5b81a-177">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="5b81a-177">Checksum</span></span>

<span data-ttu-id="5b81a-178">Ja</span><span class="sxs-lookup"><span data-stu-id="5b81a-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5b81a-179">Definition</span><span class="sxs-lookup"><span data-stu-id="5b81a-179">Definition</span></span>

<span data-ttu-id="5b81a-180">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-181">Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5b81a-182">Ein Schlüsselwort `Keywords_croatia_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="5b81a-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5b81a-183">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-184">Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_croatia_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5b81a-185">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="5b81a-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="5b81a-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5b81a-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5b81a-187">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-187">personal identification number</span></span>
  
<span data-ttu-id="5b81a-188">Master-Bürgerzahl</span><span class="sxs-lookup"><span data-stu-id="5b81a-188">master citizen number</span></span>
  
<span data-ttu-id="5b81a-189">national identification number</span><span class="sxs-lookup"><span data-stu-id="5b81a-189">national identification number</span></span>
  
<span data-ttu-id="5b81a-190">social security number</span><span class="sxs-lookup"><span data-stu-id="5b81a-190">social security number</span></span>
  
<span data-ttu-id="5b81a-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="5b81a-191">nationalnumber#</span></span>
  
<span data-ttu-id="5b81a-192">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-192">ssn#</span></span>
  
<span data-ttu-id="5b81a-193">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-193">ssn</span></span>
  
<span data-ttu-id="5b81a-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="5b81a-194">nationalnumber</span></span>
  
<span data-ttu-id="5b81a-195">BNN</span><span class="sxs-lookup"><span data-stu-id="5b81a-195">bnn#</span></span>
  
<span data-ttu-id="5b81a-196">BNN</span><span class="sxs-lookup"><span data-stu-id="5b81a-196">bnn</span></span>
  
<span data-ttu-id="5b81a-197">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-197">personal id number</span></span>
  
<span data-ttu-id="5b81a-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="5b81a-198">personalidnumber#</span></span>
  
<span data-ttu-id="5b81a-199">OIB</span><span class="sxs-lookup"><span data-stu-id="5b81a-199">oib</span></span>
  
<span data-ttu-id="5b81a-200">Osobni identifikacijski Broj</span><span class="sxs-lookup"><span data-stu-id="5b81a-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="5b81a-201">Tschechien</span><span class="sxs-lookup"><span data-stu-id="5b81a-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="5b81a-202">Format</span><span class="sxs-lookup"><span data-stu-id="5b81a-202">Format</span></span>

<span data-ttu-id="5b81a-203">Zehn Ziffern und ein umgekehrter Schrägstrich im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="5b81a-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5b81a-204">Muster</span><span class="sxs-lookup"><span data-stu-id="5b81a-204">Pattern</span></span>

<span data-ttu-id="5b81a-205">Zehn Ziffern und ein umgekehrter Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="5b81a-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="5b81a-206">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT):</span><span class="sxs-lookup"><span data-stu-id="5b81a-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="5b81a-207">Einen umgekehrten Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="5b81a-207">A backslash</span></span>
    
- <span data-ttu-id="5b81a-208">Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am selben Datum geboren wurden</span><span class="sxs-lookup"><span data-stu-id="5b81a-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="5b81a-209">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="5b81a-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5b81a-210">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="5b81a-210">Checksum</span></span>

<span data-ttu-id="5b81a-211">Ja</span><span class="sxs-lookup"><span data-stu-id="5b81a-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5b81a-212">Definition</span><span class="sxs-lookup"><span data-stu-id="5b81a-212">Definition</span></span>

<span data-ttu-id="5b81a-213">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-214">Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5b81a-215">Ein Schlüsselwort `Keywords_czech_republic_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="5b81a-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5b81a-216">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-217">Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_czech_republic_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5b81a-218">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="5b81a-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="5b81a-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5b81a-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5b81a-220">Geburtsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-220">birth number</span></span>
  
<span data-ttu-id="5b81a-221">national identification number</span><span class="sxs-lookup"><span data-stu-id="5b81a-221">national identification number</span></span>
  
<span data-ttu-id="5b81a-222">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-222">personal identification number</span></span>
  
<span data-ttu-id="5b81a-223">social security number</span><span class="sxs-lookup"><span data-stu-id="5b81a-223">social security number</span></span>
  
<span data-ttu-id="5b81a-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="5b81a-224">nationalnumber#</span></span>
  
<span data-ttu-id="5b81a-225">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-225">ssn#</span></span>
  
<span data-ttu-id="5b81a-226">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-226">ssn</span></span>
  
<span data-ttu-id="5b81a-227">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-227">national number</span></span>
  
<span data-ttu-id="5b81a-228">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-228">personal id number</span></span>
  
<span data-ttu-id="5b81a-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="5b81a-229">personalidnumber#</span></span>
  
<span data-ttu-id="5b81a-230">rč</span><span class="sxs-lookup"><span data-stu-id="5b81a-230">rč</span></span>
  
<span data-ttu-id="5b81a-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="5b81a-231">rodné číslo</span></span>
  
<span data-ttu-id="5b81a-232">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="5b81a-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="5b81a-233">Dänemark</span><span class="sxs-lookup"><span data-stu-id="5b81a-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="5b81a-234">Format</span><span class="sxs-lookup"><span data-stu-id="5b81a-234">Format</span></span>

<span data-ttu-id="5b81a-235">Zehn Ziffern und ein Bindestrich im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="5b81a-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5b81a-236">Muster</span><span class="sxs-lookup"><span data-stu-id="5b81a-236">Pattern</span></span>

<span data-ttu-id="5b81a-237">Zehn Ziffern und ein Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="5b81a-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="5b81a-238">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="5b81a-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="5b81a-239">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="5b81a-239">A hyphen</span></span>
    
- <span data-ttu-id="5b81a-240">Vier Ziffern, die einer Sequenznummer entsprechen</span><span class="sxs-lookup"><span data-stu-id="5b81a-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5b81a-241">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="5b81a-241">Checksum</span></span>

<span data-ttu-id="5b81a-242">Ja</span><span class="sxs-lookup"><span data-stu-id="5b81a-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5b81a-243">Definition</span><span class="sxs-lookup"><span data-stu-id="5b81a-243">Definition</span></span>

<span data-ttu-id="5b81a-244">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-245">Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5b81a-246">Ein Schlüsselwort `Keywords_denmark_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="5b81a-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5b81a-247">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-248">Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_denmark_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5b81a-249">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="5b81a-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="5b81a-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5b81a-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5b81a-251">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-251">personal identification number</span></span>
  
<span data-ttu-id="5b81a-252">national identification number</span><span class="sxs-lookup"><span data-stu-id="5b81a-252">national identification number</span></span>
  
<span data-ttu-id="5b81a-253">social security number</span><span class="sxs-lookup"><span data-stu-id="5b81a-253">social security number</span></span>
  
<span data-ttu-id="5b81a-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="5b81a-254">nationalnumber#</span></span>
  
<span data-ttu-id="5b81a-255">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-255">ssn#</span></span>
  
<span data-ttu-id="5b81a-256">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-256">ssn</span></span>
  
<span data-ttu-id="5b81a-257">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-257">national number</span></span>
  
<span data-ttu-id="5b81a-258">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-258">personal id number</span></span>
  
<span data-ttu-id="5b81a-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="5b81a-259">personalidnumber#</span></span>
  
<span data-ttu-id="5b81a-260">CPR-Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-260">cpr-nummer</span></span>
  
<span data-ttu-id="5b81a-261">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="5b81a-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="5b81a-262">Finnland</span><span class="sxs-lookup"><span data-stu-id="5b81a-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="5b81a-263">Format</span><span class="sxs-lookup"><span data-stu-id="5b81a-263">Format</span></span>

<span data-ttu-id="5b81a-264">Eine Kombination aus 11 Zeichen im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="5b81a-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5b81a-265">Muster</span><span class="sxs-lookup"><span data-stu-id="5b81a-265">Pattern</span></span>

<span data-ttu-id="5b81a-266">Eine Kombination aus 11 Zeichen im angegebenen Format:</span><span class="sxs-lookup"><span data-stu-id="5b81a-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="5b81a-267">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="5b81a-267">Six digits</span></span> 
    
- <span data-ttu-id="5b81a-268">Eine der folgenden Instanzen:</span><span class="sxs-lookup"><span data-stu-id="5b81a-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="5b81a-269">Plus-Symbol</span><span class="sxs-lookup"><span data-stu-id="5b81a-269">Plus symbol</span></span>
    
  - <span data-ttu-id="5b81a-270">Minus Zeichen</span><span class="sxs-lookup"><span data-stu-id="5b81a-270">Minus symbol</span></span>
    
  - <span data-ttu-id="5b81a-271">Der Buchstabe "A" (Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="5b81a-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="5b81a-272">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="5b81a-272">Three digits</span></span>
    
- <span data-ttu-id="5b81a-273">Ein Buchstabe oder eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="5b81a-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5b81a-274">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="5b81a-274">Checksum</span></span>

<span data-ttu-id="5b81a-275">Ja</span><span class="sxs-lookup"><span data-stu-id="5b81a-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5b81a-276">Definition</span><span class="sxs-lookup"><span data-stu-id="5b81a-276">Definition</span></span>

<span data-ttu-id="5b81a-277">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-278">Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5b81a-279">Ein Schlüsselwort `Keywords_finland_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="5b81a-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5b81a-280">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-281">Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_finland_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5b81a-282">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="5b81a-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="5b81a-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5b81a-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5b81a-284">identification number</span><span class="sxs-lookup"><span data-stu-id="5b81a-284">identification number</span></span>
  
<span data-ttu-id="5b81a-285">persönliche ID</span><span class="sxs-lookup"><span data-stu-id="5b81a-285">personal id</span></span>
  
<span data-ttu-id="5b81a-286">Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-286">identity number</span></span>
  
<span data-ttu-id="5b81a-287">nationale finnische ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-287">finnish national id number</span></span>
  
<span data-ttu-id="5b81a-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="5b81a-288">personalidnumber#</span></span>
  
<span data-ttu-id="5b81a-289">national identification number</span><span class="sxs-lookup"><span data-stu-id="5b81a-289">national identification number</span></span>
  
<span data-ttu-id="5b81a-290">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-290">id number</span></span>
  
<span data-ttu-id="5b81a-291">nationale ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="5b81a-291">national id no.</span></span>
  
<span data-ttu-id="5b81a-292">nationale ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-292">national id number</span></span>
  
<span data-ttu-id="5b81a-293">ID Nein</span><span class="sxs-lookup"><span data-stu-id="5b81a-293">id no</span></span>
  
<span data-ttu-id="5b81a-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="5b81a-294">tunnistenumero</span></span>
  
<span data-ttu-id="5b81a-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="5b81a-295">henkilötunnus</span></span>
  
<span data-ttu-id="5b81a-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="5b81a-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="5b81a-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="5b81a-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="5b81a-298">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="5b81a-298">identiteetti numero</span></span>
  
<span data-ttu-id="5b81a-299">Suomen der Kok henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="5b81a-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="5b81a-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="5b81a-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="5b81a-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="5b81a-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="5b81a-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="5b81a-302">tunnusnumero</span></span>
  
<span data-ttu-id="5b81a-303">der Kok tunnus numero</span><span class="sxs-lookup"><span data-stu-id="5b81a-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="5b81a-304">Hetu</span><span class="sxs-lookup"><span data-stu-id="5b81a-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="5b81a-305">Frankreich</span><span class="sxs-lookup"><span data-stu-id="5b81a-305">France</span></span>

<span data-ttu-id="5b81a-306">Weitere Informationen finden Sie im Abschnitt "französische sozialVersicherungsNummer (INSEE)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5b81a-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="5b81a-307">Deutschland</span><span class="sxs-lookup"><span data-stu-id="5b81a-307">Germany</span></span>

<span data-ttu-id="5b81a-308">Weitere Informationen finden Sie im Abschnitt "Deutschland PersonalausweisNummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5b81a-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="5b81a-309">Griechenland</span><span class="sxs-lookup"><span data-stu-id="5b81a-309">Greece</span></span>

<span data-ttu-id="5b81a-310">Weitere Informationen finden Sie im Abschnitt "GriechenLand National ID Card" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5b81a-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="5b81a-311">Ungarn</span><span class="sxs-lookup"><span data-stu-id="5b81a-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="5b81a-312">Format</span><span class="sxs-lookup"><span data-stu-id="5b81a-312">Format</span></span>

<span data-ttu-id="5b81a-313">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="5b81a-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5b81a-314">Muster</span><span class="sxs-lookup"><span data-stu-id="5b81a-314">Pattern</span></span>

<span data-ttu-id="5b81a-315">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="5b81a-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="5b81a-316">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="5b81a-316">Checksum</span></span>

<span data-ttu-id="5b81a-317">Ja</span><span class="sxs-lookup"><span data-stu-id="5b81a-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5b81a-318">Definition</span><span class="sxs-lookup"><span data-stu-id="5b81a-318">Definition</span></span>

<span data-ttu-id="5b81a-319">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-320">Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5b81a-321">Ein Schlüsselwort `Keywords_hungary_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="5b81a-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5b81a-322">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-323">Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_hungary_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5b81a-324">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="5b81a-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="5b81a-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5b81a-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5b81a-326">Sozialversicherungsnummer (ungarisch)</span><span class="sxs-lookup"><span data-stu-id="5b81a-326">hungarian social security number</span></span>
  
<span data-ttu-id="5b81a-327">social security number</span><span class="sxs-lookup"><span data-stu-id="5b81a-327">social security number</span></span>
  
<span data-ttu-id="5b81a-328">socialsecuritynumber #</span><span class="sxs-lookup"><span data-stu-id="5b81a-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="5b81a-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="5b81a-329">hssn#</span></span>
  
<span data-ttu-id="5b81a-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="5b81a-330">socialsecuritynno</span></span>
  
<span data-ttu-id="5b81a-331">hssn</span><span class="sxs-lookup"><span data-stu-id="5b81a-331">hssn</span></span>
  
<span data-ttu-id="5b81a-332">Taj</span><span class="sxs-lookup"><span data-stu-id="5b81a-332">taj</span></span>
  
<span data-ttu-id="5b81a-333">Taj</span><span class="sxs-lookup"><span data-stu-id="5b81a-333">taj#</span></span>
  
<span data-ttu-id="5b81a-334">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-334">ssn</span></span>
  
<span data-ttu-id="5b81a-335">SSN</span><span class="sxs-lookup"><span data-stu-id="5b81a-335">ssn#</span></span>
  
<span data-ttu-id="5b81a-336">Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-336">social security no</span></span>
  
<span data-ttu-id="5b81a-337">ÁFA</span><span class="sxs-lookup"><span data-stu-id="5b81a-337">áfa</span></span>
  
<span data-ttu-id="5b81a-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="5b81a-338">közösségi adószám</span></span>
  
<span data-ttu-id="5b81a-339">Általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="5b81a-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="5b81a-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="5b81a-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="5b81a-341">ÁFA szám</span><span class="sxs-lookup"><span data-stu-id="5b81a-341">áfa szám</span></span>
  
<span data-ttu-id="5b81a-342">Magyar ÁFA szám</span><span class="sxs-lookup"><span data-stu-id="5b81a-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="5b81a-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="5b81a-343">Portugal</span></span>

<span data-ttu-id="5b81a-344">Weitere Informationen finden Sie im Abschnitt "portugiesische Bürgerkarten Nummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5b81a-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="5b81a-345">Spanien</span><span class="sxs-lookup"><span data-stu-id="5b81a-345">Spain</span></span>

<span data-ttu-id="5b81a-346">Weitere Informationen finden Sie im Abschnitt "sozialVersicherungsNummer (SSN) in Spanien" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5b81a-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="5b81a-347">Schweden</span><span class="sxs-lookup"><span data-stu-id="5b81a-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="5b81a-348">Format</span><span class="sxs-lookup"><span data-stu-id="5b81a-348">Format</span></span>

<span data-ttu-id="5b81a-349">12 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="5b81a-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="5b81a-350">Muster</span><span class="sxs-lookup"><span data-stu-id="5b81a-350">Pattern</span></span>

<span data-ttu-id="5b81a-351">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="5b81a-351">12 digits:</span></span>
  
-  <span data-ttu-id="5b81a-352">Acht Ziffern, die dem Geburtsdatum entsprechen (JJJJMMTT)</span><span class="sxs-lookup"><span data-stu-id="5b81a-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="5b81a-353">Drei Ziffern, die einer Seriennummer entsprechen, wobei:</span><span class="sxs-lookup"><span data-stu-id="5b81a-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="5b81a-354">Die letzte Ziffer in der Seriennummer kennzeichnet das Geschlecht durch die Zuweisung einer ungerade Zahl für männliche und eine gerade Zahl für weibliche</span><span class="sxs-lookup"><span data-stu-id="5b81a-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="5b81a-355">Bis zu 1990 entspricht die Zuordnung der Seriennummer der Grafschaft, in der der Träger der Nummer geboren wurde, oder (wenn er vor 1947 geboren wurde), in dem er nach Steuerdaten Sätzen am 1. Januar 1947 lebte, mit einem speziellen Code (in der Regel 9 als 7. Ziffer) für Einwanderer</span><span class="sxs-lookup"><span data-stu-id="5b81a-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="5b81a-356">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="5b81a-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="5b81a-357">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="5b81a-357">Checksum</span></span>

<span data-ttu-id="5b81a-358">Ja</span><span class="sxs-lookup"><span data-stu-id="5b81a-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="5b81a-359">Definition</span><span class="sxs-lookup"><span data-stu-id="5b81a-359">Definition</span></span>

<span data-ttu-id="5b81a-360">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-361">Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="5b81a-362">Ein Schlüsselwort `Keywords_sweden_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="5b81a-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="5b81a-363">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="5b81a-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="5b81a-364">Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5b81a-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_sweden_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5b81a-365">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="5b81a-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="5b81a-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="5b81a-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="5b81a-367">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-367">personal id number</span></span>
  
<span data-ttu-id="5b81a-368">identification number</span><span class="sxs-lookup"><span data-stu-id="5b81a-368">identification number</span></span>
  
<span data-ttu-id="5b81a-369">persönliche ID Nein</span><span class="sxs-lookup"><span data-stu-id="5b81a-369">personal id no</span></span>
  
<span data-ttu-id="5b81a-370">Identität Nein</span><span class="sxs-lookup"><span data-stu-id="5b81a-370">identity no</span></span>
  
<span data-ttu-id="5b81a-371">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-371">identification no</span></span>
  
<span data-ttu-id="5b81a-372">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-372">personal identification no</span></span>
  
<span data-ttu-id="5b81a-373">PERSONNUMMER-ID</span><span class="sxs-lookup"><span data-stu-id="5b81a-373">personnummer id</span></span>
  
<span data-ttu-id="5b81a-374">personligt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-374">personligt id-nummer</span></span>
  
<span data-ttu-id="5b81a-375">unikt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="5b81a-375">unikt id-nummer</span></span>
  
<span data-ttu-id="5b81a-376">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="5b81a-376">personnummer</span></span>
  
<span data-ttu-id="5b81a-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="5b81a-377">identifikationsnumret</span></span>
  
<span data-ttu-id="5b81a-378">PERSONNUMMER #</span><span class="sxs-lookup"><span data-stu-id="5b81a-378">personnummer#</span></span>
  
<span data-ttu-id="5b81a-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="5b81a-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5b81a-380">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b81a-380">See also</span></span>

[<span data-ttu-id="5b81a-381">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="5b81a-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

