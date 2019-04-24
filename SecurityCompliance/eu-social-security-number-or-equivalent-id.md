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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255553"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="06410-104">EU-sozialVersicherungsNummer oder entsprechende ID</span><span class="sxs-lookup"><span data-stu-id="06410-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="06410-105">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn die EU-sozialVersicherungsNummer (SSN) oder der entsprechende ID-vertrauliche Informationstyp erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="06410-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type.</span></span> <span data-ttu-id="06410-106">Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="06410-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="06410-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="06410-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="06410-108">Format</span><span class="sxs-lookup"><span data-stu-id="06410-108">Format</span></span>

<span data-ttu-id="06410-109">10 Ziffern im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="06410-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="06410-110">Muster</span><span class="sxs-lookup"><span data-stu-id="06410-110">Pattern</span></span>

<span data-ttu-id="06410-111">10 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="06410-111">10 digits:</span></span>
  
-  <span data-ttu-id="06410-112">Drei Ziffern, die einer Seriennummer entsprechen</span><span class="sxs-lookup"><span data-stu-id="06410-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="06410-113">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="06410-113">One check digit</span></span>
    
- <span data-ttu-id="06410-114">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="06410-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="06410-115">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="06410-115">Checksum</span></span>

<span data-ttu-id="06410-116">Ja</span><span class="sxs-lookup"><span data-stu-id="06410-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="06410-117">Definition</span><span class="sxs-lookup"><span data-stu-id="06410-117">Definition</span></span>

<span data-ttu-id="06410-118">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-119">Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="06410-120">Ein Schlüsselwort `Keywords_austria_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="06410-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="06410-121">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-122">Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="06410-123">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="06410-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="06410-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="06410-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="06410-125">Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-125">social security no</span></span>
  
<span data-ttu-id="06410-126">social security number</span><span class="sxs-lookup"><span data-stu-id="06410-126">social security number</span></span>
  
<span data-ttu-id="06410-127">social security code</span><span class="sxs-lookup"><span data-stu-id="06410-127">social security code</span></span>
  
<span data-ttu-id="06410-128">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-128">insurance number</span></span>
  
<span data-ttu-id="06410-129">Austrian SSN</span><span class="sxs-lookup"><span data-stu-id="06410-129">austrian ssn</span></span>
  
<span data-ttu-id="06410-130">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-130">ssn#</span></span>
  
<span data-ttu-id="06410-131">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-131">ssn</span></span>
  
<span data-ttu-id="06410-132">versicherungscode</span><span class="sxs-lookup"><span data-stu-id="06410-132">insurance code</span></span>
  
<span data-ttu-id="06410-133">versicherungscode #</span><span class="sxs-lookup"><span data-stu-id="06410-133">insurance code#</span></span>
  
<span data-ttu-id="06410-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="06410-134">socialsecurityno#</span></span>
  
<span data-ttu-id="06410-135">Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="06410-136">soziale Sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="06410-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="06410-137">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="06410-138">Belgien</span><span class="sxs-lookup"><span data-stu-id="06410-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="06410-139">Format</span><span class="sxs-lookup"><span data-stu-id="06410-139">Format</span></span>

<span data-ttu-id="06410-140">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="06410-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="06410-141">Muster</span><span class="sxs-lookup"><span data-stu-id="06410-141">Pattern</span></span>

<span data-ttu-id="06410-142">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="06410-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="06410-143">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="06410-143">Checksum</span></span>

<span data-ttu-id="06410-144">Ja</span><span class="sxs-lookup"><span data-stu-id="06410-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="06410-145">Definition</span><span class="sxs-lookup"><span data-stu-id="06410-145">Definition</span></span>

<span data-ttu-id="06410-146">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-147">Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="06410-148">Ein Schlüsselwort `Keywords_belgium_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="06410-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="06410-149">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-150">Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="06410-151">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="06410-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="06410-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="06410-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="06410-153">belgische nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-153">belgian national number</span></span>
  
<span data-ttu-id="06410-154">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-154">national number</span></span>
  
<span data-ttu-id="06410-155">social security number</span><span class="sxs-lookup"><span data-stu-id="06410-155">social security number</span></span>
  
<span data-ttu-id="06410-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="06410-156">nationalnumber#</span></span>
  
<span data-ttu-id="06410-157">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-157">ssn#</span></span>
  
<span data-ttu-id="06410-158">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-158">ssn</span></span>
  
<span data-ttu-id="06410-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="06410-159">nationalnumber</span></span>
  
<span data-ttu-id="06410-160">BNN</span><span class="sxs-lookup"><span data-stu-id="06410-160">bnn#</span></span>
  
<span data-ttu-id="06410-161">BNN</span><span class="sxs-lookup"><span data-stu-id="06410-161">bnn</span></span>
  
<span data-ttu-id="06410-162">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-162">personal id number</span></span>
  
<span data-ttu-id="06410-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="06410-163">personalidnumber#</span></span>
  
<span data-ttu-id="06410-164">Numéro National</span><span class="sxs-lookup"><span data-stu-id="06410-164">numéro national</span></span>
  
<span data-ttu-id="06410-165">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="06410-165">numéro de sécurité</span></span>
  
<span data-ttu-id="06410-166">Numéro d'assuré</span><span class="sxs-lookup"><span data-stu-id="06410-166">numéro d'assuré</span></span>
  
<span data-ttu-id="06410-167">identifizierbare nationale</span><span class="sxs-lookup"><span data-stu-id="06410-167">identifiant national</span></span>
  
<span data-ttu-id="06410-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="06410-168">identifiantnational#</span></span>
  
<span data-ttu-id="06410-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="06410-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="06410-170">Kroatien</span><span class="sxs-lookup"><span data-stu-id="06410-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="06410-171">Format</span><span class="sxs-lookup"><span data-stu-id="06410-171">Format</span></span>

<span data-ttu-id="06410-172">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="06410-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="06410-173">Muster</span><span class="sxs-lookup"><span data-stu-id="06410-173">Pattern</span></span>

 <span data-ttu-id="06410-174">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="06410-174">11 digits:</span></span> 
  
-  <span data-ttu-id="06410-175">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="06410-175">Ten digits</span></span> 
    
- <span data-ttu-id="06410-176">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="06410-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="06410-177">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="06410-177">Checksum</span></span>

<span data-ttu-id="06410-178">Ja</span><span class="sxs-lookup"><span data-stu-id="06410-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="06410-179">Definition</span><span class="sxs-lookup"><span data-stu-id="06410-179">Definition</span></span>

<span data-ttu-id="06410-180">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-181">Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="06410-182">Ein Schlüsselwort `Keywords_croatia_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="06410-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="06410-183">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-184">Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="06410-185">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="06410-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="06410-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="06410-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="06410-187">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-187">personal identification number</span></span>
  
<span data-ttu-id="06410-188">Master-Bürgerzahl</span><span class="sxs-lookup"><span data-stu-id="06410-188">master citizen number</span></span>
  
<span data-ttu-id="06410-189">national identification number</span><span class="sxs-lookup"><span data-stu-id="06410-189">national identification number</span></span>
  
<span data-ttu-id="06410-190">social security number</span><span class="sxs-lookup"><span data-stu-id="06410-190">social security number</span></span>
  
<span data-ttu-id="06410-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="06410-191">nationalnumber#</span></span>
  
<span data-ttu-id="06410-192">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-192">ssn#</span></span>
  
<span data-ttu-id="06410-193">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-193">ssn</span></span>
  
<span data-ttu-id="06410-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="06410-194">nationalnumber</span></span>
  
<span data-ttu-id="06410-195">BNN</span><span class="sxs-lookup"><span data-stu-id="06410-195">bnn#</span></span>
  
<span data-ttu-id="06410-196">BNN</span><span class="sxs-lookup"><span data-stu-id="06410-196">bnn</span></span>
  
<span data-ttu-id="06410-197">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-197">personal id number</span></span>
  
<span data-ttu-id="06410-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="06410-198">personalidnumber#</span></span>
  
<span data-ttu-id="06410-199">OIB</span><span class="sxs-lookup"><span data-stu-id="06410-199">oib</span></span>
  
<span data-ttu-id="06410-200">Osobni identifikacijski Broj</span><span class="sxs-lookup"><span data-stu-id="06410-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="06410-201">Tschechien</span><span class="sxs-lookup"><span data-stu-id="06410-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="06410-202">Format</span><span class="sxs-lookup"><span data-stu-id="06410-202">Format</span></span>

<span data-ttu-id="06410-203">Zehn Ziffern und ein umgekehrter Schrägstrich im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="06410-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="06410-204">Muster</span><span class="sxs-lookup"><span data-stu-id="06410-204">Pattern</span></span>

<span data-ttu-id="06410-205">Zehn Ziffern und ein umgekehrter Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="06410-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="06410-206">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT):</span><span class="sxs-lookup"><span data-stu-id="06410-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="06410-207">Einen umgekehrten Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="06410-207">A backslash</span></span>
    
- <span data-ttu-id="06410-208">Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am selben Datum geboren wurden</span><span class="sxs-lookup"><span data-stu-id="06410-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="06410-209">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="06410-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="06410-210">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="06410-210">Checksum</span></span>

<span data-ttu-id="06410-211">Ja</span><span class="sxs-lookup"><span data-stu-id="06410-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="06410-212">Definition</span><span class="sxs-lookup"><span data-stu-id="06410-212">Definition</span></span>

<span data-ttu-id="06410-213">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-214">Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="06410-215">Ein Schlüsselwort `Keywords_czech_republic_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="06410-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="06410-216">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-217">Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="06410-218">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="06410-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="06410-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="06410-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="06410-220">Geburtsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-220">birth number</span></span>
  
<span data-ttu-id="06410-221">national identification number</span><span class="sxs-lookup"><span data-stu-id="06410-221">national identification number</span></span>
  
<span data-ttu-id="06410-222">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-222">personal identification number</span></span>
  
<span data-ttu-id="06410-223">social security number</span><span class="sxs-lookup"><span data-stu-id="06410-223">social security number</span></span>
  
<span data-ttu-id="06410-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="06410-224">nationalnumber#</span></span>
  
<span data-ttu-id="06410-225">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-225">ssn#</span></span>
  
<span data-ttu-id="06410-226">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-226">ssn</span></span>
  
<span data-ttu-id="06410-227">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-227">national number</span></span>
  
<span data-ttu-id="06410-228">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-228">personal id number</span></span>
  
<span data-ttu-id="06410-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="06410-229">personalidnumber#</span></span>
  
<span data-ttu-id="06410-230">rč</span><span class="sxs-lookup"><span data-stu-id="06410-230">rč</span></span>
  
<span data-ttu-id="06410-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="06410-231">rodné číslo</span></span>
  
<span data-ttu-id="06410-232">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="06410-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="06410-233">Dänemark</span><span class="sxs-lookup"><span data-stu-id="06410-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="06410-234">Format</span><span class="sxs-lookup"><span data-stu-id="06410-234">Format</span></span>

<span data-ttu-id="06410-235">Zehn Ziffern und ein Bindestrich im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="06410-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="06410-236">Muster</span><span class="sxs-lookup"><span data-stu-id="06410-236">Pattern</span></span>

<span data-ttu-id="06410-237">Zehn Ziffern und ein Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="06410-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="06410-238">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="06410-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="06410-239">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="06410-239">A hyphen</span></span>
    
- <span data-ttu-id="06410-240">Vier Ziffern, die einer Sequenznummer entsprechen</span><span class="sxs-lookup"><span data-stu-id="06410-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="06410-241">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="06410-241">Checksum</span></span>

<span data-ttu-id="06410-242">Ja</span><span class="sxs-lookup"><span data-stu-id="06410-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="06410-243">Definition</span><span class="sxs-lookup"><span data-stu-id="06410-243">Definition</span></span>

<span data-ttu-id="06410-244">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-245">Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="06410-246">Ein Schlüsselwort `Keywords_denmark_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="06410-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="06410-247">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-248">Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="06410-249">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="06410-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="06410-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="06410-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="06410-251">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-251">personal identification number</span></span>
  
<span data-ttu-id="06410-252">national identification number</span><span class="sxs-lookup"><span data-stu-id="06410-252">national identification number</span></span>
  
<span data-ttu-id="06410-253">social security number</span><span class="sxs-lookup"><span data-stu-id="06410-253">social security number</span></span>
  
<span data-ttu-id="06410-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="06410-254">nationalnumber#</span></span>
  
<span data-ttu-id="06410-255">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-255">ssn#</span></span>
  
<span data-ttu-id="06410-256">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-256">ssn</span></span>
  
<span data-ttu-id="06410-257">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-257">national number</span></span>
  
<span data-ttu-id="06410-258">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-258">personal id number</span></span>
  
<span data-ttu-id="06410-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="06410-259">personalidnumber#</span></span>
  
<span data-ttu-id="06410-260">CPR-Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-260">cpr-nummer</span></span>
  
<span data-ttu-id="06410-261">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="06410-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="06410-262">Finnland</span><span class="sxs-lookup"><span data-stu-id="06410-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="06410-263">Format</span><span class="sxs-lookup"><span data-stu-id="06410-263">Format</span></span>

<span data-ttu-id="06410-264">Eine Kombination aus 11 Zeichen im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="06410-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="06410-265">Muster</span><span class="sxs-lookup"><span data-stu-id="06410-265">Pattern</span></span>

<span data-ttu-id="06410-266">Eine Kombination aus 11 Zeichen im angegebenen Format:</span><span class="sxs-lookup"><span data-stu-id="06410-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="06410-267">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="06410-267">Six digits</span></span> 
    
- <span data-ttu-id="06410-268">Eine der folgenden Instanzen:</span><span class="sxs-lookup"><span data-stu-id="06410-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="06410-269">Plus-Symbol</span><span class="sxs-lookup"><span data-stu-id="06410-269">Plus symbol</span></span>
    
  - <span data-ttu-id="06410-270">Minus Zeichen</span><span class="sxs-lookup"><span data-stu-id="06410-270">Minus symbol</span></span>
    
  - <span data-ttu-id="06410-271">Der Buchstabe "A" (Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="06410-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="06410-272">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="06410-272">Three digits</span></span>
    
- <span data-ttu-id="06410-273">Ein Buchstabe oder eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="06410-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="06410-274">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="06410-274">Checksum</span></span>

<span data-ttu-id="06410-275">Ja</span><span class="sxs-lookup"><span data-stu-id="06410-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="06410-276">Definition</span><span class="sxs-lookup"><span data-stu-id="06410-276">Definition</span></span>

<span data-ttu-id="06410-277">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-278">Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="06410-279">Ein Schlüsselwort `Keywords_finland_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="06410-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="06410-280">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-281">Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="06410-282">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="06410-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="06410-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="06410-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="06410-284">identification number</span><span class="sxs-lookup"><span data-stu-id="06410-284">identification number</span></span>
  
<span data-ttu-id="06410-285">persönliche ID</span><span class="sxs-lookup"><span data-stu-id="06410-285">personal id</span></span>
  
<span data-ttu-id="06410-286">Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-286">identity number</span></span>
  
<span data-ttu-id="06410-287">nationale finnische ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-287">finnish national id number</span></span>
  
<span data-ttu-id="06410-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="06410-288">personalidnumber#</span></span>
  
<span data-ttu-id="06410-289">national identification number</span><span class="sxs-lookup"><span data-stu-id="06410-289">national identification number</span></span>
  
<span data-ttu-id="06410-290">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-290">id number</span></span>
  
<span data-ttu-id="06410-291">nationale ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="06410-291">national id no.</span></span>
  
<span data-ttu-id="06410-292">nationale ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-292">national id number</span></span>
  
<span data-ttu-id="06410-293">ID Nein</span><span class="sxs-lookup"><span data-stu-id="06410-293">id no</span></span>
  
<span data-ttu-id="06410-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="06410-294">tunnistenumero</span></span>
  
<span data-ttu-id="06410-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="06410-295">henkilötunnus</span></span>
  
<span data-ttu-id="06410-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="06410-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="06410-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="06410-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="06410-298">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="06410-298">identiteetti numero</span></span>
  
<span data-ttu-id="06410-299">Suomen der Kok henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="06410-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="06410-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="06410-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="06410-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="06410-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="06410-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="06410-302">tunnusnumero</span></span>
  
<span data-ttu-id="06410-303">der Kok tunnus numero</span><span class="sxs-lookup"><span data-stu-id="06410-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="06410-304">Hetu</span><span class="sxs-lookup"><span data-stu-id="06410-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="06410-305">Frankreich</span><span class="sxs-lookup"><span data-stu-id="06410-305">France</span></span>

<span data-ttu-id="06410-306">Weitere Informationen finden Sie im Abschnitt "französische sozialVersicherungsNummer (INSEE)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="06410-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="06410-307">Deutschland</span><span class="sxs-lookup"><span data-stu-id="06410-307">Germany</span></span>

<span data-ttu-id="06410-308">Weitere Informationen finden Sie im Abschnitt "Deutschland PersonalausweisNummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="06410-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="06410-309">Griechenland</span><span class="sxs-lookup"><span data-stu-id="06410-309">Greece</span></span>

<span data-ttu-id="06410-310">Weitere Informationen finden Sie im Abschnitt "GriechenLand National ID Card" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="06410-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="06410-311">Ungarn</span><span class="sxs-lookup"><span data-stu-id="06410-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="06410-312">Format</span><span class="sxs-lookup"><span data-stu-id="06410-312">Format</span></span>

<span data-ttu-id="06410-313">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="06410-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="06410-314">Muster</span><span class="sxs-lookup"><span data-stu-id="06410-314">Pattern</span></span>

<span data-ttu-id="06410-315">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="06410-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="06410-316">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="06410-316">Checksum</span></span>

<span data-ttu-id="06410-317">Ja</span><span class="sxs-lookup"><span data-stu-id="06410-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="06410-318">Definition</span><span class="sxs-lookup"><span data-stu-id="06410-318">Definition</span></span>

<span data-ttu-id="06410-319">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-320">Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="06410-321">Ein Schlüsselwort `Keywords_hungary_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="06410-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="06410-322">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-323">Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="06410-324">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="06410-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="06410-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="06410-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="06410-326">Sozialversicherungsnummer (ungarisch)</span><span class="sxs-lookup"><span data-stu-id="06410-326">hungarian social security number</span></span>
  
<span data-ttu-id="06410-327">social security number</span><span class="sxs-lookup"><span data-stu-id="06410-327">social security number</span></span>
  
<span data-ttu-id="06410-328">socialsecuritynumber #</span><span class="sxs-lookup"><span data-stu-id="06410-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="06410-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="06410-329">hssn#</span></span>
  
<span data-ttu-id="06410-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="06410-330">socialsecuritynno</span></span>
  
<span data-ttu-id="06410-331">hssn</span><span class="sxs-lookup"><span data-stu-id="06410-331">hssn</span></span>
  
<span data-ttu-id="06410-332">Taj</span><span class="sxs-lookup"><span data-stu-id="06410-332">taj</span></span>
  
<span data-ttu-id="06410-333">Taj</span><span class="sxs-lookup"><span data-stu-id="06410-333">taj#</span></span>
  
<span data-ttu-id="06410-334">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-334">ssn</span></span>
  
<span data-ttu-id="06410-335">SSN</span><span class="sxs-lookup"><span data-stu-id="06410-335">ssn#</span></span>
  
<span data-ttu-id="06410-336">Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-336">social security no</span></span>
  
<span data-ttu-id="06410-337">ÁFA</span><span class="sxs-lookup"><span data-stu-id="06410-337">áfa</span></span>
  
<span data-ttu-id="06410-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="06410-338">közösségi adószám</span></span>
  
<span data-ttu-id="06410-339">Általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="06410-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="06410-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="06410-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="06410-341">ÁFA szám</span><span class="sxs-lookup"><span data-stu-id="06410-341">áfa szám</span></span>
  
<span data-ttu-id="06410-342">Magyar ÁFA szám</span><span class="sxs-lookup"><span data-stu-id="06410-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="06410-343">Portugal</span><span class="sxs-lookup"><span data-stu-id="06410-343">Portugal</span></span>

<span data-ttu-id="06410-344">Weitere Informationen finden Sie im Abschnitt "portugiesische Bürgerkarten Nummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="06410-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="06410-345">Spanien</span><span class="sxs-lookup"><span data-stu-id="06410-345">Spain</span></span>

<span data-ttu-id="06410-346">Weitere Informationen finden Sie im Abschnitt "sozialVersicherungsNummer (SSN) in Spanien" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="06410-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="06410-347">Schweden</span><span class="sxs-lookup"><span data-stu-id="06410-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="06410-348">Format</span><span class="sxs-lookup"><span data-stu-id="06410-348">Format</span></span>

<span data-ttu-id="06410-349">12 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="06410-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="06410-350">Muster</span><span class="sxs-lookup"><span data-stu-id="06410-350">Pattern</span></span>

<span data-ttu-id="06410-351">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="06410-351">12 digits:</span></span>
  
-  <span data-ttu-id="06410-352">Acht Ziffern, die dem Geburtsdatum entsprechen (JJJJMMTT)</span><span class="sxs-lookup"><span data-stu-id="06410-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="06410-353">Drei Ziffern, die einer Seriennummer entsprechen, wobei:</span><span class="sxs-lookup"><span data-stu-id="06410-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="06410-354">Die letzte Ziffer in der Seriennummer kennzeichnet das Geschlecht durch die Zuweisung einer ungerade Zahl für männliche und eine gerade Zahl für weibliche</span><span class="sxs-lookup"><span data-stu-id="06410-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="06410-355">Bis zu 1990 entspricht die Zuordnung der Seriennummer der Grafschaft, in der der Träger der Nummer geboren wurde, oder (wenn er vor 1947 geboren wurde), in dem er nach Steuerdaten Sätzen am 1. Januar 1947 lebte, mit einem speziellen Code (in der Regel 9 als 7. Ziffer) für Einwanderer</span><span class="sxs-lookup"><span data-stu-id="06410-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="06410-356">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="06410-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="06410-357">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="06410-357">Checksum</span></span>

<span data-ttu-id="06410-358">Ja</span><span class="sxs-lookup"><span data-stu-id="06410-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="06410-359">Definition</span><span class="sxs-lookup"><span data-stu-id="06410-359">Definition</span></span>

<span data-ttu-id="06410-360">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-361">Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="06410-362">Ein Schlüsselwort `Keywords_sweden_eu_ssn_or_equivalent` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="06410-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="06410-363">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="06410-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="06410-364">Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="06410-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="06410-365">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="06410-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="06410-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="06410-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="06410-367">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-367">personal id number</span></span>
  
<span data-ttu-id="06410-368">identification number</span><span class="sxs-lookup"><span data-stu-id="06410-368">identification number</span></span>
  
<span data-ttu-id="06410-369">persönliche ID Nein</span><span class="sxs-lookup"><span data-stu-id="06410-369">personal id no</span></span>
  
<span data-ttu-id="06410-370">Identität Nein</span><span class="sxs-lookup"><span data-stu-id="06410-370">identity no</span></span>
  
<span data-ttu-id="06410-371">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-371">identification no</span></span>
  
<span data-ttu-id="06410-372">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="06410-372">personal identification no</span></span>
  
<span data-ttu-id="06410-373">PERSONNUMMER-ID</span><span class="sxs-lookup"><span data-stu-id="06410-373">personnummer id</span></span>
  
<span data-ttu-id="06410-374">personligt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-374">personligt id-nummer</span></span>
  
<span data-ttu-id="06410-375">unikt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="06410-375">unikt id-nummer</span></span>
  
<span data-ttu-id="06410-376">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="06410-376">personnummer</span></span>
  
<span data-ttu-id="06410-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="06410-377">identifikationsnumret</span></span>
  
<span data-ttu-id="06410-378">PERSONNUMMER #</span><span class="sxs-lookup"><span data-stu-id="06410-378">personnummer#</span></span>
  
<span data-ttu-id="06410-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="06410-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06410-380">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06410-380">See also</span></span>

[<span data-ttu-id="06410-381">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="06410-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

