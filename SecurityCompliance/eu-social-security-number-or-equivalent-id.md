---
title: EU-sozialVersicherungsNummer oder entsprechende ID
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn die EU-sozialVersicherungsNummer oder der entsprechende ID-vertrauliche Informationstyp erkannt wird. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: abcefb6930e9c02d2f32d84b65accfecf1e20d95
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216525"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="e0530-104">EU-sozialVersicherungsNummer oder entsprechende ID</span><span class="sxs-lookup"><span data-stu-id="e0530-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="e0530-p102">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn die EU-sozialVersicherungsNummer (SSN) oder der entsprechende ID-vertrauliche Informationstyp erkannt wird. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="e0530-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="e0530-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="e0530-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="e0530-108">Format</span><span class="sxs-lookup"><span data-stu-id="e0530-108">Format</span></span>

<span data-ttu-id="e0530-109">10 Ziffern im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="e0530-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e0530-110">Muster</span><span class="sxs-lookup"><span data-stu-id="e0530-110">Pattern</span></span>

<span data-ttu-id="e0530-111">10 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e0530-111">10 digits:</span></span>
  
-  <span data-ttu-id="e0530-112">Drei Ziffern, die einer Seriennummer entsprechen</span><span class="sxs-lookup"><span data-stu-id="e0530-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="e0530-113">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e0530-113">One check digit</span></span>
    
- <span data-ttu-id="e0530-114">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="e0530-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e0530-115">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e0530-115">Checksum</span></span>

<span data-ttu-id="e0530-116">Ja</span><span class="sxs-lookup"><span data-stu-id="e0530-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e0530-117">Definition</span><span class="sxs-lookup"><span data-stu-id="e0530-117">Definition</span></span>

<span data-ttu-id="e0530-118">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-119">Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e0530-120">Ein Schlüsselwort `Keywords_austria_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e0530-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e0530-121">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-122">Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e0530-123">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e0530-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="e0530-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e0530-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e0530-125">Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-125">social security no</span></span>
  
<span data-ttu-id="e0530-126">social security number
</span><span class="sxs-lookup"><span data-stu-id="e0530-126">social security number</span></span>
  
<span data-ttu-id="e0530-127">
social security code</span><span class="sxs-lookup"><span data-stu-id="e0530-127">social security code</span></span>
  
<span data-ttu-id="e0530-128">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-128">insurance number</span></span>
  
<span data-ttu-id="e0530-129">Austrian SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-129">austrian ssn</span></span>
  
<span data-ttu-id="e0530-130">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-130">ssn#</span></span>
  
<span data-ttu-id="e0530-131">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-131">ssn</span></span>
  
<span data-ttu-id="e0530-132">versicherungscode</span><span class="sxs-lookup"><span data-stu-id="e0530-132">insurance code</span></span>
  
<span data-ttu-id="e0530-133">versicherungscode #</span><span class="sxs-lookup"><span data-stu-id="e0530-133">insurance code#</span></span>
  
<span data-ttu-id="e0530-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="e0530-134">socialsecurityno#</span></span>
  
<span data-ttu-id="e0530-135">Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="e0530-136">soziale Sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="e0530-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="e0530-137">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="e0530-138">Belgien</span><span class="sxs-lookup"><span data-stu-id="e0530-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="e0530-139">Format</span><span class="sxs-lookup"><span data-stu-id="e0530-139">Format</span></span>

<span data-ttu-id="e0530-140">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e0530-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e0530-141">Muster</span><span class="sxs-lookup"><span data-stu-id="e0530-141">Pattern</span></span>

<span data-ttu-id="e0530-142">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e0530-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e0530-143">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e0530-143">Checksum</span></span>

<span data-ttu-id="e0530-144">Ja</span><span class="sxs-lookup"><span data-stu-id="e0530-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e0530-145">Definition</span><span class="sxs-lookup"><span data-stu-id="e0530-145">Definition</span></span>

<span data-ttu-id="e0530-146">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-147">Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e0530-148">Ein Schlüsselwort `Keywords_belgium_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e0530-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e0530-149">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-150">Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e0530-151">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e0530-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="e0530-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e0530-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e0530-153">belgische nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-153">belgian national number</span></span>
  
<span data-ttu-id="e0530-154">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-154">national number</span></span>
  
<span data-ttu-id="e0530-155">social security number
</span><span class="sxs-lookup"><span data-stu-id="e0530-155">social security number</span></span>
  
<span data-ttu-id="e0530-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="e0530-156">nationalnumber#</span></span>
  
<span data-ttu-id="e0530-157">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-157">ssn#</span></span>
  
<span data-ttu-id="e0530-158">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-158">ssn</span></span>
  
<span data-ttu-id="e0530-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="e0530-159">nationalnumber</span></span>
  
<span data-ttu-id="e0530-160">BNN</span><span class="sxs-lookup"><span data-stu-id="e0530-160">bnn#</span></span>
  
<span data-ttu-id="e0530-161">BNN</span><span class="sxs-lookup"><span data-stu-id="e0530-161">bnn</span></span>
  
<span data-ttu-id="e0530-162">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-162">personal id number</span></span>
  
<span data-ttu-id="e0530-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e0530-163">personalidnumber#</span></span>
  
<span data-ttu-id="e0530-164">Numéro National</span><span class="sxs-lookup"><span data-stu-id="e0530-164">numéro national</span></span>
  
<span data-ttu-id="e0530-165">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="e0530-165">numéro de sécurité</span></span>
  
<span data-ttu-id="e0530-166">Numéro d'assuré</span><span class="sxs-lookup"><span data-stu-id="e0530-166">numéro d'assuré</span></span>
  
<span data-ttu-id="e0530-167">identifizierbare nationale</span><span class="sxs-lookup"><span data-stu-id="e0530-167">identifiant national</span></span>
  
<span data-ttu-id="e0530-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="e0530-168">identifiantnational#</span></span>
  
<span data-ttu-id="e0530-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="e0530-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="e0530-170">Kroatien</span><span class="sxs-lookup"><span data-stu-id="e0530-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="e0530-171">Format</span><span class="sxs-lookup"><span data-stu-id="e0530-171">Format</span></span>

<span data-ttu-id="e0530-172">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e0530-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e0530-173">Muster</span><span class="sxs-lookup"><span data-stu-id="e0530-173">Pattern</span></span>

 <span data-ttu-id="e0530-174">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e0530-174">11 digits:</span></span> 
  
-  <span data-ttu-id="e0530-175">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="e0530-175">Ten digits</span></span> 
    
- <span data-ttu-id="e0530-176">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e0530-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e0530-177">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e0530-177">Checksum</span></span>

<span data-ttu-id="e0530-178">Ja</span><span class="sxs-lookup"><span data-stu-id="e0530-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e0530-179">Definition</span><span class="sxs-lookup"><span data-stu-id="e0530-179">Definition</span></span>

<span data-ttu-id="e0530-180">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-181">Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e0530-182">Ein Schlüsselwort `Keywords_croatia_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e0530-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e0530-183">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-184">Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e0530-185">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e0530-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="e0530-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e0530-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e0530-187">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-187">personal identification number</span></span>
  
<span data-ttu-id="e0530-188">Master-Bürgerzahl</span><span class="sxs-lookup"><span data-stu-id="e0530-188">master citizen number</span></span>
  
<span data-ttu-id="e0530-189">nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-189">national identification number</span></span>
  
<span data-ttu-id="e0530-190">social security number
</span><span class="sxs-lookup"><span data-stu-id="e0530-190">social security number</span></span>
  
<span data-ttu-id="e0530-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="e0530-191">nationalnumber#</span></span>
  
<span data-ttu-id="e0530-192">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-192">ssn#</span></span>
  
<span data-ttu-id="e0530-193">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-193">ssn</span></span>
  
<span data-ttu-id="e0530-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="e0530-194">nationalnumber</span></span>
  
<span data-ttu-id="e0530-195">BNN</span><span class="sxs-lookup"><span data-stu-id="e0530-195">bnn#</span></span>
  
<span data-ttu-id="e0530-196">BNN</span><span class="sxs-lookup"><span data-stu-id="e0530-196">bnn</span></span>
  
<span data-ttu-id="e0530-197">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-197">personal id number</span></span>
  
<span data-ttu-id="e0530-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e0530-198">personalidnumber#</span></span>
  
<span data-ttu-id="e0530-199">OIB</span><span class="sxs-lookup"><span data-stu-id="e0530-199">oib</span></span>
  
<span data-ttu-id="e0530-200">Osobni identifikacijski Broj</span><span class="sxs-lookup"><span data-stu-id="e0530-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="e0530-201">Tschechien</span><span class="sxs-lookup"><span data-stu-id="e0530-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="e0530-202">Format</span><span class="sxs-lookup"><span data-stu-id="e0530-202">Format</span></span>

<span data-ttu-id="e0530-203">Zehn Ziffern und ein umgekehrter Schrägstrich im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="e0530-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e0530-204">Muster</span><span class="sxs-lookup"><span data-stu-id="e0530-204">Pattern</span></span>

<span data-ttu-id="e0530-205">Zehn Ziffern und ein umgekehrter Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="e0530-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="e0530-206">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT):</span><span class="sxs-lookup"><span data-stu-id="e0530-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="e0530-207">Einen umgekehrten Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="e0530-207">A backslash</span></span>
    
- <span data-ttu-id="e0530-208">Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am selben Datum geboren wurden</span><span class="sxs-lookup"><span data-stu-id="e0530-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="e0530-209">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e0530-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e0530-210">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e0530-210">Checksum</span></span>

<span data-ttu-id="e0530-211">Ja</span><span class="sxs-lookup"><span data-stu-id="e0530-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e0530-212">Definition</span><span class="sxs-lookup"><span data-stu-id="e0530-212">Definition</span></span>

<span data-ttu-id="e0530-213">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-214">Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e0530-215">Ein Schlüsselwort `Keywords_czech_republic_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e0530-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e0530-216">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-217">Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e0530-218">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e0530-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="e0530-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e0530-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e0530-220">Geburtsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-220">birth number</span></span>
  
<span data-ttu-id="e0530-221">nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-221">national identification number</span></span>
  
<span data-ttu-id="e0530-222">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-222">personal identification number</span></span>
  
<span data-ttu-id="e0530-223">social security number
</span><span class="sxs-lookup"><span data-stu-id="e0530-223">social security number</span></span>
  
<span data-ttu-id="e0530-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="e0530-224">nationalnumber#</span></span>
  
<span data-ttu-id="e0530-225">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-225">ssn#</span></span>
  
<span data-ttu-id="e0530-226">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-226">ssn</span></span>
  
<span data-ttu-id="e0530-227">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-227">national number</span></span>
  
<span data-ttu-id="e0530-228">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-228">personal id number</span></span>
  
<span data-ttu-id="e0530-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e0530-229">personalidnumber#</span></span>
  
<span data-ttu-id="e0530-230">rč</span><span class="sxs-lookup"><span data-stu-id="e0530-230">rč</span></span>
  
<span data-ttu-id="e0530-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="e0530-231">rodné číslo</span></span>
  
<span data-ttu-id="e0530-232">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="e0530-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="e0530-233">Dänemark</span><span class="sxs-lookup"><span data-stu-id="e0530-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="e0530-234">Format</span><span class="sxs-lookup"><span data-stu-id="e0530-234">Format</span></span>

<span data-ttu-id="e0530-235">Zehn Ziffern und ein Bindestrich im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="e0530-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e0530-236">Muster</span><span class="sxs-lookup"><span data-stu-id="e0530-236">Pattern</span></span>

<span data-ttu-id="e0530-237">Zehn Ziffern und ein Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="e0530-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="e0530-238">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="e0530-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="e0530-239">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e0530-239">A hyphen</span></span>
    
- <span data-ttu-id="e0530-240">Vier Ziffern, die einer Sequenznummer entsprechen</span><span class="sxs-lookup"><span data-stu-id="e0530-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e0530-241">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e0530-241">Checksum</span></span>

<span data-ttu-id="e0530-242">Ja</span><span class="sxs-lookup"><span data-stu-id="e0530-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e0530-243">Definition</span><span class="sxs-lookup"><span data-stu-id="e0530-243">Definition</span></span>

<span data-ttu-id="e0530-244">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-245">Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e0530-246">Ein Schlüsselwort `Keywords_denmark_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e0530-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e0530-247">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-248">Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e0530-249">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e0530-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="e0530-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e0530-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e0530-251">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-251">personal identification number</span></span>
  
<span data-ttu-id="e0530-252">nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-252">national identification number</span></span>
  
<span data-ttu-id="e0530-253">social security number
</span><span class="sxs-lookup"><span data-stu-id="e0530-253">social security number</span></span>
  
<span data-ttu-id="e0530-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="e0530-254">nationalnumber#</span></span>
  
<span data-ttu-id="e0530-255">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-255">ssn#</span></span>
  
<span data-ttu-id="e0530-256">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-256">ssn</span></span>
  
<span data-ttu-id="e0530-257">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-257">national number</span></span>
  
<span data-ttu-id="e0530-258">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-258">personal id number</span></span>
  
<span data-ttu-id="e0530-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e0530-259">personalidnumber#</span></span>
  
<span data-ttu-id="e0530-260">CPR-Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-260">cpr-nummer</span></span>
  
<span data-ttu-id="e0530-261">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="e0530-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="e0530-262">Finnland</span><span class="sxs-lookup"><span data-stu-id="e0530-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="e0530-263">Format</span><span class="sxs-lookup"><span data-stu-id="e0530-263">Format</span></span>

<span data-ttu-id="e0530-264">Eine Kombination aus 11 Zeichen im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="e0530-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e0530-265">Muster</span><span class="sxs-lookup"><span data-stu-id="e0530-265">Pattern</span></span>

<span data-ttu-id="e0530-266">Eine Kombination aus 11 Zeichen im angegebenen Format:</span><span class="sxs-lookup"><span data-stu-id="e0530-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="e0530-267">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="e0530-267">Six digits</span></span> 
    
- <span data-ttu-id="e0530-268">Eine der folgenden Instanzen:</span><span class="sxs-lookup"><span data-stu-id="e0530-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="e0530-269">Plus-Symbol</span><span class="sxs-lookup"><span data-stu-id="e0530-269">Plus symbol</span></span>
    
  - <span data-ttu-id="e0530-270">Minus Zeichen</span><span class="sxs-lookup"><span data-stu-id="e0530-270">Minus symbol</span></span>
    
  - <span data-ttu-id="e0530-271">Der Buchstabe "A" (Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="e0530-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="e0530-272">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e0530-272">Three digits</span></span>
    
- <span data-ttu-id="e0530-273">Ein Buchstabe oder eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="e0530-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e0530-274">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e0530-274">Checksum</span></span>

<span data-ttu-id="e0530-275">Ja</span><span class="sxs-lookup"><span data-stu-id="e0530-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e0530-276">Definition</span><span class="sxs-lookup"><span data-stu-id="e0530-276">Definition</span></span>

<span data-ttu-id="e0530-277">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-278">Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e0530-279">Ein Schlüsselwort `Keywords_finland_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e0530-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e0530-280">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-281">Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e0530-282">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e0530-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="e0530-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e0530-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e0530-284">identification number
</span><span class="sxs-lookup"><span data-stu-id="e0530-284">identification number</span></span>
  
<span data-ttu-id="e0530-285">persönliche ID</span><span class="sxs-lookup"><span data-stu-id="e0530-285">personal id</span></span>
  
<span data-ttu-id="e0530-286">Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-286">identity number</span></span>
  
<span data-ttu-id="e0530-287">nationale finnische ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-287">finnish national id number</span></span>
  
<span data-ttu-id="e0530-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e0530-288">personalidnumber#</span></span>
  
<span data-ttu-id="e0530-289">nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-289">national identification number</span></span>
  
<span data-ttu-id="e0530-290">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-290">id number</span></span>
  
<span data-ttu-id="e0530-291">nationale ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="e0530-291">national id no.</span></span>
  
<span data-ttu-id="e0530-292">nationale ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-292">national id number</span></span>
  
<span data-ttu-id="e0530-293">ID Nein</span><span class="sxs-lookup"><span data-stu-id="e0530-293">id no</span></span>
  
<span data-ttu-id="e0530-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="e0530-294">tunnistenumero</span></span>
  
<span data-ttu-id="e0530-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="e0530-295">henkilötunnus</span></span>
  
<span data-ttu-id="e0530-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="e0530-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="e0530-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="e0530-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="e0530-298">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="e0530-298">identiteetti numero</span></span>
  
<span data-ttu-id="e0530-299">Suomen der Kok henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="e0530-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="e0530-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="e0530-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="e0530-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="e0530-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="e0530-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="e0530-302">tunnusnumero</span></span>
  
<span data-ttu-id="e0530-303">der Kok tunnus numero</span><span class="sxs-lookup"><span data-stu-id="e0530-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="e0530-304">Hetu</span><span class="sxs-lookup"><span data-stu-id="e0530-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="e0530-305">Frankreich</span><span class="sxs-lookup"><span data-stu-id="e0530-305">France</span></span>

<span data-ttu-id="e0530-306">Weitere Informationen finden Sie im Abschnitt "französische sozialVersicherungsNummer (INSEE)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e0530-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="e0530-307">Deutschland</span><span class="sxs-lookup"><span data-stu-id="e0530-307">Germany</span></span>

<span data-ttu-id="e0530-308">Weitere Informationen finden Sie im Abschnitt "Deutschland PersonalausweisNummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e0530-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="e0530-309">Griechenland</span><span class="sxs-lookup"><span data-stu-id="e0530-309">Greece</span></span>

<span data-ttu-id="e0530-310">Weitere Informationen finden Sie im Abschnitt "GriechenLand National ID Card" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e0530-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="e0530-311">Ungarn</span><span class="sxs-lookup"><span data-stu-id="e0530-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="e0530-312">Format</span><span class="sxs-lookup"><span data-stu-id="e0530-312">Format</span></span>

<span data-ttu-id="e0530-313">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e0530-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e0530-314">Muster</span><span class="sxs-lookup"><span data-stu-id="e0530-314">Pattern</span></span>

<span data-ttu-id="e0530-315">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e0530-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e0530-316">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e0530-316">Checksum</span></span>

<span data-ttu-id="e0530-317">Ja</span><span class="sxs-lookup"><span data-stu-id="e0530-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e0530-318">Definition</span><span class="sxs-lookup"><span data-stu-id="e0530-318">Definition</span></span>

<span data-ttu-id="e0530-319">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-320">Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e0530-321">Ein Schlüsselwort `Keywords_hungary_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e0530-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e0530-322">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-323">Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e0530-324">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e0530-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="e0530-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e0530-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e0530-326">Sozialversicherungsnummer (ungarisch)</span><span class="sxs-lookup"><span data-stu-id="e0530-326">hungarian social security number</span></span>
  
<span data-ttu-id="e0530-327">social security number
</span><span class="sxs-lookup"><span data-stu-id="e0530-327">social security number</span></span>
  
<span data-ttu-id="e0530-328">socialsecuritynumber #</span><span class="sxs-lookup"><span data-stu-id="e0530-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="e0530-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="e0530-329">hssn#</span></span>
  
<span data-ttu-id="e0530-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="e0530-330">socialsecuritynno</span></span>
  
<span data-ttu-id="e0530-331">hssn</span><span class="sxs-lookup"><span data-stu-id="e0530-331">hssn</span></span>
  
<span data-ttu-id="e0530-332">Taj</span><span class="sxs-lookup"><span data-stu-id="e0530-332">taj</span></span>
  
<span data-ttu-id="e0530-333">Taj</span><span class="sxs-lookup"><span data-stu-id="e0530-333">taj#</span></span>
  
<span data-ttu-id="e0530-334">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-334">ssn</span></span>
  
<span data-ttu-id="e0530-335">SSN</span><span class="sxs-lookup"><span data-stu-id="e0530-335">ssn#</span></span>
  
<span data-ttu-id="e0530-336">Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-336">social security no</span></span>
  
<span data-ttu-id="e0530-337">ÁFA</span><span class="sxs-lookup"><span data-stu-id="e0530-337">áfa</span></span>
  
<span data-ttu-id="e0530-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="e0530-338">közösségi adószám</span></span>
  
<span data-ttu-id="e0530-339">Általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="e0530-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="e0530-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="e0530-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="e0530-341">ÁFA szám</span><span class="sxs-lookup"><span data-stu-id="e0530-341">áfa szám</span></span>
  
<span data-ttu-id="e0530-342">Magyar ÁFA szám</span><span class="sxs-lookup"><span data-stu-id="e0530-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="e0530-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="e0530-343">Portugal</span></span>

<span data-ttu-id="e0530-344">Weitere Informationen finden Sie im Abschnitt "portugiesische Bürgerkarten Nummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e0530-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="e0530-345">Spanien</span><span class="sxs-lookup"><span data-stu-id="e0530-345">Spain</span></span>

<span data-ttu-id="e0530-346">Weitere Informationen finden Sie im Abschnitt "sozialVersicherungsNummer (SSN) in Spanien" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e0530-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="e0530-347">Schweden</span><span class="sxs-lookup"><span data-stu-id="e0530-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="e0530-348">Format</span><span class="sxs-lookup"><span data-stu-id="e0530-348">Format</span></span>

<span data-ttu-id="e0530-349">12 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e0530-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e0530-350">Muster</span><span class="sxs-lookup"><span data-stu-id="e0530-350">Pattern</span></span>

<span data-ttu-id="e0530-351">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e0530-351">12 digits:</span></span>
  
-  <span data-ttu-id="e0530-352">Acht Ziffern, die dem Geburtsdatum entsprechen (JJJJMMTT)</span><span class="sxs-lookup"><span data-stu-id="e0530-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="e0530-353">Drei Ziffern, die einer Seriennummer entsprechen, wobei:</span><span class="sxs-lookup"><span data-stu-id="e0530-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="e0530-354">Die letzte Ziffer in der Seriennummer kennzeichnet das Geschlecht durch die Zuweisung einer ungerade Zahl für männliche und eine gerade Zahl für weibliche</span><span class="sxs-lookup"><span data-stu-id="e0530-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="e0530-355">Bis zu 1990 entspricht die Zuordnung der Seriennummer der Grafschaft, in der der Träger der Nummer geboren wurde, oder (wenn er vor 1947 geboren wurde), in dem er nach Steuerdaten Sätzen am 1. Januar 1947 lebte, mit einem speziellen Code (in der Regel 9 als 7. Ziffer) für Einwanderer</span><span class="sxs-lookup"><span data-stu-id="e0530-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="e0530-356">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e0530-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e0530-357">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e0530-357">Checksum</span></span>

<span data-ttu-id="e0530-358">Ja</span><span class="sxs-lookup"><span data-stu-id="e0530-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e0530-359">Definition</span><span class="sxs-lookup"><span data-stu-id="e0530-359">Definition</span></span>

<span data-ttu-id="e0530-360">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-361">Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e0530-362">Ein Schlüsselwort `Keywords_sweden_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e0530-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e0530-363">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e0530-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e0530-364">Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e0530-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e0530-365">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e0530-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="e0530-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="e0530-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e0530-367">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-367">personal id number</span></span>
  
<span data-ttu-id="e0530-368">identification number
</span><span class="sxs-lookup"><span data-stu-id="e0530-368">identification number</span></span>
  
<span data-ttu-id="e0530-369">persönliche ID Nein</span><span class="sxs-lookup"><span data-stu-id="e0530-369">personal id no</span></span>
  
<span data-ttu-id="e0530-370">Identität Nein</span><span class="sxs-lookup"><span data-stu-id="e0530-370">identity no</span></span>
  
<span data-ttu-id="e0530-371">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-371">identification no</span></span>
  
<span data-ttu-id="e0530-372">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e0530-372">personal identification no</span></span>
  
<span data-ttu-id="e0530-373">PERSONNUMMER-ID</span><span class="sxs-lookup"><span data-stu-id="e0530-373">personnummer id</span></span>
  
<span data-ttu-id="e0530-374">personligt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-374">personligt id-nummer</span></span>
  
<span data-ttu-id="e0530-375">unikt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e0530-375">unikt id-nummer</span></span>
  
<span data-ttu-id="e0530-376">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="e0530-376">personnummer</span></span>
  
<span data-ttu-id="e0530-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="e0530-377">identifikationsnumret</span></span>
  
<span data-ttu-id="e0530-378">PERSONNUMMER #</span><span class="sxs-lookup"><span data-stu-id="e0530-378">personnummer#</span></span>
  
<span data-ttu-id="e0530-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="e0530-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0530-380">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0530-380">See also</span></span>

[<span data-ttu-id="e0530-381">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="e0530-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

