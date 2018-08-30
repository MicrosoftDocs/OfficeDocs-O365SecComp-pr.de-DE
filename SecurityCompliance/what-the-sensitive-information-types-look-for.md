---
title: Wonach die Typen von vertraulichen Informationen suchen
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
ms.assetid: fd505979-76be-4d9f-b459-abef3fc9e86b
description: Verhinderung von Datenverlust (DLP) in die Office 365-Sicherheit &amp; Compliance Center umfasst 80 vertraulichen Informationstypen, die Sie in Ihrer DLP-Richtlinien verwendet werden. Dieses Thema enthält eine Liste aller diese Typen vertraulicher Informationen und dargestellt was eine DLP-Richtlinie für jeden Typ erkannt.
ms.openlocfilehash: 064606085363ba9de972511642993277451c8ce3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529825"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="6b58c-104">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="6b58c-104">What the sensitive information types look for</span></span>

<span data-ttu-id="6b58c-p102">Verhinderung von Datenverlust (DLP) in die Office 365-Sicherheit &amp; Compliance Center enthält viele Arten von vertraulichen Informationen, die Sie in Ihrer DLP-Richtlinien verwendet werden. Dieses Thema enthält eine Liste aller diese Typen vertraulicher Informationen und dargestellt was eine DLP-Richtlinie für jeden Typ erkannt. Ein Typ von vertraulichen Informationen wird durch ein Muster definiert, die mit einem regulären Ausdruck oder eine Funktion identifiziert werden kann. Darüber hinaus kann bestätigende Nachweis Stichwörter und Prüfsumme verwendet werden, um ein anderes vertrauliche Informationen zu identifizieren. Vertrauensstufe und Nähe zum werden auch in der Evaluierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b58c-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="6b58c-110">ABA Routing Number (US-Bankleitzahl)</span><span class="sxs-lookup"><span data-stu-id="6b58c-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-111">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-111">Format</span></span>

<span data-ttu-id="6b58c-112">9 Ziffern in formatiertem oder unformatiertem Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-113">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-113">Pattern</span></span>

<span data-ttu-id="6b58c-114">Formatiert:</span><span class="sxs-lookup"><span data-stu-id="6b58c-114">Formatted:</span></span>
- <span data-ttu-id="6b58c-115">Vier Ziffern, beginnend mit 0, 1, 2, 3, 6, 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="6b58c-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="6b58c-116">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-116">A hyphen</span></span>
- <span data-ttu-id="6b58c-117">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-117">Four digits</span></span>
- <span data-ttu-id="6b58c-118">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-118">A hyphen</span></span>
- <span data-ttu-id="6b58c-119">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-119">A digit</span></span>

<span data-ttu-id="6b58c-120">Unformatiert: 9 aufeinander folgenden Ziffern beginnend mit 0, 1, 2, 3, 6, 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="6b58c-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="6b58c-121">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-121">Checksum</span></span>

<span data-ttu-id="6b58c-122">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-123">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-123">Definition</span></span>

<span data-ttu-id="6b58c-124">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-125">Die Funktion Func_aba_routing findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-126">Ein Schlüsselwort aus Keyword_ABA_Routing wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="6b58c-127">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="6b58c-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="6b58c-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="6b58c-129">aba</span><span class="sxs-lookup"><span data-stu-id="6b58c-129">aba</span></span>
- <span data-ttu-id="6b58c-130">
aba #</span><span class="sxs-lookup"><span data-stu-id="6b58c-130">aba #</span></span>
- <span data-ttu-id="6b58c-131">
aba routing #</span><span class="sxs-lookup"><span data-stu-id="6b58c-131">aba routing #</span></span>
- <span data-ttu-id="6b58c-132">ABA routing Anzahl</span><span class="sxs-lookup"><span data-stu-id="6b58c-132">aba routing number</span></span>
- <span data-ttu-id="6b58c-133">
aba#</span><span class="sxs-lookup"><span data-stu-id="6b58c-133">aba#</span></span>
- <span data-ttu-id="6b58c-134">
abarouting#</span><span class="sxs-lookup"><span data-stu-id="6b58c-134">abarouting#</span></span>
- <span data-ttu-id="6b58c-135">
aba number</span><span class="sxs-lookup"><span data-stu-id="6b58c-135">aba number</span></span>
- <span data-ttu-id="6b58c-136">
abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="6b58c-136">abaroutingnumber</span></span>
- <span data-ttu-id="6b58c-137">
american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="6b58c-137">american bank association routing #</span></span>
- <span data-ttu-id="6b58c-138">
american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="6b58c-138">american bank association routing number</span></span>
- <span data-ttu-id="6b58c-139">
americanbankassociationrouting#</span><span class="sxs-lookup"><span data-stu-id="6b58c-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="6b58c-140">
americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="6b58c-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="6b58c-141">
bank routing number</span><span class="sxs-lookup"><span data-stu-id="6b58c-141">bank routing number</span></span>
- <span data-ttu-id="6b58c-142">
bankrouting#</span><span class="sxs-lookup"><span data-stu-id="6b58c-142">bankrouting#</span></span>
- <span data-ttu-id="6b58c-143">
bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="6b58c-143">bankroutingnumber</span></span>
- <span data-ttu-id="6b58c-144">
routing transit number</span><span class="sxs-lookup"><span data-stu-id="6b58c-144">routing transit number</span></span>
- <span data-ttu-id="6b58c-145">
RTN
</span><span class="sxs-lookup"><span data-stu-id="6b58c-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="6b58c-146">Argentina National Identity (DNI) Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-147">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-147">Format</span></span>

<span data-ttu-id="6b58c-148">Acht Ziffern, durch Punkte getrennt</span><span class="sxs-lookup"><span data-stu-id="6b58c-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-149">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-149">Pattern</span></span>

<span data-ttu-id="6b58c-150">Acht Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-150">Eight digits:</span></span>
- <span data-ttu-id="6b58c-151">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-151">Two digits</span></span>
- <span data-ttu-id="6b58c-152">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="6b58c-152">A period</span></span>
- <span data-ttu-id="6b58c-153">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-153">Three digits</span></span>
- <span data-ttu-id="6b58c-154">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="6b58c-154">A period</span></span>
- <span data-ttu-id="6b58c-155">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-156">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-156">Checksum</span></span>

<span data-ttu-id="6b58c-157">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-158">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-158">Definition</span></span>

<span data-ttu-id="6b58c-159">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-160">Der reguläre Ausdruck Regex_argentina_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-161">Ein Schlüsselwort aus Keyword_argentina_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-162">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="6b58c-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="6b58c-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="6b58c-164">Argentina National Identity number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="6b58c-165">Identität</span><span class="sxs-lookup"><span data-stu-id="6b58c-165">Identity</span></span> 
- <span data-ttu-id="6b58c-166">Kennung National Personalausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="6b58c-167">DNI
</span><span class="sxs-lookup"><span data-stu-id="6b58c-167">DNI</span></span> 
- <span data-ttu-id="6b58c-168">NIC National Registrierung von Personen</span><span class="sxs-lookup"><span data-stu-id="6b58c-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="6b58c-169">Documento Nacional de Identidad
</span><span class="sxs-lookup"><span data-stu-id="6b58c-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="6b58c-170">Registro Nacional de las Personas
</span><span class="sxs-lookup"><span data-stu-id="6b58c-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="6b58c-171">Identidad
</span><span class="sxs-lookup"><span data-stu-id="6b58c-171">Identidad</span></span> 
- <span data-ttu-id="6b58c-172">Identificación
</span><span class="sxs-lookup"><span data-stu-id="6b58c-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="6b58c-173">Australische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-174">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-174">Format</span></span>

<span data-ttu-id="6b58c-175">6-10 Stellen mit oder ohne Bankfilialnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-176">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-176">Pattern</span></span>

<span data-ttu-id="6b58c-p103">Account-Nummer ist 6 bis 10 Ziffern. Australien Zustand Bankleitzahl:</span><span class="sxs-lookup"><span data-stu-id="6b58c-p103">Account number is 6-10 digits. Australia bank state branch number:</span></span>
- <span data-ttu-id="6b58c-179">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-179">Three digits</span></span> 
- <span data-ttu-id="6b58c-180">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-180">A hyphen</span></span> 
- <span data-ttu-id="6b58c-181">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-182">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-182">Checksum</span></span>

<span data-ttu-id="6b58c-183">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-184">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-184">Definition</span></span>

<span data-ttu-id="6b58c-185">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-186">Der reguläre Ausdruck Regex_australia_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="6b58c-187">Ein Schlüsselwort aus Keyword_australia_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="6b58c-188">Der reguläre Ausdruck Regex_australia_bank_account_number_bsb findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="6b58c-189">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-190">Der reguläre Ausdruck Regex_australia_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="6b58c-191">Ein Schlüsselwort aus Keyword_australia_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

```
<!-- Australia Bank Account Number -->
<Entity id="74a54de9-2a30-4aa0-a8aa-3d9327fc07c7" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
        <Match idRef="Regex_australia_bank_account_number_bsb" />
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
  </Pattern>
 </Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-192">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="6b58c-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="6b58c-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="6b58c-194">swift bank code</span></span>
- <span data-ttu-id="6b58c-195">
correspondent bank</span><span class="sxs-lookup"><span data-stu-id="6b58c-195">correspondent bank</span></span>
- <span data-ttu-id="6b58c-196">
base currency</span><span class="sxs-lookup"><span data-stu-id="6b58c-196">base currency</span></span>
- <span data-ttu-id="6b58c-197">
usa account</span><span class="sxs-lookup"><span data-stu-id="6b58c-197">usa account</span></span>
- <span data-ttu-id="6b58c-198">
holder address</span><span class="sxs-lookup"><span data-stu-id="6b58c-198">holder address</span></span>
- <span data-ttu-id="6b58c-199">
bank address</span><span class="sxs-lookup"><span data-stu-id="6b58c-199">bank address</span></span>
- <span data-ttu-id="6b58c-200">
information account</span><span class="sxs-lookup"><span data-stu-id="6b58c-200">information account</span></span>
- <span data-ttu-id="6b58c-201">
fund transfers</span><span class="sxs-lookup"><span data-stu-id="6b58c-201">fund transfers</span></span>
- <span data-ttu-id="6b58c-202">
bank charges</span><span class="sxs-lookup"><span data-stu-id="6b58c-202">bank charges</span></span>
- <span data-ttu-id="6b58c-203">
bank details</span><span class="sxs-lookup"><span data-stu-id="6b58c-203">bank details</span></span>
- <span data-ttu-id="6b58c-204">
banking information</span><span class="sxs-lookup"><span data-stu-id="6b58c-204">banking information</span></span>
- <span data-ttu-id="6b58c-205">
full names</span><span class="sxs-lookup"><span data-stu-id="6b58c-205">full names</span></span>
- <span data-ttu-id="6b58c-206">

iaea</span><span class="sxs-lookup"><span data-stu-id="6b58c-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="6b58c-207">Australische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-208">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-208">Format</span></span>

<span data-ttu-id="6b58c-209">Neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-210">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-210">Pattern</span></span>

<span data-ttu-id="6b58c-211">Neun Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="6b58c-212">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="6b58c-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-213">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-213">Two digits</span></span> 
- <span data-ttu-id="6b58c-214">Fünf Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="6b58c-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="6b58c-215">ODER</span><span class="sxs-lookup"><span data-stu-id="6b58c-215">OR</span></span>

- <span data-ttu-id="6b58c-216">1-2 optionale Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="6b58c-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-217">4 bis 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-217">4-9 digits</span></span>

<span data-ttu-id="6b58c-218">ODER</span><span class="sxs-lookup"><span data-stu-id="6b58c-218">OR</span></span>

- <span data-ttu-id="6b58c-219">Neun Ziffern oder Buchstaben (Groß-/Kleinschreibung irrelevant)</span><span class="sxs-lookup"><span data-stu-id="6b58c-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-220">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-220">Checksum</span></span>

<span data-ttu-id="6b58c-221">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-222">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-222">Definition</span></span>

<span data-ttu-id="6b58c-223">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-224">Der reguläre Ausdruck Regex_australia_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-225">Ein Schlüsselwort aus Keyword_australia_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="6b58c-226">Es wurde kein Schlüsselwort aus Keyword_australia_drivers_license_number_exclusions gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

```
<!-- Australia Drivers License Number -->
<Entity id="1cbbc8f5-9216-4392-9eb5-5ac2298d1356" patternsProximity="300" recommendedConfidence="75">
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_drivers_license_number" />
        <Match idRef="Keyword_australia_drivers_license_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_australia_drivers_license_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-227">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="6b58c-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="6b58c-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="6b58c-229">international driving permits</span></span>
- <span data-ttu-id="6b58c-230">
australian automobile association</span><span class="sxs-lookup"><span data-stu-id="6b58c-230">australian automobile association</span></span>
- <span data-ttu-id="6b58c-231">
sydney nsw</span><span class="sxs-lookup"><span data-stu-id="6b58c-231">sydney nsw</span></span>
- <span data-ttu-id="6b58c-232">
international driving permit</span><span class="sxs-lookup"><span data-stu-id="6b58c-232">international driving permit</span></span>
- <span data-ttu-id="6b58c-233">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="6b58c-233">DriverLicence</span></span>
- <span data-ttu-id="6b58c-234">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="6b58c-234">DriverLicences</span></span>
- <span data-ttu-id="6b58c-235">Treiber Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-235">Driver Lic</span></span>
- <span data-ttu-id="6b58c-236">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="6b58c-236">Driver Licence</span></span>
- <span data-ttu-id="6b58c-237">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="6b58c-237">Driver Licences</span></span>
- <span data-ttu-id="6b58c-238">DriversLic</span><span class="sxs-lookup"><span data-stu-id="6b58c-238">DriversLic</span></span>
- <span data-ttu-id="6b58c-239">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="6b58c-239">DriversLicence</span></span>
- <span data-ttu-id="6b58c-240">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="6b58c-240">DriversLicences</span></span>
- <span data-ttu-id="6b58c-241">Treiber Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-241">Drivers Lic</span></span>
- <span data-ttu-id="6b58c-242">Treiber Lics</span><span class="sxs-lookup"><span data-stu-id="6b58c-242">Drivers Lics</span></span>
- <span data-ttu-id="6b58c-243">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-243">Drivers Licence</span></span>
- <span data-ttu-id="6b58c-244">Treiber-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-244">Drivers Licences</span></span>
- <span data-ttu-id="6b58c-245">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-245">Driver'Lic</span></span>
- <span data-ttu-id="6b58c-246">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="6b58c-246">Driver'Lics</span></span>
- <span data-ttu-id="6b58c-247">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="6b58c-247">Driver'Licence</span></span>
- <span data-ttu-id="6b58c-248">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="6b58c-248">Driver'Licences</span></span>
- <span data-ttu-id="6b58c-249">Treiber ' Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-249">Driver' Lic</span></span>
- <span data-ttu-id="6b58c-250">Treiber ' Lics</span><span class="sxs-lookup"><span data-stu-id="6b58c-250">Driver' Lics</span></span>
- <span data-ttu-id="6b58c-251">Treiber ' Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-251">Driver' Licence</span></span>
- <span data-ttu-id="6b58c-252">Treiber ' Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-252">Driver' Licences</span></span>
- <span data-ttu-id="6b58c-253">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="6b58c-253">Driver'sLic</span></span>
- <span data-ttu-id="6b58c-254">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="6b58c-254">Driver'sLics</span></span>
- <span data-ttu-id="6b58c-255">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="6b58c-255">Driver'sLicence</span></span>
- <span data-ttu-id="6b58c-256">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="6b58c-256">Driver'sLicences</span></span>
- <span data-ttu-id="6b58c-257">Des Treibers Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-257">Driver's Lic</span></span>
- <span data-ttu-id="6b58c-258">Lics des Treibers</span><span class="sxs-lookup"><span data-stu-id="6b58c-258">Driver's Lics</span></span>
- <span data-ttu-id="6b58c-259">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="6b58c-259">Driver's Licence</span></span>
- <span data-ttu-id="6b58c-260">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="6b58c-260">Driver's Licences</span></span>
- <span data-ttu-id="6b58c-261">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-261">DriverLic#</span></span>
- <span data-ttu-id="6b58c-262">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-262">DriverLics#</span></span>
- <span data-ttu-id="6b58c-263">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="6b58c-263">DriverLicence#</span></span>
- <span data-ttu-id="6b58c-264">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="6b58c-264">DriverLicences#</span></span>
- <span data-ttu-id="6b58c-265">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="6b58c-265">Driver Lic#</span></span>
- <span data-ttu-id="6b58c-266">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-266">Driver Lics#</span></span>
- <span data-ttu-id="6b58c-267">Treiber Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-267">Driver Licence#</span></span>
- <span data-ttu-id="6b58c-268">Treiber Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-268">Driver Licences#</span></span>
- <span data-ttu-id="6b58c-269">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-269">DriversLic#</span></span>
- <span data-ttu-id="6b58c-270">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-270">DriversLics#</span></span>
- <span data-ttu-id="6b58c-271">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="6b58c-271">DriversLicence#</span></span>
- <span data-ttu-id="6b58c-272">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="6b58c-272">DriversLicences#</span></span>
- <span data-ttu-id="6b58c-273">Treiber Lic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-273">Drivers Lic#</span></span>
- <span data-ttu-id="6b58c-274">Treiber Lics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-274">Drivers Lics#</span></span>
- <span data-ttu-id="6b58c-275">Treiber Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-275">Drivers Licence#</span></span>
- <span data-ttu-id="6b58c-276">Treiber Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-276">Drivers Licences#</span></span>
- <span data-ttu-id="6b58c-277">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-277">Driver'Lic#</span></span>
- <span data-ttu-id="6b58c-278">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-278">Driver'Lics#</span></span>
- <span data-ttu-id="6b58c-279">Driver' Licence#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-279">Driver'Licence#</span></span>
- <span data-ttu-id="6b58c-280">Driver' Licences#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-280">Driver'Licences#</span></span>
- <span data-ttu-id="6b58c-281">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-281">Driver' Lic#</span></span>
- <span data-ttu-id="6b58c-282">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-282">Driver' Lics#</span></span>
- <span data-ttu-id="6b58c-283">Treiber '-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-283">Driver' Licence#</span></span>
- <span data-ttu-id="6b58c-284">Treiber ' Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-284">Driver' Licences#</span></span>
- <span data-ttu-id="6b58c-285">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-285">Driver'sLic#</span></span>
- <span data-ttu-id="6b58c-286">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-286">Driver'sLics#</span></span>
- <span data-ttu-id="6b58c-287">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="6b58c-287">Driver'sLicence#</span></span>
- <span data-ttu-id="6b58c-288">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="6b58c-288">Driver'sLicences#</span></span>
- <span data-ttu-id="6b58c-289">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-289">Driver's Lic#</span></span>
- <span data-ttu-id="6b58c-290">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-290">Driver's Lics#</span></span>
- <span data-ttu-id="6b58c-291">Des Treibers Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-291">Driver's Licence#</span></span>
- <span data-ttu-id="6b58c-292">Des Treibers Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-292">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="6b58c-293">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="6b58c-293">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="6b58c-294">aaa</span><span class="sxs-lookup"><span data-stu-id="6b58c-294">aaa</span></span>
- <span data-ttu-id="6b58c-295">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="6b58c-295">DriverLicense</span></span>
- <span data-ttu-id="6b58c-296">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-296">DriverLicenses</span></span>
- <span data-ttu-id="6b58c-297">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-297">Driver License</span></span>
- <span data-ttu-id="6b58c-298">Treiber-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-298">Driver Licenses</span></span>
- <span data-ttu-id="6b58c-299">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="6b58c-299">DriversLicense</span></span>
- <span data-ttu-id="6b58c-300">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-300">DriversLicenses</span></span>
- <span data-ttu-id="6b58c-301">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-301">Drivers License</span></span>
- <span data-ttu-id="6b58c-302">Treiber-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-302">Drivers Licenses</span></span>
- <span data-ttu-id="6b58c-303">Driver'License</span><span class="sxs-lookup"><span data-stu-id="6b58c-303">Driver'License</span></span>
- <span data-ttu-id="6b58c-304">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-304">Driver'Licenses</span></span>
- <span data-ttu-id="6b58c-305">Treiber ' Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-305">Driver' License</span></span>
- <span data-ttu-id="6b58c-306">Treiber ' Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-306">Driver' Licenses</span></span>
- <span data-ttu-id="6b58c-307">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="6b58c-307">Driver'sLicense</span></span>
- <span data-ttu-id="6b58c-308">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-308">Driver'sLicenses</span></span>
- <span data-ttu-id="6b58c-309">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-309">Driver's License</span></span>
- <span data-ttu-id="6b58c-310">Des Treibers Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-310">Driver's Licenses</span></span>
- <span data-ttu-id="6b58c-311">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="6b58c-311">DriverLicense#</span></span>
- <span data-ttu-id="6b58c-312">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="6b58c-312">DriverLicenses#</span></span>
- <span data-ttu-id="6b58c-313">Treiber Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-313">Driver License#</span></span>
- <span data-ttu-id="6b58c-314">Treiber Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-314">Driver Licenses#</span></span>
- <span data-ttu-id="6b58c-315">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="6b58c-315">DriversLicense#</span></span>
- <span data-ttu-id="6b58c-316">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="6b58c-316">DriversLicenses#</span></span>
- <span data-ttu-id="6b58c-317">Treiber Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-317">Drivers License#</span></span>
- <span data-ttu-id="6b58c-318">Treiber Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-318">Drivers Licenses#</span></span>
- <span data-ttu-id="6b58c-319">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-319">Driver'License#</span></span>
- <span data-ttu-id="6b58c-320">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-320">Driver'Licenses#</span></span>
- <span data-ttu-id="6b58c-321">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-321">Driver' License#</span></span>
- <span data-ttu-id="6b58c-322">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-322">Driver' Licenses#</span></span>
- <span data-ttu-id="6b58c-323">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="6b58c-323">Driver'sLicense#</span></span>
- <span data-ttu-id="6b58c-324">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="6b58c-324">Driver'sLicenses#</span></span>
- <span data-ttu-id="6b58c-325">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-325">Driver's License#</span></span>
- <span data-ttu-id="6b58c-326">

Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="6b58c-326">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="6b58c-327">Australische Medical Account-Nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-327">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-328">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-328">Format</span></span>

<span data-ttu-id="6b58c-329">10-11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-329">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-330">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-330">Pattern</span></span>

<span data-ttu-id="6b58c-331">10-11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-331">10-11 digits:</span></span>
- <span data-ttu-id="6b58c-332">Erste Ziffer im Bereich von 2-6</span><span class="sxs-lookup"><span data-stu-id="6b58c-332">First digit is in the range 2-6</span></span>
- <span data-ttu-id="6b58c-333">Neunte Ziffer ist eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-333">Ninth digit is a check digit</span></span>
- <span data-ttu-id="6b58c-334">Zehnte Ziffer ist die Ausgabeziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-334">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="6b58c-335">Elfte Ziffer (optional) ist die Einzelziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-335">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-336">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-336">Checksum</span></span>

<span data-ttu-id="6b58c-337">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-337">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-338">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-338">Definition</span></span>

<span data-ttu-id="6b58c-339">Eine DLP-Richtlinie ist zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-339">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-340">Die Funktion Func_australian_medical_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-340">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-341">Ein Schlüsselwort aus Keyword_Australia_Medical_Account_Number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-341">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="6b58c-342">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-342">The checksum passes.</span></span>

<span data-ttu-id="6b58c-343">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-343">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-344">Die Funktion Func_australian_medical_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-344">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-345">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-345">The checksum passes.</span></span>

```
  <!-- Australia Medical Account Number -->
<Entity id="104a99a0-3d3b-4542-a40d-ab0b9e1efe63" recommendedConfidence="85" patternsProximity="300">
    <Pattern confidenceLevel="95">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="1">
     <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
<Pattern confidenceLevel="85">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="0" maxMatches="0">
  <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-346">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-346">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="6b58c-347">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-347">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="6b58c-348">bank account details</span><span class="sxs-lookup"><span data-stu-id="6b58c-348">bank account details</span></span>
- <span data-ttu-id="6b58c-349">
medicare payments</span><span class="sxs-lookup"><span data-stu-id="6b58c-349">medicare payments</span></span>
- <span data-ttu-id="6b58c-350">
mortgage account</span><span class="sxs-lookup"><span data-stu-id="6b58c-350">mortgage account</span></span>
- <span data-ttu-id="6b58c-351">
bank payments</span><span class="sxs-lookup"><span data-stu-id="6b58c-351">bank payments</span></span>
- <span data-ttu-id="6b58c-352">
information branch</span><span class="sxs-lookup"><span data-stu-id="6b58c-352">information branch</span></span>
- <span data-ttu-id="6b58c-353">
credit card loan</span><span class="sxs-lookup"><span data-stu-id="6b58c-353">credit card loan</span></span>
- <span data-ttu-id="6b58c-354">
department of human services</span><span class="sxs-lookup"><span data-stu-id="6b58c-354">department of human services</span></span>
- <span data-ttu-id="6b58c-355">Lokaler Dienst</span><span class="sxs-lookup"><span data-stu-id="6b58c-355">local service</span></span>
- <span data-ttu-id="6b58c-356">

medicare</span><span class="sxs-lookup"><span data-stu-id="6b58c-356">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="6b58c-357">Australische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-357">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-358">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-358">Format</span></span>

<span data-ttu-id="6b58c-359">Ein Buchstabe gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-359">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-360">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-360">Pattern</span></span>

<span data-ttu-id="6b58c-361">Ein Buchstabe (Groß-/Kleinschreibung irrelevant) gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-361">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-362">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-362">Checksum</span></span>

<span data-ttu-id="6b58c-363">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-363">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-364">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-364">Definition</span></span>

<span data-ttu-id="6b58c-365">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-365">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-366">Der reguläre Ausdruck Regex_australia_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-366">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-367">Ein Schlüsselwort aus Keyword_passport oder Keyword_australia_passport_number gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="6b58c-367">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

```
<!-- Australia Passport Number -->
<Entity id="29869db6-602d-4853-ab93-3484f905df50" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_australia_passport_number" />
        </Any>
   </Pattern>
</Entity>   
```

### <a name="keywords"></a><span data-ttu-id="6b58c-368">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-368">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="6b58c-369">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-369">Keyword_passport</span></span>

- <span data-ttu-id="6b58c-370">Passport Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-370">Passport Number</span></span>
- <span data-ttu-id="6b58c-371">
Passport No</span><span class="sxs-lookup"><span data-stu-id="6b58c-371">Passport No</span></span>
- <span data-ttu-id="6b58c-372">Passport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-372">Passport #</span></span>
- <span data-ttu-id="6b58c-373">Passport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-373">Passport#</span></span>
- <span data-ttu-id="6b58c-374">PassportID</span><span class="sxs-lookup"><span data-stu-id="6b58c-374">PassportID</span></span>
- <span data-ttu-id="6b58c-375">Passportno
</span><span class="sxs-lookup"><span data-stu-id="6b58c-375">Passportno</span></span>
- <span data-ttu-id="6b58c-376">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-376">passportnumber</span></span>
- <span data-ttu-id="6b58c-377">パスポート</span><span class="sxs-lookup"><span data-stu-id="6b58c-377">パスポート</span></span>
- <span data-ttu-id="6b58c-378">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-378">パスポート番号</span></span>
- <span data-ttu-id="6b58c-379">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-379">パスポートのNum</span></span>
- <span data-ttu-id="6b58c-380">
パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="6b58c-380">パスポート ＃</span></span> 
- <span data-ttu-id="6b58c-381">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="6b58c-381">Numéro de passeport</span></span>
- <span data-ttu-id="6b58c-382">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="6b58c-382">Passeport n °</span></span>
- <span data-ttu-id="6b58c-383">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="6b58c-383">Passeport Non</span></span>
- <span data-ttu-id="6b58c-384">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-384">Passeport #</span></span>
- <span data-ttu-id="6b58c-385">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-385">Passeport#</span></span>
- <span data-ttu-id="6b58c-386">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="6b58c-386">PasseportNon</span></span>
- <span data-ttu-id="6b58c-387">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="6b58c-387">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="6b58c-388">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-388">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="6b58c-389">passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-389">passport</span></span>
- <span data-ttu-id="6b58c-390">
passport details</span><span class="sxs-lookup"><span data-stu-id="6b58c-390">passport details</span></span>
- <span data-ttu-id="6b58c-391">
immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="6b58c-391">immigration and citizenship</span></span>
- <span data-ttu-id="6b58c-392">
commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="6b58c-392">commonwealth of australia</span></span>
- <span data-ttu-id="6b58c-393">
department of immigration</span><span class="sxs-lookup"><span data-stu-id="6b58c-393">department of immigration</span></span>
- <span data-ttu-id="6b58c-394">
residential address</span><span class="sxs-lookup"><span data-stu-id="6b58c-394">residential address</span></span>
- <span data-ttu-id="6b58c-395">
department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="6b58c-395">department of immigration and citizenship</span></span>
- <span data-ttu-id="6b58c-396">visa
</span><span class="sxs-lookup"><span data-stu-id="6b58c-396">visa</span></span>
- <span data-ttu-id="6b58c-397">
national identity card</span><span class="sxs-lookup"><span data-stu-id="6b58c-397">national identity card</span></span>
- <span data-ttu-id="6b58c-398">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-398">passport number</span></span>
- <span data-ttu-id="6b58c-399">
travel document</span><span class="sxs-lookup"><span data-stu-id="6b58c-399">travel document</span></span>
- <span data-ttu-id="6b58c-400">

issuing authority</span><span class="sxs-lookup"><span data-stu-id="6b58c-400">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="6b58c-401">Australische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-401">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-402">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-402">Format</span></span>

<span data-ttu-id="6b58c-403">8-9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-403">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-404">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-404">Pattern</span></span>

<span data-ttu-id="6b58c-405">8 bis 9 Ziffern, die in der Regel wie folgt mit Leerzeichen dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="6b58c-405">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="6b58c-406">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-406">Three digits</span></span> 
- <span data-ttu-id="6b58c-407">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-407">An optional space</span></span> 
- <span data-ttu-id="6b58c-408">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-408">Three digits</span></span> 
- <span data-ttu-id="6b58c-409">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-409">An optional space</span></span> 
- <span data-ttu-id="6b58c-410">2 bis 3 Ziffern, wobei die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="6b58c-410">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-411">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-411">Checksum</span></span>

<span data-ttu-id="6b58c-412">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-412">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-413">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-413">Definition</span></span>

<span data-ttu-id="6b58c-414">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-415">Die Funktion Func_australian_tax_file_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-415">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-416">Es wurde kein Schlüsselwort aus Keyword_Australia_Tax_File_Number oder Keyword_number_exclusions gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-416">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="6b58c-417">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-417">The checksum passes.</span></span>

```
    <!-- Australia Tax File Number -->
<Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
    
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_Australia_Tax_File_Number" />
          <Match idRef="Keyword_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-418">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-418">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="6b58c-419">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-419">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="6b58c-420">australian business number</span><span class="sxs-lookup"><span data-stu-id="6b58c-420">australian business number</span></span>
- <span data-ttu-id="6b58c-421">
marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="6b58c-421">marginal tax rate</span></span>
- <span data-ttu-id="6b58c-422">
medicare levy</span><span class="sxs-lookup"><span data-stu-id="6b58c-422">medicare levy</span></span>
- <span data-ttu-id="6b58c-423">
portfolio number</span><span class="sxs-lookup"><span data-stu-id="6b58c-423">portfolio number</span></span>
- <span data-ttu-id="6b58c-424">
service veterans</span><span class="sxs-lookup"><span data-stu-id="6b58c-424">service veterans</span></span>
- <span data-ttu-id="6b58c-425">
withholding tax</span><span class="sxs-lookup"><span data-stu-id="6b58c-425">withholding tax</span></span>
- <span data-ttu-id="6b58c-426">
individual tax return</span><span class="sxs-lookup"><span data-stu-id="6b58c-426">individual tax return</span></span>
- <span data-ttu-id="6b58c-427">

tax file number</span><span class="sxs-lookup"><span data-stu-id="6b58c-427">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="6b58c-428">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="6b58c-428">Keyword_number_exclusions</span></span>

- <span data-ttu-id="6b58c-429">00000000</span><span class="sxs-lookup"><span data-stu-id="6b58c-429">00000000</span></span>
- <span data-ttu-id="6b58c-430">11111111</span><span class="sxs-lookup"><span data-stu-id="6b58c-430">11111111</span></span>
- <span data-ttu-id="6b58c-431">22222222</span><span class="sxs-lookup"><span data-stu-id="6b58c-431">22222222</span></span>
- <span data-ttu-id="6b58c-432">33333333</span><span class="sxs-lookup"><span data-stu-id="6b58c-432">33333333</span></span>
- <span data-ttu-id="6b58c-433">44444444</span><span class="sxs-lookup"><span data-stu-id="6b58c-433">44444444</span></span>
- <span data-ttu-id="6b58c-434">55555555</span><span class="sxs-lookup"><span data-stu-id="6b58c-434">55555555</span></span>
- <span data-ttu-id="6b58c-435">66666666</span><span class="sxs-lookup"><span data-stu-id="6b58c-435">66666666</span></span>
- <span data-ttu-id="6b58c-436">77777777</span><span class="sxs-lookup"><span data-stu-id="6b58c-436">77777777</span></span>
- <span data-ttu-id="6b58c-437">88888888</span><span class="sxs-lookup"><span data-stu-id="6b58c-437">88888888</span></span>
- <span data-ttu-id="6b58c-438">99999999 sein</span><span class="sxs-lookup"><span data-stu-id="6b58c-438">99999999</span></span>
- <span data-ttu-id="6b58c-439">000000000</span><span class="sxs-lookup"><span data-stu-id="6b58c-439">000000000</span></span>
- <span data-ttu-id="6b58c-440">111111111</span><span class="sxs-lookup"><span data-stu-id="6b58c-440">111111111</span></span>
- <span data-ttu-id="6b58c-441">222222222</span><span class="sxs-lookup"><span data-stu-id="6b58c-441">222222222</span></span>
- <span data-ttu-id="6b58c-442">333333333</span><span class="sxs-lookup"><span data-stu-id="6b58c-442">333333333</span></span>
- <span data-ttu-id="6b58c-443">444444444</span><span class="sxs-lookup"><span data-stu-id="6b58c-443">444444444</span></span>
- <span data-ttu-id="6b58c-444">555555555</span><span class="sxs-lookup"><span data-stu-id="6b58c-444">555555555</span></span>
- <span data-ttu-id="6b58c-445">666666666</span><span class="sxs-lookup"><span data-stu-id="6b58c-445">666666666</span></span>
- <span data-ttu-id="6b58c-446">777777777</span><span class="sxs-lookup"><span data-stu-id="6b58c-446">777777777</span></span>
- <span data-ttu-id="6b58c-447">888888888</span><span class="sxs-lookup"><span data-stu-id="6b58c-447">888888888</span></span>
- <span data-ttu-id="6b58c-448">999999999</span><span class="sxs-lookup"><span data-stu-id="6b58c-448">999999999</span></span>
- <span data-ttu-id="6b58c-449">0000000000</span><span class="sxs-lookup"><span data-stu-id="6b58c-449">0000000000</span></span>
- <span data-ttu-id="6b58c-450">1111111111</span><span class="sxs-lookup"><span data-stu-id="6b58c-450">1111111111</span></span>
- <span data-ttu-id="6b58c-451">2222222222</span><span class="sxs-lookup"><span data-stu-id="6b58c-451">2222222222</span></span>
- <span data-ttu-id="6b58c-452">3333333333</span><span class="sxs-lookup"><span data-stu-id="6b58c-452">3333333333</span></span>
- <span data-ttu-id="6b58c-453">4444444444</span><span class="sxs-lookup"><span data-stu-id="6b58c-453">4444444444</span></span>
- <span data-ttu-id="6b58c-454">5555555555</span><span class="sxs-lookup"><span data-stu-id="6b58c-454">5555555555</span></span>
- <span data-ttu-id="6b58c-455">6666666666</span><span class="sxs-lookup"><span data-stu-id="6b58c-455">6666666666</span></span>
- <span data-ttu-id="6b58c-456">7777777777</span><span class="sxs-lookup"><span data-stu-id="6b58c-456">7777777777</span></span>
- <span data-ttu-id="6b58c-457">8888888888</span><span class="sxs-lookup"><span data-stu-id="6b58c-457">8888888888</span></span>
- <span data-ttu-id="6b58c-458">9999999999</span><span class="sxs-lookup"><span data-stu-id="6b58c-458">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="6b58c-459">Belgien – Nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-459">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-460">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-460">Format</span></span>

<span data-ttu-id="6b58c-461">11 Ziffern plus Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-461">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-462">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-462">Pattern</span></span>

<span data-ttu-id="6b58c-463">11 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="6b58c-463">11 digits plus delimiters:</span></span>
- <span data-ttu-id="6b58c-464">Sechs Ziffern und zwei Punkte im Format JJ.MM.TT für das Geburtsdatum </span><span class="sxs-lookup"><span data-stu-id="6b58c-464">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="6b58c-465">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-465">A hyphen</span></span> 
- <span data-ttu-id="6b58c-466">Drei aufeinander folgende Ziffern (ungerade für Männer, gerade für Frauen) </span><span class="sxs-lookup"><span data-stu-id="6b58c-466">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="6b58c-467">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="6b58c-467">A period</span></span> 
- <span data-ttu-id="6b58c-468">Zwei Ziffern als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-468">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-469">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-469">Checksum</span></span>

<span data-ttu-id="6b58c-470">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-470">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-471">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-471">Definition</span></span>

<span data-ttu-id="6b58c-472">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-472">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-473">Die Funktion Func_belgium_national_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-473">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-474">Ein Schlüsselwort aus Keyword_belgium_national_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-474">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="6b58c-475">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-475">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-476">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-476">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="6b58c-477">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-477">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="6b58c-478">Identity</span><span class="sxs-lookup"><span data-stu-id="6b58c-478">Identity</span></span>
- <span data-ttu-id="6b58c-479">Registration</span><span class="sxs-lookup"><span data-stu-id="6b58c-479">Registration</span></span>
- <span data-ttu-id="6b58c-480">Identification</span><span class="sxs-lookup"><span data-stu-id="6b58c-480">Identification</span></span> 
- <span data-ttu-id="6b58c-481">ID</span><span class="sxs-lookup"><span data-stu-id="6b58c-481">ID</span></span> 
- <span data-ttu-id="6b58c-482">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="6b58c-482">Identiteitskaart</span></span>
- <span data-ttu-id="6b58c-483">Registratie nummer 
</span><span class="sxs-lookup"><span data-stu-id="6b58c-483">Registratie nummer</span></span> 
- <span data-ttu-id="6b58c-484">Identificatie nummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-484">Identificatie nummer</span></span> 
- <span data-ttu-id="6b58c-485">Identiteit</span><span class="sxs-lookup"><span data-stu-id="6b58c-485">Identiteit</span></span>
- <span data-ttu-id="6b58c-486">Registratie</span><span class="sxs-lookup"><span data-stu-id="6b58c-486">Registratie</span></span>
- <span data-ttu-id="6b58c-487">Identificatie

</span><span class="sxs-lookup"><span data-stu-id="6b58c-487">Identificatie</span></span> 
- <span data-ttu-id="6b58c-488">Carte d’identité
</span><span class="sxs-lookup"><span data-stu-id="6b58c-488">Carte d’identité</span></span> 
- <span data-ttu-id="6b58c-489">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="6b58c-489">numéro d'immatriculation</span></span>
- <span data-ttu-id="6b58c-490">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="6b58c-490">numéro d'identification</span></span>
- <span data-ttu-id="6b58c-491">
identité
</span><span class="sxs-lookup"><span data-stu-id="6b58c-491">identité</span></span> 
- <span data-ttu-id="6b58c-492">inscription
</span><span class="sxs-lookup"><span data-stu-id="6b58c-492">inscription</span></span> 
- <span data-ttu-id="6b58c-493">Identifikation</span><span class="sxs-lookup"><span data-stu-id="6b58c-493">Identifikation</span></span>
- <span data-ttu-id="6b58c-494">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="6b58c-494">Identifizierung</span></span>
- <span data-ttu-id="6b58c-495">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-495">Identifikationsnummer</span></span>
- <span data-ttu-id="6b58c-496">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-496">Personalausweis</span></span>
- <span data-ttu-id="6b58c-497">Registrierung</span><span class="sxs-lookup"><span data-stu-id="6b58c-497">Registrierung</span></span>
- <span data-ttu-id="6b58c-498">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-498">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="6b58c-499">Brazil CPF Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-499">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-500">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-500">Format</span></span>

<span data-ttu-id="6b58c-501">11 Ziffern, die eine Prüfziffer umfassen und die formatiert oder unformatiert sein können</span><span class="sxs-lookup"><span data-stu-id="6b58c-501">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-502">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-502">Pattern</span></span>

<span data-ttu-id="6b58c-503">Formatiert:</span><span class="sxs-lookup"><span data-stu-id="6b58c-503">Formatted:</span></span>
- <span data-ttu-id="6b58c-504">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-504">Three digits</span></span> 
- <span data-ttu-id="6b58c-505">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="6b58c-505">A period</span></span> 
- <span data-ttu-id="6b58c-506">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-506">Three digits</span></span> 
- <span data-ttu-id="6b58c-507">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="6b58c-507">A period</span></span> 
- <span data-ttu-id="6b58c-508">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-508">Three digits</span></span> 
- <span data-ttu-id="6b58c-509">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-509">A hyphen</span></span> 
- <span data-ttu-id="6b58c-510">Zwei Ziffern, die Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="6b58c-510">Two digits which are check digits</span></span>

<span data-ttu-id="6b58c-511">Unformatiert:</span><span class="sxs-lookup"><span data-stu-id="6b58c-511">Unformatted:</span></span>
- <span data-ttu-id="6b58c-512">11 Ziffern, wobei die letzten beiden Ziffern Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="6b58c-512">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-513">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-513">Checksum</span></span>

<span data-ttu-id="6b58c-514">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-514">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-515">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-515">Definition</span></span>

<span data-ttu-id="6b58c-516">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-516">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-517">Die Funktion Func_brazil_cpf findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-517">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-518">Ein Schlüsselwort aus Keyword_brazil_cpf wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-518">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="6b58c-519">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-519">The checksum passes.</span></span>

<span data-ttu-id="6b58c-520">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-520">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-521">Die Funktion Func_brazil_cpf findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-521">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-522">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-522">The checksum passes.</span></span>

```
<!-- Brazil CPF Number -->
<Entity id="78e09124-f2c3-4656-b32a-c1a132cd2711" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cpf"/>
     <Match idRef="Keyword_brazil_cpf"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cpf"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-523">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-523">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="6b58c-524">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="6b58c-524">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="6b58c-525">CPF</span><span class="sxs-lookup"><span data-stu-id="6b58c-525">CPF</span></span>
- <span data-ttu-id="6b58c-526">Identification</span><span class="sxs-lookup"><span data-stu-id="6b58c-526">Identification</span></span>
- <span data-ttu-id="6b58c-527">Registration</span><span class="sxs-lookup"><span data-stu-id="6b58c-527">Registration</span></span>
- <span data-ttu-id="6b58c-528">Revenue</span><span class="sxs-lookup"><span data-stu-id="6b58c-528">Revenue</span></span>
- <span data-ttu-id="6b58c-529">Cadastro de Pessoas Físicas
</span><span class="sxs-lookup"><span data-stu-id="6b58c-529">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="6b58c-530">Imposto
</span><span class="sxs-lookup"><span data-stu-id="6b58c-530">Imposto</span></span> 
- <span data-ttu-id="6b58c-531">Identificação
</span><span class="sxs-lookup"><span data-stu-id="6b58c-531">Identificação</span></span> 
- <span data-ttu-id="6b58c-532">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="6b58c-532">Inscrição</span></span> 
- <span data-ttu-id="6b58c-533">Receita

</span><span class="sxs-lookup"><span data-stu-id="6b58c-533">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="6b58c-534">Brasilien – Juristische Personennummer (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="6b58c-534">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-535">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-535">Format</span></span>

<span data-ttu-id="6b58c-536">14 Ziffern, die eine Registrierungsnummer, eine Zweignummer und Prüfnziffern sowie Trennzeichen umfassen</span><span class="sxs-lookup"><span data-stu-id="6b58c-536">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-537">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-537">Pattern</span></span>
<span data-ttu-id="6b58c-538">14 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="6b58c-538">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="6b58c-539">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-539">Two digits</span></span> 
- <span data-ttu-id="6b58c-540">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="6b58c-540">A period</span></span> 
- <span data-ttu-id="6b58c-541">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-541">Three digits</span></span> 
- <span data-ttu-id="6b58c-542">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="6b58c-542">A period</span></span> 
- <span data-ttu-id="6b58c-543">Drei Ziffern (diese ersten acht Ziffern sind die Registrierungsnummer) </span><span class="sxs-lookup"><span data-stu-id="6b58c-543">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="6b58c-544">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-544">A forward slash</span></span> 
- <span data-ttu-id="6b58c-545">Vierstellige Zweignummer </span><span class="sxs-lookup"><span data-stu-id="6b58c-545">Four-digit branch number</span></span> 
- <span data-ttu-id="6b58c-546">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-546">A hyphen</span></span> 
- <span data-ttu-id="6b58c-547">Zwei Ziffern, die Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="6b58c-547">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-548">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-548">Checksum</span></span>

<span data-ttu-id="6b58c-549">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-549">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-550">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-550">Definition</span></span>

<span data-ttu-id="6b58c-551">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-551">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-552">Die Funktion Func_brazil_cnpj findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-552">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-553">Ein Schlüsselwort aus Keyword_brazil_cnpj wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-553">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="6b58c-554">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-554">The checksum passes.</span></span>

<span data-ttu-id="6b58c-555">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-555">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-556">Die Funktion Func_brazil_cnpj findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-556">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-557">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-557">The checksum passes.</span></span>

```
<!-- Brazil Legal Entity Number (CNPJ) -->
<Entity id="9b58b5cd-5e90-4df6-b34f-1ebcc88ceae4" recommendedConfidence="85" patternsProximity="300">
   <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cnpj"/>
     <Match idRef="Keyword_brazil_cnpj"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cnpj"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-558">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-558">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="6b58c-559">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="6b58c-559">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="6b58c-560">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="6b58c-560">CNPJ</span></span> 
- <span data-ttu-id="6b58c-561">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="6b58c-561">CNPJ/MF</span></span> 
- <span data-ttu-id="6b58c-562">CNPJ-MF
</span><span class="sxs-lookup"><span data-stu-id="6b58c-562">CNPJ-MF</span></span> 
- <span data-ttu-id="6b58c-563">National Registry of Legal Entities
</span><span class="sxs-lookup"><span data-stu-id="6b58c-563">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="6b58c-564">Taxpayers Registry
</span><span class="sxs-lookup"><span data-stu-id="6b58c-564">Taxpayers Registry</span></span> 
- <span data-ttu-id="6b58c-565">Legal entity
</span><span class="sxs-lookup"><span data-stu-id="6b58c-565">Legal entity</span></span> 
- <span data-ttu-id="6b58c-566">Legal entities
</span><span class="sxs-lookup"><span data-stu-id="6b58c-566">Legal entities</span></span> 
- <span data-ttu-id="6b58c-567">Registration Status
</span><span class="sxs-lookup"><span data-stu-id="6b58c-567">Registration Status</span></span> 
- <span data-ttu-id="6b58c-568">Business
</span><span class="sxs-lookup"><span data-stu-id="6b58c-568">Business</span></span> 
- <span data-ttu-id="6b58c-569">Company</span><span class="sxs-lookup"><span data-stu-id="6b58c-569">Company</span></span>
- <span data-ttu-id="6b58c-570">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="6b58c-570">CNPJ</span></span> 
- <span data-ttu-id="6b58c-571">Cadastro Nacional da Pessoa Jurídica
</span><span class="sxs-lookup"><span data-stu-id="6b58c-571">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="6b58c-572">Cadastro Geral de Contribuintes
</span><span class="sxs-lookup"><span data-stu-id="6b58c-572">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="6b58c-573">CGC
</span><span class="sxs-lookup"><span data-stu-id="6b58c-573">CGC</span></span> 
- <span data-ttu-id="6b58c-574">Pessoa jurídica
</span><span class="sxs-lookup"><span data-stu-id="6b58c-574">Pessoa jurídica</span></span> 
- <span data-ttu-id="6b58c-575">Pessoas jurídicas
</span><span class="sxs-lookup"><span data-stu-id="6b58c-575">Pessoas jurídicas</span></span> 
- <span data-ttu-id="6b58c-576">Situação cadastral
</span><span class="sxs-lookup"><span data-stu-id="6b58c-576">Situação cadastral</span></span> 
- <span data-ttu-id="6b58c-577">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="6b58c-577">Inscrição</span></span> 
- <span data-ttu-id="6b58c-578">Empresa
</span><span class="sxs-lookup"><span data-stu-id="6b58c-578">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="6b58c-579">	Brasilien – Personalausweis (RG)</span><span class="sxs-lookup"><span data-stu-id="6b58c-579">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-580">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-580">Format</span></span>

<span data-ttu-id="6b58c-581">Registro Geral (altes Format): neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-581">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="6b58c-582">Registro de Identidade (RIC) (neue-Format): 11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-582">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-583">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-583">Pattern</span></span>

<span data-ttu-id="6b58c-584">Registro Geral (altes Format):</span><span class="sxs-lookup"><span data-stu-id="6b58c-584">Registro Geral (old format):</span></span>
- <span data-ttu-id="6b58c-585">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-585">Two digits</span></span> 
- <span data-ttu-id="6b58c-586">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="6b58c-586">A period</span></span> 
- <span data-ttu-id="6b58c-587">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-587">Three digits</span></span> 
- <span data-ttu-id="6b58c-588">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="6b58c-588">A period</span></span> 
- <span data-ttu-id="6b58c-589">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-589">Three digits</span></span> 
- <span data-ttu-id="6b58c-590">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-590">A hyphen</span></span> 
- <span data-ttu-id="6b58c-591">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-591">One digit which is a check digit</span></span>

<span data-ttu-id="6b58c-592">Registro de Identidade (RIC) (neue-Format):</span><span class="sxs-lookup"><span data-stu-id="6b58c-592">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="6b58c-593">10 Ziffern </span><span class="sxs-lookup"><span data-stu-id="6b58c-593">10 digits</span></span> 
- <span data-ttu-id="6b58c-594">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-594">A hyphen</span></span> 
- <span data-ttu-id="6b58c-595">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-595">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-596">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-596">Checksum</span></span>

<span data-ttu-id="6b58c-597">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-597">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-598">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-598">Definition</span></span>

<span data-ttu-id="6b58c-599">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-599">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-600">Die Funktion Func_brazil_rg findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-600">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-601">Ein Schlüsselwort aus Keyword_brazil_rg wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-601">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="6b58c-602">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-602">The checksum passes.</span></span>

<span data-ttu-id="6b58c-603">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-603">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-604">Die Funktion Func_brazil_rg findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-604">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-605">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-605">The checksum passes.</span></span>

```
<!-- Brazil National ID Card (RG) -->
<Entity id="486de900-db70-41b3-a886-abdf25af119c" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_rg"/>
     <Match idRef="Keyword_brazil_rg"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_rg"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-606">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-606">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="6b58c-607">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="6b58c-607">Keyword_brazil_rg</span></span>

<span data-ttu-id="6b58c-608">Cédula de Identidade Personalausweis Personalausweis Número de Rregistro Registro de Iidentidade Registro Geral RG (dieses Schlüsselwort ist Groß-/Kleinschreibung beachten) RIC (dieses Schlüsselwort ist Groß-/Kleinschreibung beachten)</span><span class="sxs-lookup"><span data-stu-id="6b58c-608">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="6b58c-609">Kanadische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-609">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-610">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-610">Format</span></span>

<span data-ttu-id="6b58c-611">Sieben oder zwölf Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-611">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-612">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-612">Pattern</span></span>

<span data-ttu-id="6b58c-613">Eine kanadische Kontonummer umfasst sieben oder zwölf Ziffern.</span><span class="sxs-lookup"><span data-stu-id="6b58c-613">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="6b58c-614">Eine kanadische Bankkontonummer setzt sich wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="6b58c-614">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="6b58c-615">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-615">Five digits</span></span> 
- <span data-ttu-id="6b58c-616">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-616">A hyphen</span></span> 
- <span data-ttu-id="6b58c-617">Drei Ziffern oder</span><span class="sxs-lookup"><span data-stu-id="6b58c-617">Three digits OR</span></span>
- <span data-ttu-id="6b58c-618">Eine 0 (null) </span><span class="sxs-lookup"><span data-stu-id="6b58c-618">A zero "0"</span></span> 
- <span data-ttu-id="6b58c-619">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-619">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-620">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-620">Checksum</span></span>

<span data-ttu-id="6b58c-621">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-621">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-622">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-622">Definition</span></span>

<span data-ttu-id="6b58c-623">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-623">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-624">Der reguläre Ausdruck Regex_canada_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-624">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-625">Ein Schlüsselwort aus Keyword_canada_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-625">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="6b58c-626">Der reguläre Ausdruck Regex_canada_bank_account_transit_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-626">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="6b58c-627">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-627">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-628">Der reguläre Ausdruck Regex_canada_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-628">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-629">Ein Schlüsselwort aus Keyword_canada_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-629">A keyword from Keyword_canada_bank_account_number is found.</span></span>

```
<!-- Canada Bank Account Number -->
<Entity id="552e814c-cb50-4d94-bbaa-bb1d1ffb34de" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
        <Match idRef="Regex_canada_bank_account_transit_number" />
   </Pattern>
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-630">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-630">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="6b58c-631">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-631">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="6b58c-632">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="6b58c-632">canada savings bonds</span></span>
- <span data-ttu-id="6b58c-633">
canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="6b58c-633">canada revenue agency</span></span>
- <span data-ttu-id="6b58c-634">
canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="6b58c-634">canadian financial institution</span></span>
- <span data-ttu-id="6b58c-635">
direct deposit form</span><span class="sxs-lookup"><span data-stu-id="6b58c-635">direct deposit form</span></span>
- <span data-ttu-id="6b58c-636">
canadian citizen</span><span class="sxs-lookup"><span data-stu-id="6b58c-636">canadian citizen</span></span>
- <span data-ttu-id="6b58c-637">
legal representative</span><span class="sxs-lookup"><span data-stu-id="6b58c-637">legal representative</span></span>
- <span data-ttu-id="6b58c-638">
notary public</span><span class="sxs-lookup"><span data-stu-id="6b58c-638">notary public</span></span>
- <span data-ttu-id="6b58c-639">
commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="6b58c-639">commissioner for oaths</span></span>
- <span data-ttu-id="6b58c-640">
child care benefit</span><span class="sxs-lookup"><span data-stu-id="6b58c-640">child care benefit</span></span>
- <span data-ttu-id="6b58c-641">
universal child care</span><span class="sxs-lookup"><span data-stu-id="6b58c-641">universal child care</span></span>
- <span data-ttu-id="6b58c-642">
canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="6b58c-642">canada child tax benefit</span></span>
- <span data-ttu-id="6b58c-643">
income tax benefit</span><span class="sxs-lookup"><span data-stu-id="6b58c-643">income tax benefit</span></span>
- <span data-ttu-id="6b58c-644">
harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="6b58c-644">harmonized sales tax</span></span>
- <span data-ttu-id="6b58c-645">social insurance number</span><span class="sxs-lookup"><span data-stu-id="6b58c-645">social insurance number</span></span>
- <span data-ttu-id="6b58c-646">
income tax refund</span><span class="sxs-lookup"><span data-stu-id="6b58c-646">income tax refund</span></span>
- <span data-ttu-id="6b58c-647">
child tax benefit</span><span class="sxs-lookup"><span data-stu-id="6b58c-647">child tax benefit</span></span>
- <span data-ttu-id="6b58c-648">
territorial payments</span><span class="sxs-lookup"><span data-stu-id="6b58c-648">territorial payments</span></span>
- <span data-ttu-id="6b58c-649">
institution number</span><span class="sxs-lookup"><span data-stu-id="6b58c-649">institution number</span></span>
- <span data-ttu-id="6b58c-650">
deposit request</span><span class="sxs-lookup"><span data-stu-id="6b58c-650">deposit request</span></span>
- <span data-ttu-id="6b58c-651">
banking information</span><span class="sxs-lookup"><span data-stu-id="6b58c-651">banking information</span></span>
- <span data-ttu-id="6b58c-652">

direct deposit</span><span class="sxs-lookup"><span data-stu-id="6b58c-652">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="6b58c-653">Kanadische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-653">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-654">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-654">Format</span></span>

<span data-ttu-id="6b58c-655">Variiert je nach Provinz</span><span class="sxs-lookup"><span data-stu-id="6b58c-655">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-656">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-656">Pattern</span></span>

<span data-ttu-id="6b58c-657">Verschiedene Muster in Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec und Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="6b58c-657">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-658">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-658">Checksum</span></span>

<span data-ttu-id="6b58c-659">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-659">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-660">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-660">Definition</span></span>

<span data-ttu-id="6b58c-661">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-661">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-662">Die Funktion Func_[province_name]_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-662">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-663">Ein Schlüsselwort aus Keyword_[province_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-663">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="6b58c-664">Ein Schlüsselwort aus Keyword_canada_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-664">A keyword from Keyword_canada_drivers_license is found.</span></span>

```
<!-- Canada Driver's License Number -->
    <Entity id="37186abb-8e48-4800-ad3c-e3d1610b3db0" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_alberta_drivers_license_number" />
        <Match idRef="Keyword_alberta_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_british_columbia_drivers_license_number" />
        <Match idRef="Keyword_british_columbia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_manitoba_drivers_license_number" />
        <Match idRef="Keyword_manitoba_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_brunswick_drivers_license_number" />
        <Match idRef="Keyword_new_brunswick_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_newfoundland_labrador_drivers_license_number" />
        <Match idRef="Keyword_newfoundland_labrador_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_nova_scotia_drivers_license_number" />
        <Match idRef="Keyword_nova_scotia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_ontario_drivers_license_number" />
        <Match idRef="Keyword_ontario_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_prince_edward_island_drivers_license_number" />
        <Match idRef="Keyword_prince_edward_island_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_quebec_drivers_license_number" />
        <Match idRef="Keyword_quebec_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_saskatchewan_drivers_license_number" />
        <Match idRef="Keyword_saskatchewan_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-665">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-665">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="6b58c-666">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="6b58c-666">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="6b58c-667">Die Abkürzung für die Provinz, z. B. AB</span><span class="sxs-lookup"><span data-stu-id="6b58c-667">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="6b58c-668">
Der Name der Provinz, beispielsweise „Alberta“</span><span class="sxs-lookup"><span data-stu-id="6b58c-668">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="6b58c-669">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="6b58c-669">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="6b58c-670">DL</span><span class="sxs-lookup"><span data-stu-id="6b58c-670">DL</span></span>
- <span data-ttu-id="6b58c-671">DLS</span><span class="sxs-lookup"><span data-stu-id="6b58c-671">DLS</span></span>
- <span data-ttu-id="6b58c-672">CDL</span><span class="sxs-lookup"><span data-stu-id="6b58c-672">CDL</span></span>
- <span data-ttu-id="6b58c-673">CDLS</span><span class="sxs-lookup"><span data-stu-id="6b58c-673">CDLS</span></span>
- <span data-ttu-id="6b58c-674">DriverLic</span><span class="sxs-lookup"><span data-stu-id="6b58c-674">DriverLic</span></span>
- <span data-ttu-id="6b58c-675">DriverLics</span><span class="sxs-lookup"><span data-stu-id="6b58c-675">DriverLics</span></span>
- <span data-ttu-id="6b58c-676">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="6b58c-676">DriverLicense</span></span>
- <span data-ttu-id="6b58c-677">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-677">DriverLicenses</span></span>
- <span data-ttu-id="6b58c-678">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="6b58c-678">DriverLicence</span></span>
- <span data-ttu-id="6b58c-679">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="6b58c-679">DriverLicences</span></span>
- <span data-ttu-id="6b58c-680">Treiber Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-680">Driver Lic</span></span>
- <span data-ttu-id="6b58c-681">Treiber Lics</span><span class="sxs-lookup"><span data-stu-id="6b58c-681">Driver Lics</span></span>
- <span data-ttu-id="6b58c-682">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-682">Driver License</span></span>
- <span data-ttu-id="6b58c-683">Treiber-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-683">Driver Licenses</span></span>
- <span data-ttu-id="6b58c-684">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="6b58c-684">Driver Licence</span></span>
- <span data-ttu-id="6b58c-685">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="6b58c-685">Driver Licences</span></span>
- <span data-ttu-id="6b58c-686">DriversLic</span><span class="sxs-lookup"><span data-stu-id="6b58c-686">DriversLic</span></span>
- <span data-ttu-id="6b58c-687">DriversLics</span><span class="sxs-lookup"><span data-stu-id="6b58c-687">DriversLics</span></span>
- <span data-ttu-id="6b58c-688">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="6b58c-688">DriversLicence</span></span>
- <span data-ttu-id="6b58c-689">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="6b58c-689">DriversLicences</span></span>
- <span data-ttu-id="6b58c-690">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="6b58c-690">DriversLicense</span></span>
- <span data-ttu-id="6b58c-691">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-691">DriversLicenses</span></span>
- <span data-ttu-id="6b58c-692">Treiber Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-692">Drivers Lic</span></span>
- <span data-ttu-id="6b58c-693">Treiber Lics</span><span class="sxs-lookup"><span data-stu-id="6b58c-693">Drivers Lics</span></span>
- <span data-ttu-id="6b58c-694">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-694">Drivers License</span></span>
- <span data-ttu-id="6b58c-695">Treiber-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-695">Drivers Licenses</span></span>
- <span data-ttu-id="6b58c-696">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-696">Drivers Licence</span></span>
- <span data-ttu-id="6b58c-697">Treiber-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-697">Drivers Licences</span></span>
- <span data-ttu-id="6b58c-698">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-698">Driver'Lic</span></span>
- <span data-ttu-id="6b58c-699">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="6b58c-699">Driver'Lics</span></span>
- <span data-ttu-id="6b58c-700">Driver'License</span><span class="sxs-lookup"><span data-stu-id="6b58c-700">Driver'License</span></span>
- <span data-ttu-id="6b58c-701">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-701">Driver'Licenses</span></span>
- <span data-ttu-id="6b58c-702">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="6b58c-702">Driver'Licence</span></span>
- <span data-ttu-id="6b58c-703">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="6b58c-703">Driver'Licences</span></span>
- <span data-ttu-id="6b58c-704">Treiber ' Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-704">Driver' Lic</span></span>
- <span data-ttu-id="6b58c-705">Treiber ' Lics</span><span class="sxs-lookup"><span data-stu-id="6b58c-705">Driver' Lics</span></span>
- <span data-ttu-id="6b58c-706">Treiber ' Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-706">Driver' License</span></span>
- <span data-ttu-id="6b58c-707">Treiber ' Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-707">Driver' Licenses</span></span>
- <span data-ttu-id="6b58c-708">Treiber ' Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-708">Driver' Licence</span></span>
- <span data-ttu-id="6b58c-709">Treiber ' Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-709">Driver' Licences</span></span>
- <span data-ttu-id="6b58c-710">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="6b58c-710">Driver'sLic</span></span>
- <span data-ttu-id="6b58c-711">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="6b58c-711">Driver'sLics</span></span>
- <span data-ttu-id="6b58c-712">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="6b58c-712">Driver'sLicense</span></span>
- <span data-ttu-id="6b58c-713">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-713">Driver'sLicenses</span></span>
- <span data-ttu-id="6b58c-714">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="6b58c-714">Driver'sLicence</span></span>
- <span data-ttu-id="6b58c-715">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="6b58c-715">Driver'sLicences</span></span>
- <span data-ttu-id="6b58c-716">Des Treibers Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-716">Driver's Lic</span></span>
- <span data-ttu-id="6b58c-717">Lics des Treibers</span><span class="sxs-lookup"><span data-stu-id="6b58c-717">Driver's Lics</span></span>
- <span data-ttu-id="6b58c-718">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-718">Driver's License</span></span>
- <span data-ttu-id="6b58c-719">Des Treibers Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-719">Driver's Licenses</span></span>
- <span data-ttu-id="6b58c-720">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="6b58c-720">Driver's Licence</span></span>
- <span data-ttu-id="6b58c-721">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="6b58c-721">Driver's Licences</span></span>
- <span data-ttu-id="6b58c-722">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="6b58c-722">Permis de Conduire</span></span>
- <span data-ttu-id="6b58c-723">id</span><span class="sxs-lookup"><span data-stu-id="6b58c-723">id</span></span>
- <span data-ttu-id="6b58c-724">IDs</span><span class="sxs-lookup"><span data-stu-id="6b58c-724">ids</span></span>
- <span data-ttu-id="6b58c-725">
idcard number</span><span class="sxs-lookup"><span data-stu-id="6b58c-725">idcard number</span></span>
- <span data-ttu-id="6b58c-726">
idcard numbers</span><span class="sxs-lookup"><span data-stu-id="6b58c-726">idcard numbers</span></span>
- <span data-ttu-id="6b58c-727">
idcard #</span><span class="sxs-lookup"><span data-stu-id="6b58c-727">idcard #</span></span>
- <span data-ttu-id="6b58c-728">
idcard #s</span><span class="sxs-lookup"><span data-stu-id="6b58c-728">idcard #s</span></span>
- <span data-ttu-id="6b58c-729">Idcard Karte</span><span class="sxs-lookup"><span data-stu-id="6b58c-729">idcard card</span></span>
- <span data-ttu-id="6b58c-730">Idcard Karten</span><span class="sxs-lookup"><span data-stu-id="6b58c-730">idcard cards</span></span>
- <span data-ttu-id="6b58c-731">idcard</span><span class="sxs-lookup"><span data-stu-id="6b58c-731">idcard</span></span>
- <span data-ttu-id="6b58c-732">identification number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-732">identification number</span></span>
- <span data-ttu-id="6b58c-733">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="6b58c-733">identification numbers</span></span>
- <span data-ttu-id="6b58c-734">identification#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-734">identification #</span></span>
- <span data-ttu-id="6b58c-735">
identification #s</span><span class="sxs-lookup"><span data-stu-id="6b58c-735">identification #s</span></span>
- <span data-ttu-id="6b58c-736">Ausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-736">identification card</span></span>
- <span data-ttu-id="6b58c-737">Kennung Visitenkarten (engl.)</span><span class="sxs-lookup"><span data-stu-id="6b58c-737">identification cards</span></span>
- <span data-ttu-id="6b58c-738">
identification
</span><span class="sxs-lookup"><span data-stu-id="6b58c-738">identification</span></span> 
- <span data-ttu-id="6b58c-739">DL#</span><span class="sxs-lookup"><span data-stu-id="6b58c-739">DL#</span></span>
- <span data-ttu-id="6b58c-740">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-740">DLS#</span></span> 
- <span data-ttu-id="6b58c-741">CDL#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-741">CDL#</span></span> 
- <span data-ttu-id="6b58c-742">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-742">CDLS#</span></span> 
- <span data-ttu-id="6b58c-743">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-743">DriverLic#</span></span> 
- <span data-ttu-id="6b58c-744">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-744">DriverLics#</span></span> 
- <span data-ttu-id="6b58c-745">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="6b58c-745">DriverLicense#</span></span> 
- <span data-ttu-id="6b58c-746">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="6b58c-746">DriverLicenses#</span></span> 
- <span data-ttu-id="6b58c-747">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="6b58c-747">DriverLicence#</span></span> 
- <span data-ttu-id="6b58c-748">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="6b58c-748">DriverLicences#</span></span> 
- <span data-ttu-id="6b58c-749">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="6b58c-749">Driver Lic#</span></span>
- <span data-ttu-id="6b58c-750">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-750">Driver Lics#</span></span> 
- <span data-ttu-id="6b58c-751">Treiber Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-751">Driver License#</span></span> 
- <span data-ttu-id="6b58c-752">Treiber Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-752">Driver Licenses#</span></span> 
- <span data-ttu-id="6b58c-753">Treiber Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-753">Driver License#</span></span> 
- <span data-ttu-id="6b58c-754">Treiber Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-754">Driver Licences#</span></span> 
- <span data-ttu-id="6b58c-755">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-755">DriversLic#</span></span> 
- <span data-ttu-id="6b58c-756">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-756">DriversLics#</span></span> 
- <span data-ttu-id="6b58c-757">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="6b58c-757">DriversLicense#</span></span> 
- <span data-ttu-id="6b58c-758">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="6b58c-758">DriversLicenses#</span></span> 
- <span data-ttu-id="6b58c-759">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="6b58c-759">DriversLicence#</span></span> 
- <span data-ttu-id="6b58c-760">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="6b58c-760">DriversLicences#</span></span> 
- <span data-ttu-id="6b58c-761">Treiber Lic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-761">Drivers Lic#</span></span> 
- <span data-ttu-id="6b58c-762">Treiber Lics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-762">Drivers Lics#</span></span> 
- <span data-ttu-id="6b58c-763">Treiber Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-763">Drivers License#</span></span> 
- <span data-ttu-id="6b58c-764">Treiber Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-764">Drivers Licenses#</span></span> 
- <span data-ttu-id="6b58c-765">Treiber Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-765">Drivers Licence#</span></span> 
- <span data-ttu-id="6b58c-766">Treiber Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-766">Drivers Licences#</span></span> 
- <span data-ttu-id="6b58c-767">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-767">Driver'Lic#</span></span> 
- <span data-ttu-id="6b58c-768">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-768">Driver'Lics#</span></span> 
- <span data-ttu-id="6b58c-769">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-769">Driver'License#</span></span> 
- <span data-ttu-id="6b58c-770">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-770">Driver'Licenses#</span></span> 
- <span data-ttu-id="6b58c-771">Driver' Licence#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-771">Driver'Licence#</span></span> 
- <span data-ttu-id="6b58c-772">Driver' Licences#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-772">Driver'Licences#</span></span> 
- <span data-ttu-id="6b58c-773">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-773">Driver' Lic#</span></span> 
- <span data-ttu-id="6b58c-774">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-774">Driver' Lics#</span></span> 
- <span data-ttu-id="6b58c-775">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-775">Driver' License#</span></span> 
- <span data-ttu-id="6b58c-776">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-776">Driver' Licenses#</span></span> 
- <span data-ttu-id="6b58c-777">Treiber '-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-777">Driver' Licence#</span></span> 
- <span data-ttu-id="6b58c-778">Treiber ' Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-778">Driver' Licences#</span></span> 
- <span data-ttu-id="6b58c-779">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-779">Driver'sLic#</span></span> 
- <span data-ttu-id="6b58c-780">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-780">Driver'sLics#</span></span> 
- <span data-ttu-id="6b58c-781">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="6b58c-781">Driver'sLicense#</span></span> 
- <span data-ttu-id="6b58c-782">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="6b58c-782">Driver'sLicenses#</span></span> 
- <span data-ttu-id="6b58c-783">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="6b58c-783">Driver'sLicence#</span></span> 
- <span data-ttu-id="6b58c-784">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="6b58c-784">Driver'sLicences#</span></span> 
- <span data-ttu-id="6b58c-785">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-785">Driver's Lic#</span></span> 
- <span data-ttu-id="6b58c-786">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-786">Driver's Lics#</span></span> 
- <span data-ttu-id="6b58c-787">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-787">Driver's License#</span></span> 
- <span data-ttu-id="6b58c-788">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-788">Driver's Licenses#</span></span> 
- <span data-ttu-id="6b58c-789">Des Treibers Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-789">Driver's Licence#</span></span> 
- <span data-ttu-id="6b58c-790">Des Treibers Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-790">Driver's Licences#</span></span> 
- <span data-ttu-id="6b58c-791">Permis de Conduire #</span><span class="sxs-lookup"><span data-stu-id="6b58c-791">Permis de Conduire#</span></span> 
- <span data-ttu-id="6b58c-792">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-792">id#</span></span> 
- <span data-ttu-id="6b58c-793">-IDs</span><span class="sxs-lookup"><span data-stu-id="6b58c-793">ids#</span></span> 
- <span data-ttu-id="6b58c-794">idcard card#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-794">idcard card#</span></span> 
- <span data-ttu-id="6b58c-795">idcard cards#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-795">idcard cards#</span></span> 
- <span data-ttu-id="6b58c-796">idcard#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-796">idcard#</span></span> 
- <span data-ttu-id="6b58c-797">identification card#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-797">identification card#</span></span> 
- <span data-ttu-id="6b58c-798">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-798">identification cards#</span></span> 
- <span data-ttu-id="6b58c-799">identification#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-799">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="6b58c-800">Kanadische Health Service-Nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-800">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-801">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-801">Format</span></span>

<span data-ttu-id="6b58c-802">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-802">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-803">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-803">Pattern</span></span>

<span data-ttu-id="6b58c-804">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-804">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-805">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-805">Checksum</span></span>

<span data-ttu-id="6b58c-806">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-806">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-807">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-807">Definition</span></span>

<span data-ttu-id="6b58c-808">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-808">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-809">Der reguläre Ausdruck Regex_canada_health_service_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-809">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-810">Ein Schlüsselwort aus Keyword_canada_health_service_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-810">A keyword from Keyword_canada_health_service_number is found.</span></span>

```
<!-- Canada Health Service Number -->
<Entity id="59c0bf39-7fab-482c-af25-00faa4384c94" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_health_service_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_health_service_number" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-811">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-811">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="6b58c-812">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-812">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="6b58c-813">personal health number</span><span class="sxs-lookup"><span data-stu-id="6b58c-813">personal health number</span></span>
- <span data-ttu-id="6b58c-814">
patient information</span><span class="sxs-lookup"><span data-stu-id="6b58c-814">patient information</span></span>
- <span data-ttu-id="6b58c-815">
health services</span><span class="sxs-lookup"><span data-stu-id="6b58c-815">health services</span></span>
- <span data-ttu-id="6b58c-816">
speciality services</span><span class="sxs-lookup"><span data-stu-id="6b58c-816">speciality services</span></span>
- <span data-ttu-id="6b58c-817">
automobile accident</span><span class="sxs-lookup"><span data-stu-id="6b58c-817">automobile accident</span></span>
- <span data-ttu-id="6b58c-818">
patient hospital</span><span class="sxs-lookup"><span data-stu-id="6b58c-818">patient hospital</span></span>
- <span data-ttu-id="6b58c-819">
psychiatrist</span><span class="sxs-lookup"><span data-stu-id="6b58c-819">psychiatrist</span></span>
- <span data-ttu-id="6b58c-820">
workers compensation</span><span class="sxs-lookup"><span data-stu-id="6b58c-820">workers compensation</span></span>
- <span data-ttu-id="6b58c-821">
disability</span><span class="sxs-lookup"><span data-stu-id="6b58c-821">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="6b58c-822">Kanadische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-822">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-823">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-823">Format</span></span>

<span data-ttu-id="6b58c-824">Zwei Großbuchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-824">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-825">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-825">Pattern</span></span>

<span data-ttu-id="6b58c-826">Zwei Großbuchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-826">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-827">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-827">Checksum</span></span>

<span data-ttu-id="6b58c-828">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-828">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-829">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-829">Definition</span></span>

<span data-ttu-id="6b58c-830">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-830">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-831">Der reguläre Ausdruck Regex_canada_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-831">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-832">Ein Schlüsselwort aus Keyword_canada_passport_number oder Keyword_passport gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="6b58c-832">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

``` 
<!-- Canada Passport Number -->
<Entity id="14d0db8b-498a-43ed-9fca-f6097ae687eb" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_passport_number" />
          <Match idRef="Keyword_passport" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-833">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-833">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="6b58c-834">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-834">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="6b58c-835">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="6b58c-835">canadian citizenship</span></span>
- <span data-ttu-id="6b58c-836">
canadian passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-836">canadian passport</span></span>
- <span data-ttu-id="6b58c-837">
passport application</span><span class="sxs-lookup"><span data-stu-id="6b58c-837">passport application</span></span>
- <span data-ttu-id="6b58c-838">
passport photos</span><span class="sxs-lookup"><span data-stu-id="6b58c-838">passport photos</span></span>
- <span data-ttu-id="6b58c-839">
certified translator</span><span class="sxs-lookup"><span data-stu-id="6b58c-839">certified translator</span></span>
- <span data-ttu-id="6b58c-840">
canadian citizens</span><span class="sxs-lookup"><span data-stu-id="6b58c-840">canadian citizens</span></span>
- <span data-ttu-id="6b58c-841">
processing times</span><span class="sxs-lookup"><span data-stu-id="6b58c-841">processing times</span></span>
- <span data-ttu-id="6b58c-842">

renewal application</span><span class="sxs-lookup"><span data-stu-id="6b58c-842">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="6b58c-843">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-843">Keyword_passport</span></span>

- <span data-ttu-id="6b58c-844">Passport Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-844">Passport Number</span></span>
- <span data-ttu-id="6b58c-845">
Passport No</span><span class="sxs-lookup"><span data-stu-id="6b58c-845">Passport No</span></span>
- <span data-ttu-id="6b58c-846">Passport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-846">Passport #</span></span>
- <span data-ttu-id="6b58c-847">Passport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-847">Passport#</span></span>
- <span data-ttu-id="6b58c-848">PassportID</span><span class="sxs-lookup"><span data-stu-id="6b58c-848">PassportID</span></span>
- <span data-ttu-id="6b58c-849">Passportno
</span><span class="sxs-lookup"><span data-stu-id="6b58c-849">Passportno</span></span>
- <span data-ttu-id="6b58c-850">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-850">passportnumber</span></span>
- <span data-ttu-id="6b58c-851">パスポート</span><span class="sxs-lookup"><span data-stu-id="6b58c-851">パスポート</span></span>
- <span data-ttu-id="6b58c-852">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-852">パスポート番号</span></span>
- <span data-ttu-id="6b58c-853">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-853">パスポートのNum</span></span>
- <span data-ttu-id="6b58c-854">パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="6b58c-854">パスポート＃</span></span>
- <span data-ttu-id="6b58c-855">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="6b58c-855">Numéro de passeport</span></span>
- <span data-ttu-id="6b58c-856">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="6b58c-856">Passeport n °</span></span>
- <span data-ttu-id="6b58c-857">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="6b58c-857">Passeport Non</span></span>
- <span data-ttu-id="6b58c-858">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-858">Passeport #</span></span>
- <span data-ttu-id="6b58c-859">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-859">Passeport#</span></span>
- <span data-ttu-id="6b58c-860">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="6b58c-860">PasseportNon</span></span>
- <span data-ttu-id="6b58c-861">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="6b58c-861">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="6b58c-862">Kanadische Personal Health Identification-Nummer (PHIN)</span><span class="sxs-lookup"><span data-stu-id="6b58c-862">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-863">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-863">Format</span></span>

<span data-ttu-id="6b58c-864">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-864">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-865">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-865">Pattern</span></span>

<span data-ttu-id="6b58c-866">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-866">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-867">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-867">Checksum</span></span>

<span data-ttu-id="6b58c-868">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-868">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-869">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-869">Definition</span></span>

<span data-ttu-id="6b58c-p104">Eine DLP-Richtlinie ist 75 % sicher, dass diese Art von vertraulichen Informationen festgestellt wurde "If"; innerhalb einer Nähe von 300 Zeichen: der reguläre Ausdruck Regex_canada_phin sucht nach Inhalten, die dem Muster entspricht. Mindestens zwei Schlüsselwörter aus Keyword_canada_phin oder Keyword_canada_provinces gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-p104">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern. At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

```
<!-- Canada PHIN -->
<Entity id="722e12ac-c89a-4ec8-a1b7-fea3469f89db" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_phin" />
        <Any minMatches="2">
          <Match idRef="Keyword_canada_phin" />
          <Match idRef="Keyword_canada_provinces" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-872">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-872">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="6b58c-873">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="6b58c-873">Keyword_canada_phin</span></span>

- <span data-ttu-id="6b58c-874">social insurance number</span><span class="sxs-lookup"><span data-stu-id="6b58c-874">social insurance number</span></span>
- <span data-ttu-id="6b58c-875">
health information act</span><span class="sxs-lookup"><span data-stu-id="6b58c-875">health information act</span></span>
- <span data-ttu-id="6b58c-876">
income tax information</span><span class="sxs-lookup"><span data-stu-id="6b58c-876">income tax information</span></span>
- <span data-ttu-id="6b58c-877">
manitoba health</span><span class="sxs-lookup"><span data-stu-id="6b58c-877">manitoba health</span></span>
- <span data-ttu-id="6b58c-878">
health registration</span><span class="sxs-lookup"><span data-stu-id="6b58c-878">health registration</span></span>
- <span data-ttu-id="6b58c-879">
prescription purchases</span><span class="sxs-lookup"><span data-stu-id="6b58c-879">prescription purchases</span></span>
- <span data-ttu-id="6b58c-880">
benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="6b58c-880">benefit eligibility</span></span>
- <span data-ttu-id="6b58c-881">
personal health</span><span class="sxs-lookup"><span data-stu-id="6b58c-881">personal health</span></span>
- <span data-ttu-id="6b58c-882">
power of attorney</span><span class="sxs-lookup"><span data-stu-id="6b58c-882">power of attorney</span></span>
- <span data-ttu-id="6b58c-883">
registration number</span><span class="sxs-lookup"><span data-stu-id="6b58c-883">registration number</span></span>
- <span data-ttu-id="6b58c-884">personal health number</span><span class="sxs-lookup"><span data-stu-id="6b58c-884">personal health number</span></span>
- <span data-ttu-id="6b58c-885">
practitioner referral</span><span class="sxs-lookup"><span data-stu-id="6b58c-885">practitioner referral</span></span>
- <span data-ttu-id="6b58c-886">
wellness professional</span><span class="sxs-lookup"><span data-stu-id="6b58c-886">wellness professional</span></span>
- <span data-ttu-id="6b58c-887">
patient referral</span><span class="sxs-lookup"><span data-stu-id="6b58c-887">patient referral</span></span>
- <span data-ttu-id="6b58c-888">

health and wellness</span><span class="sxs-lookup"><span data-stu-id="6b58c-888">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="6b58c-889">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="6b58c-889">Keyword_canada_provinces</span></span>

- <span data-ttu-id="6b58c-890">Nunavut</span><span class="sxs-lookup"><span data-stu-id="6b58c-890">Nunavut</span></span>
- <span data-ttu-id="6b58c-891">
Quebec</span><span class="sxs-lookup"><span data-stu-id="6b58c-891">Quebec</span></span>
- <span data-ttu-id="6b58c-892">
Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="6b58c-892">Northwest Territories</span></span>
- <span data-ttu-id="6b58c-893">
Ontario</span><span class="sxs-lookup"><span data-stu-id="6b58c-893">Ontario</span></span>
- <span data-ttu-id="6b58c-894">
British Columbia</span><span class="sxs-lookup"><span data-stu-id="6b58c-894">British Columbia</span></span>
- <span data-ttu-id="6b58c-895">
Alberta</span><span class="sxs-lookup"><span data-stu-id="6b58c-895">Alberta</span></span>
- <span data-ttu-id="6b58c-896">
Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="6b58c-896">Saskatchewan</span></span>
- <span data-ttu-id="6b58c-897">
Manitoba</span><span class="sxs-lookup"><span data-stu-id="6b58c-897">Manitoba</span></span>
- <span data-ttu-id="6b58c-898">
Yukon</span><span class="sxs-lookup"><span data-stu-id="6b58c-898">Yukon</span></span>
- <span data-ttu-id="6b58c-899">
Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="6b58c-899">Newfoundland and Labrador</span></span>
- <span data-ttu-id="6b58c-900">
New Brunswick</span><span class="sxs-lookup"><span data-stu-id="6b58c-900">New Brunswick</span></span>
- <span data-ttu-id="6b58c-901">
Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="6b58c-901">Nova Scotia</span></span>
- <span data-ttu-id="6b58c-902">
Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="6b58c-902">Prince Edward Island</span></span>
- <span data-ttu-id="6b58c-903">Kanada</span><span class="sxs-lookup"><span data-stu-id="6b58c-903">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="6b58c-904">Kanadische Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-904">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-905">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-905">Format</span></span>

<span data-ttu-id="6b58c-906">Neun Ziffern mit optionalen Bindestrichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-906">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-907">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-907">Pattern</span></span>

<span data-ttu-id="6b58c-908">Formatiert:</span><span class="sxs-lookup"><span data-stu-id="6b58c-908">Formatted:</span></span>
- <span data-ttu-id="6b58c-909">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-909">Three digits</span></span> 
- <span data-ttu-id="6b58c-910">Ein Bindestrich oder ein Leerzeichen </span><span class="sxs-lookup"><span data-stu-id="6b58c-910">A hyphen or space</span></span> 
- <span data-ttu-id="6b58c-911">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-911">Three digits</span></span> 
- <span data-ttu-id="6b58c-912">Ein Bindestrich oder ein Leerzeichen </span><span class="sxs-lookup"><span data-stu-id="6b58c-912">A hyphen or space</span></span> 
- <span data-ttu-id="6b58c-913">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-913">Three digits</span></span>

<span data-ttu-id="6b58c-914">Unformatiert: Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-914">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-915">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-915">Checksum</span></span>

<span data-ttu-id="6b58c-916">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-916">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-917">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-917">Definition</span></span>

<span data-ttu-id="6b58c-918">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-918">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-919">Die Funktion Func_canadian_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-919">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-920">Mindestens zwei dieser eine beliebige Kombination der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="6b58c-920">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="6b58c-921">Ein Schlüsselwort aus Keyword_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-921">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="6b58c-922">Ein Schlüsselwort aus Keyword_sin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-922">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="6b58c-923">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="6b58c-923">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="6b58c-924">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-924">The checksum passes.</span></span>

<span data-ttu-id="6b58c-925">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-925">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-926">Die Funktion Func_unformatted_canadian_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-926">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-927">Ein Schlüsselwort aus Keyword_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-927">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="6b58c-928">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-928">The checksum passes.</span></span>

```
<!-- Canada Social Insurance Number -->
<Entity id="a2f29c85-ecb8-4514-a610-364790c0773e" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_canadian_sin" />
        <Any minMatches="2">
          <Match idRef="Keyword_sin" />
          <Match idRef="Keyword_sin_collaborative" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_canadian_sin" />
        <Match idRef="Keyword_sin" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-929">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-929">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="6b58c-930">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="6b58c-930">Keyword_sin</span></span>

- <span data-ttu-id="6b58c-931">sin</span><span class="sxs-lookup"><span data-stu-id="6b58c-931">sin</span></span> 
- <span data-ttu-id="6b58c-932">social insurance
</span><span class="sxs-lookup"><span data-stu-id="6b58c-932">social insurance</span></span> 
- <span data-ttu-id="6b58c-933">numero d'assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="6b58c-933">numero d'assurance sociale</span></span> 
- <span data-ttu-id="6b58c-934">sins
</span><span class="sxs-lookup"><span data-stu-id="6b58c-934">sins</span></span> 
- <span data-ttu-id="6b58c-935">ssn</span><span class="sxs-lookup"><span data-stu-id="6b58c-935">ssn</span></span> 
- <span data-ttu-id="6b58c-936">ssns</span><span class="sxs-lookup"><span data-stu-id="6b58c-936">ssns</span></span> 
- <span data-ttu-id="6b58c-937">soziale Sicherheit</span><span class="sxs-lookup"><span data-stu-id="6b58c-937">social security</span></span> 
- <span data-ttu-id="6b58c-938">numero d'assurance social
</span><span class="sxs-lookup"><span data-stu-id="6b58c-938">numero d'assurance social</span></span> 
- <span data-ttu-id="6b58c-939">National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-939">national identification number</span></span> 
- <span data-ttu-id="6b58c-940">
national id</span><span class="sxs-lookup"><span data-stu-id="6b58c-940">national id</span></span> 
- <span data-ttu-id="6b58c-941">sin#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-941">sin#</span></span> 
- <span data-ttu-id="6b58c-942">soc ins
</span><span class="sxs-lookup"><span data-stu-id="6b58c-942">soc ins</span></span> 
- <span data-ttu-id="6b58c-943">social ins
</span><span class="sxs-lookup"><span data-stu-id="6b58c-943">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="6b58c-944">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="6b58c-944">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="6b58c-945">driver's license</span><span class="sxs-lookup"><span data-stu-id="6b58c-945">driver's license</span></span> 
- <span data-ttu-id="6b58c-946">drivers license</span><span class="sxs-lookup"><span data-stu-id="6b58c-946">drivers license</span></span> 
- <span data-ttu-id="6b58c-947">des Treibers-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-947">driver's licence</span></span> 
- <span data-ttu-id="6b58c-948">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6b58c-948">drivers licence</span></span> 
- <span data-ttu-id="6b58c-949">DOB
</span><span class="sxs-lookup"><span data-stu-id="6b58c-949">DOB</span></span> 
- <span data-ttu-id="6b58c-950">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="6b58c-950">Birthdate</span></span> 
- <span data-ttu-id="6b58c-951">Geburtstag </span><span class="sxs-lookup"><span data-stu-id="6b58c-951">Birthday</span></span> 
- <span data-ttu-id="6b58c-952">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="6b58c-952">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="6b58c-953">	Chile Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-953">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-954">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-954">Format</span></span>

<span data-ttu-id="6b58c-955">7 und 8 Ziffern plus Trennzeichen ein Kontrollkästchen Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="6b58c-955">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-956">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-956">Pattern</span></span>

<span data-ttu-id="6b58c-957">7-8 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="6b58c-957">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="6b58c-958">1-2 Ziffern </span><span class="sxs-lookup"><span data-stu-id="6b58c-958">1-2 digits</span></span> 
- <span data-ttu-id="6b58c-959">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="6b58c-959">A period</span></span> 
- <span data-ttu-id="6b58c-960">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-960">Three digits</span></span> 
- <span data-ttu-id="6b58c-961">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="6b58c-961">A period</span></span> 
- <span data-ttu-id="6b58c-962">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-962">Three digits</span></span> 
- <span data-ttu-id="6b58c-963">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-963">A dash</span></span> 
- <span data-ttu-id="6b58c-964">Eine Ziffer oder ein Buchstabe (Groß-/Kleinschreibung nicht unterschieden), die bzw. der eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="6b58c-964">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-965">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-965">Checksum</span></span>

<span data-ttu-id="6b58c-966">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-967">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-967">Definition</span></span>

<span data-ttu-id="6b58c-968">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-969">Die Funktion Func_chile_id_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-969">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-970">Ein Schlüsselwort aus Keyword_chile_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-970">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="6b58c-971">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-971">The checksum passes.</span></span>

<span data-ttu-id="6b58c-972">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-972">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-973">Die Funktion Func_chile_id_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-973">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-974">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-974">The checksum passes.</span></span>

```
<!-- Chile Identity Card Number -->
<Entity id="4e979794-49a0-407e-a0b9-2c536937b925" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_chile_id_card"/>
     <Match idRef="Keyword_chile_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_chile_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-975">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-975">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="6b58c-976">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="6b58c-976">Keyword_chile_id_card</span></span>

- <span data-ttu-id="6b58c-977">National Identification Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-977">National Identification Number</span></span> 
- <span data-ttu-id="6b58c-978">Identity card</span><span class="sxs-lookup"><span data-stu-id="6b58c-978">Identity card</span></span> 
- <span data-ttu-id="6b58c-979">ID</span><span class="sxs-lookup"><span data-stu-id="6b58c-979">ID</span></span> 
- <span data-ttu-id="6b58c-980">Identification</span><span class="sxs-lookup"><span data-stu-id="6b58c-980">Identification</span></span> 
- <span data-ttu-id="6b58c-981">Rol Único Nacional
</span><span class="sxs-lookup"><span data-stu-id="6b58c-981">Rol Único Nacional</span></span> 
- <span data-ttu-id="6b58c-982">AUSFÜHREN</span><span class="sxs-lookup"><span data-stu-id="6b58c-982">RUN</span></span> 
- <span data-ttu-id="6b58c-983">Rol Único Tributario
</span><span class="sxs-lookup"><span data-stu-id="6b58c-983">Rol Único Tributario</span></span> 
- <span data-ttu-id="6b58c-984">RUT
</span><span class="sxs-lookup"><span data-stu-id="6b58c-984">RUT</span></span> 
- <span data-ttu-id="6b58c-985">Cédula de Identidad
</span><span class="sxs-lookup"><span data-stu-id="6b58c-985">Cédula de Identidad</span></span> 
- <span data-ttu-id="6b58c-986">Número De Identificación Nacional
</span><span class="sxs-lookup"><span data-stu-id="6b58c-986">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="6b58c-987">Tarjeta de identificación
</span><span class="sxs-lookup"><span data-stu-id="6b58c-987">Tarjeta de identificación</span></span> 
- <span data-ttu-id="6b58c-988">Identificación
</span><span class="sxs-lookup"><span data-stu-id="6b58c-988">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="6b58c-989">	China (PRC) – Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-989">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-990">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-990">Format</span></span>

<span data-ttu-id="6b58c-991">18 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-991">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-992">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-992">Pattern</span></span>

<span data-ttu-id="6b58c-993">18 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-993">18 digits:</span></span>
- <span data-ttu-id="6b58c-994">Sechs Ziffern, die einen Adresscode angeben </span><span class="sxs-lookup"><span data-stu-id="6b58c-994">Six digits which are an address code</span></span> 
- <span data-ttu-id="6b58c-995">Acht Ziffern im Fomat JJJJMMTT, wobei es sich um das Geburtsdatum handelt </span><span class="sxs-lookup"><span data-stu-id="6b58c-995">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="6b58c-996">Drei Ziffern, die ein Reihenfolgencode sind </span><span class="sxs-lookup"><span data-stu-id="6b58c-996">Three digits which are an order code</span></span> 
- <span data-ttu-id="6b58c-997">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-997">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-998">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-998">Checksum</span></span>

<span data-ttu-id="6b58c-999">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-999">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1000">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1000">Definition</span></span>

<span data-ttu-id="6b58c-1001">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1001">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1002">Die Funktion Func_china_resident_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1002">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1003">Ein Schlüsselwort aus Keyword_china_resident_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1003">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="6b58c-1004">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1004">The checksum passes.</span></span>

<span data-ttu-id="6b58c-1005">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1005">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1006">Die Funktion Func_china_resident_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1006">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1007">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1007">The checksum passes.</span></span>

```
<!-- China Resident Identity Card (PRC) Number -->
<Entity id="c92daa86-2d16-4871-901f-816b3f554fc1" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_china_resident_id"/>
     <Match idRef="Keyword_china_resident_id"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_china_resident_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1008">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1008">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="6b58c-1009">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="6b58c-1009">Keyword_china_resident_id</span></span>

- <span data-ttu-id="6b58c-1010">Resident Identity Card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1010">Resident Identity Card</span></span> 
- <span data-ttu-id="6b58c-1011">PRC
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1011">PRC</span></span> 
- <span data-ttu-id="6b58c-1012">National Identification Card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1012">National Identification Card</span></span> 
- <span data-ttu-id="6b58c-1013">身份证 </span><span class="sxs-lookup"><span data-stu-id="6b58c-1013">身份证</span></span> 
- <span data-ttu-id="6b58c-1014">居民 身份证 </span><span class="sxs-lookup"><span data-stu-id="6b58c-1014">居民 身份证</span></span> 
- <span data-ttu-id="6b58c-1015">居民身份证
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1015">居民身份证</span></span> 
- <span data-ttu-id="6b58c-1016">鉴定

</span><span class="sxs-lookup"><span data-stu-id="6b58c-1016">鉴定</span></span> 
- <span data-ttu-id="6b58c-1017">身分證 </span><span class="sxs-lookup"><span data-stu-id="6b58c-1017">身分證</span></span> 
- <span data-ttu-id="6b58c-1018">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="6b58c-1018">居民 身份證</span></span>
- <span data-ttu-id="6b58c-1019">鑑定 </span><span class="sxs-lookup"><span data-stu-id="6b58c-1019">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="6b58c-1020">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1020">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1021">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1021">Format</span></span>

<span data-ttu-id="6b58c-1022">16 Stellen die formatiert werden können oder unformatierte (Dddddddddddddddd), und geben Sie den Test mit Luhn müssen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1022">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1023">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1023">Pattern</span></span>

<span data-ttu-id="6b58c-1024">Sehr komplexe und robuste Muster, die Karten aller wichtigen Marken weltweit, einschließlich Visa, MasterCard, Discover-Karte, JCB, American Express, Geschenkgutscheine und Restaurantkarten erkennen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1024">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1025">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1025">Checksum</span></span>

<span data-ttu-id="6b58c-1026">Ja, die Luhn-Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1026">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1027">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1027">Definition</span></span>

<span data-ttu-id="6b58c-1028">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1028">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1029">Die Funktion Func_credit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1029">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1030">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1030">One of the following is true:</span></span>
    - <span data-ttu-id="6b58c-1031">Ein Schlüsselwort aus Keyword_cc_verification wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1031">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="6b58c-1032">Ein Schlüsselwort aus Keyword_cc_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1032">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="6b58c-1033">Die Funktion Func_expiration_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1033">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="6b58c-1034">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1034">The checksum passes.</span></span>

<span data-ttu-id="6b58c-1035">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1035">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1036">Die Funktion Func_credit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1036">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1037">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1037">The checksum passes.</span></span>

```
<!-- Credit Card Number -->
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_credit_card" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1038">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1038">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="6b58c-1039">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="6b58c-1039">Keyword_cc_verification</span></span>

- <span data-ttu-id="6b58c-1040">card verification</span><span class="sxs-lookup"><span data-stu-id="6b58c-1040">card verification</span></span>
- <span data-ttu-id="6b58c-1041">card identification number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1041">card identification number</span></span>
- <span data-ttu-id="6b58c-1042">cvn
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1042">cvn</span></span>
- <span data-ttu-id="6b58c-1043">cid
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1043">cid</span></span>
- <span data-ttu-id="6b58c-1044">CVC2</span><span class="sxs-lookup"><span data-stu-id="6b58c-1044">cvc2</span></span>
- <span data-ttu-id="6b58c-1045">CVV2</span><span class="sxs-lookup"><span data-stu-id="6b58c-1045">cvv2</span></span>
- <span data-ttu-id="6b58c-1046">pin block
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1046">pin block</span></span>
- <span data-ttu-id="6b58c-1047">security code
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1047">security code</span></span>
- <span data-ttu-id="6b58c-1048">security number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1048">security number</span></span>
- <span data-ttu-id="6b58c-1049">security no
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1049">security no</span></span>
- <span data-ttu-id="6b58c-1050">issue number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1050">issue number</span></span>
- <span data-ttu-id="6b58c-1051">issue no
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1051">issue no</span></span>
- <span data-ttu-id="6b58c-1052">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1052">cryptogramme</span></span>
- <span data-ttu-id="6b58c-1053">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1053">numéro de sécurité</span></span>
- <span data-ttu-id="6b58c-1054">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1054">numero de securite</span></span>
- <span data-ttu-id="6b58c-1055">Kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1055">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="6b58c-1056">Kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1056">kreditkartenprufnummer</span></span>
- <span data-ttu-id="6b58c-1057">Prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1057">prüfziffer</span></span>
- <span data-ttu-id="6b58c-1058">Prufziffer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1058">prufziffer</span></span>
- <span data-ttu-id="6b58c-1059">Sicherheits-Kode</span><span class="sxs-lookup"><span data-stu-id="6b58c-1059">sicherheits Kode</span></span>
- <span data-ttu-id="6b58c-1060">Sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1060">sicherheitscode</span></span>
- <span data-ttu-id="6b58c-1061">Sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1061">sicherheitsnummer</span></span>
- <span data-ttu-id="6b58c-1062">Verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1062">verfalldatum</span></span>
- <span data-ttu-id="6b58c-1063">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1063">codice di verifica</span></span>
- <span data-ttu-id="6b58c-p105">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p105">cod. sicurezza</span></span>
- <span data-ttu-id="6b58c-1066">COD sicurezza</span><span class="sxs-lookup"><span data-stu-id="6b58c-1066">cod sicurezza</span></span>
- <span data-ttu-id="6b58c-1067">
n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="6b58c-1067">n autorizzazione</span></span>
- <span data-ttu-id="6b58c-1068">código
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1068">código</span></span>
- <span data-ttu-id="6b58c-1069">codigo
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1069">codigo</span></span>
- <span data-ttu-id="6b58c-p106">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p106">cod. seg</span></span>
- <span data-ttu-id="6b58c-1072">COD seg</span><span class="sxs-lookup"><span data-stu-id="6b58c-1072">cod seg</span></span>
- <span data-ttu-id="6b58c-1073">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1073">código de segurança</span></span>
- <span data-ttu-id="6b58c-1074">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1074">codigo de seguranca</span></span>
- <span data-ttu-id="6b58c-1075">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1075">codigo de segurança</span></span>
- <span data-ttu-id="6b58c-1076">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1076">código de seguranca</span></span>
- <span data-ttu-id="6b58c-p107">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p107">cód. segurança</span></span>
- <span data-ttu-id="6b58c-p108">COD. Seguranca Cod. segurança</span><span class="sxs-lookup"><span data-stu-id="6b58c-p108">cod. seguranca cod. segurança</span></span>
- <span data-ttu-id="6b58c-p109">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p109">cód. seguranca</span></span>
- <span data-ttu-id="6b58c-1084">Cód segurança</span><span class="sxs-lookup"><span data-stu-id="6b58c-1084">cód segurança</span></span>
- <span data-ttu-id="6b58c-1085">Kabeljau Seguranca Cod segurança</span><span class="sxs-lookup"><span data-stu-id="6b58c-1085">cod seguranca cod segurança</span></span>
- <span data-ttu-id="6b58c-1086">Cód seguranca</span><span class="sxs-lookup"><span data-stu-id="6b58c-1086">cód seguranca</span></span>
- <span data-ttu-id="6b58c-1087">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1087">número de verificação</span></span>
- <span data-ttu-id="6b58c-1088">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1088">numero de verificacao</span></span>
- <span data-ttu-id="6b58c-1089">Ablauf
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1089">ablauf</span></span>
- <span data-ttu-id="6b58c-1090">Gültig bis
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1090">gültig bis</span></span>
- <span data-ttu-id="6b58c-1091">Gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1091">gültigkeitsdatum</span></span>
- <span data-ttu-id="6b58c-1092">Gultig bis
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1092">gultig bis</span></span>
- <span data-ttu-id="6b58c-1093">Gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1093">gultigkeitsdatum</span></span>
- <span data-ttu-id="6b58c-1094">scadenza
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1094">scadenza</span></span>
- <span data-ttu-id="6b58c-1095">data scad
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1095">data scad</span></span>
- <span data-ttu-id="6b58c-1096">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1096">fecha de expiracion</span></span>
- <span data-ttu-id="6b58c-1097">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1097">fecha de venc</span></span>
- <span data-ttu-id="6b58c-1098">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1098">vencimiento</span></span>
- <span data-ttu-id="6b58c-1099">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1099">válido hasta</span></span>
- <span data-ttu-id="6b58c-1100">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1100">valido hasta</span></span>
- <span data-ttu-id="6b58c-1101">vto
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1101">vto</span></span>
- <span data-ttu-id="6b58c-1102">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1102">data de expiração</span></span>
- <span data-ttu-id="6b58c-1103">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1103">data de expiracao</span></span>
- <span data-ttu-id="6b58c-1104">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1104">data em que expira</span></span>
- <span data-ttu-id="6b58c-1105">validade
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1105">validade</span></span>
- <span data-ttu-id="6b58c-1106">valor
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1106">valor</span></span>
- <span data-ttu-id="6b58c-1107">vencimento
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1107">vencimento</span></span>
- <span data-ttu-id="6b58c-1108">Venc</span><span class="sxs-lookup"><span data-stu-id="6b58c-1108">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="6b58c-1109">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="6b58c-1109">Keyword_cc_name</span></span>

- <span data-ttu-id="6b58c-1110">amex</span><span class="sxs-lookup"><span data-stu-id="6b58c-1110">amex</span></span>
- <span data-ttu-id="6b58c-1111">
american express</span><span class="sxs-lookup"><span data-stu-id="6b58c-1111">american express</span></span>
- <span data-ttu-id="6b58c-1112">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1112">americanexpress</span></span>
- <span data-ttu-id="6b58c-1113">Visa</span><span class="sxs-lookup"><span data-stu-id="6b58c-1113">Visa</span></span>
- <span data-ttu-id="6b58c-1114">mastercard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1114">mastercard</span></span>
- <span data-ttu-id="6b58c-1115">master card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1115">master card</span></span>
- <span data-ttu-id="6b58c-1116">
mc
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1116">mc</span></span> 
- <span data-ttu-id="6b58c-1117">mastercards</span><span class="sxs-lookup"><span data-stu-id="6b58c-1117">mastercards</span></span>
- <span data-ttu-id="6b58c-1118">
master cards</span><span class="sxs-lookup"><span data-stu-id="6b58c-1118">master cards</span></span>
- <span data-ttu-id="6b58c-1119">die Bestellung Club</span><span class="sxs-lookup"><span data-stu-id="6b58c-1119">diner's Club</span></span>
- <span data-ttu-id="6b58c-1120">diners club
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1120">diners club</span></span>
- <span data-ttu-id="6b58c-1121">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1121">dinersclub</span></span>
- <span data-ttu-id="6b58c-1122">discover card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1122">discover card</span></span>
- <span data-ttu-id="6b58c-1123">discovercard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1123">discovercard</span></span>
- <span data-ttu-id="6b58c-1124">discover cards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1124">discover cards</span></span>
- <span data-ttu-id="6b58c-1125">JCB</span><span class="sxs-lookup"><span data-stu-id="6b58c-1125">JCB</span></span>
- <span data-ttu-id="6b58c-1126">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1126">japanese card bureau</span></span>
- <span data-ttu-id="6b58c-1127">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1127">carte blanche</span></span>
- <span data-ttu-id="6b58c-1128">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1128">carteblanche</span></span>
- <span data-ttu-id="6b58c-1129">credit card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1129">credit card</span></span>
- <span data-ttu-id="6b58c-1130">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1130">cc#</span></span>
- <span data-ttu-id="6b58c-1131">cc:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1131">cc#:</span></span>
- <span data-ttu-id="6b58c-1132">
expiration date</span><span class="sxs-lookup"><span data-stu-id="6b58c-1132">expiration date</span></span>
- <span data-ttu-id="6b58c-1133">exp date
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1133">exp date</span></span>
- <span data-ttu-id="6b58c-1134">
expiry date</span><span class="sxs-lookup"><span data-stu-id="6b58c-1134">expiry date</span></span>
- <span data-ttu-id="6b58c-1135">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="6b58c-1135">date d’expiration</span></span>
- <span data-ttu-id="6b58c-1136">
date d'exp</span><span class="sxs-lookup"><span data-stu-id="6b58c-1136">date d'exp</span></span>
- <span data-ttu-id="6b58c-1137">
date expiration</span><span class="sxs-lookup"><span data-stu-id="6b58c-1137">date expiration</span></span>
- <span data-ttu-id="6b58c-1138">bank card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1138">bank card</span></span>
- <span data-ttu-id="6b58c-1139">
bankcard</span><span class="sxs-lookup"><span data-stu-id="6b58c-1139">bankcard</span></span>
- <span data-ttu-id="6b58c-1140">card number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1140">card number</span></span>
- <span data-ttu-id="6b58c-1141">card num
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1141">card num</span></span>
- <span data-ttu-id="6b58c-1142">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1142">cardnumber</span></span>
- <span data-ttu-id="6b58c-1143">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1143">cardnumbers</span></span>
- <span data-ttu-id="6b58c-1144">card numbers
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1144">card numbers</span></span>
- <span data-ttu-id="6b58c-1145">creditcard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1145">creditcard</span></span>
- <span data-ttu-id="6b58c-1146">credit cards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1146">credit cards</span></span>
- <span data-ttu-id="6b58c-1147">creditcards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1147">creditcards</span></span>
- <span data-ttu-id="6b58c-1148">ccn
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1148">ccn</span></span>
- <span data-ttu-id="6b58c-1149">card holder
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1149">card holder</span></span>
- <span data-ttu-id="6b58c-1150">cardholder
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1150">cardholder</span></span>
- <span data-ttu-id="6b58c-1151">card holders
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1151">card holders</span></span>
- <span data-ttu-id="6b58c-1152">cardholders
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1152">cardholders</span></span>
- <span data-ttu-id="6b58c-1153">check card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1153">check card</span></span>
- <span data-ttu-id="6b58c-1154">checkcard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1154">checkcard</span></span>
- <span data-ttu-id="6b58c-1155">check cards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1155">check cards</span></span>
- <span data-ttu-id="6b58c-1156">checkcards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1156">checkcards</span></span>
- <span data-ttu-id="6b58c-1157">debit card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1157">debit card</span></span>
- <span data-ttu-id="6b58c-1158">debitcard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1158">debitcard</span></span>
- <span data-ttu-id="6b58c-1159">debit cards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1159">debit cards</span></span>
- <span data-ttu-id="6b58c-1160">debitcards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1160">debitcards</span></span>
- <span data-ttu-id="6b58c-1161">atm card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1161">atm card</span></span>
- <span data-ttu-id="6b58c-1162">atmcard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1162">atmcard</span></span>
- <span data-ttu-id="6b58c-1163">atm cards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1163">atm cards</span></span>
- <span data-ttu-id="6b58c-1164">atmcards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1164">atmcards</span></span>
- <span data-ttu-id="6b58c-1165">
enroute</span><span class="sxs-lookup"><span data-stu-id="6b58c-1165">enroute</span></span>
- <span data-ttu-id="6b58c-1166">
en route</span><span class="sxs-lookup"><span data-stu-id="6b58c-1166">en route</span></span>
- <span data-ttu-id="6b58c-1167">card type
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1167">card type</span></span>
- <span data-ttu-id="6b58c-1168">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1168">carte bancaire</span></span>
- <span data-ttu-id="6b58c-1169">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1169">carte de crédit</span></span>
- <span data-ttu-id="6b58c-1170">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1170">carte de credit</span></span>
- <span data-ttu-id="6b58c-1171">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1171">numéro de carte</span></span>
- <span data-ttu-id="6b58c-1172">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1172">numero de carte</span></span>
- <span data-ttu-id="6b58c-1173">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1173">nº de la carte</span></span>
- <span data-ttu-id="6b58c-1174">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1174">nº de carte</span></span>
- <span data-ttu-id="6b58c-1175">Kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1175">kreditkarte</span></span>
- <span data-ttu-id="6b58c-1176">Karte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1176">karte</span></span>
- <span data-ttu-id="6b58c-1177">Karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1177">karteninhaber</span></span>
- <span data-ttu-id="6b58c-1178">Karteninhaber</span><span class="sxs-lookup"><span data-stu-id="6b58c-1178">karteninhabers</span></span>
- <span data-ttu-id="6b58c-1179">Kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1179">kreditkarteninhaber</span></span>
- <span data-ttu-id="6b58c-1180">Kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1180">kreditkarteninstitut</span></span>
- <span data-ttu-id="6b58c-1181">Kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1181">kreditkartentyp</span></span>
- <span data-ttu-id="6b58c-1182">Eigentümername
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1182">eigentümername</span></span>
- <span data-ttu-id="6b58c-1183">
Kartennr
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1183">kartennr</span></span> 
- <span data-ttu-id="6b58c-1184">Kartennummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1184">kartennummer</span></span>
- <span data-ttu-id="6b58c-1185">
Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1185">kreditkartennummer</span></span>
- <span data-ttu-id="6b58c-1186">Kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1186">kreditkarten-nummer</span></span>
- <span data-ttu-id="6b58c-1187">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1187">carta di credito</span></span>
- <span data-ttu-id="6b58c-1188">carta credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1188">carta credito</span></span>
- <span data-ttu-id="6b58c-1189">Carta</span><span class="sxs-lookup"><span data-stu-id="6b58c-1189">carta</span></span>
- <span data-ttu-id="6b58c-1190">n carta</span><span class="sxs-lookup"><span data-stu-id="6b58c-1190">n carta</span></span>
- <span data-ttu-id="6b58c-p110">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p110">nr. carta</span></span>
- <span data-ttu-id="6b58c-1193">Carta Nr.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1193">nr carta</span></span>
- <span data-ttu-id="6b58c-1194">numero carta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1194">numero carta</span></span>
- <span data-ttu-id="6b58c-1195">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1195">numero della carta</span></span>
- <span data-ttu-id="6b58c-1196">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1196">numero di carta</span></span>
- <span data-ttu-id="6b58c-1197">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1197">tarjeta credito</span></span>
- <span data-ttu-id="6b58c-1198">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1198">tarjeta de credito</span></span>
- <span data-ttu-id="6b58c-1199">
tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="6b58c-1199">tarjeta crédito</span></span>
- <span data-ttu-id="6b58c-1200">
tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="6b58c-1200">tarjeta de crédito</span></span>
- <span data-ttu-id="6b58c-1201">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1201">tarjeta de atm</span></span>
- <span data-ttu-id="6b58c-1202">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1202">tarjeta atm</span></span>
- <span data-ttu-id="6b58c-1203">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1203">tarjeta debito</span></span>
- <span data-ttu-id="6b58c-1204">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1204">tarjeta de debito</span></span>
- <span data-ttu-id="6b58c-1205">
tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="6b58c-1205">tarjeta débito</span></span>
- <span data-ttu-id="6b58c-1206">
tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="6b58c-1206">tarjeta de débito</span></span>
- <span data-ttu-id="6b58c-1207">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1207">nº de tarjeta</span></span>
- <span data-ttu-id="6b58c-p111">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p111">no. de tarjeta</span></span>
- <span data-ttu-id="6b58c-1210">keine de tarjeta</span><span class="sxs-lookup"><span data-stu-id="6b58c-1210">no de tarjeta</span></span>
- <span data-ttu-id="6b58c-1211">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1211">numero de tarjeta</span></span>
- <span data-ttu-id="6b58c-1212">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1212">número de tarjeta</span></span>
- <span data-ttu-id="6b58c-1213">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1213">tarjeta no</span></span>
- <span data-ttu-id="6b58c-1214">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1214">tarjetahabiente</span></span>
- <span data-ttu-id="6b58c-1215">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1215">cartão de crédito</span></span>
- <span data-ttu-id="6b58c-1216">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1216">cartão de credito</span></span>
- <span data-ttu-id="6b58c-1217">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1217">cartao de crédito</span></span>
- <span data-ttu-id="6b58c-1218">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1218">cartao de credito</span></span>
- <span data-ttu-id="6b58c-1219">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1219">cartão de débito</span></span>
- <span data-ttu-id="6b58c-1220">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1220">cartao de débito</span></span>
- <span data-ttu-id="6b58c-1221">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1221">cartão de debito</span></span>
- <span data-ttu-id="6b58c-1222">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1222">cartao de debito</span></span>
- <span data-ttu-id="6b58c-1223">débito automático</span><span class="sxs-lookup"><span data-stu-id="6b58c-1223">débito automático</span></span>
- <span data-ttu-id="6b58c-1224">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1224">debito automatico</span></span>
- <span data-ttu-id="6b58c-1225">
número do cartão</span><span class="sxs-lookup"><span data-stu-id="6b58c-1225">número do cartão</span></span>
- <span data-ttu-id="6b58c-1226">
numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1226">numero do cartão</span></span> 
- <span data-ttu-id="6b58c-1227">número do cartao</span><span class="sxs-lookup"><span data-stu-id="6b58c-1227">número do cartao</span></span>
- <span data-ttu-id="6b58c-1228">
numero do cartao</span><span class="sxs-lookup"><span data-stu-id="6b58c-1228">numero do cartao</span></span>
- <span data-ttu-id="6b58c-1229">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1229">número de cartão</span></span>
- <span data-ttu-id="6b58c-1230">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1230">numero de cartão</span></span>
- <span data-ttu-id="6b58c-1231">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1231">número de cartao</span></span>
- <span data-ttu-id="6b58c-1232">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1232">numero de cartao</span></span>
- <span data-ttu-id="6b58c-1233">Nº cartão</span><span class="sxs-lookup"><span data-stu-id="6b58c-1233">nº do cartão</span></span>
- <span data-ttu-id="6b58c-1234">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1234">nº do cartao</span></span>
- <span data-ttu-id="6b58c-p112">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p112">nº. do cartão</span></span>
- <span data-ttu-id="6b58c-1237">keine cartão</span><span class="sxs-lookup"><span data-stu-id="6b58c-1237">no do cartão</span></span>
- <span data-ttu-id="6b58c-1238">keine cartao</span><span class="sxs-lookup"><span data-stu-id="6b58c-1238">no do cartao</span></span>
- <span data-ttu-id="6b58c-p113">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p113">no. do cartão</span></span>
- <span data-ttu-id="6b58c-p114">
no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p114">no. do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="6b58c-1243">	Kroatien – Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1243">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1244">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1244">Format</span></span>

<span data-ttu-id="6b58c-1245">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1245">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1246">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1246">Pattern</span></span>

<span data-ttu-id="6b58c-1247">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1247">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1248">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1248">Checksum</span></span>

<span data-ttu-id="6b58c-1249">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-1249">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1250">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1250">Definition</span></span>

<span data-ttu-id="6b58c-1251">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1251">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1252">Die Funktion Func_croatia_id_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1252">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1253">Ein Schlüsselwort aus Keyword_croatia_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1253">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1254">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1254">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="6b58c-1255">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="6b58c-1255">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="6b58c-1256">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="6b58c-1256">Croatian identity card</span></span>
- <span data-ttu-id="6b58c-1257">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="6b58c-1257">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="6b58c-1258">	Croatia Personal Identification (OIB) Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1258">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1259">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1259">Format</span></span>

<span data-ttu-id="6b58c-1260">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1260">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1261">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1261">Pattern</span></span>

<span data-ttu-id="6b58c-1262">10 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1262">10 digits:</span></span>
- <span data-ttu-id="6b58c-1263">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="6b58c-1263">Six digits in the form DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="6b58c-1264">Vier Ziffern, bei denen die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="6b58c-1264">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1265">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1265">Checksum</span></span>

<span data-ttu-id="6b58c-1266">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-1266">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1267">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1267">Definition</span></span>

<span data-ttu-id="6b58c-1268">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1268">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1269">Die Funktion Func_croatia_oib_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1269">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1270">Ein Schlüsselwort aus Keyword_croatia_oib_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1270">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="6b58c-1271">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1271">The checksum passes.</span></span>

<span data-ttu-id="6b58c-1272">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1272">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1273">Die Funktion Func_croatia_oib_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1273">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1274">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1274">The checksum passes.</span></span>

```
<!-- Croatia Personal Identification (OIB) Number -->
<Entity id="31983b6d-db95-4eb2-a630-b44bd091968d" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_croatia_oib_number"/>
     <Match idRef="Keyword_croatia_oib_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_oib_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1275">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1275">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="6b58c-1276">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1276">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="6b58c-1277">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1277">Personal Identification Number</span></span>
- <span data-ttu-id="6b58c-1278">Osobni identifikacijski broj
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1278">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="6b58c-1279">OIB
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1279">OIB</span></span> 

   
## <a name="czech-national-identity-card-number"></a><span data-ttu-id="6b58c-1280">	Tschechien – Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1280">Czech National Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1281">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1281">Format</span></span>

<span data-ttu-id="6b58c-1282">10 Ziffern, die einen Schrägstrich enthalten</span><span class="sxs-lookup"><span data-stu-id="6b58c-1282">10 digits containing a forward slash</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1283">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1283">Pattern</span></span>

<span data-ttu-id="6b58c-1284">10 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1284">10 digits:</span></span>
- <span data-ttu-id="6b58c-1285">Sechs Ziffern, die das Geburtsdatum darstellen </span><span class="sxs-lookup"><span data-stu-id="6b58c-1285">Six digits which are the date of birth</span></span> 
- <span data-ttu-id="6b58c-1286">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-1286">A forward slash</span></span> 
- <span data-ttu-id="6b58c-1287">Vier Ziffern, bei denen die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="6b58c-1287">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1288">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1288">Checksum</span></span>

<span data-ttu-id="6b58c-1289">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-1289">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1290">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1290">Definition</span></span>

<span data-ttu-id="6b58c-p115">Eine DLP-Richtlinie ist 85 % sicher, dass diese Art von vertraulichen Informationen festgestellt wurde "If"; innerhalb einer Nähe von 300 Zeichen: die Funktion Func_czech_id_card sucht nach Inhalten, die dem Muster entspricht. Ein Schlüsselwort aus Keyword_czech_id_card gefunden wird. Die Prüfsumme übergibt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-p115">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern. A keyword from Keyword_czech_id_card is found. The checksum passes.</span></span>

```
<!-- Czech National Identity Card Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_czech_id_card"/>
     <Match idRef="Keyword_czech_id_card"/>
  </Pattern>
</Entity>
```


### <a name="keywords"></a><span data-ttu-id="6b58c-1294">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1294">Keywords</span></span>

- <span data-ttu-id="6b58c-1295">Keyword_czech_id_card</span><span class="sxs-lookup"><span data-stu-id="6b58c-1295">Keyword_czech_id_card</span></span>
- <span data-ttu-id="6b58c-1296">Czech national identity card</span><span class="sxs-lookup"><span data-stu-id="6b58c-1296">Czech national identity card</span></span>
- <span data-ttu-id="6b58c-1297">Občanský průka</span><span class="sxs-lookup"><span data-stu-id="6b58c-1297">Občanský průka</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="6b58c-1298">	Dänemark – Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1298">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1299">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1299">Format</span></span>

<span data-ttu-id="6b58c-1300">10 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="6b58c-1300">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1301">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1301">Pattern</span></span>

<span data-ttu-id="6b58c-1302">10 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1302">10 digits:</span></span>
- <span data-ttu-id="6b58c-1303">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="6b58c-1303">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="6b58c-1304">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-1304">A hyphen</span></span> 
- <span data-ttu-id="6b58c-1305">Vier Ziffern, bei denen die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="6b58c-1305">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1306">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1306">Checksum</span></span>

<span data-ttu-id="6b58c-1307">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-1307">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1308">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1308">Definition</span></span>

<span data-ttu-id="6b58c-p116">Eine DLP-Richtlinie ist 75 % sicher, dass diese Art von vertraulichen Informationen festgestellt wurde "If"; innerhalb einer Nähe von 300 Zeichen: der reguläre Ausdruck Regex_denmark_id sucht nach Inhalten, die dem Muster entspricht. Ein Schlüsselwort aus Keyword_denmark_id gefunden wird. Die Prüfsumme übergibt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-p116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern. A keyword from Keyword_denmark_id is found. The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1312">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1312">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="6b58c-1313">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="6b58c-1313">Keyword_denmark_id</span></span>

- <span data-ttu-id="6b58c-1314">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1314">Personal Identification Number</span></span>
- <span data-ttu-id="6b58c-1315">CPR</span><span class="sxs-lookup"><span data-stu-id="6b58c-1315">CPR</span></span>
- <span data-ttu-id="6b58c-1316">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="6b58c-1316">Det Centrale Personregister</span></span>
- <span data-ttu-id="6b58c-1317">Personnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1317">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="6b58c-1318">Drug Enforcement Agency (DEA)-Nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1318">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1319">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1319">Format</span></span>

<span data-ttu-id="6b58c-1320">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1320">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1321">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1321">Pattern</span></span>

<span data-ttu-id="6b58c-1322">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1322">Pattern must include all of the following:</span></span>
- <span data-ttu-id="6b58c-1323">Einen Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) aus der folgenden Gruppe möglicher Buchstaben: abcdefghjklmnprstux, was einem Registrantencode entspricht</span><span class="sxs-lookup"><span data-stu-id="6b58c-1323">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="6b58c-1324">Ein Buchstabe (bei dem die Groß-und Kleinschreibung nicht beachtet wird), der dem ersten Buchstaben des Nachnamens des Registrants entspricht</span><span class="sxs-lookup"><span data-stu-id="6b58c-1324">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="6b58c-1325">Sieben Ziffern, von denen die letzte die Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="6b58c-1325">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1326">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1326">Checksum</span></span>

<span data-ttu-id="6b58c-1327">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-1327">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1328">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1328">Definition</span></span>

<span data-ttu-id="6b58c-1329">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1329">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1330">Die Funktion Func_dea_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1330">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1331">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1331">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1332">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1332">Keywords</span></span>

<span data-ttu-id="6b58c-1333">Keine</span><span class="sxs-lookup"><span data-stu-id="6b58c-1333">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="6b58c-1334">EU Debit Card-Nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1334">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1335">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1335">Format</span></span>

<span data-ttu-id="6b58c-1336">16 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1336">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1337">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1337">Pattern</span></span>

<span data-ttu-id="6b58c-1338">Sehr komplexes und robustes Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1338">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1339">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1339">Checksum</span></span>

<span data-ttu-id="6b58c-1340">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-1340">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1341">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1341">Definition</span></span>

<span data-ttu-id="6b58c-1342">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1343">Die Funktion Func_eu_debit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1343">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1344">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1344">At least one of the following is true:</span></span>
    - <span data-ttu-id="6b58c-1345">Ein Schlüsselwort aus Keyword_eu_debit_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1345">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="6b58c-1346">Ein Schlüsselwort aus Keyword_card_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1346">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="6b58c-1347">Ein Schlüsselwort aus Keyword_card_security_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1347">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="6b58c-1348">Ein Schlüsselwort aus Keyword_card_expiration_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1348">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="6b58c-1349">Die Funktion Func_expiration_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1349">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="6b58c-1350">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1350">The checksum passes.</span></span>

```
    <!-- EU Debit Card Number -->
    <Entity id="0e9b3178-9678-47dd-a509-37222ca96b42" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_eu_debit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_eu_debit_card" />
          <Match idRef="Keyword_card_terms_dict" />
          <Match idRef="Keyword_card_security_terms_dict" />
          <Match idRef="Keyword_card_expiration_terms_dict" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1351">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1351">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="6b58c-1352">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="6b58c-1352">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="6b58c-1353">Account-Nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1353">account number</span></span> 
- <span data-ttu-id="6b58c-1354">card number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1354">card number</span></span> 
- <span data-ttu-id="6b58c-1355">card no.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1355">card no.</span></span> 
- <span data-ttu-id="6b58c-1356">security number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1356">security number</span></span> 
- <span data-ttu-id="6b58c-1357">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1357">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="6b58c-1358">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="6b58c-1358">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="6b58c-1359">acct nbr
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1359">acct nbr</span></span> 
- <span data-ttu-id="6b58c-1360">acct num
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1360">acct num</span></span> 
- <span data-ttu-id="6b58c-1361">acct no
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1361">acct no</span></span> 
- <span data-ttu-id="6b58c-1362">american express
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1362">american express</span></span> 
- <span data-ttu-id="6b58c-1363">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1363">americanexpress</span></span> 
- <span data-ttu-id="6b58c-1364">americano espresso
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1364">americano espresso</span></span> 
- <span data-ttu-id="6b58c-1365">amex</span><span class="sxs-lookup"><span data-stu-id="6b58c-1365">amex</span></span> 
- <span data-ttu-id="6b58c-1366">atm card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1366">atm card</span></span> 
- <span data-ttu-id="6b58c-1367">atm cards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1367">atm cards</span></span> 
- <span data-ttu-id="6b58c-1368">atm kaart
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1368">atm kaart</span></span> 
- <span data-ttu-id="6b58c-1369">atmcard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1369">atmcard</span></span> 
- <span data-ttu-id="6b58c-1370">atmcards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1370">atmcards</span></span> 
- <span data-ttu-id="6b58c-1371">atmkaart
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1371">atmkaart</span></span> 
- <span data-ttu-id="6b58c-1372">atmkaarten
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1372">atmkaarten</span></span> 
- <span data-ttu-id="6b58c-1373">bancontact
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1373">bancontact</span></span> 
- <span data-ttu-id="6b58c-1374">bank card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1374">bank card</span></span> 
- <span data-ttu-id="6b58c-1375">bankkaart
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1375">bankkaart</span></span> 
- <span data-ttu-id="6b58c-1376">card holder
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1376">card holder</span></span> 
- <span data-ttu-id="6b58c-1377">card holders
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1377">card holders</span></span> 
- <span data-ttu-id="6b58c-1378">card num
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1378">card num</span></span> 
- <span data-ttu-id="6b58c-1379">card number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1379">card number</span></span> 
- <span data-ttu-id="6b58c-1380">card numbers
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1380">card numbers</span></span> 
- <span data-ttu-id="6b58c-1381">card type
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1381">card type</span></span> 
- <span data-ttu-id="6b58c-1382">cardano numerico
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1382">cardano numerico</span></span> 
- <span data-ttu-id="6b58c-1383">cardholder
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1383">cardholder</span></span> 
- <span data-ttu-id="6b58c-1384">cardholders
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1384">cardholders</span></span> 
- <span data-ttu-id="6b58c-1385">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1385">cardnumber</span></span> 
- <span data-ttu-id="6b58c-1386">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1386">cardnumbers</span></span> 
- <span data-ttu-id="6b58c-1387">carta bianca
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1387">carta bianca</span></span> 
- <span data-ttu-id="6b58c-1388">carta credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1388">carta credito</span></span> 
- <span data-ttu-id="6b58c-1389">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1389">carta di credito</span></span> 
- <span data-ttu-id="6b58c-1390">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1390">cartao de credito</span></span> 
- <span data-ttu-id="6b58c-1391">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1391">cartao de crédito</span></span> 
- <span data-ttu-id="6b58c-1392">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1392">cartao de debito</span></span> 
- <span data-ttu-id="6b58c-1393">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1393">cartao de débito</span></span> 
- <span data-ttu-id="6b58c-1394">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1394">carte bancaire</span></span> 
- <span data-ttu-id="6b58c-1395">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1395">carte blanche</span></span> 
- <span data-ttu-id="6b58c-1396">carte bleue
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1396">carte bleue</span></span> 
- <span data-ttu-id="6b58c-1397">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1397">carte de credit</span></span> 
- <span data-ttu-id="6b58c-1398">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1398">carte de crédit</span></span> 
- <span data-ttu-id="6b58c-1399">carte di credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1399">carte di credito</span></span> 
- <span data-ttu-id="6b58c-1400">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1400">carteblanche</span></span> 
- <span data-ttu-id="6b58c-1401">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1401">cartão de credito</span></span> 
- <span data-ttu-id="6b58c-1402">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1402">cartão de crédito</span></span> 
- <span data-ttu-id="6b58c-1403">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1403">cartão de debito</span></span> 
- <span data-ttu-id="6b58c-1404">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1404">cartão de débito</span></span> 
- <span data-ttu-id="6b58c-1405">cb
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1405">cb</span></span> 
- <span data-ttu-id="6b58c-1406">ccn
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1406">ccn</span></span> 
- <span data-ttu-id="6b58c-1407">check card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1407">check card</span></span> 
- <span data-ttu-id="6b58c-1408">check cards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1408">check cards</span></span> 
- <span data-ttu-id="6b58c-1409">checkcard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1409">checkcard</span></span>
- <span data-ttu-id="6b58c-1410">checkcards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1410">checkcards</span></span> 
- <span data-ttu-id="6b58c-1411">chequekaart
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1411">chequekaart</span></span> 
- <span data-ttu-id="6b58c-1412">cirrus
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1412">cirrus</span></span> 
- <span data-ttu-id="6b58c-1413">cirrus-edc-maestro
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1413">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="6b58c-1414">controlekaart
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1414">controlekaart</span></span> 
- <span data-ttu-id="6b58c-1415">controlekaarten
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1415">controlekaarten</span></span> 
- <span data-ttu-id="6b58c-1416">credit card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1416">credit card</span></span> 
- <span data-ttu-id="6b58c-1417">credit cards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1417">credit cards</span></span> 
- <span data-ttu-id="6b58c-1418">creditcard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1418">creditcard</span></span> 
- <span data-ttu-id="6b58c-1419">creditcards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1419">creditcards</span></span> 
- <span data-ttu-id="6b58c-1420">debetkaart
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1420">debetkaart</span></span> 
- <span data-ttu-id="6b58c-1421">debetkaarten
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1421">debetkaarten</span></span> 
- <span data-ttu-id="6b58c-1422">debit card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1422">debit card</span></span> 
- <span data-ttu-id="6b58c-1423">debit cards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1423">debit cards</span></span> 
- <span data-ttu-id="6b58c-1424">debitcard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1424">debitcard</span></span> 
- <span data-ttu-id="6b58c-1425">debitcards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1425">debitcards</span></span> 
- <span data-ttu-id="6b58c-1426">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1426">debito automatico</span></span> 
- <span data-ttu-id="6b58c-1427">diners club
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1427">diners club</span></span> 
- <span data-ttu-id="6b58c-1428">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1428">dinersclub</span></span> 
- <span data-ttu-id="6b58c-1429">Entdecken</span><span class="sxs-lookup"><span data-stu-id="6b58c-1429">discover</span></span> 
- <span data-ttu-id="6b58c-1430">discover card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1430">discover card</span></span> 
- <span data-ttu-id="6b58c-1431">discover cards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1431">discover cards</span></span> 
- <span data-ttu-id="6b58c-1432">discovercard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1432">discovercard</span></span> 
- <span data-ttu-id="6b58c-1433">discovercards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1433">discovercards</span></span> 
- <span data-ttu-id="6b58c-1434">débito automático</span><span class="sxs-lookup"><span data-stu-id="6b58c-1434">débito automático</span></span>
- <span data-ttu-id="6b58c-1435">
edc
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1435">edc</span></span> 
- <span data-ttu-id="6b58c-1436">Eigentümername
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1436">eigentümername</span></span> 
- <span data-ttu-id="6b58c-1437">european debit card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1437">european debit card</span></span> 
- <span data-ttu-id="6b58c-1438">hoofdkaart
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1438">hoofdkaart</span></span> 
- <span data-ttu-id="6b58c-1439">hoofdkaarten
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1439">hoofdkaarten</span></span> 
- <span data-ttu-id="6b58c-1440">in viaggio
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1440">in viaggio</span></span> 
- <span data-ttu-id="6b58c-1441">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1441">japanese card bureau</span></span> 
- <span data-ttu-id="6b58c-1442">japanse kaartdienst
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1442">japanse kaartdienst</span></span> 
- <span data-ttu-id="6b58c-1443">jcb
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1443">jcb</span></span> 
- <span data-ttu-id="6b58c-1444">kaart
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1444">kaart</span></span> 
- <span data-ttu-id="6b58c-1445">kaart num
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1445">kaart num</span></span> 
- <span data-ttu-id="6b58c-1446">kaartaantal
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1446">kaartaantal</span></span> 
- <span data-ttu-id="6b58c-1447">kaartaantallen
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1447">kaartaantallen</span></span> 
- <span data-ttu-id="6b58c-1448">kaarthouder
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1448">kaarthouder</span></span> 
- <span data-ttu-id="6b58c-1449">kaarthouders
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1449">kaarthouders</span></span> 
- <span data-ttu-id="6b58c-1450">Karte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1450">karte</span></span>  
- <span data-ttu-id="6b58c-1451">Karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1451">karteninhaber</span></span> 
- <span data-ttu-id="6b58c-1452">Karteninhaber</span><span class="sxs-lookup"><span data-stu-id="6b58c-1452">karteninhabers</span></span>
- <span data-ttu-id="6b58c-1453">
Kartennr
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1453">kartennr</span></span> 
- <span data-ttu-id="6b58c-1454">Kartennummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1454">kartennummer</span></span> 
- <span data-ttu-id="6b58c-1455">Kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1455">kreditkarte</span></span> 
- <span data-ttu-id="6b58c-1456">Kreditkarten-nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1456">kreditkarten-nummer</span></span> 
- <span data-ttu-id="6b58c-1457">Kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1457">kreditkarteninhaber</span></span> 
- <span data-ttu-id="6b58c-1458">Kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1458">kreditkarteninstitut</span></span> 
- <span data-ttu-id="6b58c-1459">Kreditkartennummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1459">kreditkartennummer</span></span> 
- <span data-ttu-id="6b58c-1460">Kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1460">kreditkartentyp</span></span> 
- <span data-ttu-id="6b58c-1461">Maestro
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1461">maestro</span></span> 
- <span data-ttu-id="6b58c-1462">master card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1462">master card</span></span> 
- <span data-ttu-id="6b58c-1463">master cards
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1463">master cards</span></span> 
- <span data-ttu-id="6b58c-1464">mastercard
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1464">mastercard</span></span> 
- <span data-ttu-id="6b58c-1465">mastercards</span><span class="sxs-lookup"><span data-stu-id="6b58c-1465">mastercards</span></span> 
- <span data-ttu-id="6b58c-1466">MC</span><span class="sxs-lookup"><span data-stu-id="6b58c-1466">mc</span></span> 
- <span data-ttu-id="6b58c-1467">mister cash
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1467">mister cash</span></span> 
- <span data-ttu-id="6b58c-1468">n carta</span><span class="sxs-lookup"><span data-stu-id="6b58c-1468">n carta</span></span> 
- <span data-ttu-id="6b58c-1469">Carta</span><span class="sxs-lookup"><span data-stu-id="6b58c-1469">carta</span></span> 
- <span data-ttu-id="6b58c-1470">keine de tarjeta</span><span class="sxs-lookup"><span data-stu-id="6b58c-1470">no de tarjeta</span></span> 
- <span data-ttu-id="6b58c-1471">keine cartao</span><span class="sxs-lookup"><span data-stu-id="6b58c-1471">no do cartao</span></span> 
- <span data-ttu-id="6b58c-1472">keine cartão</span><span class="sxs-lookup"><span data-stu-id="6b58c-1472">no do cartão</span></span> 
- <span data-ttu-id="6b58c-p117">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p117">no. de tarjeta</span></span> 
- <span data-ttu-id="6b58c-p118">no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p118">no. do cartao</span></span> 
- <span data-ttu-id="6b58c-p119">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p119">no. do cartão</span></span> 
- <span data-ttu-id="6b58c-1479">Carta Nr.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1479">nr carta</span></span> 
- <span data-ttu-id="6b58c-p120">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p120">nr. carta</span></span> 
- <span data-ttu-id="6b58c-1482">numeri di scheda
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1482">numeri di scheda</span></span> 
- <span data-ttu-id="6b58c-1483">numero carta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1483">numero carta</span></span> 
- <span data-ttu-id="6b58c-1484">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1484">numero de cartao</span></span> 
- <span data-ttu-id="6b58c-1485">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1485">numero de carte</span></span> 
- <span data-ttu-id="6b58c-1486">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1486">numero de cartão</span></span> 
- <span data-ttu-id="6b58c-1487">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1487">numero de tarjeta</span></span>
- <span data-ttu-id="6b58c-1488">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1488">numero della carta</span></span> 
- <span data-ttu-id="6b58c-1489">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1489">numero di carta</span></span> 
- <span data-ttu-id="6b58c-1490">numero di scheda
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1490">numero di scheda</span></span> 
- <span data-ttu-id="6b58c-1491">numero do cartao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1491">numero do cartao</span></span> 
- <span data-ttu-id="6b58c-1492">numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1492">numero do cartão</span></span> 
- <span data-ttu-id="6b58c-1493">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1493">numéro de carte</span></span> 
- <span data-ttu-id="6b58c-1494">nº carta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1494">nº carta</span></span> 
- <span data-ttu-id="6b58c-1495">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1495">nº de carte</span></span> 
- <span data-ttu-id="6b58c-1496">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1496">nº de la carte</span></span> 
- <span data-ttu-id="6b58c-1497">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1497">nº de tarjeta</span></span> 
- <span data-ttu-id="6b58c-1498">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1498">nº do cartao</span></span> 
- <span data-ttu-id="6b58c-1499">Nº cartão</span><span class="sxs-lookup"><span data-stu-id="6b58c-1499">nº do cartão</span></span> 
- <span data-ttu-id="6b58c-p121">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p121">nº. do cartão</span></span> 
- <span data-ttu-id="6b58c-1502">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1502">número de cartao</span></span> 
- <span data-ttu-id="6b58c-1503">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1503">número de cartão</span></span> 
- <span data-ttu-id="6b58c-1504">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1504">número de tarjeta</span></span> 
- <span data-ttu-id="6b58c-1505">número do cartao</span><span class="sxs-lookup"><span data-stu-id="6b58c-1505">número do cartao</span></span> 
- <span data-ttu-id="6b58c-1506">scheda dell'assegno
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1506">scheda dell'assegno</span></span> 
- <span data-ttu-id="6b58c-1507">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1507">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="6b58c-1508">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1508">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="6b58c-1509">scheda della banca
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1509">scheda della banca</span></span> 
- <span data-ttu-id="6b58c-1510">scheda di controllo
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1510">scheda di controllo</span></span> 
- <span data-ttu-id="6b58c-1511">scheda di debito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1511">scheda di debito</span></span> 
- <span data-ttu-id="6b58c-1512">scheda matrice
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1512">scheda matrice</span></span> 
- <span data-ttu-id="6b58c-1513">schede dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1513">schede dell'atmosfera</span></span> 
- <span data-ttu-id="6b58c-1514">schede di controllo
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1514">schede di controllo</span></span> 
- <span data-ttu-id="6b58c-1515">schede di debito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1515">schede di debito</span></span> 
- <span data-ttu-id="6b58c-1516">schede matrici
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1516">schede matrici</span></span> 
- <span data-ttu-id="6b58c-1517">scoprono la scheda
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1517">scoprono la scheda</span></span> 
- <span data-ttu-id="6b58c-1518">scoprono le schede
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1518">scoprono le schede</span></span> 
- <span data-ttu-id="6b58c-1519">solo
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1519">solo</span></span> 
- <span data-ttu-id="6b58c-1520">supporti di scheda
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1520">supporti di scheda</span></span> 
- <span data-ttu-id="6b58c-1521">supporto di scheda
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1521">supporto di scheda</span></span> 
- <span data-ttu-id="6b58c-1522">Schalter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1522">switch</span></span> 
- <span data-ttu-id="6b58c-1523">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1523">tarjeta atm</span></span> 
- <span data-ttu-id="6b58c-1524">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1524">tarjeta credito</span></span> 
- <span data-ttu-id="6b58c-1525">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1525">tarjeta de atm</span></span> 
- <span data-ttu-id="6b58c-1526">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1526">tarjeta de credito</span></span> 
- <span data-ttu-id="6b58c-1527">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1527">tarjeta de debito</span></span> 
- <span data-ttu-id="6b58c-1528">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1528">tarjeta debito</span></span> 
- <span data-ttu-id="6b58c-1529">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1529">tarjeta no</span></span>
- <span data-ttu-id="6b58c-1530">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1530">tarjetahabiente</span></span> 
- <span data-ttu-id="6b58c-1531">tipo della scheda
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1531">tipo della scheda</span></span> 
- <span data-ttu-id="6b58c-1532">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="6b58c-1532">ufficio giapponese della</span></span> 
- <span data-ttu-id="6b58c-1533">scheda
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1533">scheda</span></span> 
- <span data-ttu-id="6b58c-1534">v pay
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1534">v pay</span></span> 
- <span data-ttu-id="6b58c-1535">V kostenpflichtig</span><span class="sxs-lookup"><span data-stu-id="6b58c-1535">v-pay</span></span> 
- <span data-ttu-id="6b58c-1536">visa
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1536">visa</span></span> 
- <span data-ttu-id="6b58c-1537">visa plus
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1537">visa plus</span></span> 
- <span data-ttu-id="6b58c-1538">visa electron
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1538">visa electron</span></span> 
- <span data-ttu-id="6b58c-1539">visto
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1539">visto</span></span> 
- <span data-ttu-id="6b58c-1540">visum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1540">visum</span></span> 
- <span data-ttu-id="6b58c-1541">vpay
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1541">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="6b58c-1542">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="6b58c-1542">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="6b58c-1543">card identification number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1543">card identification number</span></span>
- <span data-ttu-id="6b58c-1544">card verification</span><span class="sxs-lookup"><span data-stu-id="6b58c-1544">card verification</span></span> 
- <span data-ttu-id="6b58c-1545">cardi la verifica
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1545">cardi la verifica</span></span> 
- <span data-ttu-id="6b58c-1546">cid
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1546">cid</span></span> 
- <span data-ttu-id="6b58c-1547">COD seg</span><span class="sxs-lookup"><span data-stu-id="6b58c-1547">cod seg</span></span> 
- <span data-ttu-id="6b58c-1548">COD seguranca</span><span class="sxs-lookup"><span data-stu-id="6b58c-1548">cod seguranca</span></span> 
- <span data-ttu-id="6b58c-1549">COD segurança</span><span class="sxs-lookup"><span data-stu-id="6b58c-1549">cod segurança</span></span> 
- <span data-ttu-id="6b58c-1550">COD sicurezza</span><span class="sxs-lookup"><span data-stu-id="6b58c-1550">cod sicurezza</span></span> 
- <span data-ttu-id="6b58c-p122">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p122">cod. seg</span></span> 
- <span data-ttu-id="6b58c-p123">cod. seguranca
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p123">cod. seguranca</span></span> 
- <span data-ttu-id="6b58c-p124">cod. segurança
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p124">cod. segurança</span></span> 
- <span data-ttu-id="6b58c-p125">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p125">cod. sicurezza</span></span> 
- <span data-ttu-id="6b58c-1559">codice di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1559">codice di sicurezza</span></span> 
- <span data-ttu-id="6b58c-1560">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1560">codice di verifica</span></span> 
- <span data-ttu-id="6b58c-1561">codigo
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1561">codigo</span></span> 
- <span data-ttu-id="6b58c-1562">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1562">codigo de seguranca</span></span> 
- <span data-ttu-id="6b58c-1563">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1563">codigo de segurança</span></span> 
- <span data-ttu-id="6b58c-1564">crittogramma
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1564">crittogramma</span></span> 
- <span data-ttu-id="6b58c-1565">cryptogram
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1565">cryptogram</span></span> 
- <span data-ttu-id="6b58c-1566">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1566">cryptogramme</span></span> 
- <span data-ttu-id="6b58c-1567">cv2</span><span class="sxs-lookup"><span data-stu-id="6b58c-1567">cv2</span></span> 
- <span data-ttu-id="6b58c-1568">cvc
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1568">cvc</span></span> 
- <span data-ttu-id="6b58c-1569">CVC2</span><span class="sxs-lookup"><span data-stu-id="6b58c-1569">cvc2</span></span> 
- <span data-ttu-id="6b58c-1570">cvn
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1570">cvn</span></span> 
- <span data-ttu-id="6b58c-1571">cvv
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1571">cvv</span></span> 
- <span data-ttu-id="6b58c-1572">CVV2</span><span class="sxs-lookup"><span data-stu-id="6b58c-1572">cvv2</span></span> 
- <span data-ttu-id="6b58c-1573">Cód seguranca</span><span class="sxs-lookup"><span data-stu-id="6b58c-1573">cód seguranca</span></span> 
- <span data-ttu-id="6b58c-1574">Cód segurança</span><span class="sxs-lookup"><span data-stu-id="6b58c-1574">cód segurança</span></span> 
- <span data-ttu-id="6b58c-p126">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p126">cód. seguranca</span></span> 
- <span data-ttu-id="6b58c-p127">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p127">cód. segurança</span></span> 
- <span data-ttu-id="6b58c-1579">código
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1579">código</span></span> 
- <span data-ttu-id="6b58c-1580">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1580">código de seguranca</span></span> 
- <span data-ttu-id="6b58c-1581">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1581">código de segurança</span></span> 
- <span data-ttu-id="6b58c-1582">de kaart controle
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1582">de kaart controle</span></span> 
- <span data-ttu-id="6b58c-1583">geeft nr uit
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1583">geeft nr uit</span></span> 
- <span data-ttu-id="6b58c-1584">issue no
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1584">issue no</span></span> 
- <span data-ttu-id="6b58c-1585">issue number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1585">issue number</span></span> 
- <span data-ttu-id="6b58c-1586">kaartidentificatienummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1586">kaartidentificatienummer</span></span> 
- <span data-ttu-id="6b58c-1587">Kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1587">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="6b58c-1588">Kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1588">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="6b58c-1589">kwestieaantal
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1589">kwestieaantal</span></span> 
- <span data-ttu-id="6b58c-p128">no. dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p128">no. dell'edizione</span></span> 
- <span data-ttu-id="6b58c-p129">no. di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p129">no. di sicurezza</span></span> 
- <span data-ttu-id="6b58c-1594">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1594">numero de securite</span></span> 
- <span data-ttu-id="6b58c-1595">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1595">numero de verificacao</span></span> 
- <span data-ttu-id="6b58c-1596">numero dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1596">numero dell'edizione</span></span> 
- <span data-ttu-id="6b58c-1597">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="6b58c-1597">numero di identificazione della</span></span> 
- <span data-ttu-id="6b58c-1598">scheda
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1598">scheda</span></span> 
- <span data-ttu-id="6b58c-1599">numero di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1599">numero di sicurezza</span></span> 
- <span data-ttu-id="6b58c-1600">numero van veiligheid
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1600">numero van veiligheid</span></span> 
- <span data-ttu-id="6b58c-1601">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1601">numéro de sécurité</span></span> 
- <span data-ttu-id="6b58c-1602">nº autorizzazione
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1602">nº autorizzazione</span></span> 
- <span data-ttu-id="6b58c-1603">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1603">número de verificação</span></span> 
- <span data-ttu-id="6b58c-1604">perno il blocco
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1604">perno il blocco</span></span> 
- <span data-ttu-id="6b58c-1605">pin block
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1605">pin block</span></span> 
- <span data-ttu-id="6b58c-1606">Prufziffer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1606">prufziffer</span></span> 
- <span data-ttu-id="6b58c-1607">Prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1607">prüfziffer</span></span> 
- <span data-ttu-id="6b58c-1608">security code
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1608">security code</span></span> 
- <span data-ttu-id="6b58c-1609">security no
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1609">security no</span></span> 
- <span data-ttu-id="6b58c-1610">security number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1610">security number</span></span> 
- <span data-ttu-id="6b58c-1611">Sicherheitskode
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1611">sicherheits kode</span></span> 
- <span data-ttu-id="6b58c-1612">Sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1612">sicherheitscode</span></span> 
- <span data-ttu-id="6b58c-1613">Sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1613">sicherheitsnummer</span></span> 
- <span data-ttu-id="6b58c-1614">speldblok
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1614">speldblok</span></span> 
- <span data-ttu-id="6b58c-1615">veiligheid nr
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1615">veiligheid nr</span></span> 
- <span data-ttu-id="6b58c-1616">veiligheidsaantal
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1616">veiligheidsaantal</span></span> 
- <span data-ttu-id="6b58c-1617">veiligheidscode
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1617">veiligheidscode</span></span> 
- <span data-ttu-id="6b58c-1618">veiligheidsnummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1618">veiligheidsnummer</span></span> 
- <span data-ttu-id="6b58c-1619">Verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1619">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="6b58c-1620">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="6b58c-1620">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="6b58c-1621">Ablauf
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1621">ablauf</span></span> 
- <span data-ttu-id="6b58c-1622">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1622">data de expiracao</span></span> 
- <span data-ttu-id="6b58c-1623">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1623">data de expiração</span></span> 
- <span data-ttu-id="6b58c-1624">data del exp
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1624">data del exp</span></span> 
- <span data-ttu-id="6b58c-1625">data di exp
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1625">data di exp</span></span> 
- <span data-ttu-id="6b58c-1626">data di scadenza
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1626">data di scadenza</span></span> 
- <span data-ttu-id="6b58c-1627">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1627">data em que expira</span></span> 
- <span data-ttu-id="6b58c-1628">data scad
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1628">data scad</span></span> 
- <span data-ttu-id="6b58c-1629">data scadenza
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1629">data scadenza</span></span> 
- <span data-ttu-id="6b58c-1630">date de validité
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1630">date de validité</span></span> 
- <span data-ttu-id="6b58c-1631">datum afloop
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1631">datum afloop</span></span> 
- <span data-ttu-id="6b58c-1632">datum van exp
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1632">datum van exp</span></span> 
- <span data-ttu-id="6b58c-1633">de afloop
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1633">de afloop</span></span> 
- <span data-ttu-id="6b58c-1634">espira
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1634">espira</span></span> 
- <span data-ttu-id="6b58c-1635">espira
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1635">espira</span></span> 
- <span data-ttu-id="6b58c-1636">exp date
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1636">exp date</span></span> 
- <span data-ttu-id="6b58c-1637">exp datum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1637">exp datum</span></span> 
- <span data-ttu-id="6b58c-1638">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="6b58c-1638">expiration</span></span> 
- <span data-ttu-id="6b58c-1639">expire
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1639">expire</span></span> 
- <span data-ttu-id="6b58c-1640">expires
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1640">expires</span></span> 
- <span data-ttu-id="6b58c-1641">expiry
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1641">expiry</span></span> 
- <span data-ttu-id="6b58c-1642">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1642">fecha de expiracion</span></span> 
- <span data-ttu-id="6b58c-1643">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1643">fecha de venc</span></span> 
- <span data-ttu-id="6b58c-1644">Gultig bis
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1644">gultig bis</span></span> 
- <span data-ttu-id="6b58c-1645">Gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1645">gultigkeitsdatum</span></span> 
- <span data-ttu-id="6b58c-1646">Gültig bis
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1646">gültig bis</span></span> 
- <span data-ttu-id="6b58c-1647">Gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1647">gültigkeitsdatum</span></span> 
- <span data-ttu-id="6b58c-1648">la scadenza
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1648">la scadenza</span></span> 
- <span data-ttu-id="6b58c-1649">scadenza
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1649">scadenza</span></span> 
- <span data-ttu-id="6b58c-1650">valable
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1650">valable</span></span> 
- <span data-ttu-id="6b58c-1651">validade
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1651">validade</span></span> 
- <span data-ttu-id="6b58c-1652">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1652">valido hasta</span></span> 
- <span data-ttu-id="6b58c-1653">valor
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1653">valor</span></span> 
- <span data-ttu-id="6b58c-1654">venc
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1654">venc</span></span> 
- <span data-ttu-id="6b58c-1655">vencimento
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1655">vencimento</span></span> 
- <span data-ttu-id="6b58c-1656">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1656">vencimiento</span></span> 
- <span data-ttu-id="6b58c-1657">verloopt
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1657">verloopt</span></span> 
- <span data-ttu-id="6b58c-1658">vervaldag
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1658">vervaldag</span></span> 
- <span data-ttu-id="6b58c-1659">vervaldatum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1659">vervaldatum</span></span> 
- <span data-ttu-id="6b58c-1660">vto
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1660">vto</span></span> 
- <span data-ttu-id="6b58c-1661">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1661">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="6b58c-1662">EU Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1662">EU Driver's License Number</span></span>

<span data-ttu-id="6b58c-1663">Finden Sie weitere Informationen finden Sie unter [vertrauliche Informationen vom Typ des Treibers EU-Lizenz Zahl](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="6b58c-1663">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="6b58c-1664">EU National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1664">EU National Identification Number</span></span>

<span data-ttu-id="6b58c-1665">Weitere Informationen finden Sie finden Sie unter [Identifikationsnummer der EU National vertrauliche Informationstyp](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="6b58c-1665">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="6b58c-1666">EU Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1666">EU Passport Number</span></span>

<span data-ttu-id="6b58c-1667">Finden Sie weitere Informationen finden Sie unter [EU Reisepassnummer vertrauliche Informationstyp](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="6b58c-1667">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="6b58c-1668">EU Sozialversicherungsnummer oder einer ähnlichen-ID</span><span class="sxs-lookup"><span data-stu-id="6b58c-1668">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="6b58c-1669">Weitere Informationen finden Sie unter [EU Sozialversicherungsnummer oder gleichwertige ID vertrauliche Informationstyp](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="6b58c-1669">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="6b58c-1670">EU-Steuernummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1670">EU Tax Identification Number</span></span>

<span data-ttu-id="6b58c-1671">Finden Sie weitere Informationen finden Sie unter [EU Steuernummer vertrauliche Informationstyp](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="6b58c-1671">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="6b58c-1672">Finland National ID (Finnischer Personalausweis)</span><span class="sxs-lookup"><span data-stu-id="6b58c-1672">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1673">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1673">Format</span></span>

<span data-ttu-id="6b58c-1674">Sechs Ziffern plus ein Zeichen, das ein Jahrhundert angibt, plus drei Ziffern plus einer Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1674">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1675">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1675">Pattern</span></span>

<span data-ttu-id="6b58c-1676">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1676">Pattern must include all of the following:</span></span>
- <span data-ttu-id="6b58c-1677">Sechs Ziffern im Format TTMMJJ, die ein Geburtsdatum darstellen</span><span class="sxs-lookup"><span data-stu-id="6b58c-1677">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="6b58c-1678">Jahrhundertkennzeichnung (entweder „-“, „+“ oder „a“)</span><span class="sxs-lookup"><span data-stu-id="6b58c-1678">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="6b58c-1679">Dreistellige persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1679">Three-digit personal identification number</span></span> 
- <span data-ttu-id="6b58c-1680">Eine Ziffer oder ein Buchstabe (Groß-/Kleinschreibung irrelevant), die bzw. der eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="6b58c-1680">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1681">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1681">Checksum</span></span>

<span data-ttu-id="6b58c-1682">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-1682">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1683">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1683">Definition</span></span>

<span data-ttu-id="6b58c-1684">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1684">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1685">Die Funktion Func_finnish_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1685">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1686">Ein Schlüsselwort aus Keyword_finnish_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1686">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="6b58c-1687">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1687">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1688">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1688">Keywords</span></span>

- <span data-ttu-id="6b58c-1689">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="6b58c-1689">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="6b58c-1690">

Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="6b58c-1690">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="6b58c-1691">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="6b58c-1691">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="6b58c-1692">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="6b58c-1692">Personbeteckning</span></span>
- <span data-ttu-id="6b58c-1693">Personnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1693">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="6b58c-1694">Finnische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1694">Finland Passport Number</span></span>

<span data-ttu-id="6b58c-p130">Formatieren der Kombination von neun Buchstaben und Ziffern Muster Kombination von neun Buchstaben und Ziffern: zwei Buchstaben (ohne Beachtung von Groß-/Kleinschreibung) sieben Ziffern Prüfsumme No Definition eine DLP-Richtlinie ist 75 % sicher, dass diese Art von vertraulichen Informationen Wenn festgestellt wurde, innerhalb einer Nähe von 300 Zeichen: der reguläre Ausdruck Regex_finland_passport_number sucht nach Inhalten, die dem Muster entspricht. Ein Schlüsselwort aus Keyword_finland_passport_number gefunden wird. <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity> Schlüsselwörter Keyword_finland_passport_number Passport passive</span><span class="sxs-lookup"><span data-stu-id="6b58c-p130">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern. A keyword from Keyword_finland_passport_number is found. <!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity> Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="6b58c-1699">Französische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1699">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1700">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1700">Format</span></span>

<span data-ttu-id="6b58c-1701">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1701">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1702">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1702">Pattern</span></span>

<span data-ttu-id="6b58c-1703">12 Ziffern mit Validierung, um ähnliche Muster ( z. B. französische Telefonnummern) auszuschließen</span><span class="sxs-lookup"><span data-stu-id="6b58c-1703">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1704">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1704">Checksum</span></span>

<span data-ttu-id="6b58c-1705">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-1705">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1706">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1706">Definition</span></span>

<span data-ttu-id="6b58c-1707">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1707">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1708">Die Funktion Func_french_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1708">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1709">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1709">At least one of the following is true:</span></span>
- <span data-ttu-id="6b58c-1710">Ein Schlüsselwort aus Keyword_french_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1710">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="6b58c-1711">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1711">The function Func_eu_date finds a date in the right date format.</span></span>

```
<!-- France Driver's License Number -->
<Entity id="18e55a36-a01b-4b0f-943d-dc10282a1824" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_french_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_french_drivers_license" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1712">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1712">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="6b58c-1713">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="6b58c-1713">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="6b58c-1714">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6b58c-1714">drivers licence</span></span>
- <span data-ttu-id="6b58c-1715">drivers license</span><span class="sxs-lookup"><span data-stu-id="6b58c-1715">drivers license</span></span>
- <span data-ttu-id="6b58c-1716">driving licence
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1716">driving licence</span></span>
- <span data-ttu-id="6b58c-1717">gesteuerte Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-1717">driving license</span></span>
- <span data-ttu-id="6b58c-1718">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="6b58c-1718">permis de conduire</span></span>
- <span data-ttu-id="6b58c-1719">
licence number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1719">licence number</span></span>
- <span data-ttu-id="6b58c-1720">
license number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1720">license number</span></span>
- <span data-ttu-id="6b58c-1721">
licence numbers</span><span class="sxs-lookup"><span data-stu-id="6b58c-1721">licence numbers</span></span>
- <span data-ttu-id="6b58c-1722">

license numbers</span><span class="sxs-lookup"><span data-stu-id="6b58c-1722">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="6b58c-1723">Französische Carte nationale d'identité (CNI)</span><span class="sxs-lookup"><span data-stu-id="6b58c-1723">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1724">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1724">Format</span></span>

<span data-ttu-id="6b58c-1725">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1725">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1726">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1726">Pattern</span></span>

<span data-ttu-id="6b58c-1727">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1727">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1728">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1728">Checksum</span></span>

<span data-ttu-id="6b58c-1729">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-1729">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1730">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1730">Definition</span></span>

<span data-ttu-id="6b58c-1731">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1731">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1732">Der reguläre Ausdruck Regex_france_cni findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1732">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1733">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1733">Keywords</span></span>

<span data-ttu-id="6b58c-1734">Keine</span><span class="sxs-lookup"><span data-stu-id="6b58c-1734">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="6b58c-1735">Französische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1735">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1736">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1736">Format</span></span>

<span data-ttu-id="6b58c-1737">Neun Ziffern und Buchstaben</span><span class="sxs-lookup"><span data-stu-id="6b58c-1737">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1738">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1738">Pattern</span></span>

<span data-ttu-id="6b58c-1739">Neun Ziffern und Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1739">Nine digits and letters:</span></span>
- <span data-ttu-id="6b58c-1740">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1740">Two digits</span></span> 
- <span data-ttu-id="6b58c-1741">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="6b58c-1741">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-1742">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1742">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1743">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1743">Checksum</span></span>

<span data-ttu-id="6b58c-1744">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-1744">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1745">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1745">Definition</span></span>

<span data-ttu-id="6b58c-1746">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1746">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1747">Die Funktion Func_fr_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1747">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1748">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1748">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1749">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1749">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="6b58c-1750">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-1750">Keyword_passport</span></span>

- <span data-ttu-id="6b58c-1751">Passport Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1751">Passport Number</span></span>
- <span data-ttu-id="6b58c-1752">
Passport No</span><span class="sxs-lookup"><span data-stu-id="6b58c-1752">Passport No</span></span>
- <span data-ttu-id="6b58c-1753">Passport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1753">Passport #</span></span>
- <span data-ttu-id="6b58c-1754">Passport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1754">Passport#</span></span>
- <span data-ttu-id="6b58c-1755">PassportID</span><span class="sxs-lookup"><span data-stu-id="6b58c-1755">PassportID</span></span>
- <span data-ttu-id="6b58c-1756">Passportno
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1756">Passportno</span></span>
- <span data-ttu-id="6b58c-1757">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1757">passportnumber</span></span>
- <span data-ttu-id="6b58c-1758">パスポート</span><span class="sxs-lookup"><span data-stu-id="6b58c-1758">パスポート</span></span>
- <span data-ttu-id="6b58c-1759">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1759">パスポート番号</span></span>
- <span data-ttu-id="6b58c-1760">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1760">パスポートのNum</span></span>
- <span data-ttu-id="6b58c-1761">
パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1761">パスポート ＃</span></span> 
- <span data-ttu-id="6b58c-1762">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="6b58c-1762">Numéro de passeport</span></span>
- <span data-ttu-id="6b58c-1763">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="6b58c-1763">Passeport n °</span></span>
- <span data-ttu-id="6b58c-1764">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1764">Passeport Non</span></span>
- <span data-ttu-id="6b58c-1765">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1765">Passeport #</span></span>
- <span data-ttu-id="6b58c-1766">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1766">Passeport#</span></span>
- <span data-ttu-id="6b58c-1767">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="6b58c-1767">PasseportNon</span></span>
- <span data-ttu-id="6b58c-1768">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="6b58c-1768">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="6b58c-1769">Französische Sozialversicherungsnummer (INSEE)</span><span class="sxs-lookup"><span data-stu-id="6b58c-1769">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1770">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1770">Format</span></span>

<span data-ttu-id="6b58c-1771">15 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1771">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1772">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1772">Pattern</span></span>

<span data-ttu-id="6b58c-1773">Muss einem von zwei Mustern entsprechen:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1773">Must match one of two patterns:</span></span>
- <span data-ttu-id="6b58c-1774">13 Stellen, gefolgt von einem Leerzeichen, gefolgt von zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1774">13 digits followed by a space followed by two digits</span></span></br>
<span data-ttu-id="6b58c-1775">oder</span><span class="sxs-lookup"><span data-stu-id="6b58c-1775">or</span></span>
- <span data-ttu-id="6b58c-1776">15 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1776">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1777">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1777">Checksum</span></span>

<span data-ttu-id="6b58c-1778">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-1778">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1779">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1779">Definition</span></span>

<span data-ttu-id="6b58c-1780">Eine DLP-Richtlinie ist zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1780">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1781">Die Funktion Func_french_insee oder Func_fr_insee sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1781">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1782">Ein Schlüsselwort aus Keyword_fr_insee wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1782">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="6b58c-1783">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1783">The checksum passes.</span></span>

<span data-ttu-id="6b58c-1784">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1785">Die Funktion Func_french_insee oder Func_fr_insee sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1785">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1786">Es wurde kein Schlüsselwort aus Keyword_fr_insee gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1786">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="6b58c-1787">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1787">The checksum passes.</span></span>

```
<!-- France INSEE -->
<Entity id="71f62b97-efe0-4aa1-aa49-e14de253619d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="95">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="1">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1788">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1788">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="6b58c-1789">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="6b58c-1789">Keyword_fr_insee</span></span>

- <span data-ttu-id="6b58c-1790">insee</span><span class="sxs-lookup"><span data-stu-id="6b58c-1790">insee</span></span>
- <span data-ttu-id="6b58c-1791">
securité sociale</span><span class="sxs-lookup"><span data-stu-id="6b58c-1791">securité sociale</span></span>
- <span data-ttu-id="6b58c-1792">
securite sociale</span><span class="sxs-lookup"><span data-stu-id="6b58c-1792">securite sociale</span></span>
- <span data-ttu-id="6b58c-1793">
national id</span><span class="sxs-lookup"><span data-stu-id="6b58c-1793">national id</span></span>
- <span data-ttu-id="6b58c-1794">
national identification</span><span class="sxs-lookup"><span data-stu-id="6b58c-1794">national identification</span></span>
- <span data-ttu-id="6b58c-1795">
numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="6b58c-1795">numéro d'identité</span></span>
- <span data-ttu-id="6b58c-1796">keine d'Identité</span><span class="sxs-lookup"><span data-stu-id="6b58c-1796">no d'identité</span></span>
- <span data-ttu-id="6b58c-p131">
no. d'identité</span><span class="sxs-lookup"><span data-stu-id="6b58c-p131">no. d'identité</span></span>
- <span data-ttu-id="6b58c-1799">
numero d'identite</span><span class="sxs-lookup"><span data-stu-id="6b58c-1799">numero d'identite</span></span>
- <span data-ttu-id="6b58c-1800">keine d'identite</span><span class="sxs-lookup"><span data-stu-id="6b58c-1800">no d'identite</span></span>
- <span data-ttu-id="6b58c-p132">
no. d'identite</span><span class="sxs-lookup"><span data-stu-id="6b58c-p132">no. d'identite</span></span>
- <span data-ttu-id="6b58c-1803">social security number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1803">social security number</span></span>
- <span data-ttu-id="6b58c-1804">
social security code</span><span class="sxs-lookup"><span data-stu-id="6b58c-1804">social security code</span></span>
- <span data-ttu-id="6b58c-1805">social insurance number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1805">social insurance number</span></span>
- <span data-ttu-id="6b58c-1806">
le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="6b58c-1806">le numéro d'identification nationale</span></span>
- <span data-ttu-id="6b58c-1807">
d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="6b58c-1807">d'identité nationale</span></span>
- <span data-ttu-id="6b58c-1808">
numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="6b58c-1808">numéro de sécurité sociale</span></span>
- <span data-ttu-id="6b58c-1809">
le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="6b58c-1809">le code de la sécurité sociale</span></span>
- <span data-ttu-id="6b58c-1810">
numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="6b58c-1810">numéro d'assurance sociale</span></span>
- <span data-ttu-id="6b58c-1811">
numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="6b58c-1811">numéro de sécu</span></span>
- <span data-ttu-id="6b58c-1812">
code sécu
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1812">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="6b58c-1813">Deutsche Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1813">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1814">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1814">Format</span></span>

<span data-ttu-id="6b58c-1815">Kombination von 11 Ziffern und Buchstaben</span><span class="sxs-lookup"><span data-stu-id="6b58c-1815">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1816">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1816">Pattern</span></span>

<span data-ttu-id="6b58c-1817">11 Zahlen und Buchstaben (ohne Beachtung der Groß-/Kleinschreibung):</span><span class="sxs-lookup"><span data-stu-id="6b58c-1817">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="6b58c-1818">Eine Ziffer oder ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="6b58c-1818">A digit or letter</span></span> 
- <span data-ttu-id="6b58c-1819">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1819">Two digits</span></span> 
- <span data-ttu-id="6b58c-1820">Sechs Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="6b58c-1820">Six digits or letters</span></span> 
- <span data-ttu-id="6b58c-1821">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1821">A digit</span></span> 
- <span data-ttu-id="6b58c-1822">Eine Ziffer oder ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="6b58c-1822">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1823">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1823">Checksum</span></span>

<span data-ttu-id="6b58c-1824">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-1824">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1825">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1825">Definition</span></span>

<span data-ttu-id="6b58c-1826">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1826">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1827">Die Funktion Func_german_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1827">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1828">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1828">At least one of the following is true:</span></span>
    - <span data-ttu-id="6b58c-1829">Ein Schlüsselwort aus Keyword_german_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1829">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="6b58c-1830">Ein Schlüsselwort aus Keyword_german_drivers_license_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1830">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="6b58c-1831">Ein Schlüsselwort aus Keyword_german_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1831">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="6b58c-1832">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1832">The checksum passes.</span></span>

```
<!-- German Driver's License Number -->
<Entity id="91da9335-1edb-45b7-a95f-5fe41a16c63c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_drivers_license_number" />
          <Match idRef="Keyword_german_drivers_license_collaborative" />
          <Match idRef="Keyword_german_drivers_license" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1833">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1833">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="6b58c-1834">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1834">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="6b58c-1835">Führerschein</span><span class="sxs-lookup"><span data-stu-id="6b58c-1835">Führerschein</span></span>
- <span data-ttu-id="6b58c-1836">
Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="6b58c-1836">Fuhrerschein</span></span>
- <span data-ttu-id="6b58c-1837">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="6b58c-1837">Fuehrerschein</span></span>
- <span data-ttu-id="6b58c-1838">
Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1838">Führerscheinnummer</span></span>
- <span data-ttu-id="6b58c-1839">
Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1839">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="6b58c-1840">
Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1840">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="6b58c-1841">
Führerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1841">Führerschein-</span></span> 
- <span data-ttu-id="6b58c-1842">Fuhrerschein-
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1842">Fuhrerschein-</span></span> 
- <span data-ttu-id="6b58c-1843">Fuehrerschein-
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1843">Fuehrerschein-</span></span> 
- <span data-ttu-id="6b58c-1844">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="6b58c-1844">FührerscheinnummerNr</span></span>
- <span data-ttu-id="6b58c-1845">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="6b58c-1845">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="6b58c-1846">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="6b58c-1846">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="6b58c-1847">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="6b58c-1847">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="6b58c-1848">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="6b58c-1848">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="6b58c-1849">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="6b58c-1849">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="6b58c-1850">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1850">Führerschein- Nr</span></span>
- <span data-ttu-id="6b58c-1851">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1851">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="6b58c-1852">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1852">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="6b58c-1853">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1853">Führerschein- Klasse</span></span> 
- <span data-ttu-id="6b58c-1854">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1854">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="6b58c-1855">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="6b58c-1855">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="6b58c-1856">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="6b58c-1856">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="6b58c-1857">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="6b58c-1857">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="6b58c-1858">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="6b58c-1858">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="6b58c-1859">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="6b58c-1859">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="6b58c-1860">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="6b58c-1860">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="6b58c-1861">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="6b58c-1861">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="6b58c-1862">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1862">Führerschein- Nr</span></span> 
- <span data-ttu-id="6b58c-1863">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1863">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="6b58c-1864">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1864">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="6b58c-1865">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1865">Führerschein- Klasse</span></span> 
- <span data-ttu-id="6b58c-1866">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1866">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="6b58c-1867">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="6b58c-1867">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="6b58c-1868">DL</span><span class="sxs-lookup"><span data-stu-id="6b58c-1868">DL</span></span> 
- <span data-ttu-id="6b58c-1869">DLS</span><span class="sxs-lookup"><span data-stu-id="6b58c-1869">DLS</span></span>
- <span data-ttu-id="6b58c-1870">
Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1870">Driv Lic</span></span> 
- <span data-ttu-id="6b58c-1871">Driv Licen
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1871">Driv Licen</span></span> 
- <span data-ttu-id="6b58c-1872">Driv License</span><span class="sxs-lookup"><span data-stu-id="6b58c-1872">Driv License</span></span>
- <span data-ttu-id="6b58c-1873">
Driv Licenses
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1873">Driv Licenses</span></span> 
- <span data-ttu-id="6b58c-1874">Driv Licence
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1874">Driv Licence</span></span> 
- <span data-ttu-id="6b58c-1875">Driv Licences
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1875">Driv Licences</span></span> 
- <span data-ttu-id="6b58c-1876">Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1876">Driv Lic</span></span> 
- <span data-ttu-id="6b58c-1877">Driver Licen
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1877">Driver Licen</span></span> 
- <span data-ttu-id="6b58c-1878">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-1878">Driver License</span></span> 
- <span data-ttu-id="6b58c-1879">Treiber-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-1879">Driver Licenses</span></span> 
- <span data-ttu-id="6b58c-1880">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1880">Driver Licence</span></span> 
- <span data-ttu-id="6b58c-1881">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1881">Driver Licences</span></span> 
- <span data-ttu-id="6b58c-1882">Treiber Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-1882">Drivers Lic</span></span> 
- <span data-ttu-id="6b58c-1883">Treiber Licen</span><span class="sxs-lookup"><span data-stu-id="6b58c-1883">Drivers Licen</span></span> 
- <span data-ttu-id="6b58c-1884">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-1884">Drivers License</span></span> 
- <span data-ttu-id="6b58c-1885">Treiber-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-1885">Drivers Licenses</span></span> 
- <span data-ttu-id="6b58c-1886">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-1886">Drivers Licence</span></span> 
- <span data-ttu-id="6b58c-1887">Treiber-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-1887">Drivers Licences</span></span> 
- <span data-ttu-id="6b58c-1888">Des Treibers Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-1888">Driver's Lic</span></span> 
- <span data-ttu-id="6b58c-1889">Driver's Licen
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1889">Driver's Licen</span></span> 
- <span data-ttu-id="6b58c-1890">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-1890">Driver's License</span></span> 
- <span data-ttu-id="6b58c-1891">Des Treibers Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-1891">Driver's Licenses</span></span> 
- <span data-ttu-id="6b58c-1892">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1892">Driver's Licence</span></span> 
- <span data-ttu-id="6b58c-1893">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1893">Driver's Licences</span></span> 
- <span data-ttu-id="6b58c-1894">Driving Lic
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1894">Driving Lic</span></span> 
- <span data-ttu-id="6b58c-1895">Driving Licen
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1895">Driving Licen</span></span> 
- <span data-ttu-id="6b58c-1896">Driving License
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1896">Driving License</span></span> 
- <span data-ttu-id="6b58c-1897">Driving Licenses
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1897">Driving Licenses</span></span> 
- <span data-ttu-id="6b58c-1898">Driving Licence

</span><span class="sxs-lookup"><span data-stu-id="6b58c-1898">Driving Licence</span></span> 
- <span data-ttu-id="6b58c-1899">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="6b58c-1899">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="6b58c-1900">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="6b58c-1900">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="6b58c-1901">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1901">Nr-Führerschein</span></span> 
- <span data-ttu-id="6b58c-1902">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1902">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="6b58c-1903">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1903">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="6b58c-1904">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1904">No-Führerschein</span></span> 
- <span data-ttu-id="6b58c-1905">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1905">No-Fuhrerschein</span></span> 
- <span data-ttu-id="6b58c-1906">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1906">No-Fuehrerschein</span></span> 
- <span data-ttu-id="6b58c-1907">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1907">N-Führerschein</span></span> 
- <span data-ttu-id="6b58c-1908">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1908">N-Fuhrerschein</span></span> 
- <span data-ttu-id="6b58c-1909">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="6b58c-1909">N-Fuehrerschein</span></span>
- <span data-ttu-id="6b58c-1910">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1910">Nr-Führerschein</span></span> 
- <span data-ttu-id="6b58c-1911">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1911">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="6b58c-1912">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1912">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="6b58c-1913">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1913">No-Führerschein</span></span> 
- <span data-ttu-id="6b58c-1914">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1914">No-Fuhrerschein</span></span> 
- <span data-ttu-id="6b58c-1915">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1915">No-Fuehrerschein</span></span> 
- <span data-ttu-id="6b58c-1916">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1916">N-Führerschein</span></span> 
- <span data-ttu-id="6b58c-1917">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1917">N-Fuhrerschein</span></span> 
- <span data-ttu-id="6b58c-1918">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="6b58c-1918">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="6b58c-1919">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="6b58c-1919">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="6b58c-1920">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="6b58c-1920">ausstellungsdatum</span></span>
- <span data-ttu-id="6b58c-1921">
Ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="6b58c-1921">ausstellungsort</span></span>
- <span data-ttu-id="6b58c-1922">
Ausstellende Behöde</span><span class="sxs-lookup"><span data-stu-id="6b58c-1922">ausstellende behöde</span></span>
- <span data-ttu-id="6b58c-1923">
Ausstellende Behorde</span><span class="sxs-lookup"><span data-stu-id="6b58c-1923">ausstellende behorde</span></span>
- <span data-ttu-id="6b58c-1924">

Ausstellende Behoerde</span><span class="sxs-lookup"><span data-stu-id="6b58c-1924">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="6b58c-1925">Deutsche Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1925">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1926">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1926">Format</span></span>

<span data-ttu-id="6b58c-1927">10 Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="6b58c-1927">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1928">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1928">Pattern</span></span>

<span data-ttu-id="6b58c-1929">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1929">Pattern must include all of the following:</span></span>
- <span data-ttu-id="6b58c-1930">Das erste Zeichen ist eine Ziffer oder ein Buchstabe aus dieser Gruppe (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="6b58c-1930">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="6b58c-1931">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1931">Three digits</span></span> 
- <span data-ttu-id="6b58c-1932">Fünf Ziffern oder Buchstaben aus dieser Gruppe (C -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="6b58c-1932">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="6b58c-1933">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1933">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1934">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1934">Checksum</span></span>

<span data-ttu-id="6b58c-1935">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-1935">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1936">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1936">Definition</span></span>

<span data-ttu-id="6b58c-1937">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1937">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1938">Die Funktion Func_german_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1938">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1939">Ein Schlüsselwort aus einer der fünf Schlüsselwortlisten wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1939">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="6b58c-1940">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1940">The checksum passes.</span></span>

<span data-ttu-id="6b58c-1941">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1941">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1942">Die Funktion Func_german_passport_data findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1942">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1943">Ein Schlüsselwort aus einer der fünf Schlüsselwortlisten wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1943">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="6b58c-1944">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1944">The checksum passes.</span></span>

```
<!-- German Passport Number -->
<Entity id="2e3da144-d42b-47ed-b123-fbf78604e52c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_german_passport" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_passport_data" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1945">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1945">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="6b58c-1946">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-1946">Keyword_german_passport</span></span>

- <span data-ttu-id="6b58c-1947">Reisepass</span><span class="sxs-lookup"><span data-stu-id="6b58c-1947">reisepass</span></span>
- <span data-ttu-id="6b58c-1948">
Reisepasse</span><span class="sxs-lookup"><span data-stu-id="6b58c-1948">reisepasse</span></span>
- <span data-ttu-id="6b58c-1949">
Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1949">reisepassnummer</span></span>
- <span data-ttu-id="6b58c-1950">passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-1950">passport</span></span>
- <span data-ttu-id="6b58c-1951">

passports</span><span class="sxs-lookup"><span data-stu-id="6b58c-1951">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="6b58c-1952">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="6b58c-1952">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="6b58c-1953">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="6b58c-1953">geburtsdatum</span></span>
- <span data-ttu-id="6b58c-1954">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="6b58c-1954">ausstellungsdatum</span></span>
- <span data-ttu-id="6b58c-1955">
Ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="6b58c-1955">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="6b58c-1956">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-1956">Keyword_german_passport_number</span></span>

<span data-ttu-id="6b58c-1957">Nicht-Reisepass Nr.-Reisepass</span><span class="sxs-lookup"><span data-stu-id="6b58c-1957">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="6b58c-1958">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="6b58c-1958">Keyword_german_passport1</span></span>

<span data-ttu-id="6b58c-1959">Reisepass-Nr
</span><span class="sxs-lookup"><span data-stu-id="6b58c-1959">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="6b58c-1960">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="6b58c-1960">Keyword_german_passport2</span></span>

<span data-ttu-id="6b58c-1961">bnationalit.t</span><span class="sxs-lookup"><span data-stu-id="6b58c-1961">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="6b58c-1962">Deutsche Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1962">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1963">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1963">Format</span></span>

<span data-ttu-id="6b58c-1964">Seit dem 1. November 2010: neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1964">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="6b58c-1965">Aus dem 1. April 1987 bis 31 Oktober 2010:10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1965">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1966">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1966">Pattern</span></span>

<span data-ttu-id="6b58c-1967">Seit 1. November 2010:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1967">Since 1 November 2010:</span></span>
- <span data-ttu-id="6b58c-1968">Ein Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="6b58c-1968">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-1969">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1969">Eight digits</span></span>

<span data-ttu-id="6b58c-1970">Aus dem 1. April 1987 bis 31. Oktober 2010:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1970">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="6b58c-1971">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1971">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1972">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1972">Checksum</span></span>

<span data-ttu-id="6b58c-1973">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-1973">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-1974">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-1974">Definition</span></span>

<span data-ttu-id="6b58c-1975">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-1975">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-1976">Der reguläre Ausdruck Regex_germany_id_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1976">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-1977">Ein Schlüsselwort aus Keyword_germany_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-1977">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-1978">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-1978">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="6b58c-1979">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="6b58c-1979">Keyword_germany_id_card</span></span>

- <span data-ttu-id="6b58c-1980">Identity Card</span><span class="sxs-lookup"><span data-stu-id="6b58c-1980">Identity Card</span></span>
- <span data-ttu-id="6b58c-1981">ID</span><span class="sxs-lookup"><span data-stu-id="6b58c-1981">ID</span></span>
- <span data-ttu-id="6b58c-1982">Identification</span><span class="sxs-lookup"><span data-stu-id="6b58c-1982">Identification</span></span>
- <span data-ttu-id="6b58c-1983">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-1983">Personalausweis</span></span>
- <span data-ttu-id="6b58c-1984">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-1984">Identifizierungsnummer</span></span>
- <span data-ttu-id="6b58c-1985">Ausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-1985">Ausweis</span></span>
- <span data-ttu-id="6b58c-1986">Identifikation</span><span class="sxs-lookup"><span data-stu-id="6b58c-1986">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="6b58c-1987">Griechenland – Personalausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-1987">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-1988">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-1988">Format</span></span>

<span data-ttu-id="6b58c-1989">Kombination von 7-8 Buchstaben und Zahlen plus einem Gedankenstrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-1989">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-1990">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-1990">Pattern</span></span>

<span data-ttu-id="6b58c-1991">Sieben Buchstaben und Zahlen (altes Format):</span><span class="sxs-lookup"><span data-stu-id="6b58c-1991">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="6b58c-1992">Ein Buchstabe (jeder Buchstabe des griechischen Alphabets) </span><span class="sxs-lookup"><span data-stu-id="6b58c-1992">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="6b58c-1993">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-1993">A dash</span></span> 
- <span data-ttu-id="6b58c-1994">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1994">Six digits</span></span>

<span data-ttu-id="6b58c-1995">Acht Buchstaben und Zahlen (neues Format):</span><span class="sxs-lookup"><span data-stu-id="6b58c-1995">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="6b58c-1996">Zwei Buchstaben, deren Großbuchstabe sowohl im griechischen als auch lateinischen Alphabet (ABEZHIKMNOPTYX) vorkommt </span><span class="sxs-lookup"><span data-stu-id="6b58c-1996">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="6b58c-1997">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-1997">A dash</span></span> 
- <span data-ttu-id="6b58c-1998">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-1998">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-1999">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-1999">Checksum</span></span>

<span data-ttu-id="6b58c-2000">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2000">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2001">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2001">Definition</span></span>

<span data-ttu-id="6b58c-2002">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2002">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2003">Der reguläre Ausdruck Regex_greece_id_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2003">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2004">Ein Schlüsselwort aus Keyword_greece_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2004">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2005">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2005">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="6b58c-2006">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2006">Keyword_greece_id_card</span></span>

- <span data-ttu-id="6b58c-2007">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2007">Greek identity Card</span></span>
- <span data-ttu-id="6b58c-2008">Tautotita</span><span class="sxs-lookup"><span data-stu-id="6b58c-2008">Tautotita</span></span>
- <span data-ttu-id="6b58c-2009">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="6b58c-2009">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="6b58c-2010">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="6b58c-2010">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="6b58c-2011">Hongkong (HKID) - Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2011">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2012">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2012">Format</span></span>

<span data-ttu-id="6b58c-2013">Kombination aus 8-9Buchstaben und Zahlen sowie optionale Klammern um das letzte Zeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-2013">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2014">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2014">Pattern</span></span>

<span data-ttu-id="6b58c-2015">Kombination aus Buchstaben 8-9 Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2015">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="6b58c-2016">1-2 Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2016">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-2017">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2017">Six digits</span></span> 
- <span data-ttu-id="6b58c-2018">Das letzte Zeichen (eine Ziffer oder der Buchstabe A), bei dem es sich um die Prüfziffer handelt, die optional in Klammern eingeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2018">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2019">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2019">Checksum</span></span>

<span data-ttu-id="6b58c-2020">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2020">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2021">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2021">Definition</span></span>

<span data-ttu-id="6b58c-2022">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2022">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2023">Die Funktion Func_hong_kong_id_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2023">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2024">Ein Schlüsselwort aus Keyword_hong_kong_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2024">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="6b58c-2025">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2025">The checksum passes.</span></span>

<span data-ttu-id="6b58c-2026">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2026">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2027">Die Funktion Func_hong_kong_id_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2027">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2028">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2028">The checksum passes.</span></span>

```
<!-- Hong Kong Identity Card (HKID) number -->
<Entity id="e63c28a7-ad29-4c17-a41a-3d2a0b70fd9c" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_hong_kong_id_card"/>
     <Match idRef="Keyword_hong_kong_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_hong_kong_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2029">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2029">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="6b58c-2030">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2030">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="6b58c-2031">Hong Kong Identity Card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2031">Hong Kong Identity Card</span></span>
- <span data-ttu-id="6b58c-2032">HKID</span><span class="sxs-lookup"><span data-stu-id="6b58c-2032">HKID</span></span>
- <span data-ttu-id="6b58c-2033">ID card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2033">ID card</span></span>
- <span data-ttu-id="6b58c-2034">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2034">香港身份證</span></span> 
- <span data-ttu-id="6b58c-2035">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2035">香港永久性居民身份證</span></span> 
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="6b58c-2036">Indien – Permanente Kontonummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2036">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2037">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2037">Format</span></span>

<span data-ttu-id="6b58c-2038">10 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2038">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2039">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2039">Pattern</span></span>

<span data-ttu-id="6b58c-2040">10 Buchstaben oder Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2040">10 letters or digits:</span></span>
- <span data-ttu-id="6b58c-2041">Fünf Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2041">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-2042">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2042">Four digits</span></span> 
- <span data-ttu-id="6b58c-2043">Ein Buchstabe, der eine alphabetische Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="6b58c-2043">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2044">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2044">Checksum</span></span>

<span data-ttu-id="6b58c-2045">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2045">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2046">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2046">Definition</span></span>

<span data-ttu-id="6b58c-2047">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2047">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2048">Der reguläre Ausdruck Regex_india_permanent_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2048">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2049">Ein Schlüsselwort aus Keyword_india_permanent_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2049">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="6b58c-2050">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2050">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2051">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2051">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="6b58c-2052">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2052">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="6b58c-2053">Permanent Account Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2053">Permanent Account Number</span></span> 
- <span data-ttu-id="6b58c-2054">PAN
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2054">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="6b58c-2055">Indien - Eindeutige Identifikationsnummer (Aadhaar)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2055">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2056">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2056">Format</span></span>

<span data-ttu-id="6b58c-2057">12 Ziffern mit optionalen Leerzeichen oder Bindestrichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-2057">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2058">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2058">Pattern</span></span>

<span data-ttu-id="6b58c-2059">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2059">12 digits:</span></span>
- <span data-ttu-id="6b58c-2060">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2060">Four digits</span></span> 
- <span data-ttu-id="6b58c-2061">Eine optionales Leerzeichen oder ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-2061">An optional space or dash</span></span> 
- <span data-ttu-id="6b58c-2062">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2062">Four digits</span></span> 
- <span data-ttu-id="6b58c-2063">Eine optionales Leerzeichen oder ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-2063">An optional space or dash</span></span> 
- <span data-ttu-id="6b58c-2064">Die letzte Ziffer, die eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="6b58c-2064">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2065">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2065">Checksum</span></span>

<span data-ttu-id="6b58c-2066">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2066">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2067">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2067">Definition</span></span>

<span data-ttu-id="6b58c-p133">Eine DLP-Richtlinie ist 85 % sicher, dass diese Art von vertraulichen Informationen festgestellt wurde "If"; innerhalb einer Nähe von 300 Zeichen: die Funktion Func_india_aadhaar sucht nach Inhalten, die dem Muster entspricht. Ein Schlüsselwort aus Keyword_india_aadhar gefunden wird. Die Prüfsumme übergibt. Eine DLP-Richtlinie ist 75 % sicher, dass diese Art von vertraulichen Informationen festgestellt wurde "If"; innerhalb einer Nähe von 300 Zeichen: die Funktion Func_india_aadhaar sucht nach Inhalten, die dem Muster entspricht. Die Prüfsumme übergibt. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="6b58c-p133">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. A keyword from Keyword_india_aadhar is found. The checksum passes. A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. The checksum passes. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span></span>

### <a name="keywords"></a><span data-ttu-id="6b58c-2074">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2074">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="6b58c-2075">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="6b58c-2075">Keyword_india_aadhar</span></span>
- <span data-ttu-id="6b58c-2076">Aadhar</span><span class="sxs-lookup"><span data-stu-id="6b58c-2076">Aadhar</span></span>
- <span data-ttu-id="6b58c-2077">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="6b58c-2077">Aadhaar</span></span>
- <span data-ttu-id="6b58c-2078">UID</span><span class="sxs-lookup"><span data-stu-id="6b58c-2078">UID</span></span>
- <span data-ttu-id="6b58c-2079">आधार</span><span class="sxs-lookup"><span data-stu-id="6b58c-2079">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="6b58c-2080">Indonesien – Perosonalausweisnummer (KTP)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2080">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2081">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2081">Format</span></span>

<span data-ttu-id="6b58c-2082">16 Ziffern mit optionalen Punkten</span><span class="sxs-lookup"><span data-stu-id="6b58c-2082">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2083">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2083">Pattern</span></span>

<span data-ttu-id="6b58c-2084">16 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2084">16 digits:</span></span>
- <span data-ttu-id="6b58c-2085">Zweistelliger Provinzcode </span><span class="sxs-lookup"><span data-stu-id="6b58c-2085">Two-digit province code</span></span> 
- <span data-ttu-id="6b58c-2086">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2086">A period (optional)</span></span> 
- <span data-ttu-id="6b58c-2087">Zweistelliger Regency- oder Stadtcode </span><span class="sxs-lookup"><span data-stu-id="6b58c-2087">Two-digit regency or city code</span></span> 
- <span data-ttu-id="6b58c-2088">Zweistelliger Subdistrict-Code </span><span class="sxs-lookup"><span data-stu-id="6b58c-2088">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="6b58c-2089">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2089">A period (optional)</span></span> 
- <span data-ttu-id="6b58c-2090">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="6b58c-2090">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="6b58c-2091">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2091">A period (optional)</span></span> 
- <span data-ttu-id="6b58c-2092">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2092">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2093">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2093">Checksum</span></span>

<span data-ttu-id="6b58c-2094">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2094">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2095">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2095">Definition</span></span>

<span data-ttu-id="6b58c-2096">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2096">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2097">Der reguläre Ausdruck Regex_indonesia_id_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2097">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2098">Ein Schlüsselwort aus Keyword_indonesia_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2098">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="6b58c-2099">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2099">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2100">Der reguläre Ausdruck Regex_indonesia_id_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2100">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

```
<!-- Indonesia Identity Card (KTP) Number -->
<Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_indonesia_id_card"/>
     <Match idRef="Keyword_indonesia_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_indonesia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2101">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2101">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="6b58c-2102">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2102">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="6b58c-2103">KTP</span><span class="sxs-lookup"><span data-stu-id="6b58c-2103">KTP</span></span>
- <span data-ttu-id="6b58c-2104">Kartu Tanda Penduduk
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2104">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="6b58c-2105">Nomor Induk Kependudukan
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2105">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="6b58c-2106">International Banking Account Number (IBAN)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2106">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2107">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2107">Format</span></span>

<span data-ttu-id="6b58c-2108">Landeskennzahl (zwei Buchstaben) plus Prüfziffern (zwei Ziffern) plus BBAN (bis zu 30 Zeichen)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2108">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2109">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2109">Pattern</span></span>

<span data-ttu-id="6b58c-2110">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2110">Pattern must include all of the following:</span></span>

- <span data-ttu-id="6b58c-2111">Einen aus zwei Buchstaben bestehenden Ländercode</span><span class="sxs-lookup"><span data-stu-id="6b58c-2111">Two-letter country code</span></span>
- <span data-ttu-id="6b58c-2112">Zwei Prüfziffern (gefolgt von einem optionalen Leerzeichen) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2112">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="6b58c-2113">1 bis 7 Gruppen aus vier Buchstaben oder Ziffern, getrennt durch optionale Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-2113">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="6b58c-2114">1 bis 3 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2114">1-3 letters or digits</span></span>

<span data-ttu-id="6b58c-p134">Das Format jedes Landes ist etwas anders. IBAN als Typ vertraulicher Informationen deckt folgende 60 Länder ab:</span><span class="sxs-lookup"><span data-stu-id="6b58c-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="6b58c-2117">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="6b58c-2117">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2118">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2118">Checksum</span></span>

<span data-ttu-id="6b58c-2119">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2119">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2120">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2120">Definition</span></span>

<span data-ttu-id="6b58c-2121">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2121">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2122">Die Funktion Func_iban findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2122">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2123">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2123">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2124">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2124">Keywords</span></span>

<span data-ttu-id="6b58c-2125">Keine</span><span class="sxs-lookup"><span data-stu-id="6b58c-2125">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="6b58c-2126">IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="6b58c-2126">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2127">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2127">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="6b58c-2128">IPv4:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2128">IPv4:</span></span>
<span data-ttu-id="6b58c-2129">Komplexes Muster, das formatierte (Punkte) und unformatierte (keine Punkte) Versionen der IPv4-Adressen angibt</span><span class="sxs-lookup"><span data-stu-id="6b58c-2129">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="6b58c-2130">IPv6:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2130">IPv6:</span></span>
<span data-ttu-id="6b58c-2131"> Komplexes Muster, das formatierte IPv6-Nummern angibt (schließt Doppelpunkte ein)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2131">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2132">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2132">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2133">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2133">Checksum</span></span>

<span data-ttu-id="6b58c-2134">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2134">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2135">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2135">Definition</span></span>

<span data-ttu-id="6b58c-2136">Für IPv6 ist eine DLP-Richtlinie zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2136">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2137">Der reguläre Ausdruck Regex_ipv6_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2137">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2138">Es wurde kein Schlüsselwort aus Keyword_ipaddress gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2138">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="6b58c-2139">Für IPv4 ist eine DLP-Richtlinie zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2139">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2140">Der reguläre Ausdruck Regex_ipv4_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2140">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2141">Ein Schlüsselwort aus Keyword_ipaddress wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2141">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="6b58c-2142">Für IPv6 ist eine DLP-Richtlinie zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2142">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2143">Der reguläre Ausdruck Regex_ipv6_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2143">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2144">Es wurde kein Schlüsselwort aus Keyword_ipaddress gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2144">No keyword from Keyword_ipaddress is found.</span></span>

```
    <!-- IP Address -->
    <Entity id="1daa4ad5-e2dd-4ca4-a788-54722c09efb2" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv4_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2145">Keywords</span><span class="sxs-lookup"><span data-stu-id="6b58c-2145">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="6b58c-2146">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="6b58c-2146">Keyword_ipaddress</span></span>

- <span data-ttu-id="6b58c-2147">IP (bei diesem Schlüsselwort wird die Groß-/Kleinschreibung unterschieden)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2147">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="6b58c-2148">ip address
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2148">ip address</span></span> 
- <span data-ttu-id="6b58c-2149">IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="6b58c-2149">ip addresses</span></span>
- <span data-ttu-id="6b58c-2150">internet protocol</span><span class="sxs-lookup"><span data-stu-id="6b58c-2150">internet protocol</span></span>
- <span data-ttu-id="6b58c-2151">
IP-כתובת ה
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2151">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="6b58c-2152">Internationale Klassifikation Krankheiten (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2152">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2153">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2153">Format</span></span>

<span data-ttu-id="6b58c-2154">Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="6b58c-2154">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2155">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2155">Pattern</span></span>

<span data-ttu-id="6b58c-2156">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="6b58c-2156">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2157">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2157">Checksum</span></span>

<span data-ttu-id="6b58c-2158">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2158">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2159">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2159">Definition</span></span>

<span data-ttu-id="6b58c-2160">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2160">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2161">Ein Schlüsselwort aus Dictionary_icd_10_cm gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2161">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="6b58c-2162">Keywords</span><span class="sxs-lookup"><span data-stu-id="6b58c-2162">Keywords</span></span>

<span data-ttu-id="6b58c-p135">Jedem anderen Begriff aus dem Dictionary_icd_10_cm Schlüsselwort Wörterbuch der [International Klassifizierung der Krankheiten, Zehntelsekunde Version klinischer Änderung (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604)basiert. Dieses Typs sucht nur nach dem Begriff, nicht die Versicherungsvertreter Codes.</span><span class="sxs-lookup"><span data-stu-id="6b58c-p135">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="6b58c-2165">Internationale Klassifikation Krankheiten (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2165">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2166">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2166">Format</span></span>

<span data-ttu-id="6b58c-2167">Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="6b58c-2167">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2168">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2168">Pattern</span></span>

<span data-ttu-id="6b58c-2169">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="6b58c-2169">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2170">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2170">Checksum</span></span>

<span data-ttu-id="6b58c-2171">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2172">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2172">Definition</span></span>

<span data-ttu-id="6b58c-2173">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2173">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2174">Ein Schlüsselwort aus Dictionary_icd_9_cm gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2174">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2175">Keywords</span><span class="sxs-lookup"><span data-stu-id="6b58c-2175">Keywords</span></span>

<span data-ttu-id="6b58c-p136">Jedem anderen Begriff aus dem Dictionary_icd_9_cm Schlüsselwort Wörterbuch der [International Klassifizierung der Krankheiten, neunte Version klinischer Änderung (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605)basiert. Dieses Typs sucht nur nach dem Begriff, nicht die Versicherungsvertreter Codes.</span><span class="sxs-lookup"><span data-stu-id="6b58c-p136">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="6b58c-2178">Irland – Personal Public Service-Nummer (PPS)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2178">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2179">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2179">Format</span></span>

<span data-ttu-id="6b58c-2180">Altes Format (bis zum 31. Dezember 2012):</span><span class="sxs-lookup"><span data-stu-id="6b58c-2180">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="6b58c-2181">Sieben Ziffern, gefolgt von 1-2 Buchstaben </span><span class="sxs-lookup"><span data-stu-id="6b58c-2181">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="6b58c-2182">Neue Format (1. Januar 2013 und nach):</span><span class="sxs-lookup"><span data-stu-id="6b58c-2182">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="6b58c-2183">Sieben Ziffern, gefolgt von zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="6b58c-2183">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2184">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2184">Pattern</span></span>

<span data-ttu-id="6b58c-2185">Altes Format (bis zum 31. Dezember 2012):</span><span class="sxs-lookup"><span data-stu-id="6b58c-2185">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="6b58c-2186">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="6b58c-2186">Seven digits</span></span> 
- <span data-ttu-id="6b58c-2187">1-2 Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2187">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="6b58c-2188">Neue Format (1. Januar 2013 und nach):</span><span class="sxs-lookup"><span data-stu-id="6b58c-2188">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="6b58c-2189">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="6b58c-2189">Seven digits</span></span> 
- <span data-ttu-id="6b58c-2190">Ein Buchstabe (Groß-/Kleinschreibung irrelevant), wobei es sich um eine alphabetische Prüfziffer handelt </span><span class="sxs-lookup"><span data-stu-id="6b58c-2190">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="6b58c-2191">Die Buchstaben "A" oder "H" (Groß-/Kleinschreibung irrelevant)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2191">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2192">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2192">Checksum</span></span>

<span data-ttu-id="6b58c-2193">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2194">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2194">Definition</span></span>

<span data-ttu-id="6b58c-2195">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2196">Die Funktion Func_ireland_pps findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2196">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2197">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2197">One of the following is true:</span></span>
    - <span data-ttu-id="6b58c-2198">Ein Schlüsselwort aus Keyword_ireland_pps wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2198">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="6b58c-2199">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2199">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="6b58c-2200">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2200">The checksum passes.</span></span>

<span data-ttu-id="6b58c-2201">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2201">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2202">Die Funktion Func_ireland_pps findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2202">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2203">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2203">The checksum passes.</span></span>

```
<!-- Ireland Personal Public Service (PPS) Number -->
<Entity id="1cdb674d-c19a-4fcf-9f4b-7f56cc87345a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_ireland_pps"/>
     <Any minMatches="1">
  <Match idRef="Keyword_ireland_pps"/>
  <Match idRef="Func_eu_date"/>
     </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_ireland_pps"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2204">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2204">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="6b58c-2205">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="6b58c-2205">Keyword_ireland_pps</span></span>

- <span data-ttu-id="6b58c-2206">Personal Public Service Number 
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2206">Personal Public Service Number</span></span> 
- <span data-ttu-id="6b58c-2207">PPS Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2207">PPS Number</span></span> 
- <span data-ttu-id="6b58c-2208">PPS Num
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2208">PPS Num</span></span> 
- <span data-ttu-id="6b58c-2209">PPS No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2209">PPS No.</span></span> 
- <span data-ttu-id="6b58c-2210">PPS #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2210">PPS #</span></span> 
- <span data-ttu-id="6b58c-2211">PPS-</span><span class="sxs-lookup"><span data-stu-id="6b58c-2211">PPS#</span></span> 
- <span data-ttu-id="6b58c-2212">PPSN
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2212">PPSN</span></span> 
- <span data-ttu-id="6b58c-2213">Public Services Card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2213">Public Services Card</span></span> 
- <span data-ttu-id="6b58c-2214">Uimhir Phearsanta Seirbhíse Poiblí
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2214">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="6b58c-p137">Uimh. PSP
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p137">Uimh. PSP</span></span> 
- <span data-ttu-id="6b58c-2217">PSP
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2217">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="6b58c-2218">Israelische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2218">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2219">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2219">Format</span></span>

<span data-ttu-id="6b58c-2220">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2220">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2221">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2221">Pattern</span></span>

<span data-ttu-id="6b58c-2222">Formatiert:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2222">Formatted:</span></span>
- <span data-ttu-id="6b58c-2223">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2223">Two digits</span></span> 
- <span data-ttu-id="6b58c-2224">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-2224">A dash</span></span> 
- <span data-ttu-id="6b58c-2225">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2225">Three digits</span></span> 
- <span data-ttu-id="6b58c-2226">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-2226">A dash</span></span> 
- <span data-ttu-id="6b58c-2227">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2227">Eight digits</span></span>

<span data-ttu-id="6b58c-2228">Unformatiert:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2228">Unformatted:</span></span>
- <span data-ttu-id="6b58c-2229">	13 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2229">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2230">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2230">Checksum</span></span>

<span data-ttu-id="6b58c-2231">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2231">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2232">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2232">Definition</span></span>

<span data-ttu-id="6b58c-2233">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2234">Der reguläre Ausdruck Regex_israel_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2234">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2235">Ein Schlüsselwort aus Keyword_israel_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2235">A keyword from Keyword_israel_bank_account_number is found.</span></span>

```
<!-- Israel Bank Account Number -->
<Entity id="7d08b2ff-a0b9-437f-957c-aeddbf9b2b25" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_israel_bank_account_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_israel_bank_account_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2236">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2236">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="6b58c-2237">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2237">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="6b58c-2238">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2238">Bank Account Number</span></span> 
- <span data-ttu-id="6b58c-2239">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2239">Bank Account</span></span> 
- <span data-ttu-id="6b58c-2240">Account Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2240">Account Number</span></span> 
- <span data-ttu-id="6b58c-2241">מספר חשבון בנק
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2241">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="6b58c-2242">Israelische Ausweis-ID</span><span class="sxs-lookup"><span data-stu-id="6b58c-2242">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2243">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2243">Format</span></span>

<span data-ttu-id="6b58c-2244">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2245">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2245">Pattern</span></span>

<span data-ttu-id="6b58c-2246">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2247">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2247">Checksum</span></span>

<span data-ttu-id="6b58c-2248">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2248">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2249">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2249">Definition</span></span>

<span data-ttu-id="6b58c-2250">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2251">Die Funktion Func_israeli_national_id_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2251">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2252">Ein Schlüsselwort aus Keyword_Israel_National_ID wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2252">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="6b58c-2253">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2253">The checksum passes.</span></span>

```
<!-- Israel National ID Number -->
<Entity id="e05881f5-1db1-418c-89aa-a3ac5c5277ee" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_israeli_national_id_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_Israel_National_ID" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2254">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2254">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="6b58c-2255">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="6b58c-2255">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="6b58c-2256">מספר זהות
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2256">מספר זהות</span></span> 
- <span data-ttu-id="6b58c-2257">National ID Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2257">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="6b58c-2258">Italienische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2258">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2259">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2259">Format</span></span>

<span data-ttu-id="6b58c-2260">Eine Kombination von 10 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2260">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2261">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2261">Pattern</span></span>

- <span data-ttu-id="6b58c-2262">Eine Kombination aus 10 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2262">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="6b58c-2263">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2263">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-2264">Der Buchstabe „A“ oder „W“ (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2264">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-2265">Sieben Buchstaben (ohne Beachtung der Groß-/Kleinschreibung), Ziffern oder der Unterstrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-2265">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="6b58c-2266">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2266">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2267">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2267">Checksum</span></span>

<span data-ttu-id="6b58c-2268">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2269">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2269">Definition</span></span>

<span data-ttu-id="6b58c-2270">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2271">Der reguläre Ausdruck Regex_italy_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2271">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2272">Ein Schlüsselwort aus Keyword_italy_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2272">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

```
<!-- Italy Driver's license Number -->
<Entity id="97d6244f-9157-41bd-8e0c-9d669a5c4d71" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_italy_drivers_license_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_italy_drivers_license_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2273">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2273">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="6b58c-2274">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2274">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="6b58c-2275">numero di patente di guida
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2275">numero di patente di guida</span></span> 
- <span data-ttu-id="6b58c-2276">patente di guida
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2276">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="6b58c-2277">Japanische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2277">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2278">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2278">Format</span></span>

<span data-ttu-id="6b58c-2279">Sieben oder acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2279">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2280">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2280">Pattern</span></span>

<span data-ttu-id="6b58c-2281">Bankkontonummer:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2281">Bank account number:</span></span>
- <span data-ttu-id="6b58c-2282">Sieben oder acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2282">Seven or eight digits</span></span>
- <span data-ttu-id="6b58c-2283">Niederlassungscode der Bank:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2283">Bank account branch code:</span></span>
- <span data-ttu-id="6b58c-2284">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2284">Four digits</span></span> 
- <span data-ttu-id="6b58c-2285">Ein Leerzeichen oder ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2285">A space or dash (optional)</span></span> 
- <span data-ttu-id="6b58c-2286">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2286">Three digits</span></span>

<span data-ttu-id="6b58c-2287">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2287">Checksum</span></span>

<span data-ttu-id="6b58c-2288">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2288">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2289">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2289">Definition</span></span>

<span data-ttu-id="6b58c-2290">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2290">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2291">Die Funktion Func_jp_bank_account findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2291">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2292">Ein Schlüsselwort aus Keyword_jp_bank_account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2292">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="6b58c-2293">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2293">One of the following is true:</span></span>
- <span data-ttu-id="6b58c-2294">Die Funktion Func_jp_bank_account_branch_code findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2294">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2295">Ein Schlüsselwort aus Keyword_jp_bank_branch_code wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2295">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="6b58c-2296">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2296">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2297">Die Funktion Func_jp_bank_account findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2297">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2298">Ein Schlüsselwort aus Keyword_jp_bank_account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2298">A keyword from Keyword_jp_bank_account is found.</span></span>

```
<!-- Japan Bank Account Number -->
<Entity id="d354f95b-96ee-4b80-80bc-4377312b55bc" patternsProximity="300" recommendedConfidence="75">
  <Version minEngineVersion="15.01.0131.000">
    <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_jp_bank_account" />
          <Match idRef="Keyword_jp_bank_account" />
          <Any minMatches="1">
            <Match idRef="Func_jp_bank_account_branch_code" />
            <Match idRef="Keyword_jp_bank_branch_code" />
          </Any>
      </Pattern>
  </Version>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_bank_account" />
        <Match idRef="Keyword_jp_bank_account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2299">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2299">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="6b58c-2300">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="6b58c-2300">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="6b58c-2301">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2301">Checking Account Number</span></span> 
- <span data-ttu-id="6b58c-2302">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2302">Checking Account</span></span> 
- <span data-ttu-id="6b58c-2303">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2303">Checking Account #</span></span> 
- <span data-ttu-id="6b58c-2304">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2304">Checking Acct Number</span></span> 
- <span data-ttu-id="6b58c-2305">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2305">Checking Acct #</span></span> 
- <span data-ttu-id="6b58c-2306">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2306">Checking Acct No.</span></span> 
- <span data-ttu-id="6b58c-2307">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2307">Checking Account No.</span></span> 
- <span data-ttu-id="6b58c-2308">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2308">Bank Account Number</span></span> 
- <span data-ttu-id="6b58c-2309">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2309">Bank Account</span></span> 
- <span data-ttu-id="6b58c-2310">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2310">Bank Account #</span></span> 
- <span data-ttu-id="6b58c-2311">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2311">Bank Acct Number</span></span> 
- <span data-ttu-id="6b58c-2312">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2312">Bank Acct #</span></span> 
- <span data-ttu-id="6b58c-2313">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2313">Bank Acct No.</span></span> 
- <span data-ttu-id="6b58c-2314">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2314">Bank Account No.</span></span> 
- <span data-ttu-id="6b58c-2315">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2315">Savings Account Number</span></span> 
- <span data-ttu-id="6b58c-2316">Einsparungen Konto</span><span class="sxs-lookup"><span data-stu-id="6b58c-2316">Savings Account</span></span> 
- <span data-ttu-id="6b58c-2317">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2317">Savings Account #</span></span> 
- <span data-ttu-id="6b58c-2318">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2318">Savings Acct Number</span></span> 
- <span data-ttu-id="6b58c-2319">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2319">Savings Acct #</span></span> 
- <span data-ttu-id="6b58c-2320">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2320">Savings Acct No.</span></span> 
- <span data-ttu-id="6b58c-2321">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2321">Savings Account No.</span></span> 
- <span data-ttu-id="6b58c-2322">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2322">Debit Account Number</span></span> 
- <span data-ttu-id="6b58c-2323">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2323">Debit Account</span></span> 
- <span data-ttu-id="6b58c-2324">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2324">Debit Account #</span></span> 
- <span data-ttu-id="6b58c-2325">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2325">Debit Acct Number</span></span> 
- <span data-ttu-id="6b58c-2326">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2326">Debit Acct #</span></span> 
- <span data-ttu-id="6b58c-2327">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2327">Debit Acct No.</span></span> 
- <span data-ttu-id="6b58c-2328">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2328">Debit Account No.</span></span> 
- <span data-ttu-id="6b58c-2329">口座番号を当座預金口座の確認
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2329">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="6b58c-2330">#アカウントの確認、勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2330">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="6b58c-2331">#勘定の確認
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2331">＃勘定の確認</span></span> 
- <span data-ttu-id="6b58c-2332">勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2332">勘定番号の確認</span></span> 
- <span data-ttu-id="6b58c-2333">口座番号の確認
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2333">口座番号の確認</span></span> 
- <span data-ttu-id="6b58c-2334">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="6b58c-2334">銀行口座番号</span></span> 
- <span data-ttu-id="6b58c-2335">銀行口座</span><span class="sxs-lookup"><span data-stu-id="6b58c-2335">銀行口座</span></span> 
- <span data-ttu-id="6b58c-2336">銀行口座＃
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2336">銀行口座＃</span></span> 
- <span data-ttu-id="6b58c-2337">銀行の勘定番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2337">銀行の勘定番号</span></span> 
- <span data-ttu-id="6b58c-2338">銀行のacct #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2338">銀行のacct＃</span></span> 
- <span data-ttu-id="6b58c-2339">銀行の勘定いいえ
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2339">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="6b58c-2340">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="6b58c-2340">銀行口座番号</span></span>
- <span data-ttu-id="6b58c-2341">
普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2341">普通預金口座番号</span></span> 
- <span data-ttu-id="6b58c-2342">預金口座
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2342">預金口座</span></span> 
- <span data-ttu-id="6b58c-2343">貯蓄口座 #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2343">貯蓄口座＃</span></span> 
- <span data-ttu-id="6b58c-2344">貯蓄勘定の数
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2344">貯蓄勘定の数</span></span> 
- <span data-ttu-id="6b58c-2345">貯蓄勘定 #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2345">貯蓄勘定＃</span></span> 
- <span data-ttu-id="6b58c-2346">貯蓄勘定番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2346">貯蓄勘定番号</span></span> 
- <span data-ttu-id="6b58c-2347">普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2347">普通預金口座番号</span></span> 
- <span data-ttu-id="6b58c-2348">引き落とし口座番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2348">引き落とし口座番号</span></span> 
- <span data-ttu-id="6b58c-2349">口座番号</span><span class="sxs-lookup"><span data-stu-id="6b58c-2349">口座番号</span></span> 
- <span data-ttu-id="6b58c-2350">口座番号＃
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2350">口座番号＃</span></span> 
- <span data-ttu-id="6b58c-2351">デビットのacct番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2351">デビットのacct番号</span></span> 
- <span data-ttu-id="6b58c-2352">デビット勘定 #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2352">デビット勘定＃</span></span> 
- <span data-ttu-id="6b58c-2353">デビットACCTの番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2353">デビットACCTの番号</span></span> 
- <span data-ttu-id="6b58c-2354">デビット口座番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2354">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="6b58c-2355">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="6b58c-2355">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="6b58c-2356">Otemachi</span><span class="sxs-lookup"><span data-stu-id="6b58c-2356">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="6b58c-2357">Japanische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2357">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2358">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2358">Format</span></span>

<span data-ttu-id="6b58c-2359">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2359">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2360">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2360">Pattern</span></span>

<span data-ttu-id="6b58c-2361">12 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2361">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2362">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2362">Checksum</span></span>

<span data-ttu-id="6b58c-2363">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2363">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2364">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2364">Definition</span></span>

<span data-ttu-id="6b58c-2365">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2365">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2366">Die Funktion Func_jp_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2366">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2367">Ein Schlüsselwort aus Keyword_jp_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2367">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2368">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2368">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="6b58c-2369">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2369">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="6b58c-2370">dl#</span><span class="sxs-lookup"><span data-stu-id="6b58c-2370">dl#</span></span> 
- <span data-ttu-id="6b58c-2371">DL-</span><span class="sxs-lookup"><span data-stu-id="6b58c-2371">DL＃</span></span> 
- <span data-ttu-id="6b58c-2372">dls#</span><span class="sxs-lookup"><span data-stu-id="6b58c-2372">dls#</span></span> 
- <span data-ttu-id="6b58c-2373">VERTEILERLISTEN #</span><span class="sxs-lookup"><span data-stu-id="6b58c-2373">DLS＃</span></span> 
- <span data-ttu-id="6b58c-2374">driver license</span><span class="sxs-lookup"><span data-stu-id="6b58c-2374">driver license</span></span> 
- <span data-ttu-id="6b58c-2375">driver licenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-2375">driver licenses</span></span> 
- <span data-ttu-id="6b58c-2376">drivers license</span><span class="sxs-lookup"><span data-stu-id="6b58c-2376">drivers license</span></span> 
- <span data-ttu-id="6b58c-2377">driver's license</span><span class="sxs-lookup"><span data-stu-id="6b58c-2377">driver's license</span></span> 
- <span data-ttu-id="6b58c-2378">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-2378">drivers licenses</span></span> 
- <span data-ttu-id="6b58c-2379">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-2379">driver's licenses</span></span> 
- <span data-ttu-id="6b58c-2380">driving licence
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2380">driving licence</span></span> 
- <span data-ttu-id="6b58c-2381">lic#</span><span class="sxs-lookup"><span data-stu-id="6b58c-2381">lic#</span></span> 
- <span data-ttu-id="6b58c-2382">LIC #</span><span class="sxs-lookup"><span data-stu-id="6b58c-2382">LIC＃</span></span> 
- <span data-ttu-id="6b58c-2383">lics#</span><span class="sxs-lookup"><span data-stu-id="6b58c-2383">lics#</span></span> 
- <span data-ttu-id="6b58c-2384">Status-id</span><span class="sxs-lookup"><span data-stu-id="6b58c-2384">state id</span></span> 
- <span data-ttu-id="6b58c-2385">state identification
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2385">state identification</span></span> 
- <span data-ttu-id="6b58c-2386">state identification number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2386">state identification number</span></span> 
- <span data-ttu-id="6b58c-2387">低所得国 #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2387">低所得国＃</span></span> 
- <span data-ttu-id="6b58c-2388">免許証</span><span class="sxs-lookup"><span data-stu-id="6b58c-2388">免許証</span></span> 
- <span data-ttu-id="6b58c-2389">状態ID</span><span class="sxs-lookup"><span data-stu-id="6b58c-2389">状態ID</span></span>
- <span data-ttu-id="6b58c-2390">
状態の識別
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2390">状態の識別</span></span> 
- <span data-ttu-id="6b58c-2391">状態の識別番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2391">状態の識別番号</span></span> 
- <span data-ttu-id="6b58c-2392">運転免許</span><span class="sxs-lookup"><span data-stu-id="6b58c-2392">運転免許</span></span> 
- <span data-ttu-id="6b58c-2393">運転免許証</span><span class="sxs-lookup"><span data-stu-id="6b58c-2393">運転免許証</span></span> 
- <span data-ttu-id="6b58c-2394">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="6b58c-2394">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="6b58c-2395">Japanische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2395">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2396">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2396">Format</span></span>

<span data-ttu-id="6b58c-2397">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2397">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2398">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2398">Pattern</span></span>

<span data-ttu-id="6b58c-2399">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2399">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2400">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2400">Checksum</span></span>

<span data-ttu-id="6b58c-2401">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2401">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2402">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2402">Definition</span></span>

<span data-ttu-id="6b58c-2403">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2403">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2404">Die Funktion Func_jp_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2404">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2405">Ein Schlüsselwort aus Keyword_jp_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2405">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2406">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2406">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="6b58c-2407">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-2407">Keyword_jp_passport</span></span>

- <span data-ttu-id="6b58c-2408">パスポート
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2408">パスポート</span></span> 
- <span data-ttu-id="6b58c-2409">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2409">パスポート番号</span></span> 
- <span data-ttu-id="6b58c-2410">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2410">パスポートのNum</span></span> 
- <span data-ttu-id="6b58c-2411">パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2411">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="6b58c-2412">Japanische Einwohnerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2412">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2413">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2413">Format</span></span>

<span data-ttu-id="6b58c-2414">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2414">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2415">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2415">Pattern</span></span>

<span data-ttu-id="6b58c-2416">11 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2416">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2417">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2417">Checksum</span></span>

<span data-ttu-id="6b58c-2418">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2418">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2419">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2419">Definition</span></span>

<span data-ttu-id="6b58c-2420">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2420">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2421">Die Funktion Func_jp_resident_registration_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2421">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2422">Ein Schlüsselwort aus Keyword_jp_resident_registration_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2422">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2423">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2423">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="6b58c-2424">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2424">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="6b58c-2425">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2425">Resident Registration Number</span></span>
- <span data-ttu-id="6b58c-2426">Resident Register Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2426">Resident Register Number</span></span> 
- <span data-ttu-id="6b58c-2427">Residents Basic Registry Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2427">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="6b58c-2428">Resident Registration No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2428">Resident Registration No.</span></span> 
- <span data-ttu-id="6b58c-2429">Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2429">Resident Register No.</span></span> 
- <span data-ttu-id="6b58c-2430">Residents Basic Registry No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2430">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="6b58c-2431">Basic Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2431">Basic Resident Register No.</span></span> 
- <span data-ttu-id="6b58c-2432">住民登録番号、登録番号をレジデント
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2432">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="6b58c-2433">住民基本登録番号、登録番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2433">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="6b58c-2434">住民基本レジストリ番号を常駐
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2434">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="6b58c-2435">登録番号を常駐住民基本台帳登録番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2435">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="6b58c-2436">Japanische Sozialversicherungsnummer (SIN)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2436">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2437">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2437">Format</span></span>

<span data-ttu-id="6b58c-2438">7-12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2438">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2439">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2439">Pattern</span></span>

<span data-ttu-id="6b58c-2440">7 bis 12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2440">7-12 digits:</span></span>
- <span data-ttu-id="6b58c-2441">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2441">Four digits</span></span> 
- <span data-ttu-id="6b58c-2442">Ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2442">A hyphen (optional)</span></span> 
- <span data-ttu-id="6b58c-2443">Sechs Ziffern oder</span><span class="sxs-lookup"><span data-stu-id="6b58c-2443">Six digits OR</span></span>
- <span data-ttu-id="6b58c-2444">7-12 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2444">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2445">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2445">Checksum</span></span>

<span data-ttu-id="6b58c-2446">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2446">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2447">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2447">Definition</span></span>

<span data-ttu-id="6b58c-2448">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2448">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2449">Die Funktion Func_jp_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2449">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2450">Ein Schlüsselwort aus Keyword_jp_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2450">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="6b58c-2451">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2451">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2452">Die Funktion Func_jp_sin_pre_1997 findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2452">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2453">Ein Schlüsselwort aus Keyword_jp_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2453">A keyword from Keyword_jp_sin is found.</span></span>

```
<!-- Japan Social Insurance Number -->
<Entity id="c840e719-0896-45bb-84fd-1ed5c95e45ff" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_jp_sin" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_sin_pre_1997" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2454">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2454">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="6b58c-2455">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="6b58c-2455">Keyword_jp_sin</span></span>

- <span data-ttu-id="6b58c-2456">Social Insurance No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2456">Social Insurance No.</span></span> 
- <span data-ttu-id="6b58c-2457">Social Insurance Num
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2457">Social Insurance Num</span></span> 
- <span data-ttu-id="6b58c-2458">Social Insurance Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2458">Social Insurance Number</span></span> 
- <span data-ttu-id="6b58c-2459">社会保険のテンキー
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2459">社会保険のテンキー</span></span> 
- <span data-ttu-id="6b58c-2460">社会保険番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2460">社会保険番号</span></span> 
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="6b58c-2461">Malaysia -ID-Kartennummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2461">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2462">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2462">Format</span></span>

<span data-ttu-id="6b58c-2463">12 Ziffern mit optionalen Bindestrichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-2463">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2464">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2464">Pattern</span></span>

<span data-ttu-id="6b58c-2465">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2465">12 digits:</span></span>
- <span data-ttu-id="6b58c-2466">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="6b58c-2466">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="6b58c-2467">Ein Bindestrich (optional) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2467">A dash (optional)</span></span> 
- <span data-ttu-id="6b58c-2468">Zwei Buchstaben als Code für den Geburtsort </span><span class="sxs-lookup"><span data-stu-id="6b58c-2468">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="6b58c-2469">Ein Bindestrich (optional) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2469">A dash (optional)</span></span> 
- <span data-ttu-id="6b58c-2470">Drei beliebige Ziffern </span><span class="sxs-lookup"><span data-stu-id="6b58c-2470">Three random digits</span></span> 
- <span data-ttu-id="6b58c-2471">Einstelliger Code für das Geschlecht</span><span class="sxs-lookup"><span data-stu-id="6b58c-2471">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2472">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2472">Checksum</span></span>

<span data-ttu-id="6b58c-2473">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2473">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2474">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2474">Definition</span></span>

<span data-ttu-id="6b58c-2475">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2475">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2476">Der reguläre Ausdruck Regex_malaysia_id_card_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2476">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2477">Ein Schlüsselwort aus Keyword_malaysia_id_card_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2477">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

```
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2478">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2478">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="6b58c-2479">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2479">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="6b58c-2480">MyKad</span><span class="sxs-lookup"><span data-stu-id="6b58c-2480">MyKad</span></span> 
- <span data-ttu-id="6b58c-2481">Identity Card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2481">Identity Card</span></span> 
- <span data-ttu-id="6b58c-2482">ID-Karte</span><span class="sxs-lookup"><span data-stu-id="6b58c-2482">ID Card</span></span> 
- <span data-ttu-id="6b58c-2483">Ausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-2483">Identification Card</span></span> 
- <span data-ttu-id="6b58c-2484">Digital Application Card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2484">Digital Application Card</span></span> 
- <span data-ttu-id="6b58c-2485">Kad Akuan Diri
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2485">Kad Akuan Diri</span></span> 
- <span data-ttu-id="6b58c-2486">Kad Aplikasi Digital
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2486">Kad Aplikasi Digital</span></span> 
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="6b58c-2487">Niederlande – Bürgerdienstnummer (BSN)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2487">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2488">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2488">Format</span></span>

<span data-ttu-id="6b58c-2489">8-9 Ziffern mit optionalen Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-2489">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2490">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2490">Pattern</span></span>

<span data-ttu-id="6b58c-2491">8-9 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2491">8-9 digits:</span></span>
- <span data-ttu-id="6b58c-2492">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2492">Three digits</span></span> 
- <span data-ttu-id="6b58c-2493">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2493">A space (optional)</span></span> 
- <span data-ttu-id="6b58c-2494">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2494">Three digits</span></span> 
- <span data-ttu-id="6b58c-2495">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2495">A space (optional)</span></span> 
- <span data-ttu-id="6b58c-2496">2-3 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2496">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2497">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2497">Checksum</span></span>

<span data-ttu-id="6b58c-2498">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2498">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2499">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2499">Definition</span></span>

<span data-ttu-id="6b58c-2500">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2500">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2501">Die Funktion Func_netherlands_bsn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2501">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2502">Ein Schlüsselwort aus Keyword_netherlands_bsn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2502">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="6b58c-2503">Die Funktion Func_eu_date2 findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2503">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="6b58c-2504">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2504">The checksum passes.</span></span>

```
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2505">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2505">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="6b58c-2506">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="6b58c-2506">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="6b58c-2507">Citizen service number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2507">Citizen service number</span></span> 
- <span data-ttu-id="6b58c-2508">BSN

</span><span class="sxs-lookup"><span data-stu-id="6b58c-2508">BSN</span></span> 
- <span data-ttu-id="6b58c-2509">Burgerservicenummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2509">Burgerservicenummer</span></span> 
- <span data-ttu-id="6b58c-2510">Sofinummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2510">Sofinummer</span></span> 
- <span data-ttu-id="6b58c-2511">Persoonsgebonden nummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2511">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="6b58c-2512">Persoonsnummer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2512">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="6b58c-2513">Neuseeländische Gesundheitsministeriumsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2513">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2514">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2514">Format</span></span>

<span data-ttu-id="6b58c-2515">Drei Buchstaben, ein Leerzeichen (optional) und vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2515">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2516">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2516">Pattern</span></span>

<span data-ttu-id="6b58c-2517">Drei Buchstaben (nicht Groß-/Kleinschreibung) eine Speicherplatz um vier Ziffern (optional)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2517">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2518">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2518">Checksum</span></span>

<span data-ttu-id="6b58c-2519">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2519">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2520">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2520">Definition</span></span>

<span data-ttu-id="6b58c-2521">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2521">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2522">Die Funktion Func_new_zealand_ministry_of_health_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2522">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2523">Ein Schlüsselwort aus Keyword_nz_terms wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2523">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="6b58c-2524">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2524">The checksum passes.</span></span>

```
<!-- New Zealand Health Number -->
<Entity id="2b71c1c8-d14e-4430-82dc-fd1ed6bf05c7" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_new_zealand_ministry_of_health_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_nz_terms" />
        </Any>
    </Pattern>
</Entity>
```

<span data-ttu-id="6b58c-2525">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2525">Keywords</span></span>

<span data-ttu-id="6b58c-2526">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="6b58c-2526">Keyword_nz_terms</span></span>

- <span data-ttu-id="6b58c-2527">NHI
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2527">NHI</span></span> 
- <span data-ttu-id="6b58c-2528">Neuseeland</span><span class="sxs-lookup"><span data-stu-id="6b58c-2528">New Zealand</span></span> 
- <span data-ttu-id="6b58c-2529">Integrität</span><span class="sxs-lookup"><span data-stu-id="6b58c-2529">Health</span></span> 
- <span data-ttu-id="6b58c-2530">treatment
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2530">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="6b58c-2531">Norwegen – Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2531">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2532">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2532">Format</span></span>

<span data-ttu-id="6b58c-2533">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2533">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2534">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2534">Pattern</span></span>

<span data-ttu-id="6b58c-2535">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2535">11 digits:</span></span>
- <span data-ttu-id="6b58c-2536">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="6b58c-2536">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="6b58c-2537">Dreistellige individuelle Zahl </span><span class="sxs-lookup"><span data-stu-id="6b58c-2537">Three-digit individual number</span></span> 
- <span data-ttu-id="6b58c-2538">Zwei Prüfziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2538">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2539">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2539">Checksum</span></span>

<span data-ttu-id="6b58c-2540">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2540">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2541">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2541">Definition</span></span>

<span data-ttu-id="6b58c-2542">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2542">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2543">Die Funktion Func_norway_id_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2543">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2544">Ein Schlüsselwort aus Keyword_norway_id_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2544">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="6b58c-2545">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2545">The checksum passes.</span></span>
- <span data-ttu-id="6b58c-2546">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2546">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2547">Die Funktion Func_norway_id_numbe findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2547">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2548">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2548">The checksum passes.</span></span>

```
<!-- Norway Identification Number -->
<Entity id="d4c8a798-e9f2-4bd3-9652-500d24080fc3" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_norway_id_number"/>
     <Match idRef="Keyword_norway_id_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_norway_id_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2549">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2549">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="6b58c-2550">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2550">Keyword_norway_id_number</span></span>

- <span data-ttu-id="6b58c-2551">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2551">Personal identification number</span></span>
- <span data-ttu-id="6b58c-2552">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2552">Norwegian ID Number</span></span>
- <span data-ttu-id="6b58c-2553">ID Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2553">ID Number</span></span>
- <span data-ttu-id="6b58c-2554">Identification</span><span class="sxs-lookup"><span data-stu-id="6b58c-2554">Identification</span></span>
- <span data-ttu-id="6b58c-2555">Personnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2555">Personnummer</span></span>
- <span data-ttu-id="6b58c-2556">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2556">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="6b58c-2557">Philippinen – Vereinheitlichte Mehrzweck-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2557">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2558">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2558">Format</span></span>

<span data-ttu-id="6b58c-2559">12 Ziffern, durch Bindestriche getrennt</span><span class="sxs-lookup"><span data-stu-id="6b58c-2559">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2560">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2560">Pattern</span></span>

<span data-ttu-id="6b58c-2561">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2561">12 digits:</span></span>
- <span data-ttu-id="6b58c-2562">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2562">Four digits</span></span> 
- <span data-ttu-id="6b58c-2563">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-2563">A hyphen</span></span> 
- <span data-ttu-id="6b58c-2564">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="6b58c-2564">Seven digits</span></span> 
- <span data-ttu-id="6b58c-2565">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-2565">A hyphen</span></span> 
- <span data-ttu-id="6b58c-2566">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2566">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2567">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2567">Checksum</span></span>

<span data-ttu-id="6b58c-2568">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2568">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2569">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2569">Definition</span></span>

<span data-ttu-id="6b58c-2570">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2570">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2571">Der reguläre Ausdruck Regex_philippines_unified_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2571">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2572">Ein Schlüsselwort aus Keyword_philippines_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2572">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2573">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2573">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="6b58c-2574">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="6b58c-2574">Keyword_philippines_id</span></span>

- <span data-ttu-id="6b58c-2575">Unified Multi-Purpose ID
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2575">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="6b58c-2576">UMID
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2576">UMID</span></span> 
- <span data-ttu-id="6b58c-2577">Identity Card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2577">Identity Card</span></span> 
- <span data-ttu-id="6b58c-2578">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="6b58c-2578">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="6b58c-2579">Polen Personalausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-2579">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2580">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2580">Format</span></span>

<span data-ttu-id="6b58c-2581">Drei Buchstaben und sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2581">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2582">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2582">Pattern</span></span>

<span data-ttu-id="6b58c-2583">Drei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2583">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2584">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2584">Checksum</span></span>

<span data-ttu-id="6b58c-2585">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2585">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2586">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2586">Definition</span></span>

<span data-ttu-id="6b58c-p138">Eine DLP-Richtlinie ist 75 % sicher, dass diese Art von vertraulichen Informationen festgestellt wurde "If"; innerhalb einer Nähe von 300 Zeichen: die Funktion Func_polish_national_id sucht nach Inhalten, die dem Muster entspricht. Ein Schlüsselwort aus Keyword_polish_national_id_passport_number gefunden wird. Die Prüfsumme übergibt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-p138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern. A keyword from Keyword_polish_national_id_passport_number is found. The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2590">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2590">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="6b58c-2591">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2591">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="6b58c-2592">Nazwa i nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2592">Nazwa i nr dowodu tożsamości</span></span> 
- <span data-ttu-id="6b58c-2593">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2593">Dowód Tożsamości</span></span> 
- <span data-ttu-id="6b58c-p139">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p139">dow. os.</span></span> 

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="6b58c-2596">Polnische ID-Karte (PESEL)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2596">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2597">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2597">Format</span></span>

<span data-ttu-id="6b58c-2598">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2598">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2599">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2599">Pattern</span></span>

<span data-ttu-id="6b58c-2600">11 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2600">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2601">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2601">Checksum</span></span>

<span data-ttu-id="6b58c-2602">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2602">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2603">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2603">Definition</span></span>

<span data-ttu-id="6b58c-2604">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2604">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2605">Die Funktion Func_pesel_identification_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2605">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2606">Ein Schlüsselwort aus Keyword_pesel_identification_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2606">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="6b58c-2607">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2607">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2608">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2608">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="6b58c-2609">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2609">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="6b58c-2610">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="6b58c-2610">Nr PESEL</span></span>
- <span data-ttu-id="6b58c-2611">PESEL</span><span class="sxs-lookup"><span data-stu-id="6b58c-2611">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="6b58c-2612">Polen Reisepass</span><span class="sxs-lookup"><span data-stu-id="6b58c-2612">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2613">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2613">Format</span></span>

<span data-ttu-id="6b58c-2614">Zwei Buchstaben und sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2614">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2615">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2615">Pattern</span></span>

<span data-ttu-id="6b58c-2616">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2616">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2617">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2617">Checksum</span></span>

<span data-ttu-id="6b58c-2618">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2618">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2619">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2619">Definition</span></span>

<span data-ttu-id="6b58c-2620">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2620">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2621">Die Funktion Func_polish_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2621">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2622">Ein Schlüsselwort aus Keyword_polish_national_id_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2622">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="6b58c-2623">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2623">The checksum passes.</span></span>

```
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2624">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2624">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="6b58c-2625">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2625">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="6b58c-2626">Nazwa i nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2626">Nazwa i nr dowodu tożsamości</span></span> 
- <span data-ttu-id="6b58c-2627">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2627">Dowód Tożsamości</span></span> 
- <span data-ttu-id="6b58c-p140">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-p140">dow. os.</span></span> 

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="6b58c-2630">Portugal – Bürgerkartennummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2630">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2631">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2631">Format</span></span>

<span data-ttu-id="6b58c-2632">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2632">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2633">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2633">Pattern</span></span>

<span data-ttu-id="6b58c-2634">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2634">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2635">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2635">Checksum</span></span>

<span data-ttu-id="6b58c-2636">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2636">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2637">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2637">Definition</span></span>

<span data-ttu-id="6b58c-2638">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2638">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2639">Der reguläre Ausdruck Regex_portugal_citizen_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2639">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2640">Ein Schlüsselwort aus Keyword_portugal_citizen_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2640">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2641">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2641">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="6b58c-2642">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2642">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="6b58c-2643">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2643">Citizen Card</span></span>
- <span data-ttu-id="6b58c-2644">National ID Card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2644">National ID Card</span></span>
- <span data-ttu-id="6b58c-2645">CC</span><span class="sxs-lookup"><span data-stu-id="6b58c-2645">CC</span></span>
- <span data-ttu-id="6b58c-2646">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="6b58c-2646">Cartão de Cidadão</span></span>
- <span data-ttu-id="6b58c-2647">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="6b58c-2647">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="6b58c-2648">Saudi-Arabische Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2648">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2649">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2649">Format</span></span>

<span data-ttu-id="6b58c-2650">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2650">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2651">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2651">Pattern</span></span>

<span data-ttu-id="6b58c-2652">10 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2652">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2653">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2653">Checksum</span></span>

<span data-ttu-id="6b58c-2654">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2654">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2655">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2655">Definition</span></span>

<span data-ttu-id="6b58c-2656">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2656">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2657">Der reguläre Ausdruck Regex_saudi_arabia_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2657">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2658">Ein Schlüsselwort aus Keyword_saudi_arabia_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2658">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

```
<!-- Saudi Arabia National ID -->
<Entity id="8c5a0ba8-404a-41a3-8871-746aa21ee6c0" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_saudi_arabia_national_id" />
        <Any minMatches="1">
          <Match idRef="Keyword_saudi_arabia_national_id" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2659">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2659">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="6b58c-2660">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="6b58c-2660">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="6b58c-2661">Identification Card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2661">Identification Card</span></span> 
- <span data-ttu-id="6b58c-2662">I card number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2662">I card number</span></span> 
- <span data-ttu-id="6b58c-2663">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2663">ID number</span></span> 
- <span data-ttu-id="6b58c-2664">الوطنية الهوية بطاقة رقم
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2664">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="6b58c-2665">Singapur – National Registration Identity Card-Nummer (NRIC)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2665">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2666">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2666">Format</span></span>

<span data-ttu-id="6b58c-2667">Neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2667">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2668">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2668">Pattern</span></span>

- <span data-ttu-id="6b58c-2669">Neun Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2669">Nine letters and digits:</span></span>
- <span data-ttu-id="6b58c-2670">Die Buchstaben "F", "G", "S" oder "T" (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2670">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-2671">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="6b58c-2671">Seven digits</span></span> 
- <span data-ttu-id="6b58c-2672">Eine alphabetische Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2672">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2673">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2673">Checksum</span></span>

<span data-ttu-id="6b58c-2674">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2674">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2675">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2675">Definition</span></span>

<span data-ttu-id="6b58c-2676">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2676">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2677">Der reguläre Ausdruck Regex_singapore_nric findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2677">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2678">Ein Schlüsselwort aus Keyword_singapore_nric wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2678">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="6b58c-2679">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2679">The checksum passes.</span></span>

<span data-ttu-id="6b58c-2680">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2680">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2681">Der reguläre Ausdruck Regex_singapore_nric findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2681">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2682">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2682">The checksum passes.</span></span>

```
<!-- Singapore National Registration Identity Card (NRIC) Number -->
<Entity id="cead390a-dd83-4856-9751-fb6dc98c34da" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_singapore_nric"/>
     <Match idRef="Keyword_singapore_nric"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_singapore_nric"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2683">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2683">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="6b58c-2684">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="6b58c-2684">Keyword_singapore_nric</span></span>

- <span data-ttu-id="6b58c-2685">National Registration Identity Card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2685">National Registration Identity Card</span></span> 
- <span data-ttu-id="6b58c-2686">Identity Card Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2686">Identity Card Number</span></span> 
- <span data-ttu-id="6b58c-2687">NRIC
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2687">NRIC</span></span> 
- <span data-ttu-id="6b58c-2688">IC
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2688">IC</span></span> 
- <span data-ttu-id="6b58c-2689">Foreign Identification Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2689">Foreign Identification Number</span></span> 
- <span data-ttu-id="6b58c-2690">FIN
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2690">FIN</span></span> 
- <span data-ttu-id="6b58c-2691">身份证 </span><span class="sxs-lookup"><span data-stu-id="6b58c-2691">身份证</span></span> 
- <span data-ttu-id="6b58c-2692">身份證
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2692">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="6b58c-2693">Südafrika – Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2693">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2694">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2694">Format</span></span>

<span data-ttu-id="6b58c-2695">13 Ziffern, die Leerzeichen enthalten können</span><span class="sxs-lookup"><span data-stu-id="6b58c-2695">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2696">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2696">Pattern</span></span>

<span data-ttu-id="6b58c-2697">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2697">13 digits:</span></span>
- <span data-ttu-id="6b58c-2698">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="6b58c-2698">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="6b58c-2699">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2699">Four digits</span></span> 
- <span data-ttu-id="6b58c-2700">Ein einstelliger Citizenship-Indikator </span><span class="sxs-lookup"><span data-stu-id="6b58c-2700">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="6b58c-2701">Die Ziffer "8" oder "9" </span><span class="sxs-lookup"><span data-stu-id="6b58c-2701">The digit "8" or "9"</span></span> 
- <span data-ttu-id="6b58c-2702">Eine Ziffer als Prüfsummenziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2702">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2703">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2703">Checksum</span></span>

<span data-ttu-id="6b58c-2704">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2704">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2705">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2705">Definition</span></span>

<span data-ttu-id="6b58c-2706">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2706">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2707">Die Funktion Func_south_africa_identification_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2707">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2708">Ein Schlüsselwort aus Keyword_south_africa_identification_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2708">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="6b58c-2709">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2709">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2710">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2710">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="6b58c-2711">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2711">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="6b58c-2712">Identity card</span><span class="sxs-lookup"><span data-stu-id="6b58c-2712">Identity card</span></span>
- <span data-ttu-id="6b58c-2713">ID</span><span class="sxs-lookup"><span data-stu-id="6b58c-2713">ID</span></span>
- <span data-ttu-id="6b58c-2714">Identification</span><span class="sxs-lookup"><span data-stu-id="6b58c-2714">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="6b58c-2715">Südkorea – Einwohnerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2715">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2716">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2716">Format</span></span>

<span data-ttu-id="6b58c-2717">13 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="6b58c-2717">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2718">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2718">Pattern</span></span>

<span data-ttu-id="6b58c-2719">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2719">13 digits:</span></span>
- <span data-ttu-id="6b58c-2720">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="6b58c-2720">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="6b58c-2721">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="6b58c-2721">A hyphen</span></span> 
- <span data-ttu-id="6b58c-2722">Eine Ziffer, die durch das Jahrhundert und das Geschlecht bestimmt wird </span><span class="sxs-lookup"><span data-stu-id="6b58c-2722">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="6b58c-2723">Vierstelliger Code für die Geburtsregion </span><span class="sxs-lookup"><span data-stu-id="6b58c-2723">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="6b58c-2724">Eine Ziffer, um Personen zu unterscheiden, für die die vorhergehenden Zahlen identisch sind </span><span class="sxs-lookup"><span data-stu-id="6b58c-2724">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="6b58c-2725">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2725">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2726">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2726">Checksum</span></span>

<span data-ttu-id="6b58c-2727">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2727">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2728">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2728">Definition</span></span>

<span data-ttu-id="6b58c-2729">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2729">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2730">Die Funktion Func_south_korea_resident_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2730">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2731">Ein Schlüsselwort aus Keyword_south_korea_resident_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2731">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="6b58c-2732">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2732">The checksum passes.</span></span>

<span data-ttu-id="6b58c-2733">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2733">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2734">Die Funktion Func_south_korea_resident_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2734">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2735">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2735">The checksum passes.</span></span>

```
<!-- South Korea Resident Registration Number -->
<Entity id="5b802e18-ba80-44c4-bc83-bf2ad36ae36a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_korea_resident_number"/>
     <Match idRef="Keyword_south_korea_resident_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_south_korea_resident_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2736">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2736">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="6b58c-2737">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2737">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="6b58c-2738">National ID card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2738">National ID card</span></span> 
- <span data-ttu-id="6b58c-2739">Citizen's Registration Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2739">Citizen's Registration Number</span></span> 
- <span data-ttu-id="6b58c-2740">Jumin deungnok beonho
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2740">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="6b58c-2741">RRN
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2741">RRN</span></span> 
- <span data-ttu-id="6b58c-2742">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="6b58c-2742">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="6b58c-2743">Spanische Sozialversicherungsnummer (SSN)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2743">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2744">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2744">Format</span></span>

<span data-ttu-id="6b58c-2745">11-12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2745">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2746">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2746">Pattern</span></span>

<span data-ttu-id="6b58c-2747">11 bis 12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2747">11-12 digits:</span></span>
- <span data-ttu-id="6b58c-2748">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2748">Two digits</span></span> 
- <span data-ttu-id="6b58c-2749">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2749">A forward slash (optional)</span></span> 
- <span data-ttu-id="6b58c-2750">7 bis 8 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2750">7-8 digits</span></span> 
- <span data-ttu-id="6b58c-2751">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2751">A forward slash (optional)</span></span> 
- <span data-ttu-id="6b58c-2752">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2752">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2753">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2753">Checksum</span></span>

<span data-ttu-id="6b58c-2754">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2754">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2755">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2755">Definition</span></span>

<span data-ttu-id="6b58c-2756">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2756">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2757">Die Funktion Func_spanish_social_security_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2757">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2758">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2758">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2759">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2759">Keywords</span></span>

<span data-ttu-id="6b58c-2760">Keine</span><span class="sxs-lookup"><span data-stu-id="6b58c-2760">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="6b58c-2761">Schwedische Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2761">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2762">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2762">Format</span></span>

<span data-ttu-id="6b58c-2763">10 oder 12 Ziffern und ein optionales Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-2763">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2764">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2764">Pattern</span></span>

<span data-ttu-id="6b58c-2765">10 oder 12 Ziffern und ein optionals Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2765">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="6b58c-2766">2 bis 4 Ziffern (optional)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2766">2-4 digits (optional)</span></span> 
- <span data-ttu-id="6b58c-2767">Sechs Ziffern im Datumsformat JJMMTT</span><span class="sxs-lookup"><span data-stu-id="6b58c-2767">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="6b58c-2768">Trennzeichen „-“ oder „+“ (optional) und</span><span class="sxs-lookup"><span data-stu-id="6b58c-2768">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="6b58c-2769">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2769">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2770">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2770">Checksum</span></span>

<span data-ttu-id="6b58c-2771">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2771">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2772">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2772">Definition</span></span>

<span data-ttu-id="6b58c-2773">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2773">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2774">Die Funktion Func_swedish_national_identifier findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2774">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2775">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2775">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2776">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2776">Keywords</span></span>

<span data-ttu-id="6b58c-2777">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2777">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="6b58c-2778">Schwedische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2778">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2779">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2779">Format</span></span>

<span data-ttu-id="6b58c-2780">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2780">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2781">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2781">Pattern</span></span>

<span data-ttu-id="6b58c-2782">Acht aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2782">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2783">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2783">Checksum</span></span>

<span data-ttu-id="6b58c-2784">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2784">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2785">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2785">Definition</span></span>

<span data-ttu-id="6b58c-2786">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2786">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2787">Der reguläre Ausdruck Regex_sweden_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2787">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2788">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2788">One of the following is true:</span></span>
    - <span data-ttu-id="6b58c-2789">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2789">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="6b58c-2790">Ein Schlüsselwort aus Keyword_sweden_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2790">A keyword from Keyword_sweden_passport is found.</span></span>

```
<!-- Sweden Passport Number -->
<Entity id="ba4e7456-55a9-4d89-9140-c33673553526" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_sweden_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_sweden_passport" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2791">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2791">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="6b58c-2792">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-2792">Keyword_sweden_passport</span></span>

- <span data-ttu-id="6b58c-2793">visa requirements
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2793">visa requirements</span></span> 
- <span data-ttu-id="6b58c-2794">Alien Registration Card
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2794">Alien Registration Card</span></span> 
- <span data-ttu-id="6b58c-2795">Schengen visas
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2795">Schengen visas</span></span> 
- <span data-ttu-id="6b58c-2796">Schengen visa
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2796">Schengen visa</span></span> 
- <span data-ttu-id="6b58c-2797">Visa Processing
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2797">Visa Processing</span></span> 
- <span data-ttu-id="6b58c-2798">Visa Type
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2798">Visa Type</span></span> 
- <span data-ttu-id="6b58c-2799">Single Entry
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2799">Single Entry</span></span> 
- <span data-ttu-id="6b58c-2800">Multiple Entry
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2800">Multiple Entry</span></span> 
- <span data-ttu-id="6b58c-2801">G3 Processing Fees

</span><span class="sxs-lookup"><span data-stu-id="6b58c-2801">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="6b58c-2802">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-2802">Keyword_passport</span></span>

- <span data-ttu-id="6b58c-2803">Passport Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-2803">Passport Number</span></span> 
- <span data-ttu-id="6b58c-2804">
Passport No</span><span class="sxs-lookup"><span data-stu-id="6b58c-2804">Passport No</span></span> 
- <span data-ttu-id="6b58c-2805">Passport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2805">Passport #</span></span> 
- <span data-ttu-id="6b58c-2806">Passport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2806">Passport#</span></span> 
- <span data-ttu-id="6b58c-2807">PassportID</span><span class="sxs-lookup"><span data-stu-id="6b58c-2807">PassportID</span></span> 
- <span data-ttu-id="6b58c-2808">Passportno
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2808">Passportno</span></span> 
- <span data-ttu-id="6b58c-2809">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2809">passportnumber</span></span> 
- <span data-ttu-id="6b58c-2810">パスポート</span><span class="sxs-lookup"><span data-stu-id="6b58c-2810">パスポート</span></span> 
- <span data-ttu-id="6b58c-2811">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2811">パスポート番号</span></span> 
- <span data-ttu-id="6b58c-2812">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2812">パスポートのNum</span></span> 
- <span data-ttu-id="6b58c-2813">パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2813">パスポート＃</span></span> 
- <span data-ttu-id="6b58c-2814">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="6b58c-2814">Numéro de passeport</span></span> 
- <span data-ttu-id="6b58c-2815">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="6b58c-2815">Passeport n °</span></span> 
- <span data-ttu-id="6b58c-2816">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2816">Passeport Non</span></span> 
- <span data-ttu-id="6b58c-2817">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2817">Passeport #</span></span> 
- <span data-ttu-id="6b58c-2818">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2818">Passeport#</span></span> 
- <span data-ttu-id="6b58c-2819">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="6b58c-2819">PasseportNon</span></span> 
- <span data-ttu-id="6b58c-2820">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2820">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="6b58c-2821">SWIFT-Code</span><span class="sxs-lookup"><span data-stu-id="6b58c-2821">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2822">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2822">Format</span></span>

<span data-ttu-id="6b58c-2823">Vier Buchstaben, gefolgt von 5-31 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2823">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2824">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2824">Pattern</span></span>

<span data-ttu-id="6b58c-2825">Vier Buchstaben, gefolgt von 5 bis 31 Buchstaben oder Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2825">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="6b58c-2826">Vier Buchstaben für den Bankcode (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2826">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-2827">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-2827">An optional space</span></span> 
- <span data-ttu-id="6b58c-2828">4 bis 28 Buchstaben oder Ziffern (BBAN, Basic Bank Account Number)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2828">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="6b58c-2829">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-2829">An optional space</span></span> 
- <span data-ttu-id="6b58c-2830">1 bis 3 Buchstaben oder Ziffern (Rest des BBAN)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2830">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2831">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2831">Checksum</span></span>

<span data-ttu-id="6b58c-2832">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2832">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2833">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2833">Definition</span></span>

<span data-ttu-id="6b58c-2834">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2834">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2835">Der reguläre Ausdruck Regex_swift findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2835">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2836">Ein Schlüsselwort aus Keyword_swift wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2836">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2837">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2837">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="6b58c-2838">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="6b58c-2838">Keyword_swift</span></span>

- <span data-ttu-id="6b58c-2839">international organization for standardization 9362
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2839">international organization for standardization 9362</span></span> 
- <span data-ttu-id="6b58c-2840">iso 9362
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2840">iso 9362</span></span> 
- <span data-ttu-id="6b58c-2841">iso9362</span><span class="sxs-lookup"><span data-stu-id="6b58c-2841">iso9362</span></span> 
- <span data-ttu-id="6b58c-2842">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="6b58c-2842">swift\#</span></span> 
- <span data-ttu-id="6b58c-2843">swiftcode
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2843">swiftcode</span></span> 
- <span data-ttu-id="6b58c-2844">swiftnumber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2844">swiftnumber</span></span> 
- <span data-ttu-id="6b58c-2845">swiftroutingnumber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2845">swiftroutingnumber</span></span> 
- <span data-ttu-id="6b58c-2846">SWIFT-code</span><span class="sxs-lookup"><span data-stu-id="6b58c-2846">swift code</span></span> 
- <span data-ttu-id="6b58c-2847">swift number #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2847">swift number #</span></span> 
- <span data-ttu-id="6b58c-2848">swift routing number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2848">swift routing number</span></span> 
- <span data-ttu-id="6b58c-2849">bic number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2849">bic number</span></span> 
- <span data-ttu-id="6b58c-2850">bic code
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2850">bic code</span></span> 
- <span data-ttu-id="6b58c-2851">BIC\#</span><span class="sxs-lookup"><span data-stu-id="6b58c-2851">bic \#</span></span> 
- <span data-ttu-id="6b58c-2852">BIC\#</span><span class="sxs-lookup"><span data-stu-id="6b58c-2852">bic\#</span></span> 
- <span data-ttu-id="6b58c-2853">bank identifier code
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2853">bank identifier code</span></span> 
- <span data-ttu-id="6b58c-2854">標準化9362</span><span class="sxs-lookup"><span data-stu-id="6b58c-2854">標準化9362</span></span> 
- <span data-ttu-id="6b58c-2855">迅速 #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2855">迅速＃</span></span> 
- <span data-ttu-id="6b58c-2856">SWIFTコード
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2856">SWIFTコード</span></span> 
- <span data-ttu-id="6b58c-2857">SWIFT番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2857">SWIFT番号</span></span> 
- <span data-ttu-id="6b58c-2858">迅速なルーティング番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2858">迅速なルーティング番号</span></span> 
- <span data-ttu-id="6b58c-2859">BIC番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2859">BIC番号</span></span> 
- <span data-ttu-id="6b58c-2860">BICコード
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2860">BICコード</span></span> 
- <span data-ttu-id="6b58c-2861">銀行識別コードのための国際組織
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2861">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="6b58c-2862">Organisation internationale de normalisation 9362
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2862">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="6b58c-2863">rapide\#</span><span class="sxs-lookup"><span data-stu-id="6b58c-2863">rapide \#</span></span> 
- <span data-ttu-id="6b58c-2864">code SWIFT
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2864">code SWIFT</span></span> 
- <span data-ttu-id="6b58c-2865">le numéro de swift
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2865">le numéro de swift</span></span> 
- <span data-ttu-id="6b58c-2866">swift numéro d'acheminement
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2866">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="6b58c-2867">le numéro BIC
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2867">le numéro BIC</span></span> 
- <span data-ttu-id="6b58c-2868">\#BIC</span><span class="sxs-lookup"><span data-stu-id="6b58c-2868">\# BIC</span></span> 
- <span data-ttu-id="6b58c-2869">code identificateur de banque
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2869">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="6b58c-2870">Taiwanesicher Personalausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-2870">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2871">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2871">Format</span></span>

<span data-ttu-id="6b58c-2872">Ein Buchstabe (auf Englisch) gefolgt von neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2872">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2873">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2873">Pattern</span></span>

<span data-ttu-id="6b58c-2874">Ein Buchstabe (Englisch), gefolgt von neun Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2874">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="6b58c-2875">Ein Buchstabe (Englisch, Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2875">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-2876">Die Ziffer 1 oder 2</span><span class="sxs-lookup"><span data-stu-id="6b58c-2876">The digit "1" or "2"</span></span> 
- <span data-ttu-id="6b58c-2877">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2877">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2878">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2878">Checksum</span></span>

<span data-ttu-id="6b58c-2879">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2879">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2880">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2880">Definition</span></span>

<span data-ttu-id="6b58c-2881">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2881">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2882">Die Funktion Func_taiwanese_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2882">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2883">Ein Schlüsselwort aus Keyword_taiwanese_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2883">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="6b58c-2884">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2884">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2885">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2885">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="6b58c-2886">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="6b58c-2886">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="6b58c-2887">身份證字號
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2887">身份證字號</span></span> 
- <span data-ttu-id="6b58c-2888">身份證
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2888">身份證</span></span> 
- <span data-ttu-id="6b58c-2889">身份證號碼
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2889">身份證號碼</span></span> 
- <span data-ttu-id="6b58c-2890">身份證號
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2890">身份證號</span></span> 
- <span data-ttu-id="6b58c-2891">身分證字號
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2891">身分證字號</span></span> 
- <span data-ttu-id="6b58c-2892">身分證 </span><span class="sxs-lookup"><span data-stu-id="6b58c-2892">身分證</span></span> 
- <span data-ttu-id="6b58c-2893">身分證號碼
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2893">身分證號碼</span></span> 
- <span data-ttu-id="6b58c-2894">身份證號
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2894">身份證號</span></span> 
- <span data-ttu-id="6b58c-2895">身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2895">身分證統一編號</span></span> 
- <span data-ttu-id="6b58c-2896">國民身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2896">國民身分證統一編號</span></span> 
- <span data-ttu-id="6b58c-2897">簽名
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2897">簽名</span></span> 
- <span data-ttu-id="6b58c-2898">蓋章
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2898">蓋章</span></span> 
- <span data-ttu-id="6b58c-2899">簽名或蓋章

</span><span class="sxs-lookup"><span data-stu-id="6b58c-2899">簽名或蓋章</span></span> 
- <span data-ttu-id="6b58c-2900">簽章</span><span class="sxs-lookup"><span data-stu-id="6b58c-2900">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="6b58c-2901">	Taiwan – Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2901">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2902">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2902">Format</span></span>

- <span data-ttu-id="6b58c-2903">Biometrische Reisepassnummer: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2903">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="6b58c-2904">Nicht-biometrische Reisepassnummer: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2904">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2905">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2905">Pattern</span></span>
<span data-ttu-id="6b58c-2906">Biometrische Reisepassnummer:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2906">Biometric passport number:</span></span>
- <span data-ttu-id="6b58c-2907">Die Ziffer "3" </span><span class="sxs-lookup"><span data-stu-id="6b58c-2907">The digit "3"</span></span> 
- <span data-ttu-id="6b58c-2908">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2908">Eight digits</span></span>

<span data-ttu-id="6b58c-2909">Nicht-biometrische Reisepassnummer:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2909">Non-biometric passport number:</span></span>
- <span data-ttu-id="6b58c-2910">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2910">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2911">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2911">Checksum</span></span>

<span data-ttu-id="6b58c-2912">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2912">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2913">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2913">Definition</span></span>

<span data-ttu-id="6b58c-2914">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2914">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2915">Der reguläre Ausdruck Regex_taiwan_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2915">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2916">Ein Schlüsselwort aus Keyword_taiwan_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2916">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2917">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2917">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="6b58c-2918">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-2918">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="6b58c-2919">ROC passport number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2919">ROC passport number</span></span> 
- <span data-ttu-id="6b58c-2920">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2920">Passport number</span></span> 
- <span data-ttu-id="6b58c-2921">Passport keine</span><span class="sxs-lookup"><span data-stu-id="6b58c-2921">Passport no</span></span> 
- <span data-ttu-id="6b58c-2922">Passport Num
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2922">Passport Num</span></span> 
- <span data-ttu-id="6b58c-2923">Passport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2923">Passport #</span></span> 
- <span data-ttu-id="6b58c-2924">护照
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2924">护照</span></span> 
- <span data-ttu-id="6b58c-2925">中華民國護照
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2925">中華民國護照</span></span> 
- <span data-ttu-id="6b58c-2926">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="6b58c-2926">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="6b58c-2927">Taiwan – Einwohnerzertifikatsnummer (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="6b58c-2927">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2928">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2928">Format</span></span>

<span data-ttu-id="6b58c-2929">10 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2929">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2930">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2930">Pattern</span></span>

<span data-ttu-id="6b58c-2931">10 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2931">10 letters and digits:</span></span>
- <span data-ttu-id="6b58c-2932">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="6b58c-2932">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="6b58c-2933">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2933">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2934">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2934">Checksum</span></span>

<span data-ttu-id="6b58c-2935">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2935">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2936">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2936">Definition</span></span>

<span data-ttu-id="6b58c-2937">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2937">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2938">Der reguläre Ausdruck Regex_taiwan_resident_certificate findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2938">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2939">Ein Schlüsselwort aus Keyword_taiwan_resident_certificate wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2939">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2940">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2940">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="6b58c-2941">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="6b58c-2941">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="6b58c-2942">Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2942">Resident Certificate</span></span> 
- <span data-ttu-id="6b58c-2943">Wohnen Cert</span><span class="sxs-lookup"><span data-stu-id="6b58c-2943">Resident Cert</span></span> 
- <span data-ttu-id="6b58c-2944">Resident Cert.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2944">Resident Cert.</span></span> 
- <span data-ttu-id="6b58c-2945">Ausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-2945">Identification card</span></span> 
- <span data-ttu-id="6b58c-2946">Alien Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2946">Alien Resident Certificate</span></span> 
- <span data-ttu-id="6b58c-2947">ARC
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2947">ARC</span></span> 
- <span data-ttu-id="6b58c-2948">Taiwan Area Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2948">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="6b58c-2949">TARC
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2949">TARC</span></span> 
- <span data-ttu-id="6b58c-2950">居留證
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2950">居留證</span></span> 
- <span data-ttu-id="6b58c-2951">外僑居留證
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2951">外僑居留證</span></span> 
- <span data-ttu-id="6b58c-2952">台灣地區居留證
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2952">台灣地區居留證</span></span> 
   
## <a name="uk-drivers-license-number"></a><span data-ttu-id="6b58c-p141">Britische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2955">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2955">Format</span></span>

<span data-ttu-id="6b58c-2956">Kombination aus 18 Buchstaben und Ziffern im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2956">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2957">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2957">Pattern</span></span>

<span data-ttu-id="6b58c-2958">18 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2958">18 letters and digits:</span></span>
- <span data-ttu-id="6b58c-2959">Fünf Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) oder die Ziffer 9 anstelle eines Buchstabens</span><span class="sxs-lookup"><span data-stu-id="6b58c-2959">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="6b58c-2960">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-2960">One digit</span></span> 
- <span data-ttu-id="6b58c-2961">Fünf Ziffern im Datumsformat TTMMJ für das Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="6b58c-2961">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="6b58c-2962">Zwei Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) oder die Ziffer 9 anstelle eines Buchstabens</span><span class="sxs-lookup"><span data-stu-id="6b58c-2962">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="6b58c-2963">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2963">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2964">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2964">Checksum</span></span>

<span data-ttu-id="6b58c-2965">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-2965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2966">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2966">Definition</span></span>

<span data-ttu-id="6b58c-2967">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2967">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2968">Die Funktion Func_uk_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2968">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2969">Ein Schlüsselwort aus Keyword_uk_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2969">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="6b58c-2970">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2970">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-2971">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-2971">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="6b58c-2972">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="6b58c-2972">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="6b58c-2973">DVLA
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2973">DVLA</span></span> 
- <span data-ttu-id="6b58c-2974">light vans
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2974">light vans</span></span> 
- <span data-ttu-id="6b58c-2975">quadbikes
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2975">quadbikes</span></span> 
- <span data-ttu-id="6b58c-2976">motor cars
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2976">motor cars</span></span> 
- <span data-ttu-id="6b58c-2977">125cc</span><span class="sxs-lookup"><span data-stu-id="6b58c-2977">125cc</span></span> 
- <span data-ttu-id="6b58c-2978">sidecar
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2978">sidecar</span></span> 
- <span data-ttu-id="6b58c-2979">tricycles
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2979">tricycles</span></span> 
- <span data-ttu-id="6b58c-2980">motorcycles
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2980">motorcycles</span></span> 
- <span data-ttu-id="6b58c-2981">photocard licence
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2981">photocard licence</span></span> 
- <span data-ttu-id="6b58c-2982">learner drivers
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2982">learner drivers</span></span> 
- <span data-ttu-id="6b58c-2983">licence holder
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2983">licence holder</span></span> 
- <span data-ttu-id="6b58c-2984">licence holders
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2984">licence holders</span></span> 
- <span data-ttu-id="6b58c-2985">driving licences
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2985">driving licences</span></span> 
- <span data-ttu-id="6b58c-2986">driving licence
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2986">driving licence</span></span> 
- <span data-ttu-id="6b58c-2987">dual control car
</span><span class="sxs-lookup"><span data-stu-id="6b58c-2987">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="6b58c-p142">Britische Wählerverzeichnisnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-2990">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-2990">Format</span></span>

<span data-ttu-id="6b58c-2991">Zwei Buchstaben gefolgt von 1-4 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2991">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-2992">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-2992">Pattern</span></span>

<span data-ttu-id="6b58c-2993">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von 1-4 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-2993">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-2994">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-2994">Checksum</span></span>

<span data-ttu-id="6b58c-2995">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-2995">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-2996">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-2996">Definition</span></span>

<span data-ttu-id="6b58c-2997">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-2997">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-2998">Der reguläre Ausdruck Regex_uk_electoral findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2998">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-2999">Ein Schlüsselwort aus Keyword_uk_electoral wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-2999">A keyword from Keyword_uk_electoral is found.</span></span>

```
<!-- U.K. Electoral Number -->
<Entity id="a3eea206-dc0c-4f06-9e22-aa1be3059963" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_uk_electoral" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_electoral" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-3000">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-3000">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="6b58c-3001">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="6b58c-3001">Keyword_uk_electoral</span></span>

- <span data-ttu-id="6b58c-3002">council nomination
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3002">council nomination</span></span> 
- <span data-ttu-id="6b58c-3003">nomination form
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3003">nomination form</span></span> 
- <span data-ttu-id="6b58c-3004">electoral register

</span><span class="sxs-lookup"><span data-stu-id="6b58c-3004">electoral register</span></span> 
- <span data-ttu-id="6b58c-3005">electoral roll</span><span class="sxs-lookup"><span data-stu-id="6b58c-3005">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="6b58c-p143">Britische National Health Service-Nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-3008">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-3008">Format</span></span>

<span data-ttu-id="6b58c-3009">10-17 Ziffern, durch Leerzeichen getrennt</span><span class="sxs-lookup"><span data-stu-id="6b58c-3009">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-3010">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-3010">Pattern</span></span>

<span data-ttu-id="6b58c-3011">10 bis 17 Stellen:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3011">10-17 digits:</span></span>
- <span data-ttu-id="6b58c-3012">3 oder 10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3012">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="6b58c-3013">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-3013">A space</span></span> 
- <span data-ttu-id="6b58c-3014">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3014">Three digits</span></span> 
- <span data-ttu-id="6b58c-3015">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="6b58c-3015">A space</span></span> 
- <span data-ttu-id="6b58c-3016">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3016">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-3017">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-3017">Checksum</span></span>

<span data-ttu-id="6b58c-3018">Ja</span><span class="sxs-lookup"><span data-stu-id="6b58c-3018">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-3019">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-3019">Definition</span></span>

<span data-ttu-id="6b58c-3020">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3020">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3021">Die Funktion Func_uk_nhs_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3021">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3022">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3022">One of the following is true:</span></span>
    - <span data-ttu-id="6b58c-3023">Ein Schlüsselwort aus Keyword_uk_nhs_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3023">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="6b58c-3024">Ein Schlüsselwort aus Keyword_uk_nhs_number1 wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3024">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="6b58c-3025">Ein Schlüsselwort aus Keyword_uk_nhs_number_dob wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3025">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="6b58c-3026">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3026">The checksum passes.</span></span>

```
<!-- U.K. NHS Number -->
<Entity id="3192014e-2a16-44e9-aa69-4b20375c9a78" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nhs_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nhs_number" />
          <Match idRef="Keyword_uk_nhs_number1" />
          <Match idRef="Keyword_uk_nhs_number_dob" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-3027">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-3027">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="6b58c-3028">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="6b58c-3028">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="6b58c-3029">national health service
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3029">national health service</span></span> 
- <span data-ttu-id="6b58c-3030">nhs
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3030">nhs</span></span> 
- <span data-ttu-id="6b58c-3031">health services authority

</span><span class="sxs-lookup"><span data-stu-id="6b58c-3031">health services authority</span></span> 
- <span data-ttu-id="6b58c-3032">health authority</span><span class="sxs-lookup"><span data-stu-id="6b58c-3032">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="6b58c-3033">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="6b58c-3033">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="6b58c-3034">patient id
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3034">patient id</span></span> 
- <span data-ttu-id="6b58c-3035">patient identification
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3035">patient identification</span></span> 
- <span data-ttu-id="6b58c-3036">patient no

</span><span class="sxs-lookup"><span data-stu-id="6b58c-3036">patient no</span></span> 
- <span data-ttu-id="6b58c-3037">patient number</span><span class="sxs-lookup"><span data-stu-id="6b58c-3037">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="6b58c-3038">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="6b58c-3038">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="6b58c-3039">GP</span><span class="sxs-lookup"><span data-stu-id="6b58c-3039">GP</span></span> 
- <span data-ttu-id="6b58c-3040">DOB
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3040">DOB</span></span> 
- <span data-ttu-id="6b58c-3041">D.O.B</span><span class="sxs-lookup"><span data-stu-id="6b58c-3041">D.O.B</span></span> 
- <span data-ttu-id="6b58c-3042">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3042">Date of Birth</span></span> 
- <span data-ttu-id="6b58c-3043">Birth Date
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3043">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="6b58c-p144">Britische nationale Versicherungsnummer (NINO)</span><span class="sxs-lookup"><span data-stu-id="6b58c-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-3046">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-3046">Format</span></span>

<span data-ttu-id="6b58c-3047">7 oder 9 Zeichen getrennt durch Leerzeichen oder Strich</span><span class="sxs-lookup"><span data-stu-id="6b58c-3047">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-3048">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-3048">Pattern</span></span>

<span data-ttu-id="6b58c-3049">Zwei mögliche Muster:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3049">Two possible patterns:</span></span>

- <span data-ttu-id="6b58c-3050">Zwei Buchstaben (gültige NINOs verwenden Sie nur bestimmte Zeichen in dieses Präfix, das von diesem Muster überprüft; nicht Groß-/Kleinschreibung beachten)</span><span class="sxs-lookup"><span data-stu-id="6b58c-3050">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="6b58c-3051">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3051">Six digits</span></span>
- <span data-ttu-id="6b58c-3052">Entweder 'A', 'B', 'C', oder hatte ' (wie das Präfix nur bestimmte Zeichen in das Suffix; nicht zwischen Groß-und Kleinschreibung sind zulässig)</span><span class="sxs-lookup"><span data-stu-id="6b58c-3052">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="6b58c-3053">OR</span><span class="sxs-lookup"><span data-stu-id="6b58c-3053">OR</span></span>

- <span data-ttu-id="6b58c-3054">Zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="6b58c-3054">Two letters</span></span>
- <span data-ttu-id="6b58c-3055">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-3055">A space or dash</span></span>
- <span data-ttu-id="6b58c-3056">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3056">Two digits</span></span>
- <span data-ttu-id="6b58c-3057">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-3057">A space or dash</span></span>
- <span data-ttu-id="6b58c-3058">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3058">Two digits</span></span>
- <span data-ttu-id="6b58c-3059">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-3059">A space or dash</span></span>
- <span data-ttu-id="6b58c-3060">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3060">Two digits</span></span>
- <span data-ttu-id="6b58c-3061">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-3061">A space or dash</span></span>
- <span data-ttu-id="6b58c-3062">Entweder 'A', 'B', 'C', oder hatte '</span><span class="sxs-lookup"><span data-stu-id="6b58c-3062">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-3063">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-3063">Checksum</span></span>

<span data-ttu-id="6b58c-3064">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-3064">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-3065">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-3065">Definition</span></span>

<span data-ttu-id="6b58c-3066">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3066">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3067">Die Funktion Func_uk_nino findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3067">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3068">Ein Schlüsselwort aus Keyword_uk_nino wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3068">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="6b58c-3069">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3069">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3070">Die Funktion Func_uk_nino findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3070">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3071">Es wurde kein Schlüsselwort aus Keyword_uk_nino gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3071">No keyword from Keyword_uk_nino is found.</span></span>

```
<!-- U.K. NINO -->
<Entity id="16c07343-c26f-49d2-a987-3daf717e94cc" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-3072">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-3072">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="6b58c-3073">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="6b58c-3073">Keyword_uk_nino</span></span>

- <span data-ttu-id="6b58c-3074">national insurance number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3074">national insurance number</span></span> 
- <span data-ttu-id="6b58c-3075">national insurance contributions
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3075">national insurance contributions</span></span> 
- <span data-ttu-id="6b58c-3076">protection act
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3076">protection act</span></span> 
- <span data-ttu-id="6b58c-3077">insurance
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3077">insurance</span></span> 
- <span data-ttu-id="6b58c-3078">social security number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3078">social security number</span></span> 
- <span data-ttu-id="6b58c-3079">insurance application
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3079">insurance application</span></span> 
- <span data-ttu-id="6b58c-3080">medical application
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3080">medical application</span></span> 
- <span data-ttu-id="6b58c-3081">social insurance
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3081">social insurance</span></span> 
- <span data-ttu-id="6b58c-3082">medical attention
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3082">medical attention</span></span> 
- <span data-ttu-id="6b58c-3083">soziale Sicherheit</span><span class="sxs-lookup"><span data-stu-id="6b58c-3083">social security</span></span> 
- <span data-ttu-id="6b58c-3084">great britain
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3084">great britain</span></span> 
- <span data-ttu-id="6b58c-3085">insurance
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3085">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="6b58c-p145">US-amerikanische/britische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-3088">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-3088">Format</span></span>

<span data-ttu-id="6b58c-3089">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3089">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-3090">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-3090">Pattern</span></span>

<span data-ttu-id="6b58c-3091">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3091">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-3092">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-3092">Checksum</span></span>

<span data-ttu-id="6b58c-3093">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-3093">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-3094">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-3094">Definition</span></span>

<span data-ttu-id="6b58c-3095">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3095">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3096">Die Funktion Func_usa_uk_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3096">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3097">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3097">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-3098">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-3098">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="6b58c-3099">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="6b58c-3099">Keyword_passport</span></span>

- <span data-ttu-id="6b58c-3100">Passport Number</span><span class="sxs-lookup"><span data-stu-id="6b58c-3100">Passport Number</span></span> 
- <span data-ttu-id="6b58c-3101">
Passport No</span><span class="sxs-lookup"><span data-stu-id="6b58c-3101">Passport No</span></span> 
- <span data-ttu-id="6b58c-3102">Passport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3102">Passport #</span></span> 
- <span data-ttu-id="6b58c-3103">Passport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3103">Passport#</span></span> 
- <span data-ttu-id="6b58c-3104">PassportID</span><span class="sxs-lookup"><span data-stu-id="6b58c-3104">PassportID</span></span> 
- <span data-ttu-id="6b58c-3105">Passportno
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3105">Passportno</span></span> 
- <span data-ttu-id="6b58c-3106">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3106">passportnumber</span></span> 
- <span data-ttu-id="6b58c-3107">パスポート</span><span class="sxs-lookup"><span data-stu-id="6b58c-3107">パスポート</span></span> 
- <span data-ttu-id="6b58c-3108">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3108">パスポート番号</span></span> 
- <span data-ttu-id="6b58c-3109">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3109">パスポートのNum</span></span> 
- <span data-ttu-id="6b58c-3110">パスポート ＃
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3110">パスポート＃</span></span> 
- <span data-ttu-id="6b58c-3111">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="6b58c-3111">Numéro de passeport</span></span> 
- <span data-ttu-id="6b58c-3112">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="6b58c-3112">Passeport n °</span></span> 
- <span data-ttu-id="6b58c-3113">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3113">Passeport Non</span></span> 
- <span data-ttu-id="6b58c-3114">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3114">Passeport #</span></span> 
- <span data-ttu-id="6b58c-3115">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3115">Passeport#</span></span> 
- <span data-ttu-id="6b58c-3116">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="6b58c-3116">PasseportNon</span></span> 
- <span data-ttu-id="6b58c-3117">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3117">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="6b58c-3118">US-Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-3118">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-3119">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-3119">Format</span></span>

<span data-ttu-id="6b58c-3120">8-17 Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3120">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-3121">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-3121">Pattern</span></span>

<span data-ttu-id="6b58c-3122">8-17 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3122">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-3123">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-3123">Checksum</span></span>

<span data-ttu-id="6b58c-3124">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-3124">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-3125">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-3125">Definition</span></span>

<span data-ttu-id="6b58c-3126">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3126">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3127">Der reguläre Ausdruck Regex_usa_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3127">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3128">Ein Schlüsselwort aus Keyword_usa_Bank_Account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3128">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-3129">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-3129">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="6b58c-3130">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="6b58c-3130">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="6b58c-3131">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3131">Checking Account Number</span></span> 
- <span data-ttu-id="6b58c-3132">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3132">Checking Account</span></span> 
- <span data-ttu-id="6b58c-3133">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3133">Checking Account #</span></span> 
- <span data-ttu-id="6b58c-3134">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3134">Checking Acct Number</span></span> 
- <span data-ttu-id="6b58c-3135">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3135">Checking Acct #</span></span> 
- <span data-ttu-id="6b58c-3136">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3136">Checking Acct No.</span></span> 
- <span data-ttu-id="6b58c-3137">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3137">Checking Account No.</span></span> 
- <span data-ttu-id="6b58c-3138">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3138">Bank Account Number</span></span> 
- <span data-ttu-id="6b58c-3139">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3139">Bank Account #</span></span> 
- <span data-ttu-id="6b58c-3140">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3140">Bank Acct Number</span></span> 
- <span data-ttu-id="6b58c-3141">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3141">Bank Acct #</span></span> 
- <span data-ttu-id="6b58c-3142">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3142">Bank Acct No.</span></span> 
- <span data-ttu-id="6b58c-3143">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3143">Bank Account No.</span></span> 
- <span data-ttu-id="6b58c-3144">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3144">Savings Account Number</span></span> 
- <span data-ttu-id="6b58c-3145">Savings Account
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3145">Savings Account.</span></span> 
- <span data-ttu-id="6b58c-3146">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3146">Savings Account #</span></span> 
- <span data-ttu-id="6b58c-3147">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3147">Savings Acct Number</span></span> 
- <span data-ttu-id="6b58c-3148">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3148">Savings Acct #</span></span> 
- <span data-ttu-id="6b58c-3149">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3149">Savings Acct No.</span></span> 
- <span data-ttu-id="6b58c-3150">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3150">Savings Account No.</span></span> 
- <span data-ttu-id="6b58c-3151">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3151">Debit Account Number</span></span> 
- <span data-ttu-id="6b58c-3152">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3152">Debit Account</span></span> 
- <span data-ttu-id="6b58c-3153">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3153">Debit Account #</span></span> 
- <span data-ttu-id="6b58c-3154">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3154">Debit Acct Number</span></span> 
- <span data-ttu-id="6b58c-3155">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3155">Debit Acct #</span></span> 
- <span data-ttu-id="6b58c-3156">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3156">Debit Acct No.</span></span> 
- <span data-ttu-id="6b58c-3157">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3157">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="6b58c-3158">US-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-3158">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-3159">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-3159">Format</span></span>

<span data-ttu-id="6b58c-3160">Abhängig vom Bundesstaat</span><span class="sxs-lookup"><span data-stu-id="6b58c-3160">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-3161">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-3161">Pattern</span></span>

<span data-ttu-id="6b58c-3162">Abhängig vom Bundesstaat – am Beispiel für New York:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3162">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="6b58c-3163">Neun Ziffern im Format ddd ddd ddd stimmen überein.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3163">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="6b58c-3164">Neun Ziffern im Format ddddddddd stimmen nicht überein.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3164">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-3165">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-3165">Checksum</span></span>

<span data-ttu-id="6b58c-3166">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-3166">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-3167">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-3167">Definition</span></span>

<span data-ttu-id="6b58c-3168">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3168">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3169">Die Funktion Func_new_york_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3169">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3170">Ein Schlüsselwort aus Keyword_[state_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3170">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="6b58c-3171">Ein Schlüsselwort aus Keyword_us_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3171">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="6b58c-3172">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3172">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3173">Die Funktion Func_new_york_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3173">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3174">Ein Schlüsselwort aus Keyword_[state_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3174">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="6b58c-3175">Ein Schlüsselwort aus Keyword_us_drivers_license_abbreviations wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3175">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="6b58c-3176">Es wurde kein Schlüsselwort aus Keyword_us_drivers_license gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3176">No keyword from Keyword_us_drivers_license is found.</span></span>

```
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license" />
    </Pattern>
    <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license_abbreviations" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_us_drivers_license" />
        </Any>
    </Pattern>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-3177">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-3177">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="6b58c-3178">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="6b58c-3178">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="6b58c-3179">DL</span><span class="sxs-lookup"><span data-stu-id="6b58c-3179">DL</span></span> 
- <span data-ttu-id="6b58c-3180">DLS</span><span class="sxs-lookup"><span data-stu-id="6b58c-3180">DLS</span></span> 
- <span data-ttu-id="6b58c-3181">CDL</span><span class="sxs-lookup"><span data-stu-id="6b58c-3181">CDL</span></span> 
- <span data-ttu-id="6b58c-3182">CDLS</span><span class="sxs-lookup"><span data-stu-id="6b58c-3182">CDLS</span></span> 
- <span data-ttu-id="6b58c-3183">ID</span><span class="sxs-lookup"><span data-stu-id="6b58c-3183">ID</span></span> 
- <span data-ttu-id="6b58c-3184">IDs</span><span class="sxs-lookup"><span data-stu-id="6b58c-3184">IDs</span></span> 
- <span data-ttu-id="6b58c-3185">DL#</span><span class="sxs-lookup"><span data-stu-id="6b58c-3185">DL#</span></span> 
- <span data-ttu-id="6b58c-3186">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3186">DLS#</span></span> 
- <span data-ttu-id="6b58c-3187">CDL#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3187">CDL#</span></span> 
- <span data-ttu-id="6b58c-3188">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3188">CDLS#</span></span> 
- <span data-ttu-id="6b58c-3189">ID#</span><span class="sxs-lookup"><span data-stu-id="6b58c-3189">ID#</span></span>
- <span data-ttu-id="6b58c-3190">
IDs#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3190">IDs#</span></span> 
- <span data-ttu-id="6b58c-3191">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-3191">ID number</span></span> 
- <span data-ttu-id="6b58c-3192">ID numbers
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3192">ID numbers</span></span> 
- <span data-ttu-id="6b58c-3193">LIC</span><span class="sxs-lookup"><span data-stu-id="6b58c-3193">LIC</span></span> 
- <span data-ttu-id="6b58c-3194">LIC#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3194">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="6b58c-3195">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="6b58c-3195">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="6b58c-3196">DriverLic</span><span class="sxs-lookup"><span data-stu-id="6b58c-3196">DriverLic</span></span> 
- <span data-ttu-id="6b58c-3197">DriverLics</span><span class="sxs-lookup"><span data-stu-id="6b58c-3197">DriverLics</span></span> 
- <span data-ttu-id="6b58c-3198">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="6b58c-3198">DriverLicense</span></span> 
- <span data-ttu-id="6b58c-3199">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-3199">DriverLicenses</span></span> 
- <span data-ttu-id="6b58c-3200">Treiber Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-3200">Driver Lic</span></span> 
- <span data-ttu-id="6b58c-3201">Treiber Lics</span><span class="sxs-lookup"><span data-stu-id="6b58c-3201">Driver Lics</span></span> 
- <span data-ttu-id="6b58c-3202">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-3202">Driver License</span></span> 
- <span data-ttu-id="6b58c-3203">Treiber-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-3203">Driver Licenses</span></span> 
- <span data-ttu-id="6b58c-3204">DriversLic</span><span class="sxs-lookup"><span data-stu-id="6b58c-3204">DriversLic</span></span> 
- <span data-ttu-id="6b58c-3205">DriversLics</span><span class="sxs-lookup"><span data-stu-id="6b58c-3205">DriversLics</span></span> 
- <span data-ttu-id="6b58c-3206">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="6b58c-3206">DriversLicense</span></span> 
- <span data-ttu-id="6b58c-3207">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-3207">DriversLicenses</span></span> 
- <span data-ttu-id="6b58c-3208">Treiber Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-3208">Drivers Lic</span></span> 
- <span data-ttu-id="6b58c-3209">Treiber Lics</span><span class="sxs-lookup"><span data-stu-id="6b58c-3209">Drivers Lics</span></span> 
- <span data-ttu-id="6b58c-3210">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-3210">Drivers License</span></span> 
- <span data-ttu-id="6b58c-3211">Treiber-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-3211">Drivers Licenses</span></span> 
- <span data-ttu-id="6b58c-3212">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-3212">Driver'Lic</span></span> 
- <span data-ttu-id="6b58c-3213">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="6b58c-3213">Driver'Lics</span></span> 
- <span data-ttu-id="6b58c-3214">Driver'License</span><span class="sxs-lookup"><span data-stu-id="6b58c-3214">Driver'License</span></span> 
- <span data-ttu-id="6b58c-3215">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-3215">Driver'Licenses</span></span> 
- <span data-ttu-id="6b58c-3216">Treiber ' Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-3216">Driver' Lic</span></span> 
- <span data-ttu-id="6b58c-3217">Treiber ' Lics</span><span class="sxs-lookup"><span data-stu-id="6b58c-3217">Driver' Lics</span></span> 
- <span data-ttu-id="6b58c-3218">Treiber ' Lizenz</span><span class="sxs-lookup"><span data-stu-id="6b58c-3218">Driver' License</span></span> 
- <span data-ttu-id="6b58c-3219">Treiber ' Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-3219">Driver' Licenses</span></span>
- <span data-ttu-id="6b58c-3220">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="6b58c-3220">Driver'sLic</span></span> 
- <span data-ttu-id="6b58c-3221">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="6b58c-3221">Driver'sLics</span></span> 
- <span data-ttu-id="6b58c-3222">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="6b58c-3222">Driver'sLicense</span></span> 
- <span data-ttu-id="6b58c-3223">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="6b58c-3223">Driver'sLicenses</span></span> 
- <span data-ttu-id="6b58c-3224">Des Treibers Lic</span><span class="sxs-lookup"><span data-stu-id="6b58c-3224">Driver's Lic</span></span> 
- <span data-ttu-id="6b58c-3225">Lics des Treibers</span><span class="sxs-lookup"><span data-stu-id="6b58c-3225">Driver's Lics</span></span> 
- <span data-ttu-id="6b58c-3226">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-3226">Driver's License</span></span> 
- <span data-ttu-id="6b58c-3227">Des Treibers Lizenzen</span><span class="sxs-lookup"><span data-stu-id="6b58c-3227">Driver's Licenses</span></span> 
- <span data-ttu-id="6b58c-3228">identification number
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3228">identification number</span></span> 
- <span data-ttu-id="6b58c-3229">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3229">identification numbers</span></span> 
- <span data-ttu-id="6b58c-3230">identification#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3230">identification #</span></span> 
- <span data-ttu-id="6b58c-3231">ID-Karte</span><span class="sxs-lookup"><span data-stu-id="6b58c-3231">id card</span></span> 
- <span data-ttu-id="6b58c-3232">ID-Karten</span><span class="sxs-lookup"><span data-stu-id="6b58c-3232">id cards</span></span> 
- <span data-ttu-id="6b58c-3233">Ausweis</span><span class="sxs-lookup"><span data-stu-id="6b58c-3233">identification card</span></span> 
- <span data-ttu-id="6b58c-3234">Kennung Visitenkarten (engl.)</span><span class="sxs-lookup"><span data-stu-id="6b58c-3234">identification cards</span></span> 
- <span data-ttu-id="6b58c-3235">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3235">DriverLic#</span></span> 
- <span data-ttu-id="6b58c-3236">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3236">DriverLics#</span></span> 
- <span data-ttu-id="6b58c-3237">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3237">DriverLicense#</span></span> 
- <span data-ttu-id="6b58c-3238">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3238">DriverLicenses#</span></span> 
- <span data-ttu-id="6b58c-3239">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="6b58c-3239">Driver Lic#</span></span> 
- <span data-ttu-id="6b58c-3240">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3240">Driver Lics#</span></span> 
- <span data-ttu-id="6b58c-3241">Treiber Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3241">Driver License#</span></span> 
- <span data-ttu-id="6b58c-3242">Treiber Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3242">Driver Licenses#</span></span> 
- <span data-ttu-id="6b58c-3243">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3243">DriversLic#</span></span> 
- <span data-ttu-id="6b58c-3244">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3244">DriversLics#</span></span> 
- <span data-ttu-id="6b58c-3245">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3245">DriversLicense#</span></span> 
- <span data-ttu-id="6b58c-3246">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3246">DriversLicenses#</span></span> 
- <span data-ttu-id="6b58c-3247">Treiber Lic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3247">Drivers Lic#</span></span> 
- <span data-ttu-id="6b58c-3248">Treiber Lics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3248">Drivers Lics#</span></span> 
- <span data-ttu-id="6b58c-3249">Treiber Lizenz #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3249">Drivers License#</span></span> 
- <span data-ttu-id="6b58c-3250">Treiber Lizenzen #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3250">Drivers Licenses#</span></span> 
- <span data-ttu-id="6b58c-3251">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3251">Driver'Lic#</span></span> 
- <span data-ttu-id="6b58c-3252">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3252">Driver'Lics#</span></span> 
- <span data-ttu-id="6b58c-3253">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3253">Driver'License#</span></span> 
- <span data-ttu-id="6b58c-3254">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3254">Driver'Licenses#</span></span> 
- <span data-ttu-id="6b58c-3255">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3255">Driver' Lic#</span></span> 
- <span data-ttu-id="6b58c-3256">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3256">Driver' Lics#</span></span> 
- <span data-ttu-id="6b58c-3257">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3257">Driver' License#</span></span> 
- <span data-ttu-id="6b58c-3258">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3258">Driver' Licenses#</span></span> 
- <span data-ttu-id="6b58c-3259">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3259">Driver'sLic#</span></span> 
- <span data-ttu-id="6b58c-3260">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3260">Driver'sLics#</span></span> 
- <span data-ttu-id="6b58c-3261">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3261">Driver'sLicense#</span></span> 
- <span data-ttu-id="6b58c-3262">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3262">Driver'sLicenses#</span></span> 
- <span data-ttu-id="6b58c-3263">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3263">Driver's Lic#</span></span> 
- <span data-ttu-id="6b58c-3264">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3264">Driver's Lics#</span></span> 
- <span data-ttu-id="6b58c-3265">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3265">Driver's License#</span></span> 
- <span data-ttu-id="6b58c-3266">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3266">Driver's Licenses#</span></span> 
- <span data-ttu-id="6b58c-3267">d ' identité #</span><span class="sxs-lookup"><span data-stu-id="6b58c-3267">id card#</span></span> 
- <span data-ttu-id="6b58c-3268">id cards#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3268">id cards#</span></span> 
- <span data-ttu-id="6b58c-3269">identification card#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3269">identification card#</span></span> 
- <span data-ttu-id="6b58c-3270">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3270">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="6b58c-3271">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="6b58c-3271">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="6b58c-3272">Abkürzung für Bundesstaat (z. B. „NY“)
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3272">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="6b58c-3273">Name des Bundesstaats (z. B. „New York“)
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3273">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="6b58c-3274">US-Steueridentifikationsnummer (ITIN)</span><span class="sxs-lookup"><span data-stu-id="6b58c-3274">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-3275">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-3275">Format</span></span>

<span data-ttu-id="6b58c-3276">Neun Ziffern, die mit "9" beginnen und "7" oder "8" als vierte Ziffer enthalten, optional mit Leerzeichen oder Bindestrichen formatiert</span><span class="sxs-lookup"><span data-stu-id="6b58c-3276">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-3277">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-3277">Pattern</span></span>

<span data-ttu-id="6b58c-3278">Formatiert:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3278">Formatted:</span></span>
- <span data-ttu-id="6b58c-3279">Die Ziffer 9</span><span class="sxs-lookup"><span data-stu-id="6b58c-3279">The digit "9"</span></span> 
- <span data-ttu-id="6b58c-3280">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3280">Two digits</span></span> 
- <span data-ttu-id="6b58c-3281">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-3281">A space or dash</span></span> 
- <span data-ttu-id="6b58c-3282">Eine 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="6b58c-3282">A "7" or "8"</span></span> 
- <span data-ttu-id="6b58c-3283">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="6b58c-3283">A digit</span></span> 
- <span data-ttu-id="6b58c-3284">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="6b58c-3284">A space, or dash</span></span> 
- <span data-ttu-id="6b58c-3285">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3285">Four digits</span></span>

<span data-ttu-id="6b58c-3286">Unformatiert:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3286">Unformatted:</span></span>
- <span data-ttu-id="6b58c-3287">Die Ziffer 9</span><span class="sxs-lookup"><span data-stu-id="6b58c-3287">The digit "9"</span></span> 
- <span data-ttu-id="6b58c-3288">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3288">Two digits</span></span> 
- <span data-ttu-id="6b58c-3289">Eine 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="6b58c-3289">A "7" or "8"</span></span> 
- <span data-ttu-id="6b58c-3290">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="6b58c-3290">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-3291">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-3291">Checksum</span></span>

<span data-ttu-id="6b58c-3292">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-3292">No</span></span>

### <a name="definition"></a><span data-ttu-id="6b58c-3293">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-3293">Definition</span></span>

<span data-ttu-id="6b58c-3294">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3294">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3295">Die Funktion Func_formatted_itin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3295">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3296">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3296">At least one of the following is true:</span></span>
    - <span data-ttu-id="6b58c-3297">Ein Schlüsselwort aus Keyword_itin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3297">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="6b58c-3298">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3298">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="6b58c-3299">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3299">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="6b58c-3300">Ein Schlüsselwort aus Keyword_itin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3300">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="6b58c-3301">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3301">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3302">Die Funktion Func_unformatted_itin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3302">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3303">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3303">At least one of the following is true:</span></span>
    - <span data-ttu-id="6b58c-3304">Ein Schlüsselwort aus Keyword_itin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3304">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="6b58c-3305">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3305">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="6b58c-3306">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3306">The function Func_us_date finds a date in the right date format.</span></span>

```
<!-- U.S. Individual Taxpayer Identification Number (ITIN) -->
<Entity id="e55e2a32-f92d-4985-a35d-a0b269eb687b" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_formatted_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
          <Match idRef="Keyword_itin_collaborative" />
        </Any>
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_itin" />
        <Match idRef="Keyword_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin_collaborative" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-3307">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-3307">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="6b58c-3308">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="6b58c-3308">Keyword_itin</span></span>

- <span data-ttu-id="6b58c-3309">taxpayer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3309">taxpayer</span></span> 
- <span data-ttu-id="6b58c-3310">tax id
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3310">tax id</span></span> 
- <span data-ttu-id="6b58c-3311">tax identification
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3311">tax identification</span></span> 
- <span data-ttu-id="6b58c-3312">itin
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3312">itin</span></span> 
- <span data-ttu-id="6b58c-3313">ssn</span><span class="sxs-lookup"><span data-stu-id="6b58c-3313">ssn</span></span> 
- <span data-ttu-id="6b58c-3314">tin
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3314">tin</span></span> 
- <span data-ttu-id="6b58c-3315">soziale Sicherheit</span><span class="sxs-lookup"><span data-stu-id="6b58c-3315">social security</span></span> 
- <span data-ttu-id="6b58c-3316">tax payer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3316">tax payer</span></span> 
- <span data-ttu-id="6b58c-3317">itins
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3317">itins</span></span> 
- <span data-ttu-id="6b58c-3318">taxid

</span><span class="sxs-lookup"><span data-stu-id="6b58c-3318">taxid</span></span> 
- <span data-ttu-id="6b58c-3319">individual taxpayer
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3319">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="6b58c-3320">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="6b58c-3320">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="6b58c-3321">License</span><span class="sxs-lookup"><span data-stu-id="6b58c-3321">License</span></span> 
- <span data-ttu-id="6b58c-3322">DL</span><span class="sxs-lookup"><span data-stu-id="6b58c-3322">DL</span></span> 
- <span data-ttu-id="6b58c-3323">DOB
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3323">DOB</span></span> 
- <span data-ttu-id="6b58c-3324">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="6b58c-3324">Birthdate</span></span> 
- <span data-ttu-id="6b58c-3325">Geburtstag </span><span class="sxs-lookup"><span data-stu-id="6b58c-3325">Birthday</span></span> 
- <span data-ttu-id="6b58c-3326">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3326">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="6b58c-3327">US-Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="6b58c-3327">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="6b58c-3328">Format</span><span class="sxs-lookup"><span data-stu-id="6b58c-3328">Format</span></span>

<span data-ttu-id="6b58c-3329">9 Ziffern in formatiertem oder unformatiertem Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-3329">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="6b58c-3330">Vor Mitte 2011 ausgestellte US-Sozialversicherungsnummer weisen eine starke Formatierung auf. Hier müssen sich bestimmte Teile innerhalb entsprechender Bereiche befinden, damit diese gültig sind. (Es ist jedoch keine Prüfsumme vorhanden).</span><span class="sxs-lookup"><span data-stu-id="6b58c-3330">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="6b58c-3331">Muster</span><span class="sxs-lookup"><span data-stu-id="6b58c-3331">Pattern</span></span>

<span data-ttu-id="6b58c-3332">Vier Funktionen suchen nach US-Sozialversicherungsnummern mit vier verschiedenen Mustern:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3332">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="6b58c-3333">Func_ssn sucht nach US-Sozialversicherungsnummern von vor 2011, die mithilfe von Bindestrichen oder Leerzeichen (ddd-dd-dddd ODER ddd dd dddd) formatiert sind </span><span class="sxs-lookup"><span data-stu-id="6b58c-3333">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="6b58c-3334">Func_unformatted_ssn sucht nach US-Sozialversicherungnummern von vor 2011, die als neun aufeinander folgende Ziffern (ddddddddd) formatiert sind</span><span class="sxs-lookup"><span data-stu-id="6b58c-3334">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="6b58c-3335">Func_randomized_formatted_ssn sucht nach US-Sozialversicherungsnummern von nach 2011, die mithilfe von Bindestrichen oder Leerzeichen (ddd-dd-dddd ODER ddd dd dddd) formatiert sind </span><span class="sxs-lookup"><span data-stu-id="6b58c-3335">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="6b58c-3336">Func_randomized_unformatted_ssn sucht nach US-Sozialversicherungnummern von nach 2011, die als neun aufeinander folgende Ziffern (ddddddddd) formatiert sind</span><span class="sxs-lookup"><span data-stu-id="6b58c-3336">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="6b58c-3337">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="6b58c-3337">Checksum</span></span>

<span data-ttu-id="6b58c-3338">Nein</span><span class="sxs-lookup"><span data-stu-id="6b58c-3338">No</span></span>


### <a name="definition"></a><span data-ttu-id="6b58c-3339">Definition</span><span class="sxs-lookup"><span data-stu-id="6b58c-3339">Definition</span></span>

<span data-ttu-id="6b58c-3340">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3340">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3341">Die Funktion Func_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3341">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3342">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3342">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="6b58c-3343">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3343">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3344">Die Funktion Func_unformatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3344">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3345">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3345">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="6b58c-3346">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3346">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3347">Die Funktion Func_randomized_formatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3347">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3348">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3348">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="6b58c-3349">Die Funktion Func_ssn findet keine Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3349">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="6b58c-3350">Eine DLP-Richtlinie ist zu 55 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6b58c-3350">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="6b58c-3351">Die Funktion Func_randomized_unformatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3351">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="6b58c-3352">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3352">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="6b58c-3353">Die Funktion Func_unformatted_ssn findet keine Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6b58c-3353">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

```
<!-- U.S. Social Security Number (SSN) -->
    <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="6b58c-3354">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="6b58c-3354">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="6b58c-3355">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="6b58c-3355">Keyword_ssn</span></span>

- <span data-ttu-id="6b58c-3356">Social Security
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3356">Social Security</span></span> 
- <span data-ttu-id="6b58c-3357">Social Security#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3357">Social Security#</span></span> 
- <span data-ttu-id="6b58c-3358">Soc Sec
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3358">Soc Sec</span></span> 
- <span data-ttu-id="6b58c-3359">SSN</span><span class="sxs-lookup"><span data-stu-id="6b58c-3359">SSN</span></span> 
- <span data-ttu-id="6b58c-3360">SSNS
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3360">SSNS</span></span> 
- <span data-ttu-id="6b58c-3361">SSN#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3361">SSN#</span></span> 
- <span data-ttu-id="6b58c-3362">SS#
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3362">SS#</span></span> 
- <span data-ttu-id="6b58c-3363">SSID
</span><span class="sxs-lookup"><span data-stu-id="6b58c-3363">SSID</span></span> 
   

