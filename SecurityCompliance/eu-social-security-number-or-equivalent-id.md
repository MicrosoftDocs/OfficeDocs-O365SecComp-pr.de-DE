---
title: EU Sozialversicherungsnummer oder einer ähnlichen-ID
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: In diesem Thema wird eine Data Loss Prevention (DLP) Richtlinie sieht für beim Erkennen des EU Sozialversicherungsnummer oder gleichwertige ID vertrauliche Informationen-Typs. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 6f1027dcfb648ed937b8180d74d4bc6348dab650
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529332"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="23b5e-104">EU Sozialversicherungsnummer oder einer ähnlichen-ID</span><span class="sxs-lookup"><span data-stu-id="23b5e-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="23b5e-p102">In diesem Thema wird, wonach eine Data Loss Prevention (DLP) Richtlinie sucht bei der Entdeckung des EU Sozialversicherungsnummer (SSN) oder die entsprechende ID vertrauliche Informationen Typs. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="23b5e-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="23b5e-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="23b5e-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="23b5e-108">Format</span><span class="sxs-lookup"><span data-stu-id="23b5e-108">Format</span></span>

<span data-ttu-id="23b5e-109">10 Ziffern im angegebenen format</span><span class="sxs-lookup"><span data-stu-id="23b5e-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="23b5e-110">Muster</span><span class="sxs-lookup"><span data-stu-id="23b5e-110">Pattern</span></span>

<span data-ttu-id="23b5e-111">10 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="23b5e-111">10 digits:</span></span>
  
-  <span data-ttu-id="23b5e-112">Drei Ziffern, die eine fortlaufende Zahl entsprechen</span><span class="sxs-lookup"><span data-stu-id="23b5e-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="23b5e-113">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="23b5e-113">One check digit</span></span>
    
- <span data-ttu-id="23b5e-114">Sechs Ziffern, die das Geburtsdatum (DDMMYY) entsprechen</span><span class="sxs-lookup"><span data-stu-id="23b5e-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="23b5e-115">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="23b5e-115">Checksum</span></span>

<span data-ttu-id="23b5e-116">Ja</span><span class="sxs-lookup"><span data-stu-id="23b5e-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="23b5e-117">Definition</span><span class="sxs-lookup"><span data-stu-id="23b5e-117">Definition</span></span>

<span data-ttu-id="23b5e-118">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-119">Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="23b5e-120">Ein Schlüsselwort aus `Keywords_austria_eu_ssn_or_equivalent` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="23b5e-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="23b5e-121">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-122">Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="23b5e-123">Keywords</span><span class="sxs-lookup"><span data-stu-id="23b5e-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="23b5e-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="23b5e-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="23b5e-125">soziale Sicherheit keine</span><span class="sxs-lookup"><span data-stu-id="23b5e-125">social security no</span></span>
  
<span data-ttu-id="23b5e-126">social security number
</span><span class="sxs-lookup"><span data-stu-id="23b5e-126">social security number</span></span>
  
<span data-ttu-id="23b5e-127">
social security code</span><span class="sxs-lookup"><span data-stu-id="23b5e-127">social security code</span></span>
  
<span data-ttu-id="23b5e-128">Versicherungsvertreter Anzahl</span><span class="sxs-lookup"><span data-stu-id="23b5e-128">insurance number</span></span>
  
<span data-ttu-id="23b5e-129">österreichische ssn</span><span class="sxs-lookup"><span data-stu-id="23b5e-129">austrian ssn</span></span>
  
<span data-ttu-id="23b5e-130">ssn #</span><span class="sxs-lookup"><span data-stu-id="23b5e-130">ssn#</span></span>
  
<span data-ttu-id="23b5e-131">ssn</span><span class="sxs-lookup"><span data-stu-id="23b5e-131">ssn</span></span>
  
<span data-ttu-id="23b5e-132">Versicherungsvertreter code</span><span class="sxs-lookup"><span data-stu-id="23b5e-132">insurance code</span></span>
  
<span data-ttu-id="23b5e-133">Versicherungsvertreter Code #</span><span class="sxs-lookup"><span data-stu-id="23b5e-133">insurance code#</span></span>
  
<span data-ttu-id="23b5e-134">Socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="23b5e-134">socialsecurityno#</span></span>
  
<span data-ttu-id="23b5e-135">Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="23b5e-136">Soziale Sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="23b5e-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="23b5e-137">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="23b5e-138">Belgien</span><span class="sxs-lookup"><span data-stu-id="23b5e-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="23b5e-139">Format</span><span class="sxs-lookup"><span data-stu-id="23b5e-139">Format</span></span>

<span data-ttu-id="23b5e-140">11 Zahlen ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="23b5e-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="23b5e-141">Muster</span><span class="sxs-lookup"><span data-stu-id="23b5e-141">Pattern</span></span>

<span data-ttu-id="23b5e-142">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="23b5e-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="23b5e-143">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="23b5e-143">Checksum</span></span>

<span data-ttu-id="23b5e-144">Ja</span><span class="sxs-lookup"><span data-stu-id="23b5e-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="23b5e-145">Definition</span><span class="sxs-lookup"><span data-stu-id="23b5e-145">Definition</span></span>

<span data-ttu-id="23b5e-146">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-147">Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="23b5e-148">Ein Schlüsselwort aus `Keywords_belgium_eu_ssn_or_equivalent` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="23b5e-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="23b5e-149">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-150">Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="23b5e-151">Keywords</span><span class="sxs-lookup"><span data-stu-id="23b5e-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="23b5e-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="23b5e-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="23b5e-153">belgische Vorwahl</span><span class="sxs-lookup"><span data-stu-id="23b5e-153">belgian national number</span></span>
  
<span data-ttu-id="23b5e-154">Vorwahl</span><span class="sxs-lookup"><span data-stu-id="23b5e-154">national number</span></span>
  
<span data-ttu-id="23b5e-155">social security number
</span><span class="sxs-lookup"><span data-stu-id="23b5e-155">social security number</span></span>
  
<span data-ttu-id="23b5e-156">Nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="23b5e-156">nationalnumber#</span></span>
  
<span data-ttu-id="23b5e-157">ssn #</span><span class="sxs-lookup"><span data-stu-id="23b5e-157">ssn#</span></span>
  
<span data-ttu-id="23b5e-158">ssn</span><span class="sxs-lookup"><span data-stu-id="23b5e-158">ssn</span></span>
  
<span data-ttu-id="23b5e-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="23b5e-159">nationalnumber</span></span>
  
<span data-ttu-id="23b5e-160">Bnn #</span><span class="sxs-lookup"><span data-stu-id="23b5e-160">bnn#</span></span>
  
<span data-ttu-id="23b5e-161">bnn</span><span class="sxs-lookup"><span data-stu-id="23b5e-161">bnn</span></span>
  
<span data-ttu-id="23b5e-162">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-162">personal id number</span></span>
  
<span data-ttu-id="23b5e-163">Personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="23b5e-163">personalidnumber#</span></span>
  
<span data-ttu-id="23b5e-164">national numéro</span><span class="sxs-lookup"><span data-stu-id="23b5e-164">numéro national</span></span>
  
<span data-ttu-id="23b5e-165">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="23b5e-165">numéro de sécurité</span></span>
  
<span data-ttu-id="23b5e-166">Numéro d'Assuré</span><span class="sxs-lookup"><span data-stu-id="23b5e-166">numéro d'assuré</span></span>
  
<span data-ttu-id="23b5e-167">national identifiant</span><span class="sxs-lookup"><span data-stu-id="23b5e-167">identifiant national</span></span>
  
<span data-ttu-id="23b5e-168">Identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="23b5e-168">identifiantnational#</span></span>
  
<span data-ttu-id="23b5e-169">Numéronational #</span><span class="sxs-lookup"><span data-stu-id="23b5e-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="23b5e-170">Kroatien</span><span class="sxs-lookup"><span data-stu-id="23b5e-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="23b5e-171">Format</span><span class="sxs-lookup"><span data-stu-id="23b5e-171">Format</span></span>

<span data-ttu-id="23b5e-172">11 Zahlen ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="23b5e-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="23b5e-173">Muster</span><span class="sxs-lookup"><span data-stu-id="23b5e-173">Pattern</span></span>

 <span data-ttu-id="23b5e-174">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="23b5e-174">11 digits:</span></span> 
  
-  <span data-ttu-id="23b5e-175">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="23b5e-175">Ten digits</span></span> 
    
- <span data-ttu-id="23b5e-176">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="23b5e-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="23b5e-177">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="23b5e-177">Checksum</span></span>

<span data-ttu-id="23b5e-178">Ja</span><span class="sxs-lookup"><span data-stu-id="23b5e-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="23b5e-179">Definition</span><span class="sxs-lookup"><span data-stu-id="23b5e-179">Definition</span></span>

<span data-ttu-id="23b5e-180">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-181">Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="23b5e-182">Ein Schlüsselwort aus `Keywords_croatia_eu_ssn_or_equivalent` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="23b5e-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="23b5e-183">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-184">Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="23b5e-185">Keywords</span><span class="sxs-lookup"><span data-stu-id="23b5e-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="23b5e-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="23b5e-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="23b5e-187">Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-187">personal identification number</span></span>
  
<span data-ttu-id="23b5e-188">Anzahl der Master Bürger</span><span class="sxs-lookup"><span data-stu-id="23b5e-188">master citizen number</span></span>
  
<span data-ttu-id="23b5e-189">National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-189">national identification number</span></span>
  
<span data-ttu-id="23b5e-190">social security number
</span><span class="sxs-lookup"><span data-stu-id="23b5e-190">social security number</span></span>
  
<span data-ttu-id="23b5e-191">Nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="23b5e-191">nationalnumber#</span></span>
  
<span data-ttu-id="23b5e-192">ssn #</span><span class="sxs-lookup"><span data-stu-id="23b5e-192">ssn#</span></span>
  
<span data-ttu-id="23b5e-193">ssn</span><span class="sxs-lookup"><span data-stu-id="23b5e-193">ssn</span></span>
  
<span data-ttu-id="23b5e-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="23b5e-194">nationalnumber</span></span>
  
<span data-ttu-id="23b5e-195">Bnn #</span><span class="sxs-lookup"><span data-stu-id="23b5e-195">bnn#</span></span>
  
<span data-ttu-id="23b5e-196">bnn</span><span class="sxs-lookup"><span data-stu-id="23b5e-196">bnn</span></span>
  
<span data-ttu-id="23b5e-197">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-197">personal id number</span></span>
  
<span data-ttu-id="23b5e-198">Personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="23b5e-198">personalidnumber#</span></span>
  
<span data-ttu-id="23b5e-199">oib</span><span class="sxs-lookup"><span data-stu-id="23b5e-199">oib</span></span>
  
<span data-ttu-id="23b5e-200">Osobni Identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="23b5e-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="23b5e-201">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="23b5e-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="23b5e-202">Format</span><span class="sxs-lookup"><span data-stu-id="23b5e-202">Format</span></span>

<span data-ttu-id="23b5e-203">Zehn Ziffern und einem umgekehrten Schrägstrich in dem angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="23b5e-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="23b5e-204">Muster</span><span class="sxs-lookup"><span data-stu-id="23b5e-204">Pattern</span></span>

<span data-ttu-id="23b5e-205">Zehn Ziffern und einem umgekehrten Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="23b5e-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="23b5e-206">Sechs Ziffern, die das Geburtsdatum (JJMMTT) entsprechen:</span><span class="sxs-lookup"><span data-stu-id="23b5e-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="23b5e-207">Ein umgekehrter Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="23b5e-207">A backslash</span></span>
    
- <span data-ttu-id="23b5e-208">Drei Ziffern, die eine fortlaufende Zahl entsprechen, die Personen, die an demselben Tag geboren trennt</span><span class="sxs-lookup"><span data-stu-id="23b5e-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="23b5e-209">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="23b5e-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="23b5e-210">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="23b5e-210">Checksum</span></span>

<span data-ttu-id="23b5e-211">Ja</span><span class="sxs-lookup"><span data-stu-id="23b5e-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="23b5e-212">Definition</span><span class="sxs-lookup"><span data-stu-id="23b5e-212">Definition</span></span>

<span data-ttu-id="23b5e-213">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-214">Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="23b5e-215">Ein Schlüsselwort aus `Keywords_czech_republic_eu_ssn_or_equivalent` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="23b5e-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="23b5e-216">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-217">Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="23b5e-218">Keywords</span><span class="sxs-lookup"><span data-stu-id="23b5e-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="23b5e-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="23b5e-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="23b5e-220">Geburtsdatum Anzahl</span><span class="sxs-lookup"><span data-stu-id="23b5e-220">birth number</span></span>
  
<span data-ttu-id="23b5e-221">National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-221">national identification number</span></span>
  
<span data-ttu-id="23b5e-222">Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-222">personal identification number</span></span>
  
<span data-ttu-id="23b5e-223">social security number
</span><span class="sxs-lookup"><span data-stu-id="23b5e-223">social security number</span></span>
  
<span data-ttu-id="23b5e-224">Nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="23b5e-224">nationalnumber#</span></span>
  
<span data-ttu-id="23b5e-225">ssn #</span><span class="sxs-lookup"><span data-stu-id="23b5e-225">ssn#</span></span>
  
<span data-ttu-id="23b5e-226">ssn</span><span class="sxs-lookup"><span data-stu-id="23b5e-226">ssn</span></span>
  
<span data-ttu-id="23b5e-227">Vorwahl</span><span class="sxs-lookup"><span data-stu-id="23b5e-227">national number</span></span>
  
<span data-ttu-id="23b5e-228">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-228">personal id number</span></span>
  
<span data-ttu-id="23b5e-229">Personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="23b5e-229">personalidnumber#</span></span>
  
<span data-ttu-id="23b5e-230">rč</span><span class="sxs-lookup"><span data-stu-id="23b5e-230">rč</span></span>
  
<span data-ttu-id="23b5e-231">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="23b5e-231">rodné číslo</span></span>
  
<span data-ttu-id="23b5e-232">Rodne cislo</span><span class="sxs-lookup"><span data-stu-id="23b5e-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="23b5e-233">Dänemark</span><span class="sxs-lookup"><span data-stu-id="23b5e-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="23b5e-234">Format</span><span class="sxs-lookup"><span data-stu-id="23b5e-234">Format</span></span>

<span data-ttu-id="23b5e-235">Zehn Ziffern und ein Bindestrich in dem angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="23b5e-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="23b5e-236">Muster</span><span class="sxs-lookup"><span data-stu-id="23b5e-236">Pattern</span></span>

<span data-ttu-id="23b5e-237">Zehn Ziffern und ein Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="23b5e-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="23b5e-238">Sechs Ziffern, die das Geburtsdatum (DDMMYY) entsprechen</span><span class="sxs-lookup"><span data-stu-id="23b5e-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="23b5e-239">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="23b5e-239">A hyphen</span></span>
    
- <span data-ttu-id="23b5e-240">Vier Ziffern, die eine Sequenznummer entsprechen</span><span class="sxs-lookup"><span data-stu-id="23b5e-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="23b5e-241">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="23b5e-241">Checksum</span></span>

<span data-ttu-id="23b5e-242">Ja</span><span class="sxs-lookup"><span data-stu-id="23b5e-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="23b5e-243">Definition</span><span class="sxs-lookup"><span data-stu-id="23b5e-243">Definition</span></span>

<span data-ttu-id="23b5e-244">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-245">Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="23b5e-246">Ein Schlüsselwort aus `Keywords_denmark_eu_ssn_or_equivalent` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="23b5e-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="23b5e-247">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-248">Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="23b5e-249">Keywords</span><span class="sxs-lookup"><span data-stu-id="23b5e-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="23b5e-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="23b5e-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="23b5e-251">Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-251">personal identification number</span></span>
  
<span data-ttu-id="23b5e-252">National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-252">national identification number</span></span>
  
<span data-ttu-id="23b5e-253">social security number
</span><span class="sxs-lookup"><span data-stu-id="23b5e-253">social security number</span></span>
  
<span data-ttu-id="23b5e-254">Nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="23b5e-254">nationalnumber#</span></span>
  
<span data-ttu-id="23b5e-255">ssn #</span><span class="sxs-lookup"><span data-stu-id="23b5e-255">ssn#</span></span>
  
<span data-ttu-id="23b5e-256">ssn</span><span class="sxs-lookup"><span data-stu-id="23b5e-256">ssn</span></span>
  
<span data-ttu-id="23b5e-257">Vorwahl</span><span class="sxs-lookup"><span data-stu-id="23b5e-257">national number</span></span>
  
<span data-ttu-id="23b5e-258">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-258">personal id number</span></span>
  
<span data-ttu-id="23b5e-259">Personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="23b5e-259">personalidnumber#</span></span>
  
<span data-ttu-id="23b5e-260">CPR-nummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-260">cpr-nummer</span></span>
  
<span data-ttu-id="23b5e-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="23b5e-262">Finnland</span><span class="sxs-lookup"><span data-stu-id="23b5e-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="23b5e-263">Format</span><span class="sxs-lookup"><span data-stu-id="23b5e-263">Format</span></span>

<span data-ttu-id="23b5e-264">Eine Kombination 11 Zeichen im angegebenen format</span><span class="sxs-lookup"><span data-stu-id="23b5e-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="23b5e-265">Muster</span><span class="sxs-lookup"><span data-stu-id="23b5e-265">Pattern</span></span>

<span data-ttu-id="23b5e-266">Eine Kombination der 11 Zeichen im angegebenen Format:</span><span class="sxs-lookup"><span data-stu-id="23b5e-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="23b5e-267">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="23b5e-267">Six digits</span></span> 
    
- <span data-ttu-id="23b5e-268">Eine Instanz einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="23b5e-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="23b5e-269">Plus -symbol</span><span class="sxs-lookup"><span data-stu-id="23b5e-269">Plus symbol</span></span>
    
  - <span data-ttu-id="23b5e-270">Minuszeichen</span><span class="sxs-lookup"><span data-stu-id="23b5e-270">Minus symbol</span></span>
    
  - <span data-ttu-id="23b5e-271">Die Buchstaben "A" (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="23b5e-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="23b5e-272">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="23b5e-272">Three digits</span></span>
    
- <span data-ttu-id="23b5e-273">Einen Buchstaben oder eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="23b5e-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="23b5e-274">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="23b5e-274">Checksum</span></span>

<span data-ttu-id="23b5e-275">Ja</span><span class="sxs-lookup"><span data-stu-id="23b5e-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="23b5e-276">Definition</span><span class="sxs-lookup"><span data-stu-id="23b5e-276">Definition</span></span>

<span data-ttu-id="23b5e-277">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-278">Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="23b5e-279">Ein Schlüsselwort aus `Keywords_finland_eu_ssn_or_equivalent` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="23b5e-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="23b5e-280">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-281">Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="23b5e-282">Keywords</span><span class="sxs-lookup"><span data-stu-id="23b5e-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="23b5e-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="23b5e-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="23b5e-284">identification number
</span><span class="sxs-lookup"><span data-stu-id="23b5e-284">identification number</span></span>
  
<span data-ttu-id="23b5e-285">Persönliche id</span><span class="sxs-lookup"><span data-stu-id="23b5e-285">personal id</span></span>
  
<span data-ttu-id="23b5e-286">Anzahl der Identität</span><span class="sxs-lookup"><span data-stu-id="23b5e-286">identity number</span></span>
  
<span data-ttu-id="23b5e-287">Anzahl der Finnland Personalausweis</span><span class="sxs-lookup"><span data-stu-id="23b5e-287">finnish national id number</span></span>
  
<span data-ttu-id="23b5e-288">Personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="23b5e-288">personalidnumber#</span></span>
  
<span data-ttu-id="23b5e-289">National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-289">national identification number</span></span>
  
<span data-ttu-id="23b5e-290">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-290">id number</span></span>
  
<span data-ttu-id="23b5e-291">Personalausweis keine.</span><span class="sxs-lookup"><span data-stu-id="23b5e-291">national id no.</span></span>
  
<span data-ttu-id="23b5e-292">Ausweis-Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-292">national id number</span></span>
  
<span data-ttu-id="23b5e-293">ID keine</span><span class="sxs-lookup"><span data-stu-id="23b5e-293">id no</span></span>
  
<span data-ttu-id="23b5e-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="23b5e-294">tunnistenumero</span></span>
  
<span data-ttu-id="23b5e-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="23b5e-295">henkilötunnus</span></span>
  
<span data-ttu-id="23b5e-296">Yksilöllinen Henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="23b5e-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="23b5e-297">Ainutlaatuinen Henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="23b5e-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="23b5e-298">Identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="23b5e-298">identiteetti numero</span></span>
  
<span data-ttu-id="23b5e-299">Suomen Kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="23b5e-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="23b5e-300">Henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="23b5e-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="23b5e-301">Kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="23b5e-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="23b5e-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="23b5e-302">tunnusnumero</span></span>
  
<span data-ttu-id="23b5e-303">Kansallinen Tunnus numero</span><span class="sxs-lookup"><span data-stu-id="23b5e-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="23b5e-304">hetu</span><span class="sxs-lookup"><span data-stu-id="23b5e-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="23b5e-305">Frankreich</span><span class="sxs-lookup"><span data-stu-id="23b5e-305">France</span></span>

<span data-ttu-id="23b5e-306">Weitere Informationen hierzu finden Sie im Abschnitt "französische Sozialversicherungsnummer (INSEE)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="23b5e-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="23b5e-307">Deutschland</span><span class="sxs-lookup"><span data-stu-id="23b5e-307">Germany</span></span>

<span data-ttu-id="23b5e-308">Weitere Informationen hierzu finden Sie im Abschnitt "Deutschland Identität Card-Nummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="23b5e-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="23b5e-309">Griechenland</span><span class="sxs-lookup"><span data-stu-id="23b5e-309">Greece</span></span>

<span data-ttu-id="23b5e-310">Weitere Informationen hierzu finden Sie im Abschnitt "Griechenland nationale d ' Identité" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="23b5e-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="23b5e-311">Ungarn</span><span class="sxs-lookup"><span data-stu-id="23b5e-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="23b5e-312">Format</span><span class="sxs-lookup"><span data-stu-id="23b5e-312">Format</span></span>

<span data-ttu-id="23b5e-313">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="23b5e-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="23b5e-314">Muster</span><span class="sxs-lookup"><span data-stu-id="23b5e-314">Pattern</span></span>

<span data-ttu-id="23b5e-315">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="23b5e-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="23b5e-316">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="23b5e-316">Checksum</span></span>

<span data-ttu-id="23b5e-317">Ja</span><span class="sxs-lookup"><span data-stu-id="23b5e-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="23b5e-318">Definition</span><span class="sxs-lookup"><span data-stu-id="23b5e-318">Definition</span></span>

<span data-ttu-id="23b5e-319">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-320">Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="23b5e-321">Ein Schlüsselwort aus `Keywords_hungary_eu_ssn_or_equivalent` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="23b5e-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="23b5e-322">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-323">Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="23b5e-324">Keywords</span><span class="sxs-lookup"><span data-stu-id="23b5e-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="23b5e-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="23b5e-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="23b5e-326">Ungarisch Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-326">hungarian social security number</span></span>
  
<span data-ttu-id="23b5e-327">social security number
</span><span class="sxs-lookup"><span data-stu-id="23b5e-327">social security number</span></span>
  
<span data-ttu-id="23b5e-328">Socialsecuritynumber #</span><span class="sxs-lookup"><span data-stu-id="23b5e-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="23b5e-329">Hssn #</span><span class="sxs-lookup"><span data-stu-id="23b5e-329">hssn#</span></span>
  
<span data-ttu-id="23b5e-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="23b5e-330">socialsecuritynno</span></span>
  
<span data-ttu-id="23b5e-331">hssn</span><span class="sxs-lookup"><span data-stu-id="23b5e-331">hssn</span></span>
  
<span data-ttu-id="23b5e-332">taj</span><span class="sxs-lookup"><span data-stu-id="23b5e-332">taj</span></span>
  
<span data-ttu-id="23b5e-333">Taj #</span><span class="sxs-lookup"><span data-stu-id="23b5e-333">taj#</span></span>
  
<span data-ttu-id="23b5e-334">ssn</span><span class="sxs-lookup"><span data-stu-id="23b5e-334">ssn</span></span>
  
<span data-ttu-id="23b5e-335">ssn #</span><span class="sxs-lookup"><span data-stu-id="23b5e-335">ssn#</span></span>
  
<span data-ttu-id="23b5e-336">soziale Sicherheit keine</span><span class="sxs-lookup"><span data-stu-id="23b5e-336">social security no</span></span>
  
<span data-ttu-id="23b5e-337">áfa</span><span class="sxs-lookup"><span data-stu-id="23b5e-337">áfa</span></span>
  
<span data-ttu-id="23b5e-338">Közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="23b5e-338">közösségi adószám</span></span>
  
<span data-ttu-id="23b5e-339">Általános Forgalmi Adó szám</span><span class="sxs-lookup"><span data-stu-id="23b5e-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="23b5e-340">Hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="23b5e-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="23b5e-341">Áfa szám</span><span class="sxs-lookup"><span data-stu-id="23b5e-341">áfa szám</span></span>
  
<span data-ttu-id="23b5e-342">Magyar Áfa szám</span><span class="sxs-lookup"><span data-stu-id="23b5e-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="23b5e-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="23b5e-343">Portugal</span></span>

<span data-ttu-id="23b5e-344">Weitere Informationen hierzu finden Sie im Abschnitt "Portugal Bürger Card-Nummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="23b5e-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="23b5e-345">Spanien</span><span class="sxs-lookup"><span data-stu-id="23b5e-345">Spain</span></span>

<span data-ttu-id="23b5e-346">Weitere Informationen hierzu finden Sie im Abschnitt "Spanien Sozialversicherungsnummer (SSN)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="23b5e-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="23b5e-347">Schweden</span><span class="sxs-lookup"><span data-stu-id="23b5e-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="23b5e-348">Format</span><span class="sxs-lookup"><span data-stu-id="23b5e-348">Format</span></span>

<span data-ttu-id="23b5e-349">12 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="23b5e-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="23b5e-350">Muster</span><span class="sxs-lookup"><span data-stu-id="23b5e-350">Pattern</span></span>

<span data-ttu-id="23b5e-351">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="23b5e-351">12 digits:</span></span>
  
-  <span data-ttu-id="23b5e-352">Acht Ziffern, die das Geburtsdatum (JJJJMMTT) entsprechen</span><span class="sxs-lookup"><span data-stu-id="23b5e-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="23b5e-353">Drei Ziffern, die eine fortlaufende Zahl entsprechen, in dem:</span><span class="sxs-lookup"><span data-stu-id="23b5e-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="23b5e-354">Die letzte Ziffer in der Seriennummer gibt Geschlecht an, durch die Zuweisung von eine ungerade Anzahl für Männlich und eine gerade Anzahl für Weiblich</span><span class="sxs-lookup"><span data-stu-id="23b5e-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="23b5e-355">Bis zu 1990 entsprach die Zuordnung der Seriennummer auf den Kanton Geburtsbetriebs der Anzahl der Bearer oder (wenn vor 1947 geboren), in dem er hatte wurde Leben, gemäß Tax-Datensätze auf Januar 1, 1947 mit einen speziellen Code (in der Regel 9 als 7. Ziffer) für Einwanderer</span><span class="sxs-lookup"><span data-stu-id="23b5e-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="23b5e-356">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="23b5e-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="23b5e-357">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="23b5e-357">Checksum</span></span>

<span data-ttu-id="23b5e-358">Ja</span><span class="sxs-lookup"><span data-stu-id="23b5e-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="23b5e-359">Definition</span><span class="sxs-lookup"><span data-stu-id="23b5e-359">Definition</span></span>

<span data-ttu-id="23b5e-360">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-361">Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="23b5e-362">Ein Schlüsselwort aus `Keywords_sweden_eu_ssn_or_equivalent` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="23b5e-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="23b5e-363">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="23b5e-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="23b5e-364">Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="23b5e-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="23b5e-365">Keywords</span><span class="sxs-lookup"><span data-stu-id="23b5e-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="23b5e-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="23b5e-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="23b5e-367">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-367">personal id number</span></span>
  
<span data-ttu-id="23b5e-368">identification number
</span><span class="sxs-lookup"><span data-stu-id="23b5e-368">identification number</span></span>
  
<span data-ttu-id="23b5e-369">Persönliche Id keine</span><span class="sxs-lookup"><span data-stu-id="23b5e-369">personal id no</span></span>
  
<span data-ttu-id="23b5e-370">Identität keine</span><span class="sxs-lookup"><span data-stu-id="23b5e-370">identity no</span></span>
  
<span data-ttu-id="23b5e-371">Kennung keine</span><span class="sxs-lookup"><span data-stu-id="23b5e-371">identification no</span></span>
  
<span data-ttu-id="23b5e-372">Persönliche Identifikationsnummer keine</span><span class="sxs-lookup"><span data-stu-id="23b5e-372">personal identification no</span></span>
  
<span data-ttu-id="23b5e-373">Personnummer-id</span><span class="sxs-lookup"><span data-stu-id="23b5e-373">personnummer id</span></span>
  
<span data-ttu-id="23b5e-374">Personligt-Id-nummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-374">personligt id-nummer</span></span>
  
<span data-ttu-id="23b5e-375">Unikt-Id-nummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-375">unikt id-nummer</span></span>
  
<span data-ttu-id="23b5e-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="23b5e-376">personnummer</span></span>
  
<span data-ttu-id="23b5e-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="23b5e-377">identifikationsnumret</span></span>
  
<span data-ttu-id="23b5e-378">Personnummer #</span><span class="sxs-lookup"><span data-stu-id="23b5e-378">personnummer#</span></span>
  
<span data-ttu-id="23b5e-379">Identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="23b5e-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23b5e-380">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23b5e-380">See also</span></span>

[<span data-ttu-id="23b5e-381">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="23b5e-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

