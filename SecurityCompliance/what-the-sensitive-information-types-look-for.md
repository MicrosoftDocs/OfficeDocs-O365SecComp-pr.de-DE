---
title: Wonach die Typen von vertraulichen Informationen suchen
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: Data Loss Prevention (DLP) im Office 365 Security &amp; Compliance Center enthält 80 vertrauliche Informationstypen, die Sie in ihren DLP-Richtlinien verwenden können. Dieses Thema enthält eine Liste aller dieser vertraulichen Informationstypen und zeigt, was eine DLP-Richtlinie sucht, wenn sie den jeweiligen Typen erkennt.
ms.openlocfilehash: e9811b285e98a791570dc91e275cb5cead4f8bc9
ms.sourcegitcommit: 6e8e2b43a4bea31c1e835c5b050824651c6a0094
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/11/2019
ms.locfileid: "30537642"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="302ae-104">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="302ae-104">What the sensitive information types look for</span></span>

<span data-ttu-id="302ae-105">Data Loss Prevention (DLP) im Office 365 Security &amp; Compliance Center enthält viele vertrauliche Informationstypen, die Sie in ihren DLP-Richtlinien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="302ae-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="302ae-106">Dieses Thema enthält eine Liste aller dieser vertraulichen Informationstypen und zeigt, was eine DLP-Richtlinie sucht, wenn sie den jeweiligen Typen erkennt.</span><span class="sxs-lookup"><span data-stu-id="302ae-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="302ae-107">Ein vertraulicher Informationstyp wird durch ein Muster definiert, das durch einen regulären Ausdruck oder eine Funktion identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="302ae-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="302ae-108">Darüber hinaus können auch belegende Hinweise wie Schlüsselwörter oder Prüfsummen zum Identifizieren eines Typs vertraulicher Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="302ae-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="302ae-109">Beim Auswertungsprozess können auch die Zuverlässigkeitsstufe und die Näherung herangezogen werden.</span><span class="sxs-lookup"><span data-stu-id="302ae-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="302ae-110">ABA Routing Number (US-Bankleitzahl)</span><span class="sxs-lookup"><span data-stu-id="302ae-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-111">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-111">Format</span></span>

<span data-ttu-id="302ae-112">9 Ziffern in formatiertem oder unformatiertem Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-113">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-113">Pattern</span></span>

<span data-ttu-id="302ae-114">Formatiert</span><span class="sxs-lookup"><span data-stu-id="302ae-114">Formatted:</span></span>
- <span data-ttu-id="302ae-115">Vier Ziffern, beginnend mit 0, 1, 2, 3, 6, 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="302ae-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="302ae-116">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-116">A hyphen</span></span>
- <span data-ttu-id="302ae-117">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-117">Four digits</span></span>
- <span data-ttu-id="302ae-118">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-118">A hyphen</span></span>
- <span data-ttu-id="302ae-119">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-119">A digit</span></span>

<span data-ttu-id="302ae-120">Unformatiert: 9 aufeinanderfolgende Ziffern beginnend mit 0, 1, 2, 3, 6, 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="302ae-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="302ae-121">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-121">Checksum</span></span>

<span data-ttu-id="302ae-122">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-123">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-123">Definition</span></span>

<span data-ttu-id="302ae-124">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-125">Die Funktion Func_aba_routing findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-126">Ein Schlüsselwort aus Keyword_ABA_Routing wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="302ae-127">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="302ae-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="302ae-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="302ae-129">ABA</span><span class="sxs-lookup"><span data-stu-id="302ae-129">aba</span></span>
- <span data-ttu-id="302ae-130">aba #</span><span class="sxs-lookup"><span data-stu-id="302ae-130">aba #</span></span>
- <span data-ttu-id="302ae-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="302ae-131">aba routing #</span></span>
- <span data-ttu-id="302ae-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="302ae-132">aba routing number</span></span>
- <span data-ttu-id="302ae-133">ABA</span><span class="sxs-lookup"><span data-stu-id="302ae-133">aba#</span></span>
- <span data-ttu-id="302ae-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="302ae-134">abarouting#</span></span>
- <span data-ttu-id="302ae-135">aba number</span><span class="sxs-lookup"><span data-stu-id="302ae-135">aba number</span></span>
- <span data-ttu-id="302ae-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="302ae-136">abaroutingnumber</span></span>
- <span data-ttu-id="302ae-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="302ae-137">american bank association routing #</span></span>
- <span data-ttu-id="302ae-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="302ae-138">american bank association routing number</span></span>
- <span data-ttu-id="302ae-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="302ae-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="302ae-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="302ae-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="302ae-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="302ae-141">bank routing number</span></span>
- <span data-ttu-id="302ae-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="302ae-142">bankrouting#</span></span>
- <span data-ttu-id="302ae-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="302ae-143">bankroutingnumber</span></span>
- <span data-ttu-id="302ae-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="302ae-144">routing transit number</span></span>
- <span data-ttu-id="302ae-145">RTN</span><span class="sxs-lookup"><span data-stu-id="302ae-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="302ae-146">Argentina National Identity (DNI) Number</span><span class="sxs-lookup"><span data-stu-id="302ae-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-147">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-147">Format</span></span>

<span data-ttu-id="302ae-148">Acht Ziffern, durch Punkte getrennt</span><span class="sxs-lookup"><span data-stu-id="302ae-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-149">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-149">Pattern</span></span>

<span data-ttu-id="302ae-150">Acht Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-150">Eight digits:</span></span>
- <span data-ttu-id="302ae-151">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-151">Two digits</span></span>
- <span data-ttu-id="302ae-152">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="302ae-152">A period</span></span>
- <span data-ttu-id="302ae-153">Drei Ziffern </span><span class="sxs-lookup"><span data-stu-id="302ae-153">Three digits</span></span>
- <span data-ttu-id="302ae-154">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="302ae-154">A period</span></span>
- <span data-ttu-id="302ae-155">Drei Ziffern </span><span class="sxs-lookup"><span data-stu-id="302ae-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-156">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-156">Checksum</span></span>

<span data-ttu-id="302ae-157">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-158">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-158">Definition</span></span>

<span data-ttu-id="302ae-159">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-160">Der reguläre Ausdruck Regex_argentina_national_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-161">Ein Schlüsselwort aus Keyword_argentina_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-162">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="302ae-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="302ae-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="302ae-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="302ae-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="302ae-165">Identität</span><span class="sxs-lookup"><span data-stu-id="302ae-165">Identity</span></span> 
- <span data-ttu-id="302ae-166">Identifizierung nationaler Identitätsausweis</span><span class="sxs-lookup"><span data-stu-id="302ae-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="302ae-167">DNI</span><span class="sxs-lookup"><span data-stu-id="302ae-167">DNI</span></span> 
- <span data-ttu-id="302ae-168">NIC National Registry of persons</span><span class="sxs-lookup"><span data-stu-id="302ae-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="302ae-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="302ae-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="302ae-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="302ae-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="302ae-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="302ae-171">Identidad</span></span> 
- <span data-ttu-id="302ae-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="302ae-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="302ae-173">Australische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="302ae-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-174">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-174">Format</span></span>

<span data-ttu-id="302ae-175">6-10 Stellen mit oder ohne Bankfilialnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-176">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-176">Pattern</span></span>

<span data-ttu-id="302ae-177">Kontonummer hat 6-10 Stellen.</span><span class="sxs-lookup"><span data-stu-id="302ae-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="302ae-178">Australische Bankleitzahl:</span><span class="sxs-lookup"><span data-stu-id="302ae-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="302ae-179">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-179">Three digits</span></span> 
- <span data-ttu-id="302ae-180">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-180">A hyphen</span></span> 
- <span data-ttu-id="302ae-181">Drei Stellen</span><span class="sxs-lookup"><span data-stu-id="302ae-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-182">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-182">Checksum</span></span>

<span data-ttu-id="302ae-183">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-184">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-184">Definition</span></span>

<span data-ttu-id="302ae-185">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-186">Der reguläre Ausdruck Regex_australia_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="302ae-187">Ein Schlüsselwort aus Keyword_australia_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="302ae-188">Der reguläre Ausdruck Regex_australia_bank_account_number_bsb findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="302ae-189">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-190">Der reguläre Ausdruck Regex_australia_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="302ae-191">Ein Schlüsselwort aus Keyword_australia_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-192">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="302ae-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="302ae-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="302ae-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="302ae-194">swift bank code</span></span>
- <span data-ttu-id="302ae-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="302ae-195">correspondent bank</span></span>
- <span data-ttu-id="302ae-196">base currency</span><span class="sxs-lookup"><span data-stu-id="302ae-196">base currency</span></span>
- <span data-ttu-id="302ae-197">usa account</span><span class="sxs-lookup"><span data-stu-id="302ae-197">usa account</span></span>
- <span data-ttu-id="302ae-198">holder address</span><span class="sxs-lookup"><span data-stu-id="302ae-198">holder address</span></span>
- <span data-ttu-id="302ae-199">bank address</span><span class="sxs-lookup"><span data-stu-id="302ae-199">bank address</span></span>
- <span data-ttu-id="302ae-200">information account</span><span class="sxs-lookup"><span data-stu-id="302ae-200">information account</span></span>
- <span data-ttu-id="302ae-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="302ae-201">fund transfers</span></span>
- <span data-ttu-id="302ae-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="302ae-202">bank charges</span></span>
- <span data-ttu-id="302ae-203">bank details</span><span class="sxs-lookup"><span data-stu-id="302ae-203">bank details</span></span>
- <span data-ttu-id="302ae-204">banking information</span><span class="sxs-lookup"><span data-stu-id="302ae-204">banking information</span></span>
- <span data-ttu-id="302ae-205">full names</span><span class="sxs-lookup"><span data-stu-id="302ae-205">full names</span></span>
- <span data-ttu-id="302ae-206">IAEO</span><span class="sxs-lookup"><span data-stu-id="302ae-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="302ae-207">Australische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-208">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-208">Format</span></span>

<span data-ttu-id="302ae-209">Neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-210">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-210">Pattern</span></span>

<span data-ttu-id="302ae-211">Neun Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="302ae-212">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="302ae-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="302ae-213">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-213">Two digits</span></span> 
- <span data-ttu-id="302ae-214">Fünf Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="302ae-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="302ae-215">ODER</span><span class="sxs-lookup"><span data-stu-id="302ae-215">OR</span></span>

- <span data-ttu-id="302ae-216">1-2 optionale Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="302ae-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="302ae-217">4 bis 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-217">4-9 digits</span></span>

<span data-ttu-id="302ae-218">ODER</span><span class="sxs-lookup"><span data-stu-id="302ae-218">OR</span></span>

- <span data-ttu-id="302ae-219">Neun Ziffern oder Buchstaben (Groß-/Kleinschreibung irrelevant)</span><span class="sxs-lookup"><span data-stu-id="302ae-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-220">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-220">Checksum</span></span>

<span data-ttu-id="302ae-221">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-222">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-222">Definition</span></span>

<span data-ttu-id="302ae-223">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-224">Der reguläre Ausdruck Regex_australia_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-225">Ein Schlüsselwort aus Keyword_australia_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="302ae-226">Es wurde kein Schlüsselwort aus Keyword_australia_drivers_license_number_exclusions gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-227">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="302ae-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="302ae-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="302ae-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="302ae-229">international driving permits</span></span>
- <span data-ttu-id="302ae-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="302ae-230">australian automobile association</span></span>
- <span data-ttu-id="302ae-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="302ae-231">international driving permit</span></span>
- <span data-ttu-id="302ae-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="302ae-232">DriverLicence</span></span>
- <span data-ttu-id="302ae-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="302ae-233">DriverLicences</span></span>
- <span data-ttu-id="302ae-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-234">Driver Lic</span></span>
- <span data-ttu-id="302ae-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-235">Driver Licence</span></span>
- <span data-ttu-id="302ae-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-236">Driver Licences</span></span>
- <span data-ttu-id="302ae-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="302ae-237">DriversLic</span></span>
- <span data-ttu-id="302ae-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="302ae-238">DriversLicence</span></span>
- <span data-ttu-id="302ae-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="302ae-239">DriversLicences</span></span>
- <span data-ttu-id="302ae-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-240">Drivers Lic</span></span>
- <span data-ttu-id="302ae-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-241">Drivers Lics</span></span>
- <span data-ttu-id="302ae-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-242">Drivers Licence</span></span>
- <span data-ttu-id="302ae-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-243">Drivers Licences</span></span>
- <span data-ttu-id="302ae-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-244">Driver'Lic</span></span>
- <span data-ttu-id="302ae-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-245">Driver'Lics</span></span>
- <span data-ttu-id="302ae-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-246">Driver'Licence</span></span>
- <span data-ttu-id="302ae-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-247">Driver'Licences</span></span>
- <span data-ttu-id="302ae-248">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-248">Driver' Lic</span></span>
- <span data-ttu-id="302ae-249">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-249">Driver' Lics</span></span>
- <span data-ttu-id="302ae-250">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-250">Driver' Licence</span></span>
- <span data-ttu-id="302ae-251">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-251">Driver' Licences</span></span>
- <span data-ttu-id="302ae-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="302ae-252">Driver'sLic</span></span>
- <span data-ttu-id="302ae-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="302ae-253">Driver'sLics</span></span>
- <span data-ttu-id="302ae-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="302ae-254">Driver'sLicence</span></span>
- <span data-ttu-id="302ae-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="302ae-255">Driver'sLicences</span></span>
- <span data-ttu-id="302ae-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-256">Driver's Lic</span></span>
- <span data-ttu-id="302ae-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-257">Driver's Lics</span></span>
- <span data-ttu-id="302ae-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-258">Driver's Licence</span></span>
- <span data-ttu-id="302ae-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-259">Driver's Licences</span></span>
- <span data-ttu-id="302ae-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="302ae-260">DriverLic#</span></span>
- <span data-ttu-id="302ae-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="302ae-261">DriverLics#</span></span>
- <span data-ttu-id="302ae-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="302ae-262">DriverLicence#</span></span>
- <span data-ttu-id="302ae-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="302ae-263">DriverLicences#</span></span>
- <span data-ttu-id="302ae-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-264">Driver Lic#</span></span>
- <span data-ttu-id="302ae-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-265">Driver Lics#</span></span>
- <span data-ttu-id="302ae-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="302ae-266">Driver Licence#</span></span>
- <span data-ttu-id="302ae-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="302ae-267">Driver Licences#</span></span>
- <span data-ttu-id="302ae-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="302ae-268">DriversLic#</span></span>
- <span data-ttu-id="302ae-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="302ae-269">DriversLics#</span></span>
- <span data-ttu-id="302ae-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="302ae-270">DriversLicence#</span></span>
- <span data-ttu-id="302ae-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="302ae-271">DriversLicences#</span></span>
- <span data-ttu-id="302ae-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-272">Drivers Lic#</span></span>
- <span data-ttu-id="302ae-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-273">Drivers Lics#</span></span>
- <span data-ttu-id="302ae-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="302ae-274">Drivers Licence#</span></span>
- <span data-ttu-id="302ae-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="302ae-275">Drivers Licences#</span></span>
- <span data-ttu-id="302ae-276">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="302ae-276">Driver'Lic#</span></span>
- <span data-ttu-id="302ae-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="302ae-277">Driver'Lics#</span></span>
- <span data-ttu-id="302ae-278">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="302ae-278">Driver'Licence#</span></span>
- <span data-ttu-id="302ae-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="302ae-279">Driver'Licences#</span></span>
- <span data-ttu-id="302ae-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-280">Driver' Lic#</span></span>
- <span data-ttu-id="302ae-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-281">Driver' Lics#</span></span>
- <span data-ttu-id="302ae-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="302ae-282">Driver' Licence#</span></span>
- <span data-ttu-id="302ae-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="302ae-283">Driver' Licences#</span></span>
- <span data-ttu-id="302ae-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="302ae-284">Driver'sLic#</span></span>
- <span data-ttu-id="302ae-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="302ae-285">Driver'sLics#</span></span>
- <span data-ttu-id="302ae-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="302ae-286">Driver'sLicence#</span></span>
- <span data-ttu-id="302ae-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="302ae-287">Driver'sLicences#</span></span>
- <span data-ttu-id="302ae-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-288">Driver's Lic#</span></span>
- <span data-ttu-id="302ae-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-289">Driver's Lics#</span></span>
- <span data-ttu-id="302ae-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="302ae-290">Driver's Licence#</span></span>
- <span data-ttu-id="302ae-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="302ae-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="302ae-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="302ae-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="302ae-293">aaa</span><span class="sxs-lookup"><span data-stu-id="302ae-293">aaa</span></span>
- <span data-ttu-id="302ae-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="302ae-294">DriverLicense</span></span>
- <span data-ttu-id="302ae-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="302ae-295">DriverLicenses</span></span>
- <span data-ttu-id="302ae-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="302ae-296">Driver License</span></span>
- <span data-ttu-id="302ae-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-297">Driver Licenses</span></span>
- <span data-ttu-id="302ae-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="302ae-298">DriversLicense</span></span>
- <span data-ttu-id="302ae-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="302ae-299">DriversLicenses</span></span>
- <span data-ttu-id="302ae-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="302ae-300">Drivers License</span></span>
- <span data-ttu-id="302ae-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-301">Drivers Licenses</span></span>
- <span data-ttu-id="302ae-302">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="302ae-302">Driver'License</span></span>
- <span data-ttu-id="302ae-303">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-303">Driver'Licenses</span></span>
- <span data-ttu-id="302ae-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="302ae-304">Driver' License</span></span>
- <span data-ttu-id="302ae-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-305">Driver' Licenses</span></span>
- <span data-ttu-id="302ae-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="302ae-306">Driver'sLicense</span></span>
- <span data-ttu-id="302ae-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="302ae-307">Driver'sLicenses</span></span>
- <span data-ttu-id="302ae-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="302ae-308">Driver's License</span></span>
- <span data-ttu-id="302ae-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-309">Driver's Licenses</span></span>
- <span data-ttu-id="302ae-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="302ae-310">DriverLicense#</span></span>
- <span data-ttu-id="302ae-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="302ae-311">DriverLicenses#</span></span>
- <span data-ttu-id="302ae-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="302ae-312">Driver License#</span></span>
- <span data-ttu-id="302ae-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-313">Driver Licenses#</span></span>
- <span data-ttu-id="302ae-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="302ae-314">DriversLicense#</span></span>
- <span data-ttu-id="302ae-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="302ae-315">DriversLicenses#</span></span>
- <span data-ttu-id="302ae-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="302ae-316">Drivers License#</span></span>
- <span data-ttu-id="302ae-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-317">Drivers Licenses#</span></span>
- <span data-ttu-id="302ae-318">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="302ae-318">Driver'License#</span></span>
- <span data-ttu-id="302ae-319">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-319">Driver'Licenses#</span></span>
- <span data-ttu-id="302ae-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="302ae-320">Driver' License#</span></span>
- <span data-ttu-id="302ae-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-321">Driver' Licenses#</span></span>
- <span data-ttu-id="302ae-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="302ae-322">Driver'sLicense#</span></span>
- <span data-ttu-id="302ae-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="302ae-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="302ae-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="302ae-324">Driver's License#</span></span>
- <span data-ttu-id="302ae-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="302ae-326">Australische Medical Account-Nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-327">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-327">Format</span></span>

<span data-ttu-id="302ae-328">10-11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-329">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-329">Pattern</span></span>

<span data-ttu-id="302ae-330">10-11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-330">10-11 digits:</span></span>
- <span data-ttu-id="302ae-331">Erste Ziffer im Bereich von 2-6</span><span class="sxs-lookup"><span data-stu-id="302ae-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="302ae-332">Neunte Ziffer ist eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="302ae-333">Zehnte Ziffer ist die Ausgabeziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="302ae-334">Elfte Ziffer (optional) ist die Einzelziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-335">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-335">Checksum</span></span>

<span data-ttu-id="302ae-336">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-337">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-337">Definition</span></span>

<span data-ttu-id="302ae-338">Eine DLP-Richtlinie ist zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-339">Die Funktion Func_australian_medical_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-340">Ein Schlüsselwort aus Keyword_Australia_Medical_Account_Number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="302ae-341">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-341">The checksum passes.</span></span>

<span data-ttu-id="302ae-342">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-343">Die Funktion Func_australian_medical_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-344">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-345">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="302ae-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="302ae-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="302ae-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="302ae-347">bank account details</span></span>
- <span data-ttu-id="302ae-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="302ae-348">medicare payments</span></span>
- <span data-ttu-id="302ae-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="302ae-349">mortgage account</span></span>
- <span data-ttu-id="302ae-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="302ae-350">bank payments</span></span>
- <span data-ttu-id="302ae-351">information branch</span><span class="sxs-lookup"><span data-stu-id="302ae-351">information branch</span></span>
- <span data-ttu-id="302ae-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="302ae-352">credit card loan</span></span>
- <span data-ttu-id="302ae-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="302ae-353">department of human services</span></span>
- <span data-ttu-id="302ae-354">local service</span><span class="sxs-lookup"><span data-stu-id="302ae-354">local service</span></span>
- <span data-ttu-id="302ae-355">Medicare</span><span class="sxs-lookup"><span data-stu-id="302ae-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="302ae-356">Australische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-357">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-357">Format</span></span>

<span data-ttu-id="302ae-358">Ein Buchstabe gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-359">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-359">Pattern</span></span>

<span data-ttu-id="302ae-360">Ein Buchstabe (Groß-/Kleinschreibung irrelevant) gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-361">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-361">Checksum</span></span>

<span data-ttu-id="302ae-362">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-363">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-363">Definition</span></span>

<span data-ttu-id="302ae-364">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-365">Der reguläre Ausdruck Regex_australia_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-366">Ein Schlüsselwort aus Keyword_passport oder Keyword_australia_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-367">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="302ae-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="302ae-368">Keyword_passport</span></span>

- <span data-ttu-id="302ae-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="302ae-369">Passport Number</span></span>
- <span data-ttu-id="302ae-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="302ae-370">Passport No</span></span>
- <span data-ttu-id="302ae-371">Passport#</span><span class="sxs-lookup"><span data-stu-id="302ae-371">Passport #</span></span>
- <span data-ttu-id="302ae-372">Pass</span><span class="sxs-lookup"><span data-stu-id="302ae-372">Passport#</span></span>
- <span data-ttu-id="302ae-373">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="302ae-373">PassportID</span></span>
- <span data-ttu-id="302ae-374">Passportno</span><span class="sxs-lookup"><span data-stu-id="302ae-374">Passportno</span></span>
- <span data-ttu-id="302ae-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="302ae-375">passportnumber</span></span>
- <span data-ttu-id="302ae-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="302ae-376">パスポート</span></span>
- <span data-ttu-id="302ae-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="302ae-377">パスポート番号</span></span>
- <span data-ttu-id="302ae-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="302ae-378">パスポートのNum</span></span>
- <span data-ttu-id="302ae-379">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="302ae-379">パスポート ＃</span></span> 
- <span data-ttu-id="302ae-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="302ae-380">Numéro de passeport</span></span>
- <span data-ttu-id="302ae-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="302ae-381">Passeport n °</span></span>
- <span data-ttu-id="302ae-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="302ae-382">Passeport Non</span></span>
- <span data-ttu-id="302ae-383">Passeport#</span><span class="sxs-lookup"><span data-stu-id="302ae-383">Passeport #</span></span>
- <span data-ttu-id="302ae-384">Passeport</span><span class="sxs-lookup"><span data-stu-id="302ae-384">Passeport#</span></span>
- <span data-ttu-id="302ae-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="302ae-385">PasseportNon</span></span>
- <span data-ttu-id="302ae-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="302ae-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="302ae-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="302ae-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="302ae-388">Pass</span><span class="sxs-lookup"><span data-stu-id="302ae-388">passport</span></span>
- <span data-ttu-id="302ae-389">passport details</span><span class="sxs-lookup"><span data-stu-id="302ae-389">passport details</span></span>
- <span data-ttu-id="302ae-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="302ae-390">immigration and citizenship</span></span>
- <span data-ttu-id="302ae-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="302ae-391">commonwealth of australia</span></span>
- <span data-ttu-id="302ae-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="302ae-392">department of immigration</span></span>
- <span data-ttu-id="302ae-393">residential address</span><span class="sxs-lookup"><span data-stu-id="302ae-393">residential address</span></span>
- <span data-ttu-id="302ae-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="302ae-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="302ae-395">Visa</span><span class="sxs-lookup"><span data-stu-id="302ae-395">visa</span></span>
- <span data-ttu-id="302ae-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="302ae-396">national identity card</span></span>
- <span data-ttu-id="302ae-397">passport number</span><span class="sxs-lookup"><span data-stu-id="302ae-397">passport number</span></span>
- <span data-ttu-id="302ae-398">travel document</span><span class="sxs-lookup"><span data-stu-id="302ae-398">travel document</span></span>
- <span data-ttu-id="302ae-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="302ae-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="302ae-400">Australische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="302ae-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-401">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-401">Format</span></span>

<span data-ttu-id="302ae-402">8-9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-403">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-403">Pattern</span></span>

<span data-ttu-id="302ae-404">8 bis 9 Ziffern, die in der Regel wie folgt mit Leerzeichen dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="302ae-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="302ae-405">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-405">Three digits</span></span> 
- <span data-ttu-id="302ae-406">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-406">An optional space</span></span> 
- <span data-ttu-id="302ae-407">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-407">Three digits</span></span> 
- <span data-ttu-id="302ae-408">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-408">An optional space</span></span> 
- <span data-ttu-id="302ae-409">2 bis 3 Ziffern, wobei die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="302ae-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-410">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-410">Checksum</span></span>

<span data-ttu-id="302ae-411">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-412">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-412">Definition</span></span>

<span data-ttu-id="302ae-413">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-414">Die Funktion Func_australian_tax_file_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-415">Es wurde kein Schlüsselwort aus Keyword_Australia_Tax_File_Number oder Keyword_number_exclusions gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="302ae-416">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-416">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-417">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="302ae-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="302ae-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="302ae-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="302ae-419">australian business number</span></span>
- <span data-ttu-id="302ae-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="302ae-420">marginal tax rate</span></span>
- <span data-ttu-id="302ae-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="302ae-421">medicare levy</span></span>
- <span data-ttu-id="302ae-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="302ae-422">portfolio number</span></span>
- <span data-ttu-id="302ae-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="302ae-423">service veterans</span></span>
- <span data-ttu-id="302ae-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="302ae-424">withholding tax</span></span>
- <span data-ttu-id="302ae-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="302ae-425">individual tax return</span></span>
- <span data-ttu-id="302ae-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="302ae-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="302ae-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="302ae-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="302ae-428">00000000</span><span class="sxs-lookup"><span data-stu-id="302ae-428">00000000</span></span>
- <span data-ttu-id="302ae-429">11111111</span><span class="sxs-lookup"><span data-stu-id="302ae-429">11111111</span></span>
- <span data-ttu-id="302ae-430">22222222</span><span class="sxs-lookup"><span data-stu-id="302ae-430">22222222</span></span>
- <span data-ttu-id="302ae-431">33333333</span><span class="sxs-lookup"><span data-stu-id="302ae-431">33333333</span></span>
- <span data-ttu-id="302ae-432">44444444</span><span class="sxs-lookup"><span data-stu-id="302ae-432">44444444</span></span>
- <span data-ttu-id="302ae-433">55555555</span><span class="sxs-lookup"><span data-stu-id="302ae-433">55555555</span></span>
- <span data-ttu-id="302ae-434">66666666</span><span class="sxs-lookup"><span data-stu-id="302ae-434">66666666</span></span>
- <span data-ttu-id="302ae-435">77777777</span><span class="sxs-lookup"><span data-stu-id="302ae-435">77777777</span></span>
- <span data-ttu-id="302ae-436">88888888</span><span class="sxs-lookup"><span data-stu-id="302ae-436">88888888</span></span>
- <span data-ttu-id="302ae-437">99999999</span><span class="sxs-lookup"><span data-stu-id="302ae-437">99999999</span></span>
- <span data-ttu-id="302ae-438">000000000</span><span class="sxs-lookup"><span data-stu-id="302ae-438">000000000</span></span>
- <span data-ttu-id="302ae-439">111111111</span><span class="sxs-lookup"><span data-stu-id="302ae-439">111111111</span></span>
- <span data-ttu-id="302ae-440">222222222</span><span class="sxs-lookup"><span data-stu-id="302ae-440">222222222</span></span>
- <span data-ttu-id="302ae-441">333333333</span><span class="sxs-lookup"><span data-stu-id="302ae-441">333333333</span></span>
- <span data-ttu-id="302ae-442">444444444</span><span class="sxs-lookup"><span data-stu-id="302ae-442">444444444</span></span>
- <span data-ttu-id="302ae-443">555555555</span><span class="sxs-lookup"><span data-stu-id="302ae-443">555555555</span></span>
- <span data-ttu-id="302ae-444">666666666</span><span class="sxs-lookup"><span data-stu-id="302ae-444">666666666</span></span>
- <span data-ttu-id="302ae-445">777777777</span><span class="sxs-lookup"><span data-stu-id="302ae-445">777777777</span></span>
- <span data-ttu-id="302ae-446">888888888</span><span class="sxs-lookup"><span data-stu-id="302ae-446">888888888</span></span>
- <span data-ttu-id="302ae-447">999999999</span><span class="sxs-lookup"><span data-stu-id="302ae-447">999999999</span></span>
- <span data-ttu-id="302ae-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="302ae-448">0000000000</span></span>
- <span data-ttu-id="302ae-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="302ae-449">1111111111</span></span>
- <span data-ttu-id="302ae-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="302ae-450">2222222222</span></span>
- <span data-ttu-id="302ae-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="302ae-451">3333333333</span></span>
- <span data-ttu-id="302ae-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="302ae-452">4444444444</span></span>
- <span data-ttu-id="302ae-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="302ae-453">5555555555</span></span>
- <span data-ttu-id="302ae-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="302ae-454">6666666666</span></span>
- <span data-ttu-id="302ae-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="302ae-455">7777777777</span></span>
- <span data-ttu-id="302ae-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="302ae-456">8888888888</span></span>
- <span data-ttu-id="302ae-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="302ae-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="302ae-458">Azure-DocumentDB-auth-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="302ae-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="302ae-459">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-459">Format</span></span>

<span data-ttu-id="302ae-460">Die Zeichenfolge "DocumentDb" gefolgt von den Zeichen und Zeichenfolgen, die im folgenden Muster erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="302ae-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-461">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-461">Pattern</span></span>

- <span data-ttu-id="302ae-462">Die Zeichenfolge "DocumentDb"</span><span class="sxs-lookup"><span data-stu-id="302ae-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="302ae-463">Eine beliebige Kombination von zwischen 3-200 Buchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="302ae-464">Ein größer-als-Symbol (>), ein Gleichheitszeichen (=), ein Anführungszeichen (") oder ein Apostroph (')</span><span class="sxs-lookup"><span data-stu-id="302ae-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="302ae-465">Eine beliebige Kombination aus 86 unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="302ae-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="302ae-466">Zwei Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-467">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-467">Checksum</span></span>

<span data-ttu-id="302ae-468">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-469">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-469">Definition</span></span>

<span data-ttu-id="302ae-470">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-471">Der reguläre Ausdruck CEP_Regex_AzureDocumentDBAuthKey findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-472">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!-- Azure Document DB Auth Key -->
<Entity id="0f587d92-eb28-44a9-bd1c-90f2892b47aa" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureDocumentDBAuthKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
          </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-473">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-473">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="302ae-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="302ae-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="302ae-475">(Beachten Sie, dass dieser vertrauliche Informationstyp diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Schlüsselwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="302ae-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="302ae-476">contoso</span><span class="sxs-lookup"><span data-stu-id="302ae-476">contoso</span></span>
- <span data-ttu-id="302ae-477">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="302ae-477">fabrikam</span></span>
- <span data-ttu-id="302ae-478">Northwind</span><span class="sxs-lookup"><span data-stu-id="302ae-478">northwind</span></span>
- <span data-ttu-id="302ae-479">Sandbox</span><span class="sxs-lookup"><span data-stu-id="302ae-479">sandbox</span></span>
- <span data-ttu-id="302ae-480">OneBox</span><span class="sxs-lookup"><span data-stu-id="302ae-480">onebox</span></span>
- <span data-ttu-id="302ae-481">localhost</span><span class="sxs-lookup"><span data-stu-id="302ae-481">localhost</span></span>
- <span data-ttu-id="302ae-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="302ae-482">127.0.0.1</span></span>
- <span data-ttu-id="302ae-483">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="302ae-483">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="302ae-484">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="302ae-484">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="302ae-485">Azure IAAS-DatenbankVerbindungsZeichenfolge und Azure SQL-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="302ae-485">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="302ae-486">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-486">Format</span></span>

<span data-ttu-id="302ae-487">Die Zeichenfolge "Server", "Server" oder "Datenquelle" gefolgt von den Zeichen und Zeichenfolgen, die im folgenden Muster dargestellt sind, einschließlich der Zeichenfolge "cloudapp. Azure. <!--no-hyperlink-->com "oder" cloudapp. Azure. <!--no-hyperlink-->net "oder" Database. Windows. <!--no-hyperlink-->net "und die Zeichenfolge" Password "oder" Password "oder" pwd ".</span><span class="sxs-lookup"><span data-stu-id="302ae-487">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.<!--no-hyperlink-->com" or "cloudapp.azure.<!--no-hyperlink-->net" or "database.windows.<!--no-hyperlink-->net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-488">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-488">Pattern</span></span>

- <span data-ttu-id="302ae-489">Die Zeichenfolge "Server", "Server" oder "Datenquelle"</span><span class="sxs-lookup"><span data-stu-id="302ae-489">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="302ae-490">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-490">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-491">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-491">An equal sign (=)</span></span>
- <span data-ttu-id="302ae-492">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-492">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-493">Eine beliebige Kombination von zwischen 1-200 Buchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-493">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="302ae-494">Die Zeichenfolge "cloudapp. Azure". <!--no-hyperlink-->com "," cloudapp. Azure. <!--no-hyperlink-->net "oder" Database. Windows. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="302ae-494">The string "cloudapp.azure.<!--no-hyperlink-->com", "cloudapp.azure.<!--no-hyperlink-->net", or "database.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="302ae-495">Eine beliebige Kombination von zwischen 1-300 Buchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-495">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="302ae-496">Die Zeichenfolge "Password", "Password" oder "pwd"</span><span class="sxs-lookup"><span data-stu-id="302ae-496">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="302ae-497">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-498">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-498">An equal sign (=)</span></span>
- <span data-ttu-id="302ae-499">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-499">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-500">Ein oder mehrere Zeichen, die kein Semikolon (;), Anführungszeichen (") oder Apostroph (') sind.</span><span class="sxs-lookup"><span data-stu-id="302ae-500">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="302ae-501">Ein Semikolon (;), Anführungszeichen (") oder Apostroph (')</span><span class="sxs-lookup"><span data-stu-id="302ae-501">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-502">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-502">Checksum</span></span>

<span data-ttu-id="302ae-503">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-503">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-504">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-504">Definition</span></span>

<span data-ttu-id="302ae-505">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-505">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-506">Der reguläre Ausdruck CEP_Regex_AzureConnectionString findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-506">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-507">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-507">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure IAAS Database Connection String and Azure SQL Connection String-->
<Entity id="ce1a126d-186f-4700-8c0c-486157b953fd" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-508">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-508">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="302ae-509">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="302ae-509">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="302ae-510">(Beachten Sie, dass dieser vertrauliche Informationstyp diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Schlüsselwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="302ae-510">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="302ae-511">contoso</span><span class="sxs-lookup"><span data-stu-id="302ae-511">contoso</span></span>
- <span data-ttu-id="302ae-512">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="302ae-512">fabrikam</span></span>
- <span data-ttu-id="302ae-513">Northwind</span><span class="sxs-lookup"><span data-stu-id="302ae-513">northwind</span></span>
- <span data-ttu-id="302ae-514">Sandbox</span><span class="sxs-lookup"><span data-stu-id="302ae-514">sandbox</span></span>
- <span data-ttu-id="302ae-515">OneBox</span><span class="sxs-lookup"><span data-stu-id="302ae-515">onebox</span></span>
- <span data-ttu-id="302ae-516">localhost</span><span class="sxs-lookup"><span data-stu-id="302ae-516">localhost</span></span>
- <span data-ttu-id="302ae-517">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="302ae-517">127.0.0.1</span></span>
- <span data-ttu-id="302ae-518">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="302ae-518">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="302ae-519">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="302ae-519">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="302ae-520">Azure viele-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="302ae-520">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="302ae-521">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-521">Format</span></span>

<span data-ttu-id="302ae-522">Die Zeichenfolge "HostName" gefolgt von den Zeichen und Zeichenfolgen, die im folgenden Muster dargestellt sind, einschließlich der Zeichenfolgen "Azure-Devices". <!--no-hyperlink-->net "und" SharedAccessKey ".</span><span class="sxs-lookup"><span data-stu-id="302ae-522">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.<!--no-hyperlink-->net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-523">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-523">Pattern</span></span>

- <span data-ttu-id="302ae-524">Die Zeichenfolge "HostName"</span><span class="sxs-lookup"><span data-stu-id="302ae-524">The string "HostName"</span></span>
- <span data-ttu-id="302ae-525">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-525">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-526">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-526">An equal sign (=)</span></span>
- <span data-ttu-id="302ae-527">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-527">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-528">Eine beliebige Kombination von zwischen 1-200 Buchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-528">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="302ae-529">Die Zeichenfolge "Azure-Devices. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="302ae-529">The string "azure-devices.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="302ae-530">Eine beliebige Kombination von zwischen 1-200 Buchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-530">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="302ae-531">Die Zeichenfolge "SharedAccessKey"</span><span class="sxs-lookup"><span data-stu-id="302ae-531">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="302ae-532">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-532">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-533">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-533">An equal sign (=)</span></span>
- <span data-ttu-id="302ae-534">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-534">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-535">Eine beliebige Kombination aus 43 unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="302ae-535">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="302ae-536">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-536">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-537">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-537">Checksum</span></span>

<span data-ttu-id="302ae-538">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-538">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-539">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-539">Definition</span></span>

<span data-ttu-id="302ae-540">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-540">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-541">Der reguläre Ausdruck CEP_Regex_AzureIoTConnectionString findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-541">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-542">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-542">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure IoT Connection String-->
<Entity id="0b34bec3-d5d6-4974-b7b0-dcdb5c90c29d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureIoTConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-543">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-543">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="302ae-544">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="302ae-544">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="302ae-545">(Beachten Sie, dass dieser vertrauliche Informationstyp diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Schlüsselwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="302ae-545">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="302ae-546">contoso</span><span class="sxs-lookup"><span data-stu-id="302ae-546">contoso</span></span>
- <span data-ttu-id="302ae-547">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="302ae-547">fabrikam</span></span>
- <span data-ttu-id="302ae-548">Northwind</span><span class="sxs-lookup"><span data-stu-id="302ae-548">northwind</span></span>
- <span data-ttu-id="302ae-549">Sandbox</span><span class="sxs-lookup"><span data-stu-id="302ae-549">sandbox</span></span>
- <span data-ttu-id="302ae-550">OneBox</span><span class="sxs-lookup"><span data-stu-id="302ae-550">onebox</span></span>
- <span data-ttu-id="302ae-551">localhost</span><span class="sxs-lookup"><span data-stu-id="302ae-551">localhost</span></span>
- <span data-ttu-id="302ae-552">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="302ae-552">127.0.0.1</span></span>
- <span data-ttu-id="302ae-553">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="302ae-553">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="302ae-554">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="302ae-554">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="302ae-555">Azure Publish-Einstellungs Kennwort</span><span class="sxs-lookup"><span data-stu-id="302ae-555">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="302ae-556">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-556">Format</span></span>

<span data-ttu-id="302ae-557">Die Zeichenfolge "benutzerkwt =" gefolgt von einer alphanumerischen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="302ae-557">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-558">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-558">Pattern</span></span>

- <span data-ttu-id="302ae-559">Die Zeichenfolge "benutzerkwt ="</span><span class="sxs-lookup"><span data-stu-id="302ae-559">The string "userpwd="</span></span>
- <span data-ttu-id="302ae-560">Eine beliebige Kombination von 60 Kleinbuchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-560">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="302ae-561">Ein Anführungszeichen (")</span><span class="sxs-lookup"><span data-stu-id="302ae-561">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-562">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-562">Checksum</span></span>

<span data-ttu-id="302ae-563">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-563">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-564">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-564">Definition</span></span>

<span data-ttu-id="302ae-565">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-565">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-566">Der reguläre Ausdruck CEP_Regex_AzurePublishSettingPasswords findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-566">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-567">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-567">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


```
<!--Azure Publish Setting Password-->
<Entity id="75f4cc8a-a68e-49e5-89ce-fa8f03d286a5" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="CEP_Regex_AzurePublishSettingPasswords" />
       <Any minMatches="0" maxMatches="0">
           <Match idRef="CEP_CommonExampleKeywords" />
       </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-568">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-568">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="302ae-569">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="302ae-569">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="302ae-570">(Beachten Sie, dass dieser vertrauliche Informationstyp diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Schlüsselwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="302ae-570">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="302ae-571">contoso</span><span class="sxs-lookup"><span data-stu-id="302ae-571">contoso</span></span>
- <span data-ttu-id="302ae-572">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="302ae-572">fabrikam</span></span>
- <span data-ttu-id="302ae-573">Northwind</span><span class="sxs-lookup"><span data-stu-id="302ae-573">northwind</span></span>
- <span data-ttu-id="302ae-574">Sandbox</span><span class="sxs-lookup"><span data-stu-id="302ae-574">sandbox</span></span>
- <span data-ttu-id="302ae-575">OneBox</span><span class="sxs-lookup"><span data-stu-id="302ae-575">onebox</span></span>
- <span data-ttu-id="302ae-576">localhost</span><span class="sxs-lookup"><span data-stu-id="302ae-576">localhost</span></span>
- <span data-ttu-id="302ae-577">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="302ae-577">127.0.0.1</span></span>
- <span data-ttu-id="302ae-578">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="302ae-578">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="302ae-579">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="302ae-579">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="302ae-580">Verbindungszeichenfolge für Azure-Cache-Zwischenspeicher</span><span class="sxs-lookup"><span data-stu-id="302ae-580">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="302ae-581">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-581">Format</span></span>

<span data-ttu-id="302ae-582">Die Zeichenfolge "" "" "" "". <!--no-hyperlink-->net "gefolgt von den Zeichen und Zeichenfolgen, die im folgenden Muster dargestellt sind, einschließlich der Zeichenfolge" Password "oder" pwd ".</span><span class="sxs-lookup"><span data-stu-id="302ae-582">The string "redis.cache.windows.<!--no-hyperlink-->net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-583">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-583">Pattern</span></span>

- <span data-ttu-id="302ae-584">Die Zeichenfolge "" "" "" "". <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="302ae-584">The string "redis.cache.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="302ae-585">Eine beliebige Kombination von zwischen 1-200 Buchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-585">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="302ae-586">Die Zeichenfolge "Password" oder "pwd"</span><span class="sxs-lookup"><span data-stu-id="302ae-586">The string "password" or "pwd"</span></span>
- <span data-ttu-id="302ae-587">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-587">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-588">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-588">An equal sign (=)</span></span>
- <span data-ttu-id="302ae-589">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-589">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-590">Eine beliebige Kombination von 43 Zeichen, die klein-oder Großbuchstaben, Ziffern, Schrägstriche (/) oder ein Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="302ae-590">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="302ae-591">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-591">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-592">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-592">Checksum</span></span>

<span data-ttu-id="302ae-593">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-593">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-594">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-594">Definition</span></span>

<span data-ttu-id="302ae-595">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-596">Der reguläre Ausdruck CEP_Regex_AzureRedisCacheConnectionString findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-596">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="302ae-597">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-597">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Redis Cache Connection String-->
<Entity id="095a7e6c-efd8-46d5-af7b-5298d53a49fc" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureRedisCacheConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-598">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-598">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="302ae-599">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="302ae-599">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="302ae-600">(Beachten Sie, dass dieser vertrauliche Informationstyp diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Schlüsselwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="302ae-600">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="302ae-601">contoso</span><span class="sxs-lookup"><span data-stu-id="302ae-601">contoso</span></span>
- <span data-ttu-id="302ae-602">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="302ae-602">fabrikam</span></span>
- <span data-ttu-id="302ae-603">Northwind</span><span class="sxs-lookup"><span data-stu-id="302ae-603">northwind</span></span>
- <span data-ttu-id="302ae-604">Sandbox</span><span class="sxs-lookup"><span data-stu-id="302ae-604">sandbox</span></span>
- <span data-ttu-id="302ae-605">OneBox</span><span class="sxs-lookup"><span data-stu-id="302ae-605">onebox</span></span>
- <span data-ttu-id="302ae-606">localhost</span><span class="sxs-lookup"><span data-stu-id="302ae-606">localhost</span></span>
- <span data-ttu-id="302ae-607">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="302ae-607">127.0.0.1</span></span>
- <span data-ttu-id="302ae-608">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="302ae-608">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="302ae-609">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="302ae-609">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="302ae-610">Azure SAS</span><span class="sxs-lookup"><span data-stu-id="302ae-610">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="302ae-611">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-611">Format</span></span>

<span data-ttu-id="302ae-612">Die Zeichenfolge "SIG" gefolgt von den Zeichen und Zeichenfolgen, die im folgenden Muster erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="302ae-612">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-613">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-613">Pattern</span></span>

- <span data-ttu-id="302ae-614">Die Zeichenfolge "SIG"</span><span class="sxs-lookup"><span data-stu-id="302ae-614">The string "sig"</span></span>
- <span data-ttu-id="302ae-615">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-615">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-616">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-616">An equal sign (=)</span></span>
- <span data-ttu-id="302ae-617">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-617">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-618">Eine beliebige Kombination von zwischen 43-53 Zeichen, die klein-oder Großbuchstaben, Ziffern oder das Prozentzeichen (%)</span><span class="sxs-lookup"><span data-stu-id="302ae-618">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="302ae-619">Die Zeichenfolge "% 3D"</span><span class="sxs-lookup"><span data-stu-id="302ae-619">The string "%3d"</span></span>
- <span data-ttu-id="302ae-620">Ein beliebiges Zeichen, das kein klein-oder Großbuchstaben, eine Ziffer oder ein Prozentzeichen ist (%)</span><span class="sxs-lookup"><span data-stu-id="302ae-620">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-621">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-621">Checksum</span></span>

<span data-ttu-id="302ae-622">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-622">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-623">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-623">Definition</span></span>

<span data-ttu-id="302ae-624">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-624">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-625">Der reguläre Ausdruck CEP_Regex_AzureSAS findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-625">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="302ae-626">Azure Service Bus-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="302ae-626">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="302ae-627">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-627">Format</span></span>

<span data-ttu-id="302ae-628">Die Zeichenfolge "Endpunkt" gefolgt von den Zeichen und Zeichenfolgen, die im folgenden Muster dargestellt sind, einschließlich der Zeichenfolgen "ServiceBus. Windows. <!--no-hyperlink-->net "und" SharedAccesKey ".</span><span class="sxs-lookup"><span data-stu-id="302ae-628">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.<!--no-hyperlink-->net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-629">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-629">Pattern</span></span>

- <span data-ttu-id="302ae-630">Die Zeichenfolge "Endpunkt"</span><span class="sxs-lookup"><span data-stu-id="302ae-630">The string "EndPoint"</span></span>
- <span data-ttu-id="302ae-631">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-631">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-632">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-632">An equal sign (=)</span></span>
- <span data-ttu-id="302ae-633">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-633">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-634">Eine beliebige Kombination von zwischen 1-200 Buchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-634">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="302ae-635">Die Zeichenfolge "ServiceBus. Windows. <!--no-hyperlink-->net "</span><span class="sxs-lookup"><span data-stu-id="302ae-635">The string "servicebus.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="302ae-636">Eine beliebige Kombination von zwischen 1-200 Buchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-636">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="302ae-637">Die Zeichenfolge "SharedAccessKey"</span><span class="sxs-lookup"><span data-stu-id="302ae-637">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="302ae-638">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-638">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-639">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-639">An equal sign (=)</span></span>
- <span data-ttu-id="302ae-640">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-640">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-641">Eine beliebige Kombination von 43 Zeichen, die klein-oder Großbuchstaben, Ziffern, Schrägstriche (/) oder ein Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="302ae-641">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="302ae-642">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-642">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-643">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-643">Checksum</span></span>

<span data-ttu-id="302ae-644">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-644">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-645">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-645">Definition</span></span>

<span data-ttu-id="302ae-646">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-646">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-647">Der reguläre Ausdruck CEP_Regex_AzureServiceBusConnectionString findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-647">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="302ae-648">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-648">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Service Bus Connection String-->
<Entity id="b9a6578f-a83f-4fcd-bf44-2130bae49a6f" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureServiceBusConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-649">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-649">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="302ae-650">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="302ae-650">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="302ae-651">(Beachten Sie, dass dieser vertrauliche Informationstyp diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Schlüsselwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="302ae-651">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="302ae-652">contoso</span><span class="sxs-lookup"><span data-stu-id="302ae-652">contoso</span></span>
- <span data-ttu-id="302ae-653">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="302ae-653">fabrikam</span></span>
- <span data-ttu-id="302ae-654">Northwind</span><span class="sxs-lookup"><span data-stu-id="302ae-654">northwind</span></span>
- <span data-ttu-id="302ae-655">Sandbox</span><span class="sxs-lookup"><span data-stu-id="302ae-655">sandbox</span></span>
- <span data-ttu-id="302ae-656">OneBox</span><span class="sxs-lookup"><span data-stu-id="302ae-656">onebox</span></span>
- <span data-ttu-id="302ae-657">localhost</span><span class="sxs-lookup"><span data-stu-id="302ae-657">localhost</span></span>
- <span data-ttu-id="302ae-658">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="302ae-658">127.0.0.1</span></span>
- <span data-ttu-id="302ae-659">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="302ae-659">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="302ae-660">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="302ae-660">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="302ae-661">Azure-Speicherkontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="302ae-661">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="302ae-662">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-662">Format</span></span>

<span data-ttu-id="302ae-663">Die Zeichenfolge "DefaultEndpointsProtocol" gefolgt von den Zeichen und Zeichenfolgen, die im folgenden Muster dargestellt sind, einschließlich der Zeichenfolge "AccountKey".</span><span class="sxs-lookup"><span data-stu-id="302ae-663">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-664">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-664">Pattern</span></span>

- <span data-ttu-id="302ae-665">Die Zeichenfolge "DefaultEndpointsProtocol"</span><span class="sxs-lookup"><span data-stu-id="302ae-665">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="302ae-666">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-666">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-667">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-667">An equal sign (=)</span></span>
- <span data-ttu-id="302ae-668">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-668">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-669">Eine beliebige Kombination von zwischen 1-200 Buchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-669">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="302ae-670">Die Zeichenfolge "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="302ae-670">The string "AccountKey"</span></span>
- <span data-ttu-id="302ae-671">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-671">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-672">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-672">An equal sign (=)</span></span>
- <span data-ttu-id="302ae-673">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-673">0-2 whitespace characters</span></span>
- <span data-ttu-id="302ae-674">Eine beliebige Kombination von 86 Zeichen, die klein-oder Großbuchstaben, Ziffern, Schrägstriche (/) oder ein Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="302ae-674">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="302ae-675">Zwei Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-675">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-676">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-676">Checksum</span></span>

<span data-ttu-id="302ae-677">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-677">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-678">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-678">Definition</span></span>

<span data-ttu-id="302ae-679">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-679">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-680">Der reguläre Ausdruck CEP_Regex_AzureStorageAccountKey findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-680">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-681">Der reguläre Ausdruck CEP_AzureEmulatorStorageAccountFilter findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-681">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-682">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-682">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key-->
<Entity id="c7bc98e8-551a-4c35-a92d-d2c8cda714a7" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_AzureEmulatorStorageAccountFilter" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-683">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-683">Keywords</span></span>

#### <a name="cepazureemulatorstorageaccountfilter"></a><span data-ttu-id="302ae-684">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="302ae-684">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="302ae-685">(Beachten Sie, dass dieser vertrauliche Informationstyp diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Schlüsselwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="302ae-685">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="302ae-686">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="302ae-686">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="302ae-687">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="302ae-687">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="302ae-688">(Beachten Sie, dass dieser vertrauliche Informationstyp diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Schlüsselwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="302ae-688">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="302ae-689">contoso</span><span class="sxs-lookup"><span data-stu-id="302ae-689">contoso</span></span>
- <span data-ttu-id="302ae-690">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="302ae-690">fabrikam</span></span>
- <span data-ttu-id="302ae-691">Northwind</span><span class="sxs-lookup"><span data-stu-id="302ae-691">northwind</span></span>
- <span data-ttu-id="302ae-692">Sandbox</span><span class="sxs-lookup"><span data-stu-id="302ae-692">sandbox</span></span>
- <span data-ttu-id="302ae-693">OneBox</span><span class="sxs-lookup"><span data-stu-id="302ae-693">onebox</span></span>
- <span data-ttu-id="302ae-694">localhost</span><span class="sxs-lookup"><span data-stu-id="302ae-694">localhost</span></span>
- <span data-ttu-id="302ae-695">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="302ae-695">127.0.0.1</span></span>
- <span data-ttu-id="302ae-696">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="302ae-696">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="302ae-697">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="302ae-697">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="302ae-698">Azure-Speicherkontoschlüssel (generisch)</span><span class="sxs-lookup"><span data-stu-id="302ae-698">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-699">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-699">Format</span></span>

<span data-ttu-id="302ae-700">Eine beliebige Kombination von 86 in Groß-und Kleinbuchstaben, Ziffern, dem Schrägstrich (/) oder Pluszeichen (+), vorangestellt oder gefolgt von den im folgenden Muster beschriebenen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="302ae-700">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-701">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-701">Pattern</span></span>

- <span data-ttu-id="302ae-702">0-1 des größer-als-Zeichens (>), Apostroph ('), Gleichheitszeichen (=), Anführungszeichen (") oder Nummernzeichen (#)</span><span class="sxs-lookup"><span data-stu-id="302ae-702">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="302ae-703">Eine beliebige Kombination von 86 Zeichen, die klein-oder Großbuchstaben, Ziffern, den Schrägstrich (/) oder ein Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="302ae-703">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="302ae-704">Zwei Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-704">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="302ae-705">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-705">Checksum</span></span>

<span data-ttu-id="302ae-706">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-706">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-707">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-707">Definition</span></span>

<span data-ttu-id="302ae-708">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-708">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-709">Der reguläre Ausdruck CEP_Regex_AzureStorageAccountKeyGeneric findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-709">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="302ae-710">Belgien – Nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-710">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-711">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-711">Format</span></span>

<span data-ttu-id="302ae-712">11 Ziffern plus Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-712">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-713">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-713">Pattern</span></span>

<span data-ttu-id="302ae-714">11 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="302ae-714">11 digits plus delimiters:</span></span>
- <span data-ttu-id="302ae-715">Sechs Ziffern und zwei Punkte im Format JJ.MM.TT für das Geburtsdatum </span><span class="sxs-lookup"><span data-stu-id="302ae-715">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="302ae-716">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-716">A hyphen</span></span> 
- <span data-ttu-id="302ae-717">Drei aufeinander folgende Ziffern (ungerade für Männer, gerade für Frauen) </span><span class="sxs-lookup"><span data-stu-id="302ae-717">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="302ae-718">Ein Punkt</span><span class="sxs-lookup"><span data-stu-id="302ae-718">A period</span></span> 
- <span data-ttu-id="302ae-719">Zwei Ziffern als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-719">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-720">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-720">Checksum</span></span>

<span data-ttu-id="302ae-721">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-721">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-722">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-722">Definition</span></span>

<span data-ttu-id="302ae-723">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-723">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-724">Die Funktion Func_belgium_national_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-724">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-725">Ein Schlüsselwort aus Keyword_belgium_national_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-725">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="302ae-726">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-726">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-727">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-727">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="302ae-728">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="302ae-728">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="302ae-729">Identität</span><span class="sxs-lookup"><span data-stu-id="302ae-729">Identity</span></span>
- <span data-ttu-id="302ae-730">Registrierung</span><span class="sxs-lookup"><span data-stu-id="302ae-730">Registration</span></span>
- <span data-ttu-id="302ae-731">Identifikations</span><span class="sxs-lookup"><span data-stu-id="302ae-731">Identification</span></span> 
- <span data-ttu-id="302ae-732">ID</span><span class="sxs-lookup"><span data-stu-id="302ae-732">ID</span></span> 
- <span data-ttu-id="302ae-733">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="302ae-733">Identiteitskaart</span></span>
- <span data-ttu-id="302ae-734">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-734">Registratie nummer</span></span> 
- <span data-ttu-id="302ae-735">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-735">Identificatie nummer</span></span> 
- <span data-ttu-id="302ae-736">Identiteit</span><span class="sxs-lookup"><span data-stu-id="302ae-736">Identiteit</span></span>
- <span data-ttu-id="302ae-737">Registratie</span><span class="sxs-lookup"><span data-stu-id="302ae-737">Registratie</span></span>
- <span data-ttu-id="302ae-738">Identificatie</span><span class="sxs-lookup"><span data-stu-id="302ae-738">Identificatie</span></span> 
- <span data-ttu-id="302ae-739">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="302ae-739">Carte d’identité</span></span> 
- <span data-ttu-id="302ae-740">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="302ae-740">numéro d'immatriculation</span></span>
- <span data-ttu-id="302ae-741">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="302ae-741">numéro d'identification</span></span>
- <span data-ttu-id="302ae-742">identité</span><span class="sxs-lookup"><span data-stu-id="302ae-742">identité</span></span> 
- <span data-ttu-id="302ae-743">Inschrift</span><span class="sxs-lookup"><span data-stu-id="302ae-743">inscription</span></span> 
- <span data-ttu-id="302ae-744">Identifikation</span><span class="sxs-lookup"><span data-stu-id="302ae-744">Identifikation</span></span>
- <span data-ttu-id="302ae-745">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="302ae-745">Identifizierung</span></span>
- <span data-ttu-id="302ae-746">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-746">Identifikationsnummer</span></span>
- <span data-ttu-id="302ae-747">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="302ae-747">Personalausweis</span></span>
- <span data-ttu-id="302ae-748">Registrierung</span><span class="sxs-lookup"><span data-stu-id="302ae-748">Registrierung</span></span>
- <span data-ttu-id="302ae-749">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-749">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="302ae-750">Brazil CPF Number</span><span class="sxs-lookup"><span data-stu-id="302ae-750">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-751">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-751">Format</span></span>

<span data-ttu-id="302ae-752">11 Ziffern, die eine Prüfziffer umfassen und die formatiert oder unformatiert sein können</span><span class="sxs-lookup"><span data-stu-id="302ae-752">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-753">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-753">Pattern</span></span>

<span data-ttu-id="302ae-754">Formatiert</span><span class="sxs-lookup"><span data-stu-id="302ae-754">Formatted:</span></span>
- <span data-ttu-id="302ae-755">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-755">Three digits</span></span> 
- <span data-ttu-id="302ae-756">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="302ae-756">A period</span></span> 
- <span data-ttu-id="302ae-757">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-757">Three digits</span></span> 
- <span data-ttu-id="302ae-758">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="302ae-758">A period</span></span> 
- <span data-ttu-id="302ae-759">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-759">Three digits</span></span> 
- <span data-ttu-id="302ae-760">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-760">A hyphen</span></span> 
- <span data-ttu-id="302ae-761">Zwei Ziffern, die Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="302ae-761">Two digits which are check digits</span></span>

<span data-ttu-id="302ae-762">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="302ae-762">Unformatted:</span></span>
- <span data-ttu-id="302ae-763">11 Ziffern, wobei die letzten beiden Ziffern Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="302ae-763">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-764">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-764">Checksum</span></span>

<span data-ttu-id="302ae-765">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-765">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-766">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-766">Definition</span></span>

<span data-ttu-id="302ae-767">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-767">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-768">Die Funktion Func_brazil_cpf sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-768">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-769">Ein Schlüsselwort aus Keyword_brazil_cpf wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-769">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="302ae-770">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-770">The checksum passes.</span></span>

<span data-ttu-id="302ae-771">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-772">Die Funktion Func_brazil_cpf sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-772">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-773">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-773">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-774">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-774">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="302ae-775">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="302ae-775">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="302ae-776">CPF</span><span class="sxs-lookup"><span data-stu-id="302ae-776">CPF</span></span>
- <span data-ttu-id="302ae-777">Identifikations</span><span class="sxs-lookup"><span data-stu-id="302ae-777">Identification</span></span>
- <span data-ttu-id="302ae-778">Registrierung</span><span class="sxs-lookup"><span data-stu-id="302ae-778">Registration</span></span>
- <span data-ttu-id="302ae-779">Umsatz</span><span class="sxs-lookup"><span data-stu-id="302ae-779">Revenue</span></span>
- <span data-ttu-id="302ae-780">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="302ae-780">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="302ae-781">Imposto</span><span class="sxs-lookup"><span data-stu-id="302ae-781">Imposto</span></span> 
- <span data-ttu-id="302ae-782">Identificação</span><span class="sxs-lookup"><span data-stu-id="302ae-782">Identificação</span></span> 
- <span data-ttu-id="302ae-783">Inscrição</span><span class="sxs-lookup"><span data-stu-id="302ae-783">Inscrição</span></span> 
- <span data-ttu-id="302ae-784">Receita</span><span class="sxs-lookup"><span data-stu-id="302ae-784">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="302ae-785">Brasilien – Juristische Personennummer (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="302ae-785">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-786">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-786">Format</span></span>

<span data-ttu-id="302ae-787">14 Ziffern, die eine Registrierungsnummer, eine Zweignummer und Prüfnziffern sowie Trennzeichen umfassen</span><span class="sxs-lookup"><span data-stu-id="302ae-787">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-788">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-788">Pattern</span></span>
<span data-ttu-id="302ae-789">14 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="302ae-789">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="302ae-790">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-790">Two digits</span></span> 
- <span data-ttu-id="302ae-791">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="302ae-791">A period</span></span> 
- <span data-ttu-id="302ae-792">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-792">Three digits</span></span> 
- <span data-ttu-id="302ae-793">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="302ae-793">A period</span></span> 
- <span data-ttu-id="302ae-794">Drei Ziffern (diese ersten acht Ziffern sind die Registrierungsnummer) </span><span class="sxs-lookup"><span data-stu-id="302ae-794">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="302ae-795">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="302ae-795">A forward slash</span></span> 
- <span data-ttu-id="302ae-796">Vierstellige Zweignummer </span><span class="sxs-lookup"><span data-stu-id="302ae-796">Four-digit branch number</span></span> 
- <span data-ttu-id="302ae-797">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-797">A hyphen</span></span> 
- <span data-ttu-id="302ae-798">Zwei Ziffern, die Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="302ae-798">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-799">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-799">Checksum</span></span>

<span data-ttu-id="302ae-800">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-800">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-801">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-801">Definition</span></span>

<span data-ttu-id="302ae-802">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-802">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-803">Die Funktion Func_brazil_cnpj sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-803">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-804">Ein Schlüsselwort aus Keyword_brazil_cnpj wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-804">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="302ae-805">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-805">The checksum passes.</span></span>

<span data-ttu-id="302ae-806">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-806">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-807">Die Funktion Func_brazil_cnpj sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-807">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-808">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-808">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-809">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-809">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="302ae-810">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="302ae-810">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="302ae-811">CNPJ</span><span class="sxs-lookup"><span data-stu-id="302ae-811">CNPJ</span></span> 
- <span data-ttu-id="302ae-812">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="302ae-812">CNPJ/MF</span></span> 
- <span data-ttu-id="302ae-813">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="302ae-813">CNPJ-MF</span></span> 
- <span data-ttu-id="302ae-814">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="302ae-814">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="302ae-815">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="302ae-815">Taxpayers Registry</span></span> 
- <span data-ttu-id="302ae-816">Legal entity</span><span class="sxs-lookup"><span data-stu-id="302ae-816">Legal entity</span></span> 
- <span data-ttu-id="302ae-817">Legal entities</span><span class="sxs-lookup"><span data-stu-id="302ae-817">Legal entities</span></span> 
- <span data-ttu-id="302ae-818">Registration Status</span><span class="sxs-lookup"><span data-stu-id="302ae-818">Registration Status</span></span> 
- <span data-ttu-id="302ae-819">Business</span><span class="sxs-lookup"><span data-stu-id="302ae-819">Business</span></span> 
- <span data-ttu-id="302ae-820">Company</span><span class="sxs-lookup"><span data-stu-id="302ae-820">Company</span></span>
- <span data-ttu-id="302ae-821">CNPJ</span><span class="sxs-lookup"><span data-stu-id="302ae-821">CNPJ</span></span> 
- <span data-ttu-id="302ae-822">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="302ae-822">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="302ae-823">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="302ae-823">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="302ae-824">CGC</span><span class="sxs-lookup"><span data-stu-id="302ae-824">CGC</span></span> 
- <span data-ttu-id="302ae-825">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="302ae-825">Pessoa jurídica</span></span> 
- <span data-ttu-id="302ae-826">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="302ae-826">Pessoas jurídicas</span></span> 
- <span data-ttu-id="302ae-827">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="302ae-827">Situação cadastral</span></span> 
- <span data-ttu-id="302ae-828">Inscrição</span><span class="sxs-lookup"><span data-stu-id="302ae-828">Inscrição</span></span> 
- <span data-ttu-id="302ae-829">Empresa</span><span class="sxs-lookup"><span data-stu-id="302ae-829">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="302ae-830">	Brasilien – Personalausweis (RG)</span><span class="sxs-lookup"><span data-stu-id="302ae-830">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-831">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-831">Format</span></span>

<span data-ttu-id="302ae-832">Registro Geral (altes Format): neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-832">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="302ae-833">Registro de Identidade (RIC) (neues Format): 11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-833">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-834">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-834">Pattern</span></span>

<span data-ttu-id="302ae-835">Registro Geral (altes Format):</span><span class="sxs-lookup"><span data-stu-id="302ae-835">Registro Geral (old format):</span></span>
- <span data-ttu-id="302ae-836">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-836">Two digits</span></span> 
- <span data-ttu-id="302ae-837">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="302ae-837">A period</span></span> 
- <span data-ttu-id="302ae-838">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-838">Three digits</span></span> 
- <span data-ttu-id="302ae-839">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="302ae-839">A period</span></span> 
- <span data-ttu-id="302ae-840">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-840">Three digits</span></span> 
- <span data-ttu-id="302ae-841">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-841">A hyphen</span></span> 
- <span data-ttu-id="302ae-842">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-842">One digit which is a check digit</span></span>

<span data-ttu-id="302ae-843">Registro de Identidade (RIC) (neues Format):</span><span class="sxs-lookup"><span data-stu-id="302ae-843">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="302ae-844">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-844">10 digits</span></span> 
- <span data-ttu-id="302ae-845">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-845">A hyphen</span></span> 
- <span data-ttu-id="302ae-846">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-846">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-847">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-847">Checksum</span></span>

<span data-ttu-id="302ae-848">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-848">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-849">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-849">Definition</span></span>

<span data-ttu-id="302ae-850">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-850">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-851">Die Funktion Func_brazil_rg sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-851">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-852">Ein Schlüsselwort aus Keyword_brazil_rg wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-852">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="302ae-853">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-853">The checksum passes.</span></span>

<span data-ttu-id="302ae-854">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-854">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-855">Die Funktion Func_brazil_rg sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-855">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-856">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-856">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-857">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-857">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="302ae-858">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="302ae-858">Keyword_brazil_rg</span></span>

<span data-ttu-id="302ae-859">Cédula de identidade Identity Card National ID número de rregistro Registro de Iidentidade Registro Geral RG (dieses Schlüsselwort wird Groß-/Kleinschreibung beachtet) RIC (bei diesem Schlüsselwort wird die Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="302ae-859">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="302ae-860">Kanadische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="302ae-860">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-861">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-861">Format</span></span>

<span data-ttu-id="302ae-862">Sieben oder zwölf Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-862">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-863">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-863">Pattern</span></span>

<span data-ttu-id="302ae-864">Eine kanadische Kontonummer umfasst sieben oder zwölf Ziffern.</span><span class="sxs-lookup"><span data-stu-id="302ae-864">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="302ae-865">Eine kanadische Bankkontonummer setzt sich wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="302ae-865">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="302ae-866">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-866">Five digits</span></span> 
- <span data-ttu-id="302ae-867">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-867">A hyphen</span></span> 
- <span data-ttu-id="302ae-868">Drei Ziffern oder</span><span class="sxs-lookup"><span data-stu-id="302ae-868">Three digits OR</span></span>
- <span data-ttu-id="302ae-869">Eine 0 (null) </span><span class="sxs-lookup"><span data-stu-id="302ae-869">A zero "0"</span></span> 
- <span data-ttu-id="302ae-870">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-870">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-871">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-871">Checksum</span></span>

<span data-ttu-id="302ae-872">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-872">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-873">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-873">Definition</span></span>

<span data-ttu-id="302ae-874">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-874">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-875">Der reguläre Ausdruck Regex_canada_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-875">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-876">Ein Schlüsselwort aus Keyword_canada_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-876">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="302ae-877">Der reguläre Ausdruck Regex_canada_bank_account_transit_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-877">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="302ae-878">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-878">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-879">Der reguläre Ausdruck Regex_canada_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-879">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-880">Ein Schlüsselwort aus Keyword_canada_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-880">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-881">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-881">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="302ae-882">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="302ae-882">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="302ae-883">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="302ae-883">canada savings bonds</span></span>
- <span data-ttu-id="302ae-884">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="302ae-884">canada revenue agency</span></span>
- <span data-ttu-id="302ae-885">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="302ae-885">canadian financial institution</span></span>
- <span data-ttu-id="302ae-886">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="302ae-886">direct deposit form</span></span>
- <span data-ttu-id="302ae-887">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="302ae-887">canadian citizen</span></span>
- <span data-ttu-id="302ae-888">legal representative</span><span class="sxs-lookup"><span data-stu-id="302ae-888">legal representative</span></span>
- <span data-ttu-id="302ae-889">notary public</span><span class="sxs-lookup"><span data-stu-id="302ae-889">notary public</span></span>
- <span data-ttu-id="302ae-890">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="302ae-890">commissioner for oaths</span></span>
- <span data-ttu-id="302ae-891">child care benefit</span><span class="sxs-lookup"><span data-stu-id="302ae-891">child care benefit</span></span>
- <span data-ttu-id="302ae-892">universal child care</span><span class="sxs-lookup"><span data-stu-id="302ae-892">universal child care</span></span>
- <span data-ttu-id="302ae-893">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="302ae-893">canada child tax benefit</span></span>
- <span data-ttu-id="302ae-894">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="302ae-894">income tax benefit</span></span>
- <span data-ttu-id="302ae-895">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="302ae-895">harmonized sales tax</span></span>
- <span data-ttu-id="302ae-896">social insurance number</span><span class="sxs-lookup"><span data-stu-id="302ae-896">social insurance number</span></span>
- <span data-ttu-id="302ae-897">income tax refund</span><span class="sxs-lookup"><span data-stu-id="302ae-897">income tax refund</span></span>
- <span data-ttu-id="302ae-898">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="302ae-898">child tax benefit</span></span>
- <span data-ttu-id="302ae-899">territorial payments</span><span class="sxs-lookup"><span data-stu-id="302ae-899">territorial payments</span></span>
- <span data-ttu-id="302ae-900">institution number</span><span class="sxs-lookup"><span data-stu-id="302ae-900">institution number</span></span>
- <span data-ttu-id="302ae-901">deposit request</span><span class="sxs-lookup"><span data-stu-id="302ae-901">deposit request</span></span>
- <span data-ttu-id="302ae-902">banking information</span><span class="sxs-lookup"><span data-stu-id="302ae-902">banking information</span></span>
- <span data-ttu-id="302ae-903">direct deposit</span><span class="sxs-lookup"><span data-stu-id="302ae-903">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="302ae-904">Kanadische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-904">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-905">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-905">Format</span></span>

<span data-ttu-id="302ae-906">Variiert je nach Provinz</span><span class="sxs-lookup"><span data-stu-id="302ae-906">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-907">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-907">Pattern</span></span>

<span data-ttu-id="302ae-908">Verschiedene Muster in Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec und Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="302ae-908">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-909">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-909">Checksum</span></span>

<span data-ttu-id="302ae-910">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-910">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-911">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-911">Definition</span></span>

<span data-ttu-id="302ae-912">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-913">Die Funktion Func_[province_name]_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-913">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-914">Ein Schlüsselwort aus Keyword_[province_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-914">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="302ae-915">Ein Schlüsselwort aus Keyword_canada_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-915">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-916">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-916">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="302ae-917">Keyword_ [province_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="302ae-917">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="302ae-918">Die Abkürzung für die Provinz, z. B. AB</span><span class="sxs-lookup"><span data-stu-id="302ae-918">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="302ae-919">Der Name der Provinz, beispielsweise „Alberta“</span><span class="sxs-lookup"><span data-stu-id="302ae-919">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="302ae-920">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="302ae-920">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="302ae-921">DL</span><span class="sxs-lookup"><span data-stu-id="302ae-921">DL</span></span>
- <span data-ttu-id="302ae-922">DLS</span><span class="sxs-lookup"><span data-stu-id="302ae-922">DLS</span></span>
- <span data-ttu-id="302ae-923">CDL</span><span class="sxs-lookup"><span data-stu-id="302ae-923">CDL</span></span>
- <span data-ttu-id="302ae-924">CDLS</span><span class="sxs-lookup"><span data-stu-id="302ae-924">CDLS</span></span>
- <span data-ttu-id="302ae-925">DriverLic</span><span class="sxs-lookup"><span data-stu-id="302ae-925">DriverLic</span></span>
- <span data-ttu-id="302ae-926">DriverLics</span><span class="sxs-lookup"><span data-stu-id="302ae-926">DriverLics</span></span>
- <span data-ttu-id="302ae-927">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="302ae-927">DriverLicense</span></span>
- <span data-ttu-id="302ae-928">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="302ae-928">DriverLicenses</span></span>
- <span data-ttu-id="302ae-929">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="302ae-929">DriverLicence</span></span>
- <span data-ttu-id="302ae-930">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="302ae-930">DriverLicences</span></span>
- <span data-ttu-id="302ae-931">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-931">Driver Lic</span></span>
- <span data-ttu-id="302ae-932">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-932">Driver Lics</span></span>
- <span data-ttu-id="302ae-933">Driver License</span><span class="sxs-lookup"><span data-stu-id="302ae-933">Driver License</span></span>
- <span data-ttu-id="302ae-934">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-934">Driver Licenses</span></span>
- <span data-ttu-id="302ae-935">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-935">Driver Licence</span></span>
- <span data-ttu-id="302ae-936">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-936">Driver Licences</span></span>
- <span data-ttu-id="302ae-937">DriversLic</span><span class="sxs-lookup"><span data-stu-id="302ae-937">DriversLic</span></span>
- <span data-ttu-id="302ae-938">DriversLics</span><span class="sxs-lookup"><span data-stu-id="302ae-938">DriversLics</span></span>
- <span data-ttu-id="302ae-939">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="302ae-939">DriversLicence</span></span>
- <span data-ttu-id="302ae-940">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="302ae-940">DriversLicences</span></span>
- <span data-ttu-id="302ae-941">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="302ae-941">DriversLicense</span></span>
- <span data-ttu-id="302ae-942">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="302ae-942">DriversLicenses</span></span>
- <span data-ttu-id="302ae-943">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-943">Drivers Lic</span></span>
- <span data-ttu-id="302ae-944">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-944">Drivers Lics</span></span>
- <span data-ttu-id="302ae-945">Drivers License</span><span class="sxs-lookup"><span data-stu-id="302ae-945">Drivers License</span></span>
- <span data-ttu-id="302ae-946">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-946">Drivers Licenses</span></span>
- <span data-ttu-id="302ae-947">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-947">Drivers Licence</span></span>
- <span data-ttu-id="302ae-948">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-948">Drivers Licences</span></span>
- <span data-ttu-id="302ae-949">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-949">Driver'Lic</span></span>
- <span data-ttu-id="302ae-950">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-950">Driver'Lics</span></span>
- <span data-ttu-id="302ae-951">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="302ae-951">Driver'License</span></span>
- <span data-ttu-id="302ae-952">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-952">Driver'Licenses</span></span>
- <span data-ttu-id="302ae-953">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-953">Driver'Licence</span></span>
- <span data-ttu-id="302ae-954">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-954">Driver'Licences</span></span>
- <span data-ttu-id="302ae-955">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-955">Driver' Lic</span></span>
- <span data-ttu-id="302ae-956">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-956">Driver' Lics</span></span>
- <span data-ttu-id="302ae-957">Driver' License</span><span class="sxs-lookup"><span data-stu-id="302ae-957">Driver' License</span></span>
- <span data-ttu-id="302ae-958">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-958">Driver' Licenses</span></span>
- <span data-ttu-id="302ae-959">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-959">Driver' Licence</span></span>
- <span data-ttu-id="302ae-960">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-960">Driver' Licences</span></span>
- <span data-ttu-id="302ae-961">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="302ae-961">Driver'sLic</span></span>
- <span data-ttu-id="302ae-962">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="302ae-962">Driver'sLics</span></span>
- <span data-ttu-id="302ae-963">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="302ae-963">Driver'sLicense</span></span>
- <span data-ttu-id="302ae-964">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="302ae-964">Driver'sLicenses</span></span>
- <span data-ttu-id="302ae-965">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="302ae-965">Driver'sLicence</span></span>
- <span data-ttu-id="302ae-966">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="302ae-966">Driver'sLicences</span></span>
- <span data-ttu-id="302ae-967">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-967">Driver's Lic</span></span>
- <span data-ttu-id="302ae-968">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-968">Driver's Lics</span></span>
- <span data-ttu-id="302ae-969">Driver's License</span><span class="sxs-lookup"><span data-stu-id="302ae-969">Driver's License</span></span>
- <span data-ttu-id="302ae-970">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-970">Driver's Licenses</span></span>
- <span data-ttu-id="302ae-971">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-971">Driver's Licence</span></span>
- <span data-ttu-id="302ae-972">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-972">Driver's Licences</span></span>
- <span data-ttu-id="302ae-973">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="302ae-973">Permis de Conduire</span></span>
- <span data-ttu-id="302ae-974">id</span><span class="sxs-lookup"><span data-stu-id="302ae-974">id</span></span>
- <span data-ttu-id="302ae-975">ids</span><span class="sxs-lookup"><span data-stu-id="302ae-975">ids</span></span>
- <span data-ttu-id="302ae-976">idcard number</span><span class="sxs-lookup"><span data-stu-id="302ae-976">idcard number</span></span>
- <span data-ttu-id="302ae-977">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="302ae-977">idcard numbers</span></span>
- <span data-ttu-id="302ae-978">idcard #</span><span class="sxs-lookup"><span data-stu-id="302ae-978">idcard #</span></span>
- <span data-ttu-id="302ae-979">idcard #s</span><span class="sxs-lookup"><span data-stu-id="302ae-979">idcard #s</span></span>
- <span data-ttu-id="302ae-980">idcard card</span><span class="sxs-lookup"><span data-stu-id="302ae-980">idcard card</span></span>
- <span data-ttu-id="302ae-981">idcard cards</span><span class="sxs-lookup"><span data-stu-id="302ae-981">idcard cards</span></span>
- <span data-ttu-id="302ae-982">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="302ae-982">idcard</span></span>
- <span data-ttu-id="302ae-983">identification number</span><span class="sxs-lookup"><span data-stu-id="302ae-983">identification number</span></span>
- <span data-ttu-id="302ae-984">identification numbers</span><span class="sxs-lookup"><span data-stu-id="302ae-984">identification numbers</span></span>
- <span data-ttu-id="302ae-985">identification #</span><span class="sxs-lookup"><span data-stu-id="302ae-985">identification #</span></span>
- <span data-ttu-id="302ae-986">identification #s</span><span class="sxs-lookup"><span data-stu-id="302ae-986">identification #s</span></span>
- <span data-ttu-id="302ae-987">identification card</span><span class="sxs-lookup"><span data-stu-id="302ae-987">identification card</span></span>
- <span data-ttu-id="302ae-988">identification cards</span><span class="sxs-lookup"><span data-stu-id="302ae-988">identification cards</span></span>
- <span data-ttu-id="302ae-989">Identifikations</span><span class="sxs-lookup"><span data-stu-id="302ae-989">identification</span></span> 
- <span data-ttu-id="302ae-990">DL</span><span class="sxs-lookup"><span data-stu-id="302ae-990">DL#</span></span>
- <span data-ttu-id="302ae-991">DLS</span><span class="sxs-lookup"><span data-stu-id="302ae-991">DLS#</span></span> 
- <span data-ttu-id="302ae-992">CDL</span><span class="sxs-lookup"><span data-stu-id="302ae-992">CDL#</span></span> 
- <span data-ttu-id="302ae-993">CDLS</span><span class="sxs-lookup"><span data-stu-id="302ae-993">CDLS#</span></span> 
- <span data-ttu-id="302ae-994">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="302ae-994">DriverLic#</span></span> 
- <span data-ttu-id="302ae-995">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="302ae-995">DriverLics#</span></span> 
- <span data-ttu-id="302ae-996">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="302ae-996">DriverLicense#</span></span> 
- <span data-ttu-id="302ae-997">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="302ae-997">DriverLicenses#</span></span> 
- <span data-ttu-id="302ae-998">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="302ae-998">DriverLicence#</span></span> 
- <span data-ttu-id="302ae-999">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="302ae-999">DriverLicences#</span></span> 
- <span data-ttu-id="302ae-1000">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-1000">Driver Lic#</span></span>
- <span data-ttu-id="302ae-1001">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-1001">Driver Lics#</span></span> 
- <span data-ttu-id="302ae-1002">Driver License#</span><span class="sxs-lookup"><span data-stu-id="302ae-1002">Driver License#</span></span> 
- <span data-ttu-id="302ae-1003">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-1003">Driver Licenses#</span></span> 
- <span data-ttu-id="302ae-1004">Driver License#</span><span class="sxs-lookup"><span data-stu-id="302ae-1004">Driver License#</span></span> 
- <span data-ttu-id="302ae-1005">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="302ae-1005">Driver Licences#</span></span> 
- <span data-ttu-id="302ae-1006">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="302ae-1006">DriversLic#</span></span> 
- <span data-ttu-id="302ae-1007">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="302ae-1007">DriversLics#</span></span> 
- <span data-ttu-id="302ae-1008">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="302ae-1008">DriversLicense#</span></span> 
- <span data-ttu-id="302ae-1009">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="302ae-1009">DriversLicenses#</span></span> 
- <span data-ttu-id="302ae-1010">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="302ae-1010">DriversLicence#</span></span> 
- <span data-ttu-id="302ae-1011">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="302ae-1011">DriversLicences#</span></span> 
- <span data-ttu-id="302ae-1012">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-1012">Drivers Lic#</span></span> 
- <span data-ttu-id="302ae-1013">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-1013">Drivers Lics#</span></span> 
- <span data-ttu-id="302ae-1014">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="302ae-1014">Drivers License#</span></span> 
- <span data-ttu-id="302ae-1015">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-1015">Drivers Licenses#</span></span> 
- <span data-ttu-id="302ae-1016">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="302ae-1016">Drivers Licence#</span></span> 
- <span data-ttu-id="302ae-1017">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="302ae-1017">Drivers Licences#</span></span> 
- <span data-ttu-id="302ae-1018">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="302ae-1018">Driver'Lic#</span></span> 
- <span data-ttu-id="302ae-1019">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="302ae-1019">Driver'Lics#</span></span> 
- <span data-ttu-id="302ae-1020">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="302ae-1020">Driver'License#</span></span> 
- <span data-ttu-id="302ae-1021">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-1021">Driver'Licenses#</span></span> 
- <span data-ttu-id="302ae-1022">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="302ae-1022">Driver'Licence#</span></span> 
- <span data-ttu-id="302ae-1023">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="302ae-1023">Driver'Licences#</span></span> 
- <span data-ttu-id="302ae-1024">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-1024">Driver' Lic#</span></span> 
- <span data-ttu-id="302ae-1025">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-1025">Driver' Lics#</span></span> 
- <span data-ttu-id="302ae-1026">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="302ae-1026">Driver' License#</span></span> 
- <span data-ttu-id="302ae-1027">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-1027">Driver' Licenses#</span></span> 
- <span data-ttu-id="302ae-1028">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="302ae-1028">Driver' Licence#</span></span> 
- <span data-ttu-id="302ae-1029">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="302ae-1029">Driver' Licences#</span></span> 
- <span data-ttu-id="302ae-1030">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="302ae-1030">Driver'sLic#</span></span> 
- <span data-ttu-id="302ae-1031">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="302ae-1031">Driver'sLics#</span></span> 
- <span data-ttu-id="302ae-1032">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="302ae-1032">Driver'sLicense#</span></span> 
- <span data-ttu-id="302ae-1033">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="302ae-1033">Driver'sLicenses#</span></span> 
- <span data-ttu-id="302ae-1034">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="302ae-1034">Driver'sLicence#</span></span> 
- <span data-ttu-id="302ae-1035">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="302ae-1035">Driver'sLicences#</span></span> 
- <span data-ttu-id="302ae-1036">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-1036">Driver's Lic#</span></span> 
- <span data-ttu-id="302ae-1037">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-1037">Driver's Lics#</span></span> 
- <span data-ttu-id="302ae-1038">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="302ae-1038">Driver's License#</span></span> 
- <span data-ttu-id="302ae-1039">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-1039">Driver's Licenses#</span></span> 
- <span data-ttu-id="302ae-1040">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="302ae-1040">Driver's Licence#</span></span> 
- <span data-ttu-id="302ae-1041">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="302ae-1041">Driver's Licences#</span></span> 
- <span data-ttu-id="302ae-1042">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="302ae-1042">Permis de Conduire#</span></span> 
- <span data-ttu-id="302ae-1043">ID</span><span class="sxs-lookup"><span data-stu-id="302ae-1043">id#</span></span> 
- <span data-ttu-id="302ae-1044">IDs</span><span class="sxs-lookup"><span data-stu-id="302ae-1044">ids#</span></span> 
- <span data-ttu-id="302ae-1045">idcard card#</span><span class="sxs-lookup"><span data-stu-id="302ae-1045">idcard card#</span></span> 
- <span data-ttu-id="302ae-1046">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="302ae-1046">idcard cards#</span></span> 
- <span data-ttu-id="302ae-1047">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="302ae-1047">idcard#</span></span> 
- <span data-ttu-id="302ae-1048">identification card#</span><span class="sxs-lookup"><span data-stu-id="302ae-1048">identification card#</span></span> 
- <span data-ttu-id="302ae-1049">identification cards#</span><span class="sxs-lookup"><span data-stu-id="302ae-1049">identification cards#</span></span> 
- <span data-ttu-id="302ae-1050">Identifikations</span><span class="sxs-lookup"><span data-stu-id="302ae-1050">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="302ae-1051">Kanadische Health Service-Nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1051">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1052">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1052">Format</span></span>

<span data-ttu-id="302ae-1053">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1053">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1054">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1054">Pattern</span></span>

<span data-ttu-id="302ae-1055">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1055">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1056">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1056">Checksum</span></span>

<span data-ttu-id="302ae-1057">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-1057">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1058">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1058">Definition</span></span>

<span data-ttu-id="302ae-1059">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1059">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1060">Der reguläre Ausdruck Regex_canada_health_service_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1060">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1061">Ein Schlüsselwort aus Keyword_canada_health_service_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1061">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-1062">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1062">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="302ae-1063">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="302ae-1063">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="302ae-1064">personal health number</span><span class="sxs-lookup"><span data-stu-id="302ae-1064">personal health number</span></span>
- <span data-ttu-id="302ae-1065">patient information</span><span class="sxs-lookup"><span data-stu-id="302ae-1065">patient information</span></span>
- <span data-ttu-id="302ae-1066">health services</span><span class="sxs-lookup"><span data-stu-id="302ae-1066">health services</span></span>
- <span data-ttu-id="302ae-1067">speciality services</span><span class="sxs-lookup"><span data-stu-id="302ae-1067">speciality services</span></span>
- <span data-ttu-id="302ae-1068">automobile accident</span><span class="sxs-lookup"><span data-stu-id="302ae-1068">automobile accident</span></span>
- <span data-ttu-id="302ae-1069">patient hospital</span><span class="sxs-lookup"><span data-stu-id="302ae-1069">patient hospital</span></span>
- <span data-ttu-id="302ae-1070">Psychiater</span><span class="sxs-lookup"><span data-stu-id="302ae-1070">psychiatrist</span></span>
- <span data-ttu-id="302ae-1071">workers compensation</span><span class="sxs-lookup"><span data-stu-id="302ae-1071">workers compensation</span></span>
- <span data-ttu-id="302ae-1072">Disability</span><span class="sxs-lookup"><span data-stu-id="302ae-1072">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="302ae-1073">Kanadische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1073">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1074">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1074">Format</span></span>

<span data-ttu-id="302ae-1075">Zwei Großbuchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1075">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1076">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1076">Pattern</span></span>

<span data-ttu-id="302ae-1077">Zwei Großbuchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1077">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1078">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1078">Checksum</span></span>

<span data-ttu-id="302ae-1079">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-1079">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1080">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1080">Definition</span></span>

<span data-ttu-id="302ae-1081">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1081">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1082">Der reguläre Ausdruck Regex_canada_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1082">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1083">Ein Schlüsselwort aus Keyword_canada_passport_number oder Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1083">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-1084">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1084">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="302ae-1085">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="302ae-1085">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="302ae-1086">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="302ae-1086">canadian citizenship</span></span>
- <span data-ttu-id="302ae-1087">canadian passport</span><span class="sxs-lookup"><span data-stu-id="302ae-1087">canadian passport</span></span>
- <span data-ttu-id="302ae-1088">passport application</span><span class="sxs-lookup"><span data-stu-id="302ae-1088">passport application</span></span>
- <span data-ttu-id="302ae-1089">passport photos</span><span class="sxs-lookup"><span data-stu-id="302ae-1089">passport photos</span></span>
- <span data-ttu-id="302ae-1090">certified translator</span><span class="sxs-lookup"><span data-stu-id="302ae-1090">certified translator</span></span>
- <span data-ttu-id="302ae-1091">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="302ae-1091">canadian citizens</span></span>
- <span data-ttu-id="302ae-1092">processing times</span><span class="sxs-lookup"><span data-stu-id="302ae-1092">processing times</span></span>
- <span data-ttu-id="302ae-1093">renewal application</span><span class="sxs-lookup"><span data-stu-id="302ae-1093">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="302ae-1094">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="302ae-1094">Keyword_passport</span></span>

- <span data-ttu-id="302ae-1095">Passport Number</span><span class="sxs-lookup"><span data-stu-id="302ae-1095">Passport Number</span></span>
- <span data-ttu-id="302ae-1096">Passport No</span><span class="sxs-lookup"><span data-stu-id="302ae-1096">Passport No</span></span>
- <span data-ttu-id="302ae-1097">Passport#</span><span class="sxs-lookup"><span data-stu-id="302ae-1097">Passport #</span></span>
- <span data-ttu-id="302ae-1098">Pass</span><span class="sxs-lookup"><span data-stu-id="302ae-1098">Passport#</span></span>
- <span data-ttu-id="302ae-1099">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="302ae-1099">PassportID</span></span>
- <span data-ttu-id="302ae-1100">Passportno</span><span class="sxs-lookup"><span data-stu-id="302ae-1100">Passportno</span></span>
- <span data-ttu-id="302ae-1101">passportnumber</span><span class="sxs-lookup"><span data-stu-id="302ae-1101">passportnumber</span></span>
- <span data-ttu-id="302ae-1102">パスポート</span><span class="sxs-lookup"><span data-stu-id="302ae-1102">パスポート</span></span>
- <span data-ttu-id="302ae-1103">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="302ae-1103">パスポート番号</span></span>
- <span data-ttu-id="302ae-1104">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="302ae-1104">パスポートのNum</span></span>
- <span data-ttu-id="302ae-1105">パスポート #</span><span class="sxs-lookup"><span data-stu-id="302ae-1105">パスポート＃</span></span>
- <span data-ttu-id="302ae-1106">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="302ae-1106">Numéro de passeport</span></span>
- <span data-ttu-id="302ae-1107">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="302ae-1107">Passeport n °</span></span>
- <span data-ttu-id="302ae-1108">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="302ae-1108">Passeport Non</span></span>
- <span data-ttu-id="302ae-1109">Passeport#</span><span class="sxs-lookup"><span data-stu-id="302ae-1109">Passeport #</span></span>
- <span data-ttu-id="302ae-1110">Passeport</span><span class="sxs-lookup"><span data-stu-id="302ae-1110">Passeport#</span></span>
- <span data-ttu-id="302ae-1111">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="302ae-1111">PasseportNon</span></span>
- <span data-ttu-id="302ae-1112">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="302ae-1112">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="302ae-1113">Kanadische Personal Health Identification-Nummer (PHIN)</span><span class="sxs-lookup"><span data-stu-id="302ae-1113">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1114">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1114">Format</span></span>

<span data-ttu-id="302ae-1115">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1115">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1116">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1116">Pattern</span></span>

<span data-ttu-id="302ae-1117">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1117">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1118">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1118">Checksum</span></span>

<span data-ttu-id="302ae-1119">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-1119">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1120">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1120">Definition</span></span>

<span data-ttu-id="302ae-1121">Eine DLP-Richtlinie ist 75% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: der reguläre Ausdruck Regex_canada_phin findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="302ae-1122">Es werden mindestens zwei Schlüsselwörter aus Keyword_canada_phin oder Keyword_canada_provinces gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1122">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-1123">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1123">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="302ae-1124">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="302ae-1124">Keyword_canada_phin</span></span>

- <span data-ttu-id="302ae-1125">social insurance number</span><span class="sxs-lookup"><span data-stu-id="302ae-1125">social insurance number</span></span>
- <span data-ttu-id="302ae-1126">health information act</span><span class="sxs-lookup"><span data-stu-id="302ae-1126">health information act</span></span>
- <span data-ttu-id="302ae-1127">income tax information</span><span class="sxs-lookup"><span data-stu-id="302ae-1127">income tax information</span></span>
- <span data-ttu-id="302ae-1128">manitoba health</span><span class="sxs-lookup"><span data-stu-id="302ae-1128">manitoba health</span></span>
- <span data-ttu-id="302ae-1129">health registration</span><span class="sxs-lookup"><span data-stu-id="302ae-1129">health registration</span></span>
- <span data-ttu-id="302ae-1130">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="302ae-1130">prescription purchases</span></span>
- <span data-ttu-id="302ae-1131">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="302ae-1131">benefit eligibility</span></span>
- <span data-ttu-id="302ae-1132">personal health</span><span class="sxs-lookup"><span data-stu-id="302ae-1132">personal health</span></span>
- <span data-ttu-id="302ae-1133">power of attorney</span><span class="sxs-lookup"><span data-stu-id="302ae-1133">power of attorney</span></span>
- <span data-ttu-id="302ae-1134">registration number</span><span class="sxs-lookup"><span data-stu-id="302ae-1134">registration number</span></span>
- <span data-ttu-id="302ae-1135">personal health number</span><span class="sxs-lookup"><span data-stu-id="302ae-1135">personal health number</span></span>
- <span data-ttu-id="302ae-1136">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="302ae-1136">practitioner referral</span></span>
- <span data-ttu-id="302ae-1137">wellness professional</span><span class="sxs-lookup"><span data-stu-id="302ae-1137">wellness professional</span></span>
- <span data-ttu-id="302ae-1138">patient referral</span><span class="sxs-lookup"><span data-stu-id="302ae-1138">patient referral</span></span>
- <span data-ttu-id="302ae-1139">health and wellness</span><span class="sxs-lookup"><span data-stu-id="302ae-1139">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="302ae-1140">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="302ae-1140">Keyword_canada_provinces</span></span>

- <span data-ttu-id="302ae-1141">Nunavut</span><span class="sxs-lookup"><span data-stu-id="302ae-1141">Nunavut</span></span>
- <span data-ttu-id="302ae-1142">Quebec</span><span class="sxs-lookup"><span data-stu-id="302ae-1142">Quebec</span></span>
- <span data-ttu-id="302ae-1143">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="302ae-1143">Northwest Territories</span></span>
- <span data-ttu-id="302ae-1144">Ontario</span><span class="sxs-lookup"><span data-stu-id="302ae-1144">Ontario</span></span>
- <span data-ttu-id="302ae-1145">British Columbia</span><span class="sxs-lookup"><span data-stu-id="302ae-1145">British Columbia</span></span>
- <span data-ttu-id="302ae-1146">Alberta</span><span class="sxs-lookup"><span data-stu-id="302ae-1146">Alberta</span></span>
- <span data-ttu-id="302ae-1147">Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="302ae-1147">Saskatchewan</span></span>
- <span data-ttu-id="302ae-1148">Manitoba</span><span class="sxs-lookup"><span data-stu-id="302ae-1148">Manitoba</span></span>
- <span data-ttu-id="302ae-1149">Yukon</span><span class="sxs-lookup"><span data-stu-id="302ae-1149">Yukon</span></span>
- <span data-ttu-id="302ae-1150">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="302ae-1150">Newfoundland and Labrador</span></span>
- <span data-ttu-id="302ae-1151">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="302ae-1151">New Brunswick</span></span>
- <span data-ttu-id="302ae-1152">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="302ae-1152">Nova Scotia</span></span>
- <span data-ttu-id="302ae-1153">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="302ae-1153">Prince Edward Island</span></span>
- <span data-ttu-id="302ae-1154">Kanada</span><span class="sxs-lookup"><span data-stu-id="302ae-1154">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="302ae-1155">Kanadische Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1155">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1156">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1156">Format</span></span>

<span data-ttu-id="302ae-1157">Neun Ziffern mit optionalen Bindestrichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-1157">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1158">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1158">Pattern</span></span>

<span data-ttu-id="302ae-1159">Formatiert</span><span class="sxs-lookup"><span data-stu-id="302ae-1159">Formatted:</span></span>
- <span data-ttu-id="302ae-1160">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1160">Three digits</span></span> 
- <span data-ttu-id="302ae-1161">Ein Bindestrich oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-1161">A hyphen or space</span></span> 
- <span data-ttu-id="302ae-1162">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1162">Three digits</span></span> 
- <span data-ttu-id="302ae-1163">Ein Bindestrich oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-1163">A hyphen or space</span></span> 
- <span data-ttu-id="302ae-1164">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1164">Three digits</span></span>

<span data-ttu-id="302ae-1165">Unformatiert: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1165">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1166">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1166">Checksum</span></span>

<span data-ttu-id="302ae-1167">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-1167">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1168">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1168">Definition</span></span>

<span data-ttu-id="302ae-1169">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1169">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1170">Die Funktion Func_canadian_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1170">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1171">Mindestens zwei dieser eine beliebige Kombination der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="302ae-1171">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="302ae-1172">Ein Schlüsselwort aus Keyword_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1172">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="302ae-1173">Ein Schlüsselwort aus Keyword_sin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1173">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="302ae-1174">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="302ae-1174">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="302ae-1175">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1175">The checksum passes.</span></span>

<span data-ttu-id="302ae-1176">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1177">Die Funktion Func_unformatted_canadian_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1177">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1178">Ein Schlüsselwort aus Keyword_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1178">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="302ae-1179">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1179">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-1180">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1180">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="302ae-1181">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="302ae-1181">Keyword_sin</span></span>

- <span data-ttu-id="302ae-1182">sin</span><span class="sxs-lookup"><span data-stu-id="302ae-1182">sin</span></span> 
- <span data-ttu-id="302ae-1183">social insurance</span><span class="sxs-lookup"><span data-stu-id="302ae-1183">social insurance</span></span> 
- <span data-ttu-id="302ae-1184">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="302ae-1184">numero d'assurance sociale</span></span> 
- <span data-ttu-id="302ae-1185">Todsünden</span><span class="sxs-lookup"><span data-stu-id="302ae-1185">sins</span></span> 
- <span data-ttu-id="302ae-1186">SSN</span><span class="sxs-lookup"><span data-stu-id="302ae-1186">ssn</span></span> 
- <span data-ttu-id="302ae-1187">SSNs</span><span class="sxs-lookup"><span data-stu-id="302ae-1187">ssns</span></span> 
- <span data-ttu-id="302ae-1188">social security</span><span class="sxs-lookup"><span data-stu-id="302ae-1188">social security</span></span> 
- <span data-ttu-id="302ae-1189">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="302ae-1189">numero d'assurance social</span></span> 
- <span data-ttu-id="302ae-1190">national identification number</span><span class="sxs-lookup"><span data-stu-id="302ae-1190">national identification number</span></span> 
- <span data-ttu-id="302ae-1191">national id</span><span class="sxs-lookup"><span data-stu-id="302ae-1191">national id</span></span> 
- <span data-ttu-id="302ae-1192">Sünde</span><span class="sxs-lookup"><span data-stu-id="302ae-1192">sin#</span></span> 
- <span data-ttu-id="302ae-1193">soc ins</span><span class="sxs-lookup"><span data-stu-id="302ae-1193">soc ins</span></span> 
- <span data-ttu-id="302ae-1194">social ins</span><span class="sxs-lookup"><span data-stu-id="302ae-1194">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="302ae-1195">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="302ae-1195">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="302ae-1196">driver's license</span><span class="sxs-lookup"><span data-stu-id="302ae-1196">driver's license</span></span> 
- <span data-ttu-id="302ae-1197">drivers license</span><span class="sxs-lookup"><span data-stu-id="302ae-1197">drivers license</span></span> 
- <span data-ttu-id="302ae-1198">driver's licence</span><span class="sxs-lookup"><span data-stu-id="302ae-1198">driver's licence</span></span> 
- <span data-ttu-id="302ae-1199">drivers licence</span><span class="sxs-lookup"><span data-stu-id="302ae-1199">drivers licence</span></span> 
- <span data-ttu-id="302ae-1200">DOB</span><span class="sxs-lookup"><span data-stu-id="302ae-1200">DOB</span></span> 
- <span data-ttu-id="302ae-1201">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="302ae-1201">Birthdate</span></span> 
- <span data-ttu-id="302ae-1202">Geburtstag</span><span class="sxs-lookup"><span data-stu-id="302ae-1202">Birthday</span></span> 
- <span data-ttu-id="302ae-1203">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="302ae-1203">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="302ae-1204">	Chile Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="302ae-1204">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1205">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1205">Format</span></span>

<span data-ttu-id="302ae-1206">7-8 Ziffern Plus Trennzeichen eine Prüfziffer oder ein Buchstaben</span><span class="sxs-lookup"><span data-stu-id="302ae-1206">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1207">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1207">Pattern</span></span>

<span data-ttu-id="302ae-1208">7-8 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="302ae-1208">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="302ae-1209">1-2 Ziffern </span><span class="sxs-lookup"><span data-stu-id="302ae-1209">1-2 digits</span></span> 
- <span data-ttu-id="302ae-1210">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="302ae-1210">A period</span></span> 
- <span data-ttu-id="302ae-1211">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1211">Three digits</span></span> 
- <span data-ttu-id="302ae-1212">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="302ae-1212">A period</span></span> 
- <span data-ttu-id="302ae-1213">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1213">Three digits</span></span> 
- <span data-ttu-id="302ae-1214">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-1214">A dash</span></span> 
- <span data-ttu-id="302ae-1215">Eine Ziffer oder ein Buchstabe (Groß-/Kleinschreibung nicht unterschieden), die bzw. der eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="302ae-1215">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1216">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1216">Checksum</span></span>

<span data-ttu-id="302ae-1217">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-1217">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1218">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1218">Definition</span></span>

<span data-ttu-id="302ae-1219">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1219">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1220">Die Funktion Func_chile_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1220">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1221">Ein Schlüsselwort aus Keyword_chile_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1221">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="302ae-1222">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1222">The checksum passes.</span></span>

<span data-ttu-id="302ae-1223">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1224">Die Funktion Func_chile_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1224">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1225">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1225">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-1226">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1226">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="302ae-1227">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="302ae-1227">Keyword_chile_id_card</span></span>

- <span data-ttu-id="302ae-1228">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="302ae-1228">National Identification Number</span></span> 
- <span data-ttu-id="302ae-1229">Identity card</span><span class="sxs-lookup"><span data-stu-id="302ae-1229">Identity card</span></span> 
- <span data-ttu-id="302ae-1230">ID</span><span class="sxs-lookup"><span data-stu-id="302ae-1230">ID</span></span> 
- <span data-ttu-id="302ae-1231">Identifikations</span><span class="sxs-lookup"><span data-stu-id="302ae-1231">Identification</span></span> 
- <span data-ttu-id="302ae-1232">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="302ae-1232">Rol Único Nacional</span></span> 
- <span data-ttu-id="302ae-1233">FÜHREN</span><span class="sxs-lookup"><span data-stu-id="302ae-1233">RUN</span></span> 
- <span data-ttu-id="302ae-1234">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="302ae-1234">Rol Único Tributario</span></span> 
- <span data-ttu-id="302ae-1235">RUT</span><span class="sxs-lookup"><span data-stu-id="302ae-1235">RUT</span></span> 
- <span data-ttu-id="302ae-1236">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="302ae-1236">Cédula de Identidad</span></span> 
- <span data-ttu-id="302ae-1237">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="302ae-1237">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="302ae-1238">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="302ae-1238">Tarjeta de identificación</span></span> 
- <span data-ttu-id="302ae-1239">Identificación</span><span class="sxs-lookup"><span data-stu-id="302ae-1239">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="302ae-1240">	China (PRC) – Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1240">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1241">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1241">Format</span></span>

<span data-ttu-id="302ae-1242">18 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1242">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1243">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1243">Pattern</span></span>

<span data-ttu-id="302ae-1244">18 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-1244">18 digits:</span></span>
- <span data-ttu-id="302ae-1245">Sechs Ziffern, die einen Adresscode angeben </span><span class="sxs-lookup"><span data-stu-id="302ae-1245">Six digits which are an address code</span></span> 
- <span data-ttu-id="302ae-1246">Acht Ziffern im Fomat JJJJMMTT, wobei es sich um das Geburtsdatum handelt </span><span class="sxs-lookup"><span data-stu-id="302ae-1246">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="302ae-1247">Drei Ziffern, die ein Reihenfolgencode sind </span><span class="sxs-lookup"><span data-stu-id="302ae-1247">Three digits which are an order code</span></span> 
- <span data-ttu-id="302ae-1248">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-1248">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1249">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1249">Checksum</span></span>

<span data-ttu-id="302ae-1250">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-1250">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1251">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1251">Definition</span></span>

<span data-ttu-id="302ae-1252">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1252">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1253">Die Funktion Func_china_resident_id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1253">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1254">Ein Schlüsselwort aus Keyword_china_resident_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1254">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="302ae-1255">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1255">The checksum passes.</span></span>

<span data-ttu-id="302ae-1256">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1256">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1257">Die Funktion Func_china_resident_id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1257">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1258">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1258">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-1259">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1259">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="302ae-1260">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="302ae-1260">Keyword_china_resident_id</span></span>

- <span data-ttu-id="302ae-1261">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="302ae-1261">Resident Identity Card</span></span> 
- <span data-ttu-id="302ae-1262">PRC</span><span class="sxs-lookup"><span data-stu-id="302ae-1262">PRC</span></span> 
- <span data-ttu-id="302ae-1263">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="302ae-1263">National Identification Card</span></span> 
- <span data-ttu-id="302ae-1264">身份证</span><span class="sxs-lookup"><span data-stu-id="302ae-1264">身份证</span></span> 
- <span data-ttu-id="302ae-1265">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="302ae-1265">居民 身份证</span></span> 
- <span data-ttu-id="302ae-1266">居民身份证</span><span class="sxs-lookup"><span data-stu-id="302ae-1266">居民身份证</span></span> 
- <span data-ttu-id="302ae-1267">鉴定</span><span class="sxs-lookup"><span data-stu-id="302ae-1267">鉴定</span></span> 
- <span data-ttu-id="302ae-1268">身分證</span><span class="sxs-lookup"><span data-stu-id="302ae-1268">身分證</span></span> 
- <span data-ttu-id="302ae-1269">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-1269">居民 身份證</span></span>
- <span data-ttu-id="302ae-1270">鑑定</span><span class="sxs-lookup"><span data-stu-id="302ae-1270">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="302ae-1271">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1271">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1272">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1272">Format</span></span>

<span data-ttu-id="302ae-1273">16 Ziffern, die formatiert oder unformatiert (dddddddddddddddd) werden können und den Luhn-Test bestehen müssen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1273">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1274">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1274">Pattern</span></span>

<span data-ttu-id="302ae-1275">Sehr komplexe und robuste Muster, die Karten aller wichtigen Marken weltweit, einschließlich Visa, MasterCard, Discover-Karte, JCB, American Express, Geschenkgutscheine und Restaurantkarten erkennen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1275">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1276">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1276">Checksum</span></span>

<span data-ttu-id="302ae-1277">Ja, die Luhn-Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1277">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1278">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1278">Definition</span></span>

<span data-ttu-id="302ae-1279">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1279">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1280">Die Funktion Func_credit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1280">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1281">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="302ae-1281">One of the following is true:</span></span>
    - <span data-ttu-id="302ae-1282">Ein Schlüsselwort aus Keyword_cc_verification wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1282">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="302ae-1283">Ein Schlüsselwort aus Keyword_cc_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1283">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="302ae-1284">Die Funktion Func_expiration_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="302ae-1284">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="302ae-1285">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1285">The checksum passes.</span></span>

<span data-ttu-id="302ae-1286">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1286">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1287">Die Funktion Func_credit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1287">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1288">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1288">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-1289">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1289">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="302ae-1290">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="302ae-1290">Keyword_cc_verification</span></span>

- <span data-ttu-id="302ae-1291">card verification</span><span class="sxs-lookup"><span data-stu-id="302ae-1291">card verification</span></span>
- <span data-ttu-id="302ae-1292">card identification number</span><span class="sxs-lookup"><span data-stu-id="302ae-1292">card identification number</span></span>
- <span data-ttu-id="302ae-1293">CVN</span><span class="sxs-lookup"><span data-stu-id="302ae-1293">cvn</span></span>
- <span data-ttu-id="302ae-1294">cid</span><span class="sxs-lookup"><span data-stu-id="302ae-1294">cid</span></span>
- <span data-ttu-id="302ae-1295">CVC2</span><span class="sxs-lookup"><span data-stu-id="302ae-1295">cvc2</span></span>
- <span data-ttu-id="302ae-1296">CVV2</span><span class="sxs-lookup"><span data-stu-id="302ae-1296">cvv2</span></span>
- <span data-ttu-id="302ae-1297">pin block</span><span class="sxs-lookup"><span data-stu-id="302ae-1297">pin block</span></span>
- <span data-ttu-id="302ae-1298">security code</span><span class="sxs-lookup"><span data-stu-id="302ae-1298">security code</span></span>
- <span data-ttu-id="302ae-1299">security number</span><span class="sxs-lookup"><span data-stu-id="302ae-1299">security number</span></span>
- <span data-ttu-id="302ae-1300">security no</span><span class="sxs-lookup"><span data-stu-id="302ae-1300">security no</span></span>
- <span data-ttu-id="302ae-1301">issue number</span><span class="sxs-lookup"><span data-stu-id="302ae-1301">issue number</span></span>
- <span data-ttu-id="302ae-1302">issue no</span><span class="sxs-lookup"><span data-stu-id="302ae-1302">issue no</span></span>
- <span data-ttu-id="302ae-1303">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="302ae-1303">cryptogramme</span></span>
- <span data-ttu-id="302ae-1304">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="302ae-1304">numéro de sécurité</span></span>
- <span data-ttu-id="302ae-1305">numero de securite</span><span class="sxs-lookup"><span data-stu-id="302ae-1305">numero de securite</span></span>
- <span data-ttu-id="302ae-1306">Kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1306">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="302ae-1307">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1307">kreditkartenprufnummer</span></span>
- <span data-ttu-id="302ae-1308">Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-1308">prüfziffer</span></span>
- <span data-ttu-id="302ae-1309">prufziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-1309">prufziffer</span></span>
- <span data-ttu-id="302ae-1310">Sicherheitskode</span><span class="sxs-lookup"><span data-stu-id="302ae-1310">sicherheits Kode</span></span>
- <span data-ttu-id="302ae-1311">Sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="302ae-1311">sicherheitscode</span></span>
- <span data-ttu-id="302ae-1312">Sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1312">sicherheitsnummer</span></span>
- <span data-ttu-id="302ae-1313">Verfalldatum</span><span class="sxs-lookup"><span data-stu-id="302ae-1313">verfalldatum</span></span>
- <span data-ttu-id="302ae-1314">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="302ae-1314">codice di verifica</span></span>
- <span data-ttu-id="302ae-1315">COD.</span><span class="sxs-lookup"><span data-stu-id="302ae-1315">cod.</span></span> <span data-ttu-id="302ae-1316">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="302ae-1316">sicurezza</span></span>
- <span data-ttu-id="302ae-1317">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="302ae-1317">cod sicurezza</span></span>
- <span data-ttu-id="302ae-1318">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="302ae-1318">n autorizzazione</span></span>
- <span data-ttu-id="302ae-1319">Código</span><span class="sxs-lookup"><span data-stu-id="302ae-1319">código</span></span>
- <span data-ttu-id="302ae-1320">codigo</span><span class="sxs-lookup"><span data-stu-id="302ae-1320">codigo</span></span>
- <span data-ttu-id="302ae-1321">COD.</span><span class="sxs-lookup"><span data-stu-id="302ae-1321">cod.</span></span> <span data-ttu-id="302ae-1322">SEG</span><span class="sxs-lookup"><span data-stu-id="302ae-1322">seg</span></span>
- <span data-ttu-id="302ae-1323">cod seg</span><span class="sxs-lookup"><span data-stu-id="302ae-1323">cod seg</span></span>
- <span data-ttu-id="302ae-1324">código de segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1324">código de segurança</span></span>
- <span data-ttu-id="302ae-1325">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="302ae-1325">codigo de seguranca</span></span>
- <span data-ttu-id="302ae-1326">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1326">codigo de segurança</span></span>
- <span data-ttu-id="302ae-1327">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="302ae-1327">código de seguranca</span></span>
- <span data-ttu-id="302ae-1328">cód.</span><span class="sxs-lookup"><span data-stu-id="302ae-1328">cód.</span></span> <span data-ttu-id="302ae-1329">Segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1329">segurança</span></span>
- <span data-ttu-id="302ae-1330">COD.</span><span class="sxs-lookup"><span data-stu-id="302ae-1330">cod.</span></span> <span data-ttu-id="302ae-1331">Seguranca COD.</span><span class="sxs-lookup"><span data-stu-id="302ae-1331">seguranca cod.</span></span> <span data-ttu-id="302ae-1332">Segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1332">segurança</span></span>
- <span data-ttu-id="302ae-1333">cód.</span><span class="sxs-lookup"><span data-stu-id="302ae-1333">cód.</span></span> <span data-ttu-id="302ae-1334">Seguranca</span><span class="sxs-lookup"><span data-stu-id="302ae-1334">seguranca</span></span>
- <span data-ttu-id="302ae-1335">cód segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1335">cód segurança</span></span>
- <span data-ttu-id="302ae-1336">COD Seguranca COD Segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1336">cod seguranca cod segurança</span></span>
- <span data-ttu-id="302ae-1337">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="302ae-1337">cód seguranca</span></span>
- <span data-ttu-id="302ae-1338">número de verificação</span><span class="sxs-lookup"><span data-stu-id="302ae-1338">número de verificação</span></span>
- <span data-ttu-id="302ae-1339">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="302ae-1339">numero de verificacao</span></span>
- <span data-ttu-id="302ae-1340">Ablauf</span><span class="sxs-lookup"><span data-stu-id="302ae-1340">ablauf</span></span>
- <span data-ttu-id="302ae-1341">Gültig bis</span><span class="sxs-lookup"><span data-stu-id="302ae-1341">gültig bis</span></span>
- <span data-ttu-id="302ae-1342">Gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="302ae-1342">gültigkeitsdatum</span></span>
- <span data-ttu-id="302ae-1343">Gultig bis</span><span class="sxs-lookup"><span data-stu-id="302ae-1343">gultig bis</span></span>
- <span data-ttu-id="302ae-1344">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="302ae-1344">gultigkeitsdatum</span></span>
- <span data-ttu-id="302ae-1345">scadenza</span><span class="sxs-lookup"><span data-stu-id="302ae-1345">scadenza</span></span>
- <span data-ttu-id="302ae-1346">data scad</span><span class="sxs-lookup"><span data-stu-id="302ae-1346">data scad</span></span>
- <span data-ttu-id="302ae-1347">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="302ae-1347">fecha de expiracion</span></span>
- <span data-ttu-id="302ae-1348">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="302ae-1348">fecha de venc</span></span>
- <span data-ttu-id="302ae-1349">vencimiento</span><span class="sxs-lookup"><span data-stu-id="302ae-1349">vencimiento</span></span>
- <span data-ttu-id="302ae-1350">válido hasta</span><span class="sxs-lookup"><span data-stu-id="302ae-1350">válido hasta</span></span>
- <span data-ttu-id="302ae-1351">valido hasta</span><span class="sxs-lookup"><span data-stu-id="302ae-1351">valido hasta</span></span>
- <span data-ttu-id="302ae-1352">VTO</span><span class="sxs-lookup"><span data-stu-id="302ae-1352">vto</span></span>
- <span data-ttu-id="302ae-1353">data de expiração</span><span class="sxs-lookup"><span data-stu-id="302ae-1353">data de expiração</span></span>
- <span data-ttu-id="302ae-1354">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="302ae-1354">data de expiracao</span></span>
- <span data-ttu-id="302ae-1355">data em que expira</span><span class="sxs-lookup"><span data-stu-id="302ae-1355">data em que expira</span></span>
- <span data-ttu-id="302ae-1356">validade</span><span class="sxs-lookup"><span data-stu-id="302ae-1356">validade</span></span>
- <span data-ttu-id="302ae-1357">Valor</span><span class="sxs-lookup"><span data-stu-id="302ae-1357">valor</span></span>
- <span data-ttu-id="302ae-1358">vencimento</span><span class="sxs-lookup"><span data-stu-id="302ae-1358">vencimento</span></span>
- <span data-ttu-id="302ae-1359">Venc</span><span class="sxs-lookup"><span data-stu-id="302ae-1359">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="302ae-1360">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="302ae-1360">Keyword_cc_name</span></span>

- <span data-ttu-id="302ae-1361">Amex</span><span class="sxs-lookup"><span data-stu-id="302ae-1361">amex</span></span>
- <span data-ttu-id="302ae-1362">american express</span><span class="sxs-lookup"><span data-stu-id="302ae-1362">american express</span></span>
- <span data-ttu-id="302ae-1363">AmericanExpress</span><span class="sxs-lookup"><span data-stu-id="302ae-1363">americanexpress</span></span>
- <span data-ttu-id="302ae-1364">Visa</span><span class="sxs-lookup"><span data-stu-id="302ae-1364">Visa</span></span>
- <span data-ttu-id="302ae-1365">Card</span><span class="sxs-lookup"><span data-stu-id="302ae-1365">mastercard</span></span>
- <span data-ttu-id="302ae-1366">master card</span><span class="sxs-lookup"><span data-stu-id="302ae-1366">master card</span></span>
- <span data-ttu-id="302ae-1367">MC</span><span class="sxs-lookup"><span data-stu-id="302ae-1367">mc</span></span> 
- <span data-ttu-id="302ae-1368">MasterCards gesichert</span><span class="sxs-lookup"><span data-stu-id="302ae-1368">mastercards</span></span>
- <span data-ttu-id="302ae-1369">master cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1369">master cards</span></span>
- <span data-ttu-id="302ae-1370">diner's Club</span><span class="sxs-lookup"><span data-stu-id="302ae-1370">diner's Club</span></span>
- <span data-ttu-id="302ae-1371">diners club</span><span class="sxs-lookup"><span data-stu-id="302ae-1371">diners club</span></span>
- <span data-ttu-id="302ae-1372">DinersClub</span><span class="sxs-lookup"><span data-stu-id="302ae-1372">dinersclub</span></span>
- <span data-ttu-id="302ae-1373">discover card</span><span class="sxs-lookup"><span data-stu-id="302ae-1373">discover card</span></span>
- <span data-ttu-id="302ae-1374">discovercard</span><span class="sxs-lookup"><span data-stu-id="302ae-1374">discovercard</span></span>
- <span data-ttu-id="302ae-1375">discover cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1375">discover cards</span></span>
- <span data-ttu-id="302ae-1376">JCB</span><span class="sxs-lookup"><span data-stu-id="302ae-1376">JCB</span></span>
- <span data-ttu-id="302ae-1377">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="302ae-1377">japanese card bureau</span></span>
- <span data-ttu-id="302ae-1378">carte blanche</span><span class="sxs-lookup"><span data-stu-id="302ae-1378">carte blanche</span></span>
- <span data-ttu-id="302ae-1379">CarteBlanche</span><span class="sxs-lookup"><span data-stu-id="302ae-1379">carteblanche</span></span>
- <span data-ttu-id="302ae-1380">credit card</span><span class="sxs-lookup"><span data-stu-id="302ae-1380">credit card</span></span>
- <span data-ttu-id="302ae-1381">CC</span><span class="sxs-lookup"><span data-stu-id="302ae-1381">cc#</span></span>
- <span data-ttu-id="302ae-1382">cc #:</span><span class="sxs-lookup"><span data-stu-id="302ae-1382">cc#:</span></span>
- <span data-ttu-id="302ae-1383">expiration date</span><span class="sxs-lookup"><span data-stu-id="302ae-1383">expiration date</span></span>
- <span data-ttu-id="302ae-1384">exp date</span><span class="sxs-lookup"><span data-stu-id="302ae-1384">exp date</span></span>
- <span data-ttu-id="302ae-1385">expiry date</span><span class="sxs-lookup"><span data-stu-id="302ae-1385">expiry date</span></span>
- <span data-ttu-id="302ae-1386">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="302ae-1386">date d’expiration</span></span>
- <span data-ttu-id="302ae-1387">date d'exp</span><span class="sxs-lookup"><span data-stu-id="302ae-1387">date d'exp</span></span>
- <span data-ttu-id="302ae-1388">date expiration</span><span class="sxs-lookup"><span data-stu-id="302ae-1388">date expiration</span></span>
- <span data-ttu-id="302ae-1389">bank card</span><span class="sxs-lookup"><span data-stu-id="302ae-1389">bank card</span></span>
- <span data-ttu-id="302ae-1390">Bankcard</span><span class="sxs-lookup"><span data-stu-id="302ae-1390">bankcard</span></span>
- <span data-ttu-id="302ae-1391">card number</span><span class="sxs-lookup"><span data-stu-id="302ae-1391">card number</span></span>
- <span data-ttu-id="302ae-1392">card num</span><span class="sxs-lookup"><span data-stu-id="302ae-1392">card num</span></span>
- <span data-ttu-id="302ae-1393">cardNumber</span><span class="sxs-lookup"><span data-stu-id="302ae-1393">cardnumber</span></span>
- <span data-ttu-id="302ae-1394">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="302ae-1394">cardnumbers</span></span>
- <span data-ttu-id="302ae-1395">card numbers</span><span class="sxs-lookup"><span data-stu-id="302ae-1395">card numbers</span></span>
- <span data-ttu-id="302ae-1396">CreditCard</span><span class="sxs-lookup"><span data-stu-id="302ae-1396">creditcard</span></span>
- <span data-ttu-id="302ae-1397">credit cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1397">credit cards</span></span>
- <span data-ttu-id="302ae-1398">creditCards</span><span class="sxs-lookup"><span data-stu-id="302ae-1398">creditcards</span></span>
- <span data-ttu-id="302ae-1399">CCN</span><span class="sxs-lookup"><span data-stu-id="302ae-1399">ccn</span></span>
- <span data-ttu-id="302ae-1400">card holder</span><span class="sxs-lookup"><span data-stu-id="302ae-1400">card holder</span></span>
- <span data-ttu-id="302ae-1401">Karteninhaber</span><span class="sxs-lookup"><span data-stu-id="302ae-1401">cardholder</span></span>
- <span data-ttu-id="302ae-1402">card holders</span><span class="sxs-lookup"><span data-stu-id="302ae-1402">card holders</span></span>
- <span data-ttu-id="302ae-1403">Inhaber</span><span class="sxs-lookup"><span data-stu-id="302ae-1403">cardholders</span></span>
- <span data-ttu-id="302ae-1404">check card</span><span class="sxs-lookup"><span data-stu-id="302ae-1404">check card</span></span>
- <span data-ttu-id="302ae-1405">checkcard</span><span class="sxs-lookup"><span data-stu-id="302ae-1405">checkcard</span></span>
- <span data-ttu-id="302ae-1406">check cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1406">check cards</span></span>
- <span data-ttu-id="302ae-1407">checkcards</span><span class="sxs-lookup"><span data-stu-id="302ae-1407">checkcards</span></span>
- <span data-ttu-id="302ae-1408">debit card</span><span class="sxs-lookup"><span data-stu-id="302ae-1408">debit card</span></span>
- <span data-ttu-id="302ae-1409">Debitkarte</span><span class="sxs-lookup"><span data-stu-id="302ae-1409">debitcard</span></span>
- <span data-ttu-id="302ae-1410">debit cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1410">debit cards</span></span>
- <span data-ttu-id="302ae-1411">debitcards</span><span class="sxs-lookup"><span data-stu-id="302ae-1411">debitcards</span></span>
- <span data-ttu-id="302ae-1412">atm card</span><span class="sxs-lookup"><span data-stu-id="302ae-1412">atm card</span></span>
- <span data-ttu-id="302ae-1413">atmcard</span><span class="sxs-lookup"><span data-stu-id="302ae-1413">atmcard</span></span>
- <span data-ttu-id="302ae-1414">atm cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1414">atm cards</span></span>
- <span data-ttu-id="302ae-1415">atmcards</span><span class="sxs-lookup"><span data-stu-id="302ae-1415">atmcards</span></span>
- <span data-ttu-id="302ae-1416">enroute</span><span class="sxs-lookup"><span data-stu-id="302ae-1416">enroute</span></span>
- <span data-ttu-id="302ae-1417">en route</span><span class="sxs-lookup"><span data-stu-id="302ae-1417">en route</span></span>
- <span data-ttu-id="302ae-1418">card type</span><span class="sxs-lookup"><span data-stu-id="302ae-1418">card type</span></span>
- <span data-ttu-id="302ae-1419">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="302ae-1419">carte bancaire</span></span>
- <span data-ttu-id="302ae-1420">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="302ae-1420">carte de crédit</span></span>
- <span data-ttu-id="302ae-1421">carte de credit</span><span class="sxs-lookup"><span data-stu-id="302ae-1421">carte de credit</span></span>
- <span data-ttu-id="302ae-1422">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="302ae-1422">numéro de carte</span></span>
- <span data-ttu-id="302ae-1423">numero de carte</span><span class="sxs-lookup"><span data-stu-id="302ae-1423">numero de carte</span></span>
- <span data-ttu-id="302ae-1424">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="302ae-1424">nº de la carte</span></span>
- <span data-ttu-id="302ae-1425">nº de carte</span><span class="sxs-lookup"><span data-stu-id="302ae-1425">nº de carte</span></span>
- <span data-ttu-id="302ae-1426">Kreditkarte</span><span class="sxs-lookup"><span data-stu-id="302ae-1426">kreditkarte</span></span>
- <span data-ttu-id="302ae-1427">Karte</span><span class="sxs-lookup"><span data-stu-id="302ae-1427">karte</span></span>
- <span data-ttu-id="302ae-1428">Karteninhaber</span><span class="sxs-lookup"><span data-stu-id="302ae-1428">karteninhaber</span></span>
- <span data-ttu-id="302ae-1429">Karteninhabers</span><span class="sxs-lookup"><span data-stu-id="302ae-1429">karteninhabers</span></span>
- <span data-ttu-id="302ae-1430">Kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="302ae-1430">kreditkarteninhaber</span></span>
- <span data-ttu-id="302ae-1431">Kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="302ae-1431">kreditkarteninstitut</span></span>
- <span data-ttu-id="302ae-1432">Kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="302ae-1432">kreditkartentyp</span></span>
- <span data-ttu-id="302ae-1433">Eigentümername</span><span class="sxs-lookup"><span data-stu-id="302ae-1433">eigentümername</span></span>
- <span data-ttu-id="302ae-1434">Kartennr</span><span class="sxs-lookup"><span data-stu-id="302ae-1434">kartennr</span></span> 
- <span data-ttu-id="302ae-1435">Kartennummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1435">kartennummer</span></span>
- <span data-ttu-id="302ae-1436">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1436">kreditkartennummer</span></span>
- <span data-ttu-id="302ae-1437">Kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1437">kreditkarten-nummer</span></span>
- <span data-ttu-id="302ae-1438">carta di credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1438">carta di credito</span></span>
- <span data-ttu-id="302ae-1439">carta credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1439">carta credito</span></span>
- <span data-ttu-id="302ae-1440">Carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1440">carta</span></span>
- <span data-ttu-id="302ae-1441">n carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1441">n carta</span></span>
- <span data-ttu-id="302ae-1442">Nr.</span><span class="sxs-lookup"><span data-stu-id="302ae-1442">nr.</span></span> <span data-ttu-id="302ae-1443">Carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1443">carta</span></span>
- <span data-ttu-id="302ae-1444">nr carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1444">nr carta</span></span>
- <span data-ttu-id="302ae-1445">numero carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1445">numero carta</span></span>
- <span data-ttu-id="302ae-1446">numero della carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1446">numero della carta</span></span>
- <span data-ttu-id="302ae-1447">numero di carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1447">numero di carta</span></span>
- <span data-ttu-id="302ae-1448">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1448">tarjeta credito</span></span>
- <span data-ttu-id="302ae-1449">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1449">tarjeta de credito</span></span>
- <span data-ttu-id="302ae-1450">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="302ae-1450">tarjeta crédito</span></span>
- <span data-ttu-id="302ae-1451">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="302ae-1451">tarjeta de crédito</span></span>
- <span data-ttu-id="302ae-1452">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="302ae-1452">tarjeta de atm</span></span>
- <span data-ttu-id="302ae-1453">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="302ae-1453">tarjeta atm</span></span>
- <span data-ttu-id="302ae-1454">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="302ae-1454">tarjeta debito</span></span>
- <span data-ttu-id="302ae-1455">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="302ae-1455">tarjeta de debito</span></span>
- <span data-ttu-id="302ae-1456">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="302ae-1456">tarjeta débito</span></span>
- <span data-ttu-id="302ae-1457">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="302ae-1457">tarjeta de débito</span></span>
- <span data-ttu-id="302ae-1458">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="302ae-1458">nº de tarjeta</span></span>
- <span data-ttu-id="302ae-1459">Nein.</span><span class="sxs-lookup"><span data-stu-id="302ae-1459">no.</span></span> <span data-ttu-id="302ae-1460">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="302ae-1460">de tarjeta</span></span>
- <span data-ttu-id="302ae-1461">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="302ae-1461">no de tarjeta</span></span>
- <span data-ttu-id="302ae-1462">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="302ae-1462">numero de tarjeta</span></span>
- <span data-ttu-id="302ae-1463">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="302ae-1463">número de tarjeta</span></span>
- <span data-ttu-id="302ae-1464">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="302ae-1464">tarjeta no</span></span>
- <span data-ttu-id="302ae-1465">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="302ae-1465">tarjetahabiente</span></span>
- <span data-ttu-id="302ae-1466">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="302ae-1466">cartão de crédito</span></span>
- <span data-ttu-id="302ae-1467">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1467">cartão de credito</span></span>
- <span data-ttu-id="302ae-1468">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="302ae-1468">cartao de crédito</span></span>
- <span data-ttu-id="302ae-1469">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1469">cartao de credito</span></span>
- <span data-ttu-id="302ae-1470">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="302ae-1470">cartão de débito</span></span>
- <span data-ttu-id="302ae-1471">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="302ae-1471">cartao de débito</span></span>
- <span data-ttu-id="302ae-1472">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="302ae-1472">cartão de debito</span></span>
- <span data-ttu-id="302ae-1473">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="302ae-1473">cartao de debito</span></span>
- <span data-ttu-id="302ae-1474">débito automático</span><span class="sxs-lookup"><span data-stu-id="302ae-1474">débito automático</span></span>
- <span data-ttu-id="302ae-1475">debito automatico</span><span class="sxs-lookup"><span data-stu-id="302ae-1475">debito automatico</span></span>
- <span data-ttu-id="302ae-1476">número do cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1476">número do cartão</span></span>
- <span data-ttu-id="302ae-1477">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1477">numero do cartão</span></span> 
- <span data-ttu-id="302ae-1478">número do cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1478">número do cartao</span></span>
- <span data-ttu-id="302ae-1479">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1479">numero do cartao</span></span>
- <span data-ttu-id="302ae-1480">número de cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1480">número de cartão</span></span>
- <span data-ttu-id="302ae-1481">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1481">numero de cartão</span></span>
- <span data-ttu-id="302ae-1482">número de cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1482">número de cartao</span></span>
- <span data-ttu-id="302ae-1483">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1483">numero de cartao</span></span>
- <span data-ttu-id="302ae-1484">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1484">nº do cartão</span></span>
- <span data-ttu-id="302ae-1485">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1485">nº do cartao</span></span>
- <span data-ttu-id="302ae-1486">nº.</span><span class="sxs-lookup"><span data-stu-id="302ae-1486">nº.</span></span> <span data-ttu-id="302ae-1487">do cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1487">do cartão</span></span>
- <span data-ttu-id="302ae-1488">no do cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1488">no do cartão</span></span>
- <span data-ttu-id="302ae-1489">no do cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1489">no do cartao</span></span>
- <span data-ttu-id="302ae-1490">Nein.</span><span class="sxs-lookup"><span data-stu-id="302ae-1490">no.</span></span> <span data-ttu-id="302ae-1491">do cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1491">do cartão</span></span>
- <span data-ttu-id="302ae-1492">Nein.</span><span class="sxs-lookup"><span data-stu-id="302ae-1492">no.</span></span> <span data-ttu-id="302ae-1493">do cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1493">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="302ae-1494">	Kroatien – Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1494">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1495">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1495">Format</span></span>

<span data-ttu-id="302ae-1496">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1496">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1497">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1497">Pattern</span></span>

<span data-ttu-id="302ae-1498">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1498">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1499">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1499">Checksum</span></span>

<span data-ttu-id="302ae-1500">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-1500">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1501">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1501">Definition</span></span>

<span data-ttu-id="302ae-1502">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1502">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1503">Die Funktion Func_croatia_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1503">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1504">Ein Schlüsselwort aus Keyword_croatia_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1504">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-1505">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1505">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="302ae-1506">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="302ae-1506">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="302ae-1507">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="302ae-1507">Croatian identity card</span></span>
- <span data-ttu-id="302ae-1508">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="302ae-1508">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="302ae-1509">	Croatia Personal Identification (OIB) Number</span><span class="sxs-lookup"><span data-stu-id="302ae-1509">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1510">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1510">Format</span></span>

<span data-ttu-id="302ae-1511">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1511">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1512">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1512">Pattern</span></span>

<span data-ttu-id="302ae-1513">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-1513">11 digits:</span></span>
- <span data-ttu-id="302ae-1514">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1514">10 digits</span></span> 
- <span data-ttu-id="302ae-1515">Die letzte Ziffer ist eine Prüfziffer für die Zwecke des internationalen Datenaustauschs, die Buchstaben HR werden vor den elf Ziffern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1515">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1516">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1516">Checksum</span></span>

<span data-ttu-id="302ae-1517">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-1517">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1518">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1518">Definition</span></span>

<span data-ttu-id="302ae-1519">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1519">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1520">Die Funktion Func_croatia_oib_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1520">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1521">Ein Schlüsselwort aus Keyword_croatia_oib_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1521">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="302ae-1522">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1522">The checksum passes.</span></span>

<span data-ttu-id="302ae-1523">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1523">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1524">Die Funktion Func_croatia_oib_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1524">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1525">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1525">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-1526">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1526">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="302ae-1527">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="302ae-1527">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="302ae-1528">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="302ae-1528">Personal Identification Number</span></span>
- <span data-ttu-id="302ae-1529">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="302ae-1529">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="302ae-1530">OIB</span><span class="sxs-lookup"><span data-stu-id="302ae-1530">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="302ae-1531">Tschechische Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1531">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1532">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1532">Format</span></span>

<span data-ttu-id="302ae-1533">Neun Ziffern mit optionalem Schrägstrich (altes Format) 10 Ziffern mit optionalem Schrägstrich (neues Format)</span><span class="sxs-lookup"><span data-stu-id="302ae-1533">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1534">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1534">Pattern</span></span>

<span data-ttu-id="302ae-1535">Neun Ziffern (altes Format):</span><span class="sxs-lookup"><span data-stu-id="302ae-1535">Nine digits (old format):</span></span>
- <span data-ttu-id="302ae-1536">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1536">Nine digits</span></span>

<span data-ttu-id="302ae-1537">ODER</span><span class="sxs-lookup"><span data-stu-id="302ae-1537">OR</span></span>

- <span data-ttu-id="302ae-1538">Sechs Ziffern, die das Geburtsdatum darstellen</span><span class="sxs-lookup"><span data-stu-id="302ae-1538">Six digits that represent date of birth</span></span>
- <span data-ttu-id="302ae-1539">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="302ae-1539">A forward slash</span></span>
- <span data-ttu-id="302ae-1540">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1540">Three digits</span></span>

<span data-ttu-id="302ae-1541">10 Ziffern (neues Format):</span><span class="sxs-lookup"><span data-stu-id="302ae-1541">10 digits (new format):</span></span>
- <span data-ttu-id="302ae-1542">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1542">10 digits</span></span>

<span data-ttu-id="302ae-1543">ODER</span><span class="sxs-lookup"><span data-stu-id="302ae-1543">OR</span></span>

- <span data-ttu-id="302ae-1544">Sechs Ziffern, die das Geburtsdatum darstellen</span><span class="sxs-lookup"><span data-stu-id="302ae-1544">Six digits that represent date of birth</span></span>
- <span data-ttu-id="302ae-1545">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="302ae-1545">A forward slash</span></span> 
- <span data-ttu-id="302ae-1546">Vier Ziffern, wobei die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="302ae-1546">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1547">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1547">Checksum</span></span>

<span data-ttu-id="302ae-1548">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-1548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1549">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1549">Definition</span></span>

<span data-ttu-id="302ae-1550">Eine DLP-Richtlinie ist 85% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: die Funktion Func_czech_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="302ae-1551">Ein Schlüsselwort aus Keyword_czech_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1551">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="302ae-1552">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1552">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="302ae-1553">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1553">Keywords</span></span>

- <span data-ttu-id="302ae-1554">Tschechische Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1554">czech personal identity number</span></span>
- <span data-ttu-id="302ae-1555">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="302ae-1555">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="302ae-1556">	Dänemark – Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1556">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1557">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1557">Format</span></span>

<span data-ttu-id="302ae-1558">10 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="302ae-1558">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1559">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1559">Pattern</span></span>

<span data-ttu-id="302ae-1560">10 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-1560">10 digits:</span></span>
- <span data-ttu-id="302ae-1561">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="302ae-1561">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="302ae-1562">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-1562">A hyphen</span></span> 
- <span data-ttu-id="302ae-1563">Vier Ziffern, bei denen die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="302ae-1563">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1564">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1564">Checksum</span></span>

<span data-ttu-id="302ae-1565">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-1565">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1566">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1566">Definition</span></span>

<span data-ttu-id="302ae-1567">Eine DLP-Richtlinie ist 75% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: der reguläre Ausdruck Regex_denmark_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1567">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="302ae-1568">Ein Schlüsselwort aus Keyword_denmark_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1568">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="302ae-1569">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1569">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-1570">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1570">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="302ae-1571">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="302ae-1571">Keyword_denmark_id</span></span>

- <span data-ttu-id="302ae-1572">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="302ae-1572">Personal Identification Number</span></span>
- <span data-ttu-id="302ae-1573">CPR</span><span class="sxs-lookup"><span data-stu-id="302ae-1573">CPR</span></span>
- <span data-ttu-id="302ae-1574">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="302ae-1574">Det Centrale Personregister</span></span>
- <span data-ttu-id="302ae-1575">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="302ae-1575">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="302ae-1576">Drug Enforcement Agency (DEA)-Nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1576">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1577">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1577">Format</span></span>

<span data-ttu-id="302ae-1578">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1578">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1579">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1579">Pattern</span></span>

<span data-ttu-id="302ae-1580">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="302ae-1580">Pattern must include all of the following:</span></span>
- <span data-ttu-id="302ae-1581">Einen Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) aus der folgenden Gruppe möglicher Buchstaben: abcdefghjklmnprstux, was einem Registrantencode entspricht</span><span class="sxs-lookup"><span data-stu-id="302ae-1581">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="302ae-1582">Ein Buchstabe (bei dem die Groß-und Kleinschreibung nicht beachtet wird), der dem ersten Buchstaben des Nachnamens des Registrants entspricht</span><span class="sxs-lookup"><span data-stu-id="302ae-1582">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="302ae-1583">Sieben Ziffern, von denen die letzte die Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="302ae-1583">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1584">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1584">Checksum</span></span>

<span data-ttu-id="302ae-1585">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-1585">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1586">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1586">Definition</span></span>

<span data-ttu-id="302ae-1587">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1587">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1588">Die Funktion Func_dea_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1588">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1589">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1589">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-1590">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1590">Keywords</span></span>

<span data-ttu-id="302ae-1591">None</span><span class="sxs-lookup"><span data-stu-id="302ae-1591">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="302ae-1592">EU Debit Card-Nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1592">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1593">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1593">Format</span></span>

<span data-ttu-id="302ae-1594">16 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1594">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1595">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1595">Pattern</span></span>

<span data-ttu-id="302ae-1596">Sehr komplexes und robustes Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1596">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1597">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1597">Checksum</span></span>

<span data-ttu-id="302ae-1598">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-1598">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1599">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1599">Definition</span></span>

<span data-ttu-id="302ae-1600">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1600">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1601">Die Funktion Func_eu_debit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1601">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1602">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="302ae-1602">At least one of the following is true:</span></span>
    - <span data-ttu-id="302ae-1603">Ein Schlüsselwort aus Keyword_eu_debit_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1603">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="302ae-1604">Ein Schlüsselwort aus Keyword_card_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1604">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="302ae-1605">Ein Schlüsselwort aus Keyword_card_security_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1605">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="302ae-1606">Ein Schlüsselwort aus Keyword_card_expiration_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1606">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="302ae-1607">Die Funktion Func_expiration_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="302ae-1607">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="302ae-1608">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1608">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-1609">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1609">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="302ae-1610">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="302ae-1610">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="302ae-1611">account number</span><span class="sxs-lookup"><span data-stu-id="302ae-1611">account number</span></span> 
- <span data-ttu-id="302ae-1612">card number</span><span class="sxs-lookup"><span data-stu-id="302ae-1612">card number</span></span> 
- <span data-ttu-id="302ae-1613">card no.</span><span class="sxs-lookup"><span data-stu-id="302ae-1613">card no.</span></span> 
- <span data-ttu-id="302ae-1614">security number</span><span class="sxs-lookup"><span data-stu-id="302ae-1614">security number</span></span> 
- <span data-ttu-id="302ae-1615">CC</span><span class="sxs-lookup"><span data-stu-id="302ae-1615">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="302ae-1616">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="302ae-1616">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="302ae-1617">acct nbr</span><span class="sxs-lookup"><span data-stu-id="302ae-1617">acct nbr</span></span> 
- <span data-ttu-id="302ae-1618">acct num</span><span class="sxs-lookup"><span data-stu-id="302ae-1618">acct num</span></span> 
- <span data-ttu-id="302ae-1619">acct no</span><span class="sxs-lookup"><span data-stu-id="302ae-1619">acct no</span></span> 
- <span data-ttu-id="302ae-1620">american express</span><span class="sxs-lookup"><span data-stu-id="302ae-1620">american express</span></span> 
- <span data-ttu-id="302ae-1621">AmericanExpress</span><span class="sxs-lookup"><span data-stu-id="302ae-1621">americanexpress</span></span> 
- <span data-ttu-id="302ae-1622">americano espresso</span><span class="sxs-lookup"><span data-stu-id="302ae-1622">americano espresso</span></span> 
- <span data-ttu-id="302ae-1623">Amex</span><span class="sxs-lookup"><span data-stu-id="302ae-1623">amex</span></span> 
- <span data-ttu-id="302ae-1624">atm card</span><span class="sxs-lookup"><span data-stu-id="302ae-1624">atm card</span></span> 
- <span data-ttu-id="302ae-1625">atm cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1625">atm cards</span></span> 
- <span data-ttu-id="302ae-1626">atm kaart</span><span class="sxs-lookup"><span data-stu-id="302ae-1626">atm kaart</span></span> 
- <span data-ttu-id="302ae-1627">atmcard</span><span class="sxs-lookup"><span data-stu-id="302ae-1627">atmcard</span></span> 
- <span data-ttu-id="302ae-1628">atmcards</span><span class="sxs-lookup"><span data-stu-id="302ae-1628">atmcards</span></span> 
- <span data-ttu-id="302ae-1629">atmkaart</span><span class="sxs-lookup"><span data-stu-id="302ae-1629">atmkaart</span></span> 
- <span data-ttu-id="302ae-1630">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="302ae-1630">atmkaarten</span></span> 
- <span data-ttu-id="302ae-1631">Bancontact</span><span class="sxs-lookup"><span data-stu-id="302ae-1631">bancontact</span></span> 
- <span data-ttu-id="302ae-1632">bank card</span><span class="sxs-lookup"><span data-stu-id="302ae-1632">bank card</span></span> 
- <span data-ttu-id="302ae-1633">bankkaart</span><span class="sxs-lookup"><span data-stu-id="302ae-1633">bankkaart</span></span> 
- <span data-ttu-id="302ae-1634">card holder</span><span class="sxs-lookup"><span data-stu-id="302ae-1634">card holder</span></span> 
- <span data-ttu-id="302ae-1635">card holders</span><span class="sxs-lookup"><span data-stu-id="302ae-1635">card holders</span></span> 
- <span data-ttu-id="302ae-1636">card num</span><span class="sxs-lookup"><span data-stu-id="302ae-1636">card num</span></span> 
- <span data-ttu-id="302ae-1637">card number</span><span class="sxs-lookup"><span data-stu-id="302ae-1637">card number</span></span> 
- <span data-ttu-id="302ae-1638">card numbers</span><span class="sxs-lookup"><span data-stu-id="302ae-1638">card numbers</span></span> 
- <span data-ttu-id="302ae-1639">card type</span><span class="sxs-lookup"><span data-stu-id="302ae-1639">card type</span></span> 
- <span data-ttu-id="302ae-1640">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="302ae-1640">cardano numerico</span></span> 
- <span data-ttu-id="302ae-1641">Karteninhaber</span><span class="sxs-lookup"><span data-stu-id="302ae-1641">cardholder</span></span> 
- <span data-ttu-id="302ae-1642">Inhaber</span><span class="sxs-lookup"><span data-stu-id="302ae-1642">cardholders</span></span> 
- <span data-ttu-id="302ae-1643">cardNumber</span><span class="sxs-lookup"><span data-stu-id="302ae-1643">cardnumber</span></span> 
- <span data-ttu-id="302ae-1644">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="302ae-1644">cardnumbers</span></span> 
- <span data-ttu-id="302ae-1645">carta bianca</span><span class="sxs-lookup"><span data-stu-id="302ae-1645">carta bianca</span></span> 
- <span data-ttu-id="302ae-1646">carta credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1646">carta credito</span></span> 
- <span data-ttu-id="302ae-1647">carta di credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1647">carta di credito</span></span> 
- <span data-ttu-id="302ae-1648">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1648">cartao de credito</span></span> 
- <span data-ttu-id="302ae-1649">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="302ae-1649">cartao de crédito</span></span> 
- <span data-ttu-id="302ae-1650">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="302ae-1650">cartao de debito</span></span> 
- <span data-ttu-id="302ae-1651">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="302ae-1651">cartao de débito</span></span> 
- <span data-ttu-id="302ae-1652">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="302ae-1652">carte bancaire</span></span> 
- <span data-ttu-id="302ae-1653">carte blanche</span><span class="sxs-lookup"><span data-stu-id="302ae-1653">carte blanche</span></span> 
- <span data-ttu-id="302ae-1654">carte bleue</span><span class="sxs-lookup"><span data-stu-id="302ae-1654">carte bleue</span></span> 
- <span data-ttu-id="302ae-1655">carte de credit</span><span class="sxs-lookup"><span data-stu-id="302ae-1655">carte de credit</span></span> 
- <span data-ttu-id="302ae-1656">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="302ae-1656">carte de crédit</span></span> 
- <span data-ttu-id="302ae-1657">carte di credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1657">carte di credito</span></span> 
- <span data-ttu-id="302ae-1658">CarteBlanche</span><span class="sxs-lookup"><span data-stu-id="302ae-1658">carteblanche</span></span> 
- <span data-ttu-id="302ae-1659">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1659">cartão de credito</span></span> 
- <span data-ttu-id="302ae-1660">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="302ae-1660">cartão de crédito</span></span> 
- <span data-ttu-id="302ae-1661">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="302ae-1661">cartão de debito</span></span> 
- <span data-ttu-id="302ae-1662">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="302ae-1662">cartão de débito</span></span> 
- <span data-ttu-id="302ae-1663">cb</span><span class="sxs-lookup"><span data-stu-id="302ae-1663">cb</span></span> 
- <span data-ttu-id="302ae-1664">CCN</span><span class="sxs-lookup"><span data-stu-id="302ae-1664">ccn</span></span> 
- <span data-ttu-id="302ae-1665">check card</span><span class="sxs-lookup"><span data-stu-id="302ae-1665">check card</span></span> 
- <span data-ttu-id="302ae-1666">check cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1666">check cards</span></span> 
- <span data-ttu-id="302ae-1667">checkcard</span><span class="sxs-lookup"><span data-stu-id="302ae-1667">checkcard</span></span>
- <span data-ttu-id="302ae-1668">checkcards</span><span class="sxs-lookup"><span data-stu-id="302ae-1668">checkcards</span></span> 
- <span data-ttu-id="302ae-1669">chequekaart</span><span class="sxs-lookup"><span data-stu-id="302ae-1669">chequekaart</span></span> 
- <span data-ttu-id="302ae-1670">Cirrus</span><span class="sxs-lookup"><span data-stu-id="302ae-1670">cirrus</span></span> 
- <span data-ttu-id="302ae-1671">Cirrus-EDC-Maestro</span><span class="sxs-lookup"><span data-stu-id="302ae-1671">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="302ae-1672">controlekaart</span><span class="sxs-lookup"><span data-stu-id="302ae-1672">controlekaart</span></span> 
- <span data-ttu-id="302ae-1673">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="302ae-1673">controlekaarten</span></span> 
- <span data-ttu-id="302ae-1674">credit card</span><span class="sxs-lookup"><span data-stu-id="302ae-1674">credit card</span></span> 
- <span data-ttu-id="302ae-1675">credit cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1675">credit cards</span></span> 
- <span data-ttu-id="302ae-1676">CreditCard</span><span class="sxs-lookup"><span data-stu-id="302ae-1676">creditcard</span></span> 
- <span data-ttu-id="302ae-1677">creditCards</span><span class="sxs-lookup"><span data-stu-id="302ae-1677">creditcards</span></span> 
- <span data-ttu-id="302ae-1678">debetkaart</span><span class="sxs-lookup"><span data-stu-id="302ae-1678">debetkaart</span></span> 
- <span data-ttu-id="302ae-1679">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="302ae-1679">debetkaarten</span></span> 
- <span data-ttu-id="302ae-1680">debit card</span><span class="sxs-lookup"><span data-stu-id="302ae-1680">debit card</span></span> 
- <span data-ttu-id="302ae-1681">debit cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1681">debit cards</span></span> 
- <span data-ttu-id="302ae-1682">Debitkarte</span><span class="sxs-lookup"><span data-stu-id="302ae-1682">debitcard</span></span> 
- <span data-ttu-id="302ae-1683">debitcards</span><span class="sxs-lookup"><span data-stu-id="302ae-1683">debitcards</span></span> 
- <span data-ttu-id="302ae-1684">debito automatico</span><span class="sxs-lookup"><span data-stu-id="302ae-1684">debito automatico</span></span> 
- <span data-ttu-id="302ae-1685">diners club</span><span class="sxs-lookup"><span data-stu-id="302ae-1685">diners club</span></span> 
- <span data-ttu-id="302ae-1686">DinersClub</span><span class="sxs-lookup"><span data-stu-id="302ae-1686">dinersclub</span></span> 
- <span data-ttu-id="302ae-1687">Entdecken</span><span class="sxs-lookup"><span data-stu-id="302ae-1687">discover</span></span> 
- <span data-ttu-id="302ae-1688">discover card</span><span class="sxs-lookup"><span data-stu-id="302ae-1688">discover card</span></span> 
- <span data-ttu-id="302ae-1689">discover cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1689">discover cards</span></span> 
- <span data-ttu-id="302ae-1690">discovercard</span><span class="sxs-lookup"><span data-stu-id="302ae-1690">discovercard</span></span> 
- <span data-ttu-id="302ae-1691">discovercards</span><span class="sxs-lookup"><span data-stu-id="302ae-1691">discovercards</span></span> 
- <span data-ttu-id="302ae-1692">débito automático</span><span class="sxs-lookup"><span data-stu-id="302ae-1692">débito automático</span></span>
- <span data-ttu-id="302ae-1693">EDC</span><span class="sxs-lookup"><span data-stu-id="302ae-1693">edc</span></span> 
- <span data-ttu-id="302ae-1694">Eigentümername</span><span class="sxs-lookup"><span data-stu-id="302ae-1694">eigentümername</span></span> 
- <span data-ttu-id="302ae-1695">european debit card</span><span class="sxs-lookup"><span data-stu-id="302ae-1695">european debit card</span></span> 
- <span data-ttu-id="302ae-1696">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="302ae-1696">hoofdkaart</span></span> 
- <span data-ttu-id="302ae-1697">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="302ae-1697">hoofdkaarten</span></span> 
- <span data-ttu-id="302ae-1698">in viaggio</span><span class="sxs-lookup"><span data-stu-id="302ae-1698">in viaggio</span></span> 
- <span data-ttu-id="302ae-1699">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="302ae-1699">japanese card bureau</span></span> 
- <span data-ttu-id="302ae-1700">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="302ae-1700">japanse kaartdienst</span></span> 
- <span data-ttu-id="302ae-1701">JCB</span><span class="sxs-lookup"><span data-stu-id="302ae-1701">jcb</span></span> 
- <span data-ttu-id="302ae-1702">Kaart</span><span class="sxs-lookup"><span data-stu-id="302ae-1702">kaart</span></span> 
- <span data-ttu-id="302ae-1703">kaart num</span><span class="sxs-lookup"><span data-stu-id="302ae-1703">kaart num</span></span> 
- <span data-ttu-id="302ae-1704">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="302ae-1704">kaartaantal</span></span> 
- <span data-ttu-id="302ae-1705">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="302ae-1705">kaartaantallen</span></span> 
- <span data-ttu-id="302ae-1706">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="302ae-1706">kaarthouder</span></span> 
- <span data-ttu-id="302ae-1707">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="302ae-1707">kaarthouders</span></span> 
- <span data-ttu-id="302ae-1708">Karte</span><span class="sxs-lookup"><span data-stu-id="302ae-1708">karte</span></span>  
- <span data-ttu-id="302ae-1709">Karteninhaber</span><span class="sxs-lookup"><span data-stu-id="302ae-1709">karteninhaber</span></span> 
- <span data-ttu-id="302ae-1710">Karteninhabers</span><span class="sxs-lookup"><span data-stu-id="302ae-1710">karteninhabers</span></span>
- <span data-ttu-id="302ae-1711">Kartennr</span><span class="sxs-lookup"><span data-stu-id="302ae-1711">kartennr</span></span> 
- <span data-ttu-id="302ae-1712">Kartennummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1712">kartennummer</span></span> 
- <span data-ttu-id="302ae-1713">Kreditkarte</span><span class="sxs-lookup"><span data-stu-id="302ae-1713">kreditkarte</span></span> 
- <span data-ttu-id="302ae-1714">Kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1714">kreditkarten-nummer</span></span> 
- <span data-ttu-id="302ae-1715">Kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="302ae-1715">kreditkarteninhaber</span></span> 
- <span data-ttu-id="302ae-1716">Kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="302ae-1716">kreditkarteninstitut</span></span> 
- <span data-ttu-id="302ae-1717">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1717">kreditkartennummer</span></span> 
- <span data-ttu-id="302ae-1718">Kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="302ae-1718">kreditkartentyp</span></span> 
- <span data-ttu-id="302ae-1719">Maestro</span><span class="sxs-lookup"><span data-stu-id="302ae-1719">maestro</span></span> 
- <span data-ttu-id="302ae-1720">master card</span><span class="sxs-lookup"><span data-stu-id="302ae-1720">master card</span></span> 
- <span data-ttu-id="302ae-1721">master cards</span><span class="sxs-lookup"><span data-stu-id="302ae-1721">master cards</span></span> 
- <span data-ttu-id="302ae-1722">Card</span><span class="sxs-lookup"><span data-stu-id="302ae-1722">mastercard</span></span> 
- <span data-ttu-id="302ae-1723">MasterCards gesichert</span><span class="sxs-lookup"><span data-stu-id="302ae-1723">mastercards</span></span> 
- <span data-ttu-id="302ae-1724">MC</span><span class="sxs-lookup"><span data-stu-id="302ae-1724">mc</span></span> 
- <span data-ttu-id="302ae-1725">mister cash</span><span class="sxs-lookup"><span data-stu-id="302ae-1725">mister cash</span></span> 
- <span data-ttu-id="302ae-1726">n carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1726">n carta</span></span> 
- <span data-ttu-id="302ae-1727">Carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1727">carta</span></span> 
- <span data-ttu-id="302ae-1728">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="302ae-1728">no de tarjeta</span></span> 
- <span data-ttu-id="302ae-1729">no do cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1729">no do cartao</span></span> 
- <span data-ttu-id="302ae-1730">no do cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1730">no do cartão</span></span> 
- <span data-ttu-id="302ae-1731">Nein.</span><span class="sxs-lookup"><span data-stu-id="302ae-1731">no.</span></span> <span data-ttu-id="302ae-1732">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="302ae-1732">de tarjeta</span></span> 
- <span data-ttu-id="302ae-1733">Nein.</span><span class="sxs-lookup"><span data-stu-id="302ae-1733">no.</span></span> <span data-ttu-id="302ae-1734">do cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1734">do cartao</span></span> 
- <span data-ttu-id="302ae-1735">Nein.</span><span class="sxs-lookup"><span data-stu-id="302ae-1735">no.</span></span> <span data-ttu-id="302ae-1736">do cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1736">do cartão</span></span> 
- <span data-ttu-id="302ae-1737">nr carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1737">nr carta</span></span> 
- <span data-ttu-id="302ae-1738">Nr.</span><span class="sxs-lookup"><span data-stu-id="302ae-1738">nr.</span></span> <span data-ttu-id="302ae-1739">Carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1739">carta</span></span> 
- <span data-ttu-id="302ae-1740">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="302ae-1740">numeri di scheda</span></span> 
- <span data-ttu-id="302ae-1741">numero carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1741">numero carta</span></span> 
- <span data-ttu-id="302ae-1742">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1742">numero de cartao</span></span> 
- <span data-ttu-id="302ae-1743">numero de carte</span><span class="sxs-lookup"><span data-stu-id="302ae-1743">numero de carte</span></span> 
- <span data-ttu-id="302ae-1744">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1744">numero de cartão</span></span> 
- <span data-ttu-id="302ae-1745">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="302ae-1745">numero de tarjeta</span></span>
- <span data-ttu-id="302ae-1746">numero della carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1746">numero della carta</span></span> 
- <span data-ttu-id="302ae-1747">numero di carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1747">numero di carta</span></span> 
- <span data-ttu-id="302ae-1748">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="302ae-1748">numero di scheda</span></span> 
- <span data-ttu-id="302ae-1749">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1749">numero do cartao</span></span> 
- <span data-ttu-id="302ae-1750">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1750">numero do cartão</span></span> 
- <span data-ttu-id="302ae-1751">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="302ae-1751">numéro de carte</span></span> 
- <span data-ttu-id="302ae-1752">nº carta</span><span class="sxs-lookup"><span data-stu-id="302ae-1752">nº carta</span></span> 
- <span data-ttu-id="302ae-1753">nº de carte</span><span class="sxs-lookup"><span data-stu-id="302ae-1753">nº de carte</span></span> 
- <span data-ttu-id="302ae-1754">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="302ae-1754">nº de la carte</span></span> 
- <span data-ttu-id="302ae-1755">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="302ae-1755">nº de tarjeta</span></span> 
- <span data-ttu-id="302ae-1756">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1756">nº do cartao</span></span> 
- <span data-ttu-id="302ae-1757">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1757">nº do cartão</span></span> 
- <span data-ttu-id="302ae-1758">nº.</span><span class="sxs-lookup"><span data-stu-id="302ae-1758">nº.</span></span> <span data-ttu-id="302ae-1759">do cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1759">do cartão</span></span> 
- <span data-ttu-id="302ae-1760">número de cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1760">número de cartao</span></span> 
- <span data-ttu-id="302ae-1761">número de cartão</span><span class="sxs-lookup"><span data-stu-id="302ae-1761">número de cartão</span></span> 
- <span data-ttu-id="302ae-1762">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="302ae-1762">número de tarjeta</span></span> 
- <span data-ttu-id="302ae-1763">número do cartao</span><span class="sxs-lookup"><span data-stu-id="302ae-1763">número do cartao</span></span> 
- <span data-ttu-id="302ae-1764">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="302ae-1764">scheda dell'assegno</span></span> 
- <span data-ttu-id="302ae-1765">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="302ae-1765">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="302ae-1766">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="302ae-1766">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="302ae-1767">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="302ae-1767">scheda della banca</span></span> 
- <span data-ttu-id="302ae-1768">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="302ae-1768">scheda di controllo</span></span> 
- <span data-ttu-id="302ae-1769">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="302ae-1769">scheda di debito</span></span> 
- <span data-ttu-id="302ae-1770">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="302ae-1770">scheda matrice</span></span> 
- <span data-ttu-id="302ae-1771">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="302ae-1771">schede dell'atmosfera</span></span> 
- <span data-ttu-id="302ae-1772">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="302ae-1772">schede di controllo</span></span> 
- <span data-ttu-id="302ae-1773">schede di debito</span><span class="sxs-lookup"><span data-stu-id="302ae-1773">schede di debito</span></span> 
- <span data-ttu-id="302ae-1774">schede matrici</span><span class="sxs-lookup"><span data-stu-id="302ae-1774">schede matrici</span></span> 
- <span data-ttu-id="302ae-1775">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="302ae-1775">scoprono la scheda</span></span> 
- <span data-ttu-id="302ae-1776">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="302ae-1776">scoprono le schede</span></span> 
- <span data-ttu-id="302ae-1777">Solo</span><span class="sxs-lookup"><span data-stu-id="302ae-1777">solo</span></span> 
- <span data-ttu-id="302ae-1778">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="302ae-1778">supporti di scheda</span></span> 
- <span data-ttu-id="302ae-1779">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="302ae-1779">supporto di scheda</span></span> 
- <span data-ttu-id="302ae-1780">Wechseln</span><span class="sxs-lookup"><span data-stu-id="302ae-1780">switch</span></span> 
- <span data-ttu-id="302ae-1781">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="302ae-1781">tarjeta atm</span></span> 
- <span data-ttu-id="302ae-1782">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1782">tarjeta credito</span></span> 
- <span data-ttu-id="302ae-1783">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="302ae-1783">tarjeta de atm</span></span> 
- <span data-ttu-id="302ae-1784">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="302ae-1784">tarjeta de credito</span></span> 
- <span data-ttu-id="302ae-1785">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="302ae-1785">tarjeta de debito</span></span> 
- <span data-ttu-id="302ae-1786">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="302ae-1786">tarjeta debito</span></span> 
- <span data-ttu-id="302ae-1787">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="302ae-1787">tarjeta no</span></span>
- <span data-ttu-id="302ae-1788">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="302ae-1788">tarjetahabiente</span></span> 
- <span data-ttu-id="302ae-1789">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="302ae-1789">tipo della scheda</span></span> 
- <span data-ttu-id="302ae-1790">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="302ae-1790">ufficio giapponese della</span></span> 
- <span data-ttu-id="302ae-1791">Scheda</span><span class="sxs-lookup"><span data-stu-id="302ae-1791">scheda</span></span> 
- <span data-ttu-id="302ae-1792">v pay</span><span class="sxs-lookup"><span data-stu-id="302ae-1792">v pay</span></span> 
- <span data-ttu-id="302ae-1793">v-Pay</span><span class="sxs-lookup"><span data-stu-id="302ae-1793">v-pay</span></span> 
- <span data-ttu-id="302ae-1794">Visa</span><span class="sxs-lookup"><span data-stu-id="302ae-1794">visa</span></span> 
- <span data-ttu-id="302ae-1795">visa plus</span><span class="sxs-lookup"><span data-stu-id="302ae-1795">visa plus</span></span> 
- <span data-ttu-id="302ae-1796">visa electron</span><span class="sxs-lookup"><span data-stu-id="302ae-1796">visa electron</span></span> 
- <span data-ttu-id="302ae-1797">Visto</span><span class="sxs-lookup"><span data-stu-id="302ae-1797">visto</span></span> 
- <span data-ttu-id="302ae-1798">Visum</span><span class="sxs-lookup"><span data-stu-id="302ae-1798">visum</span></span> 
- <span data-ttu-id="302ae-1799">vpay</span><span class="sxs-lookup"><span data-stu-id="302ae-1799">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="302ae-1800">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="302ae-1800">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="302ae-1801">card identification number</span><span class="sxs-lookup"><span data-stu-id="302ae-1801">card identification number</span></span>
- <span data-ttu-id="302ae-1802">card verification</span><span class="sxs-lookup"><span data-stu-id="302ae-1802">card verification</span></span> 
- <span data-ttu-id="302ae-1803">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="302ae-1803">cardi la verifica</span></span> 
- <span data-ttu-id="302ae-1804">cid</span><span class="sxs-lookup"><span data-stu-id="302ae-1804">cid</span></span> 
- <span data-ttu-id="302ae-1805">cod seg</span><span class="sxs-lookup"><span data-stu-id="302ae-1805">cod seg</span></span> 
- <span data-ttu-id="302ae-1806">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="302ae-1806">cod seguranca</span></span> 
- <span data-ttu-id="302ae-1807">cod segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1807">cod segurança</span></span> 
- <span data-ttu-id="302ae-1808">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="302ae-1808">cod sicurezza</span></span> 
- <span data-ttu-id="302ae-1809">COD.</span><span class="sxs-lookup"><span data-stu-id="302ae-1809">cod.</span></span> <span data-ttu-id="302ae-1810">SEG</span><span class="sxs-lookup"><span data-stu-id="302ae-1810">seg</span></span> 
- <span data-ttu-id="302ae-1811">COD.</span><span class="sxs-lookup"><span data-stu-id="302ae-1811">cod.</span></span> <span data-ttu-id="302ae-1812">Seguranca</span><span class="sxs-lookup"><span data-stu-id="302ae-1812">seguranca</span></span> 
- <span data-ttu-id="302ae-1813">COD.</span><span class="sxs-lookup"><span data-stu-id="302ae-1813">cod.</span></span> <span data-ttu-id="302ae-1814">Segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1814">segurança</span></span> 
- <span data-ttu-id="302ae-1815">COD.</span><span class="sxs-lookup"><span data-stu-id="302ae-1815">cod.</span></span> <span data-ttu-id="302ae-1816">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="302ae-1816">sicurezza</span></span> 
- <span data-ttu-id="302ae-1817">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="302ae-1817">codice di sicurezza</span></span> 
- <span data-ttu-id="302ae-1818">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="302ae-1818">codice di verifica</span></span> 
- <span data-ttu-id="302ae-1819">codigo</span><span class="sxs-lookup"><span data-stu-id="302ae-1819">codigo</span></span> 
- <span data-ttu-id="302ae-1820">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="302ae-1820">codigo de seguranca</span></span> 
- <span data-ttu-id="302ae-1821">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1821">codigo de segurança</span></span> 
- <span data-ttu-id="302ae-1822">crittogramma</span><span class="sxs-lookup"><span data-stu-id="302ae-1822">crittogramma</span></span> 
- <span data-ttu-id="302ae-1823">Kryptogramm</span><span class="sxs-lookup"><span data-stu-id="302ae-1823">cryptogram</span></span> 
- <span data-ttu-id="302ae-1824">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="302ae-1824">cryptogramme</span></span> 
- <span data-ttu-id="302ae-1825">CV2</span><span class="sxs-lookup"><span data-stu-id="302ae-1825">cv2</span></span> 
- <span data-ttu-id="302ae-1826">CVC</span><span class="sxs-lookup"><span data-stu-id="302ae-1826">cvc</span></span> 
- <span data-ttu-id="302ae-1827">CVC2</span><span class="sxs-lookup"><span data-stu-id="302ae-1827">cvc2</span></span> 
- <span data-ttu-id="302ae-1828">CVN</span><span class="sxs-lookup"><span data-stu-id="302ae-1828">cvn</span></span> 
- <span data-ttu-id="302ae-1829">CVV</span><span class="sxs-lookup"><span data-stu-id="302ae-1829">cvv</span></span> 
- <span data-ttu-id="302ae-1830">CVV2</span><span class="sxs-lookup"><span data-stu-id="302ae-1830">cvv2</span></span> 
- <span data-ttu-id="302ae-1831">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="302ae-1831">cód seguranca</span></span> 
- <span data-ttu-id="302ae-1832">cód segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1832">cód segurança</span></span> 
- <span data-ttu-id="302ae-1833">cód.</span><span class="sxs-lookup"><span data-stu-id="302ae-1833">cód.</span></span> <span data-ttu-id="302ae-1834">Seguranca</span><span class="sxs-lookup"><span data-stu-id="302ae-1834">seguranca</span></span> 
- <span data-ttu-id="302ae-1835">cód.</span><span class="sxs-lookup"><span data-stu-id="302ae-1835">cód.</span></span> <span data-ttu-id="302ae-1836">Segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1836">segurança</span></span> 
- <span data-ttu-id="302ae-1837">Código</span><span class="sxs-lookup"><span data-stu-id="302ae-1837">código</span></span> 
- <span data-ttu-id="302ae-1838">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="302ae-1838">código de seguranca</span></span> 
- <span data-ttu-id="302ae-1839">código de segurança</span><span class="sxs-lookup"><span data-stu-id="302ae-1839">código de segurança</span></span> 
- <span data-ttu-id="302ae-1840">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="302ae-1840">de kaart controle</span></span> 
- <span data-ttu-id="302ae-1841">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="302ae-1841">geeft nr uit</span></span> 
- <span data-ttu-id="302ae-1842">issue no</span><span class="sxs-lookup"><span data-stu-id="302ae-1842">issue no</span></span> 
- <span data-ttu-id="302ae-1843">issue number</span><span class="sxs-lookup"><span data-stu-id="302ae-1843">issue number</span></span> 
- <span data-ttu-id="302ae-1844">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1844">kaartidentificatienummer</span></span> 
- <span data-ttu-id="302ae-1845">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1845">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="302ae-1846">Kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1846">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="302ae-1847">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="302ae-1847">kwestieaantal</span></span> 
- <span data-ttu-id="302ae-1848">Nein.</span><span class="sxs-lookup"><span data-stu-id="302ae-1848">no.</span></span> <span data-ttu-id="302ae-1849">Dell ' edizione</span><span class="sxs-lookup"><span data-stu-id="302ae-1849">dell'edizione</span></span> 
- <span data-ttu-id="302ae-1850">Nein.</span><span class="sxs-lookup"><span data-stu-id="302ae-1850">no.</span></span> <span data-ttu-id="302ae-1851">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="302ae-1851">di sicurezza</span></span> 
- <span data-ttu-id="302ae-1852">numero de securite</span><span class="sxs-lookup"><span data-stu-id="302ae-1852">numero de securite</span></span> 
- <span data-ttu-id="302ae-1853">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="302ae-1853">numero de verificacao</span></span> 
- <span data-ttu-id="302ae-1854">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="302ae-1854">numero dell'edizione</span></span> 
- <span data-ttu-id="302ae-1855">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="302ae-1855">numero di identificazione della</span></span> 
- <span data-ttu-id="302ae-1856">Scheda</span><span class="sxs-lookup"><span data-stu-id="302ae-1856">scheda</span></span> 
- <span data-ttu-id="302ae-1857">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="302ae-1857">numero di sicurezza</span></span> 
- <span data-ttu-id="302ae-1858">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="302ae-1858">numero van veiligheid</span></span> 
- <span data-ttu-id="302ae-1859">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="302ae-1859">numéro de sécurité</span></span> 
- <span data-ttu-id="302ae-1860">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="302ae-1860">nº autorizzazione</span></span> 
- <span data-ttu-id="302ae-1861">número de verificação</span><span class="sxs-lookup"><span data-stu-id="302ae-1861">número de verificação</span></span> 
- <span data-ttu-id="302ae-1862">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="302ae-1862">perno il blocco</span></span> 
- <span data-ttu-id="302ae-1863">pin block</span><span class="sxs-lookup"><span data-stu-id="302ae-1863">pin block</span></span> 
- <span data-ttu-id="302ae-1864">prufziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-1864">prufziffer</span></span> 
- <span data-ttu-id="302ae-1865">Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-1865">prüfziffer</span></span> 
- <span data-ttu-id="302ae-1866">security code</span><span class="sxs-lookup"><span data-stu-id="302ae-1866">security code</span></span> 
- <span data-ttu-id="302ae-1867">security no</span><span class="sxs-lookup"><span data-stu-id="302ae-1867">security no</span></span> 
- <span data-ttu-id="302ae-1868">security number</span><span class="sxs-lookup"><span data-stu-id="302ae-1868">security number</span></span> 
- <span data-ttu-id="302ae-1869">Sicherheitskode</span><span class="sxs-lookup"><span data-stu-id="302ae-1869">sicherheits kode</span></span> 
- <span data-ttu-id="302ae-1870">Sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="302ae-1870">sicherheitscode</span></span> 
- <span data-ttu-id="302ae-1871">Sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1871">sicherheitsnummer</span></span> 
- <span data-ttu-id="302ae-1872">speldblok</span><span class="sxs-lookup"><span data-stu-id="302ae-1872">speldblok</span></span> 
- <span data-ttu-id="302ae-1873">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="302ae-1873">veiligheid nr</span></span> 
- <span data-ttu-id="302ae-1874">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="302ae-1874">veiligheidsaantal</span></span> 
- <span data-ttu-id="302ae-1875">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="302ae-1875">veiligheidscode</span></span> 
- <span data-ttu-id="302ae-1876">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1876">veiligheidsnummer</span></span> 
- <span data-ttu-id="302ae-1877">Verfalldatum</span><span class="sxs-lookup"><span data-stu-id="302ae-1877">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="302ae-1878">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="302ae-1878">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="302ae-1879">Ablauf</span><span class="sxs-lookup"><span data-stu-id="302ae-1879">ablauf</span></span> 
- <span data-ttu-id="302ae-1880">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="302ae-1880">data de expiracao</span></span> 
- <span data-ttu-id="302ae-1881">data de expiração</span><span class="sxs-lookup"><span data-stu-id="302ae-1881">data de expiração</span></span> 
- <span data-ttu-id="302ae-1882">data del exp</span><span class="sxs-lookup"><span data-stu-id="302ae-1882">data del exp</span></span> 
- <span data-ttu-id="302ae-1883">data di exp</span><span class="sxs-lookup"><span data-stu-id="302ae-1883">data di exp</span></span> 
- <span data-ttu-id="302ae-1884">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="302ae-1884">data di scadenza</span></span> 
- <span data-ttu-id="302ae-1885">data em que expira</span><span class="sxs-lookup"><span data-stu-id="302ae-1885">data em que expira</span></span> 
- <span data-ttu-id="302ae-1886">data scad</span><span class="sxs-lookup"><span data-stu-id="302ae-1886">data scad</span></span> 
- <span data-ttu-id="302ae-1887">data scadenza</span><span class="sxs-lookup"><span data-stu-id="302ae-1887">data scadenza</span></span> 
- <span data-ttu-id="302ae-1888">date de validité</span><span class="sxs-lookup"><span data-stu-id="302ae-1888">date de validité</span></span> 
- <span data-ttu-id="302ae-1889">datum afloop</span><span class="sxs-lookup"><span data-stu-id="302ae-1889">datum afloop</span></span> 
- <span data-ttu-id="302ae-1890">datum van exp</span><span class="sxs-lookup"><span data-stu-id="302ae-1890">datum van exp</span></span> 
- <span data-ttu-id="302ae-1891">de afloop</span><span class="sxs-lookup"><span data-stu-id="302ae-1891">de afloop</span></span> 
- <span data-ttu-id="302ae-1892">Espira</span><span class="sxs-lookup"><span data-stu-id="302ae-1892">espira</span></span> 
- <span data-ttu-id="302ae-1893">Espira</span><span class="sxs-lookup"><span data-stu-id="302ae-1893">espira</span></span> 
- <span data-ttu-id="302ae-1894">exp date</span><span class="sxs-lookup"><span data-stu-id="302ae-1894">exp date</span></span> 
- <span data-ttu-id="302ae-1895">exp datum</span><span class="sxs-lookup"><span data-stu-id="302ae-1895">exp datum</span></span> 
- <span data-ttu-id="302ae-1896">Ablauf</span><span class="sxs-lookup"><span data-stu-id="302ae-1896">expiration</span></span> 
- <span data-ttu-id="302ae-1897">läuft</span><span class="sxs-lookup"><span data-stu-id="302ae-1897">expire</span></span> 
- <span data-ttu-id="302ae-1898">abläuft</span><span class="sxs-lookup"><span data-stu-id="302ae-1898">expires</span></span> 
- <span data-ttu-id="302ae-1899">Ablauf</span><span class="sxs-lookup"><span data-stu-id="302ae-1899">expiry</span></span> 
- <span data-ttu-id="302ae-1900">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="302ae-1900">fecha de expiracion</span></span> 
- <span data-ttu-id="302ae-1901">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="302ae-1901">fecha de venc</span></span> 
- <span data-ttu-id="302ae-1902">Gultig bis</span><span class="sxs-lookup"><span data-stu-id="302ae-1902">gultig bis</span></span> 
- <span data-ttu-id="302ae-1903">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="302ae-1903">gultigkeitsdatum</span></span> 
- <span data-ttu-id="302ae-1904">Gültig bis</span><span class="sxs-lookup"><span data-stu-id="302ae-1904">gültig bis</span></span> 
- <span data-ttu-id="302ae-1905">Gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="302ae-1905">gültigkeitsdatum</span></span> 
- <span data-ttu-id="302ae-1906">la scadenza</span><span class="sxs-lookup"><span data-stu-id="302ae-1906">la scadenza</span></span> 
- <span data-ttu-id="302ae-1907">scadenza</span><span class="sxs-lookup"><span data-stu-id="302ae-1907">scadenza</span></span> 
- <span data-ttu-id="302ae-1908">valable</span><span class="sxs-lookup"><span data-stu-id="302ae-1908">valable</span></span> 
- <span data-ttu-id="302ae-1909">validade</span><span class="sxs-lookup"><span data-stu-id="302ae-1909">validade</span></span> 
- <span data-ttu-id="302ae-1910">valido hasta</span><span class="sxs-lookup"><span data-stu-id="302ae-1910">valido hasta</span></span> 
- <span data-ttu-id="302ae-1911">Valor</span><span class="sxs-lookup"><span data-stu-id="302ae-1911">valor</span></span> 
- <span data-ttu-id="302ae-1912">venc</span><span class="sxs-lookup"><span data-stu-id="302ae-1912">venc</span></span> 
- <span data-ttu-id="302ae-1913">vencimento</span><span class="sxs-lookup"><span data-stu-id="302ae-1913">vencimento</span></span> 
- <span data-ttu-id="302ae-1914">vencimiento</span><span class="sxs-lookup"><span data-stu-id="302ae-1914">vencimiento</span></span> 
- <span data-ttu-id="302ae-1915">verloopt</span><span class="sxs-lookup"><span data-stu-id="302ae-1915">verloopt</span></span> 
- <span data-ttu-id="302ae-1916">vervaldag</span><span class="sxs-lookup"><span data-stu-id="302ae-1916">vervaldag</span></span> 
- <span data-ttu-id="302ae-1917">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="302ae-1917">vervaldatum</span></span> 
- <span data-ttu-id="302ae-1918">VTO</span><span class="sxs-lookup"><span data-stu-id="302ae-1918">vto</span></span> 
- <span data-ttu-id="302ae-1919">válido hasta</span><span class="sxs-lookup"><span data-stu-id="302ae-1919">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="302ae-1920">EU-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1920">EU Driver's License Number</span></span>

<span data-ttu-id="302ae-1921">Weitere Informationen finden Sie unter [sicherheitsTyp für die EU-Treiber Lizenznummer](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="302ae-1921">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="302ae-1922">Nationale IdentifikationsNummer der EU</span><span class="sxs-lookup"><span data-stu-id="302ae-1922">EU National Identification Number</span></span>

<span data-ttu-id="302ae-1923">Weitere Informationen finden Sie unter [sensibler informationsTyp der EU-nationalen Identifikationsnummer](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="302ae-1923">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="302ae-1924">EU-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1924">EU Passport Number</span></span>

<span data-ttu-id="302ae-1925">Weitere Informationen finden Sie unter Sicherheitstyp für die [EU-Passport-Nummer](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="302ae-1925">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="302ae-1926">EU-sozialVersicherungsNummer oder entsprechende ID</span><span class="sxs-lookup"><span data-stu-id="302ae-1926">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="302ae-1927">Weitere Informationen finden Sie unter [EU-Sozialversicherungsnummer oder entsprechende ID-vertraulicher Informationstyp](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="302ae-1927">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="302ae-1928">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1928">EU Tax Identification Number</span></span>

<span data-ttu-id="302ae-1929">Weitere Informationen finden Sie unter Sicherheitstyp für die [EU-Steuernummer](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="302ae-1929">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="302ae-1930">Finland National ID (Finnischer Personalausweis)</span><span class="sxs-lookup"><span data-stu-id="302ae-1930">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1931">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1931">Format</span></span>

<span data-ttu-id="302ae-1932">Sechs Ziffern plus ein Zeichen, das ein Jahrhundert angibt, plus drei Ziffern plus einer Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-1932">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1933">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1933">Pattern</span></span>

<span data-ttu-id="302ae-1934">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="302ae-1934">Pattern must include all of the following:</span></span>
- <span data-ttu-id="302ae-1935">Sechs Ziffern im Format TTMMJJ, die ein Geburtsdatum darstellen</span><span class="sxs-lookup"><span data-stu-id="302ae-1935">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="302ae-1936">Jahrhundertkennzeichnung (entweder „-“, „+“ oder „a“)</span><span class="sxs-lookup"><span data-stu-id="302ae-1936">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="302ae-1937">Dreistellige persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1937">Three-digit personal identification number</span></span> 
- <span data-ttu-id="302ae-1938">Eine Ziffer oder ein Buchstabe (Groß-/Kleinschreibung irrelevant), die bzw. der eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="302ae-1938">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1939">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1939">Checksum</span></span>

<span data-ttu-id="302ae-1940">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-1940">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1941">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1941">Definition</span></span>

<span data-ttu-id="302ae-1942">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1942">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1943">Die Funktion Func_finnish_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1943">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1944">Ein Schlüsselwort aus Keyword_finnish_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1944">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="302ae-1945">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-1945">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-1946">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1946">Keywords</span></span>

- <span data-ttu-id="302ae-1947">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="302ae-1947">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="302ae-1948">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="302ae-1948">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="302ae-1949">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="302ae-1949">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="302ae-1950">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="302ae-1950">Personbeteckning</span></span>
- <span data-ttu-id="302ae-1951">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="302ae-1951">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="302ae-1952">Finnland – Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1952">Finland Passport Number</span></span>

<span data-ttu-id="302ae-1953">Format-Kombination aus neun Buchstaben und Ziffern Muster Kombination aus neun Buchstaben und Ziffern: zwei Buchstaben (ohne Berücksichtigung von Groß-/Kleinschreibung) siebenstellige prüfSumme keine Definition eine DLP-Richtlinie ist 75% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn innerhalb eines Nähe von 300 Zeichen: der reguläre Ausdruck Regex_finland_passport_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1953">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="302ae-1954">Ein Schlüsselwort aus Keyword_finland_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1954">A keyword from Keyword_finland_passport_number is found.</span></span>
<span data-ttu-id="302ae-1955"><!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="302ae-1955"></span></span>
<span data-ttu-id="302ae-1956">Schlüsselwörter Keyword_finland_passport_number Passport Passi</span><span class="sxs-lookup"><span data-stu-id="302ae-1956">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="302ae-1957">Französische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1957">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1958">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1958">Format</span></span>

<span data-ttu-id="302ae-1959">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1959">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1960">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1960">Pattern</span></span>

<span data-ttu-id="302ae-1961">12 Ziffern mit Validierung, um ähnliche Muster ( z. B. französische Telefonnummern) auszuschließen</span><span class="sxs-lookup"><span data-stu-id="302ae-1961">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1962">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1962">Checksum</span></span>

<span data-ttu-id="302ae-1963">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-1963">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1964">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1964">Definition</span></span>

<span data-ttu-id="302ae-1965">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1965">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1966">Die Funktion Func_french_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1966">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-1967">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="302ae-1967">At least one of the following is true:</span></span>
- <span data-ttu-id="302ae-1968">Ein Schlüsselwort aus Keyword_french_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-1968">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="302ae-1969">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="302ae-1969">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-1970">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1970">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="302ae-1971">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="302ae-1971">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="302ae-1972">drivers licence</span><span class="sxs-lookup"><span data-stu-id="302ae-1972">drivers licence</span></span>
- <span data-ttu-id="302ae-1973">drivers license</span><span class="sxs-lookup"><span data-stu-id="302ae-1973">drivers license</span></span>
- <span data-ttu-id="302ae-1974">Führerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-1974">driving licence</span></span>
- <span data-ttu-id="302ae-1975">driving license</span><span class="sxs-lookup"><span data-stu-id="302ae-1975">driving license</span></span>
- <span data-ttu-id="302ae-1976">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="302ae-1976">permis de conduire</span></span>
- <span data-ttu-id="302ae-1977">licence number</span><span class="sxs-lookup"><span data-stu-id="302ae-1977">licence number</span></span>
- <span data-ttu-id="302ae-1978">license number</span><span class="sxs-lookup"><span data-stu-id="302ae-1978">license number</span></span>
- <span data-ttu-id="302ae-1979">licence numbers</span><span class="sxs-lookup"><span data-stu-id="302ae-1979">licence numbers</span></span>
- <span data-ttu-id="302ae-1980">license numbers</span><span class="sxs-lookup"><span data-stu-id="302ae-1980">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="302ae-1981">Französische Carte nationale d'identité (CNI)</span><span class="sxs-lookup"><span data-stu-id="302ae-1981">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1982">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1982">Format</span></span>

<span data-ttu-id="302ae-1983">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1983">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1984">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1984">Pattern</span></span>

<span data-ttu-id="302ae-1985">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1985">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-1986">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-1986">Checksum</span></span>

<span data-ttu-id="302ae-1987">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-1987">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-1988">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-1988">Definition</span></span>

<span data-ttu-id="302ae-1989">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-1989">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-1990">Der reguläre Ausdruck Regex_france_cni findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-1990">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-1991">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-1991">Keywords</span></span>

<span data-ttu-id="302ae-1992">None</span><span class="sxs-lookup"><span data-stu-id="302ae-1992">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="302ae-1993">Französische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-1993">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-1994">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-1994">Format</span></span>

<span data-ttu-id="302ae-1995">Neun Ziffern und Buchstaben</span><span class="sxs-lookup"><span data-stu-id="302ae-1995">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-1996">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-1996">Pattern</span></span>

<span data-ttu-id="302ae-1997">Neun Ziffern und Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="302ae-1997">Nine digits and letters:</span></span>
- <span data-ttu-id="302ae-1998">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-1998">Two digits</span></span> 
- <span data-ttu-id="302ae-1999">Zwei Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="302ae-1999">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="302ae-2000">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2000">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2001">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2001">Checksum</span></span>

<span data-ttu-id="302ae-2002">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2002">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2003">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2003">Definition</span></span>

<span data-ttu-id="302ae-2004">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2005">Die Funktion Func_fr_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2005">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2006">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2006">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2007">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2007">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="302ae-2008">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="302ae-2008">Keyword_passport</span></span>

- <span data-ttu-id="302ae-2009">Passport Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2009">Passport Number</span></span>
- <span data-ttu-id="302ae-2010">Passport No</span><span class="sxs-lookup"><span data-stu-id="302ae-2010">Passport No</span></span>
- <span data-ttu-id="302ae-2011">Passport#</span><span class="sxs-lookup"><span data-stu-id="302ae-2011">Passport #</span></span>
- <span data-ttu-id="302ae-2012">Pass</span><span class="sxs-lookup"><span data-stu-id="302ae-2012">Passport#</span></span>
- <span data-ttu-id="302ae-2013">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="302ae-2013">PassportID</span></span>
- <span data-ttu-id="302ae-2014">Passportno</span><span class="sxs-lookup"><span data-stu-id="302ae-2014">Passportno</span></span>
- <span data-ttu-id="302ae-2015">passportnumber</span><span class="sxs-lookup"><span data-stu-id="302ae-2015">passportnumber</span></span>
- <span data-ttu-id="302ae-2016">パスポート</span><span class="sxs-lookup"><span data-stu-id="302ae-2016">パスポート</span></span>
- <span data-ttu-id="302ae-2017">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2017">パスポート番号</span></span>
- <span data-ttu-id="302ae-2018">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="302ae-2018">パスポートのNum</span></span>
- <span data-ttu-id="302ae-2019">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="302ae-2019">パスポート ＃</span></span> 
- <span data-ttu-id="302ae-2020">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="302ae-2020">Numéro de passeport</span></span>
- <span data-ttu-id="302ae-2021">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="302ae-2021">Passeport n °</span></span>
- <span data-ttu-id="302ae-2022">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="302ae-2022">Passeport Non</span></span>
- <span data-ttu-id="302ae-2023">Passeport#</span><span class="sxs-lookup"><span data-stu-id="302ae-2023">Passeport #</span></span>
- <span data-ttu-id="302ae-2024">Passeport</span><span class="sxs-lookup"><span data-stu-id="302ae-2024">Passeport#</span></span>
- <span data-ttu-id="302ae-2025">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="302ae-2025">PasseportNon</span></span>
- <span data-ttu-id="302ae-2026">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="302ae-2026">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="302ae-2027">Französische Sozialversicherungsnummer (INSEE)</span><span class="sxs-lookup"><span data-stu-id="302ae-2027">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2028">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2028">Format</span></span>

<span data-ttu-id="302ae-2029">15 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2029">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2030">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2030">Pattern</span></span>

<span data-ttu-id="302ae-2031">Muss einem von zwei Mustern entsprechen:</span><span class="sxs-lookup"><span data-stu-id="302ae-2031">Must match one of two patterns:</span></span>
- <span data-ttu-id="302ae-2032">13 Ziffern gefolgt von einem Leerzeichen, gefolgt von zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2032">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="302ae-2033">oder</span><span class="sxs-lookup"><span data-stu-id="302ae-2033">or</span></span>
- <span data-ttu-id="302ae-2034">15 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2034">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2035">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2035">Checksum</span></span>

<span data-ttu-id="302ae-2036">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2036">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2037">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2037">Definition</span></span>

<span data-ttu-id="302ae-2038">Eine DLP-Richtlinie ist zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2038">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2039">Die Funktion Func_french_insee oder Func_fr_insee sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2039">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2040">Ein Schlüsselwort aus Keyword_fr_insee wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2040">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="302ae-2041">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2041">The checksum passes.</span></span>

<span data-ttu-id="302ae-2042">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2042">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2043">Die Funktion Func_french_insee oder Func_fr_insee sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2043">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2044">Es wurde kein Schlüsselwort aus Keyword_fr_insee gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2044">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="302ae-2045">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2045">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2046">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2046">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="302ae-2047">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="302ae-2047">Keyword_fr_insee</span></span>

- <span data-ttu-id="302ae-2048">INSEE</span><span class="sxs-lookup"><span data-stu-id="302ae-2048">insee</span></span>
- <span data-ttu-id="302ae-2049">securité sociale</span><span class="sxs-lookup"><span data-stu-id="302ae-2049">securité sociale</span></span>
- <span data-ttu-id="302ae-2050">securite sociale</span><span class="sxs-lookup"><span data-stu-id="302ae-2050">securite sociale</span></span>
- <span data-ttu-id="302ae-2051">national id</span><span class="sxs-lookup"><span data-stu-id="302ae-2051">national id</span></span>
- <span data-ttu-id="302ae-2052">national identification</span><span class="sxs-lookup"><span data-stu-id="302ae-2052">national identification</span></span>
- <span data-ttu-id="302ae-2053">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="302ae-2053">numéro d'identité</span></span>
- <span data-ttu-id="302ae-2054">no d'identité</span><span class="sxs-lookup"><span data-stu-id="302ae-2054">no d'identité</span></span>
- <span data-ttu-id="302ae-2055">Nein.</span><span class="sxs-lookup"><span data-stu-id="302ae-2055">no.</span></span> <span data-ttu-id="302ae-2056">d ' identité</span><span class="sxs-lookup"><span data-stu-id="302ae-2056">d'identité</span></span>
- <span data-ttu-id="302ae-2057">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="302ae-2057">numero d'identite</span></span>
- <span data-ttu-id="302ae-2058">no d'identite</span><span class="sxs-lookup"><span data-stu-id="302ae-2058">no d'identite</span></span>
- <span data-ttu-id="302ae-2059">Nein.</span><span class="sxs-lookup"><span data-stu-id="302ae-2059">no.</span></span> <span data-ttu-id="302ae-2060">d'identite</span><span class="sxs-lookup"><span data-stu-id="302ae-2060">d'identite</span></span>
- <span data-ttu-id="302ae-2061">social security number</span><span class="sxs-lookup"><span data-stu-id="302ae-2061">social security number</span></span>
- <span data-ttu-id="302ae-2062">social security code</span><span class="sxs-lookup"><span data-stu-id="302ae-2062">social security code</span></span>
- <span data-ttu-id="302ae-2063">social insurance number</span><span class="sxs-lookup"><span data-stu-id="302ae-2063">social insurance number</span></span>
- <span data-ttu-id="302ae-2064">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="302ae-2064">le numéro d'identification nationale</span></span>
- <span data-ttu-id="302ae-2065">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="302ae-2065">d'identité nationale</span></span>
- <span data-ttu-id="302ae-2066">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="302ae-2066">numéro de sécurité sociale</span></span>
- <span data-ttu-id="302ae-2067">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="302ae-2067">le code de la sécurité sociale</span></span>
- <span data-ttu-id="302ae-2068">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="302ae-2068">numéro d'assurance sociale</span></span>
- <span data-ttu-id="302ae-2069">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="302ae-2069">numéro de sécu</span></span>
- <span data-ttu-id="302ae-2070">code sécu</span><span class="sxs-lookup"><span data-stu-id="302ae-2070">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="302ae-2071">Deutsche Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2071">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2072">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2072">Format</span></span>

<span data-ttu-id="302ae-2073">Kombination von 11 Ziffern und Buchstaben</span><span class="sxs-lookup"><span data-stu-id="302ae-2073">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2074">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2074">Pattern</span></span>

<span data-ttu-id="302ae-2075">11 Zahlen und Buchstaben (ohne Beachtung der Groß-/Kleinschreibung):</span><span class="sxs-lookup"><span data-stu-id="302ae-2075">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="302ae-2076">Eine Ziffer oder ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="302ae-2076">A digit or letter</span></span> 
- <span data-ttu-id="302ae-2077">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2077">Two digits</span></span> 
- <span data-ttu-id="302ae-2078">Sechs Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="302ae-2078">Six digits or letters</span></span> 
- <span data-ttu-id="302ae-2079">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-2079">A digit</span></span> 
- <span data-ttu-id="302ae-2080">Eine Ziffer oder ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="302ae-2080">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2081">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2081">Checksum</span></span>

<span data-ttu-id="302ae-2082">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2083">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2083">Definition</span></span>

<span data-ttu-id="302ae-2084">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2084">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2085">Die Funktion Func_german_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2085">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2086">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="302ae-2086">At least one of the following is true:</span></span>
    - <span data-ttu-id="302ae-2087">Ein Schlüsselwort aus Keyword_german_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2087">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="302ae-2088">Ein Schlüsselwort aus Keyword_german_drivers_license_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2088">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="302ae-2089">Ein Schlüsselwort aus Keyword_german_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2089">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="302ae-2090">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2090">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2091">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2091">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="302ae-2092">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2092">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="302ae-2093">Führerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2093">Führerschein</span></span>
- <span data-ttu-id="302ae-2094">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2094">Fuhrerschein</span></span>
- <span data-ttu-id="302ae-2095">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2095">Fuehrerschein</span></span>
- <span data-ttu-id="302ae-2096">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2096">Führerscheinnummer</span></span>
- <span data-ttu-id="302ae-2097">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2097">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="302ae-2098">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2098">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="302ae-2099">Führerschein-</span><span class="sxs-lookup"><span data-stu-id="302ae-2099">Führerschein-</span></span> 
- <span data-ttu-id="302ae-2100">Fuhrerschein-</span><span class="sxs-lookup"><span data-stu-id="302ae-2100">Fuhrerschein-</span></span> 
- <span data-ttu-id="302ae-2101">Fuehrerschein-</span><span class="sxs-lookup"><span data-stu-id="302ae-2101">Fuehrerschein-</span></span> 
- <span data-ttu-id="302ae-2102">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="302ae-2102">FührerscheinnummerNr</span></span>
- <span data-ttu-id="302ae-2103">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="302ae-2103">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="302ae-2104">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="302ae-2104">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="302ae-2105">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2105">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="302ae-2106">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2106">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="302ae-2107">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2107">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="302ae-2108">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="302ae-2108">Führerschein- Nr</span></span>
- <span data-ttu-id="302ae-2109">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="302ae-2109">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="302ae-2110">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="302ae-2110">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="302ae-2111">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2111">Führerschein- Klasse</span></span> 
- <span data-ttu-id="302ae-2112">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2112">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="302ae-2113">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2113">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="302ae-2114">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="302ae-2114">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="302ae-2115">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="302ae-2115">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="302ae-2116">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="302ae-2116">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="302ae-2117">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2117">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="302ae-2118">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2118">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="302ae-2119">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2119">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="302ae-2120">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="302ae-2120">Führerschein- Nr</span></span> 
- <span data-ttu-id="302ae-2121">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="302ae-2121">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="302ae-2122">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="302ae-2122">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="302ae-2123">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2123">Führerschein- Klasse</span></span> 
- <span data-ttu-id="302ae-2124">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2124">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="302ae-2125">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2125">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="302ae-2126">DL</span><span class="sxs-lookup"><span data-stu-id="302ae-2126">DL</span></span> 
- <span data-ttu-id="302ae-2127">DLS</span><span class="sxs-lookup"><span data-stu-id="302ae-2127">DLS</span></span>
- <span data-ttu-id="302ae-2128">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-2128">Driv Lic</span></span> 
- <span data-ttu-id="302ae-2129">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="302ae-2129">Driv Licen</span></span> 
- <span data-ttu-id="302ae-2130">Driv License</span><span class="sxs-lookup"><span data-stu-id="302ae-2130">Driv License</span></span>
- <span data-ttu-id="302ae-2131">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-2131">Driv Licenses</span></span> 
- <span data-ttu-id="302ae-2132">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-2132">Driv Licence</span></span> 
- <span data-ttu-id="302ae-2133">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-2133">Driv Licences</span></span> 
- <span data-ttu-id="302ae-2134">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-2134">Driv Lic</span></span> 
- <span data-ttu-id="302ae-2135">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="302ae-2135">Driver Licen</span></span> 
- <span data-ttu-id="302ae-2136">Driver License</span><span class="sxs-lookup"><span data-stu-id="302ae-2136">Driver License</span></span> 
- <span data-ttu-id="302ae-2137">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-2137">Driver Licenses</span></span> 
- <span data-ttu-id="302ae-2138">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-2138">Driver Licence</span></span> 
- <span data-ttu-id="302ae-2139">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-2139">Driver Licences</span></span> 
- <span data-ttu-id="302ae-2140">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-2140">Drivers Lic</span></span> 
- <span data-ttu-id="302ae-2141">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="302ae-2141">Drivers Licen</span></span> 
- <span data-ttu-id="302ae-2142">Drivers License</span><span class="sxs-lookup"><span data-stu-id="302ae-2142">Drivers License</span></span> 
- <span data-ttu-id="302ae-2143">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-2143">Drivers Licenses</span></span> 
- <span data-ttu-id="302ae-2144">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-2144">Drivers Licence</span></span> 
- <span data-ttu-id="302ae-2145">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-2145">Drivers Licences</span></span> 
- <span data-ttu-id="302ae-2146">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-2146">Driver's Lic</span></span> 
- <span data-ttu-id="302ae-2147">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="302ae-2147">Driver's Licen</span></span> 
- <span data-ttu-id="302ae-2148">Driver's License</span><span class="sxs-lookup"><span data-stu-id="302ae-2148">Driver's License</span></span> 
- <span data-ttu-id="302ae-2149">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-2149">Driver's Licenses</span></span> 
- <span data-ttu-id="302ae-2150">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-2150">Driver's Licence</span></span> 
- <span data-ttu-id="302ae-2151">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-2151">Driver's Licences</span></span> 
- <span data-ttu-id="302ae-2152">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-2152">Driving Lic</span></span> 
- <span data-ttu-id="302ae-2153">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="302ae-2153">Driving Licen</span></span> 
- <span data-ttu-id="302ae-2154">Driving License</span><span class="sxs-lookup"><span data-stu-id="302ae-2154">Driving License</span></span> 
- <span data-ttu-id="302ae-2155">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-2155">Driving Licenses</span></span> 
- <span data-ttu-id="302ae-2156">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="302ae-2156">Driving Licence</span></span> 
- <span data-ttu-id="302ae-2157">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="302ae-2157">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="302ae-2158">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="302ae-2158">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="302ae-2159">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2159">Nr-Führerschein</span></span> 
- <span data-ttu-id="302ae-2160">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2160">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="302ae-2161">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2161">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="302ae-2162">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2162">No-Führerschein</span></span> 
- <span data-ttu-id="302ae-2163">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2163">No-Fuhrerschein</span></span> 
- <span data-ttu-id="302ae-2164">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2164">No-Fuehrerschein</span></span> 
- <span data-ttu-id="302ae-2165">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2165">N-Führerschein</span></span> 
- <span data-ttu-id="302ae-2166">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2166">N-Fuhrerschein</span></span> 
- <span data-ttu-id="302ae-2167">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2167">N-Fuehrerschein</span></span>
- <span data-ttu-id="302ae-2168">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2168">Nr-Führerschein</span></span> 
- <span data-ttu-id="302ae-2169">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2169">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="302ae-2170">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2170">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="302ae-2171">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2171">No-Führerschein</span></span> 
- <span data-ttu-id="302ae-2172">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2172">No-Fuhrerschein</span></span> 
- <span data-ttu-id="302ae-2173">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2173">No-Fuehrerschein</span></span> 
- <span data-ttu-id="302ae-2174">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2174">N-Führerschein</span></span> 
- <span data-ttu-id="302ae-2175">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2175">N-Fuhrerschein</span></span> 
- <span data-ttu-id="302ae-2176">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="302ae-2176">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="302ae-2177">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="302ae-2177">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="302ae-2178">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="302ae-2178">ausstellungsdatum</span></span>
- <span data-ttu-id="302ae-2179">Ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="302ae-2179">ausstellungsort</span></span>
- <span data-ttu-id="302ae-2180">Ausstellende Behöde</span><span class="sxs-lookup"><span data-stu-id="302ae-2180">ausstellende behöde</span></span>
- <span data-ttu-id="302ae-2181">Ausstellende Behorde</span><span class="sxs-lookup"><span data-stu-id="302ae-2181">ausstellende behorde</span></span>
- <span data-ttu-id="302ae-2182">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="302ae-2182">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="302ae-2183">Deutsche Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2183">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2184">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2184">Format</span></span>

<span data-ttu-id="302ae-2185">10 Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="302ae-2185">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2186">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2186">Pattern</span></span>

<span data-ttu-id="302ae-2187">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="302ae-2187">Pattern must include all of the following:</span></span>
- <span data-ttu-id="302ae-2188">Das erste Zeichen ist eine Ziffer oder ein Buchstabe aus dieser Gruppe (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="302ae-2188">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="302ae-2189">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2189">Three digits</span></span> 
- <span data-ttu-id="302ae-2190">Fünf Ziffern oder Buchstaben aus dieser Gruppe (C -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="302ae-2190">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="302ae-2191">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-2191">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2192">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2192">Checksum</span></span>

<span data-ttu-id="302ae-2193">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2194">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2194">Definition</span></span>

<span data-ttu-id="302ae-2195">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2196">Die Funktion Func_german_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2196">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2197">Ein Schlüsselwort aus einer der fünf Schlüsselwortlisten wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2197">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="302ae-2198">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2198">The checksum passes.</span></span>

<span data-ttu-id="302ae-2199">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2199">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2200">Die Funktion Func_german_passport_data findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2200">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2201">Ein Schlüsselwort aus einer der fünf Schlüsselwortlisten wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2201">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="302ae-2202">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2202">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2203">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2203">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="302ae-2204">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="302ae-2204">Keyword_german_passport</span></span>

- <span data-ttu-id="302ae-2205">Reisepass</span><span class="sxs-lookup"><span data-stu-id="302ae-2205">reisepass</span></span>
- <span data-ttu-id="302ae-2206">reisepasse</span><span class="sxs-lookup"><span data-stu-id="302ae-2206">reisepasse</span></span>
- <span data-ttu-id="302ae-2207">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2207">reisepassnummer</span></span>
- <span data-ttu-id="302ae-2208">Pass</span><span class="sxs-lookup"><span data-stu-id="302ae-2208">passport</span></span>
- <span data-ttu-id="302ae-2209">Pässe</span><span class="sxs-lookup"><span data-stu-id="302ae-2209">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="302ae-2210">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="302ae-2210">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="302ae-2211">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="302ae-2211">geburtsdatum</span></span>
- <span data-ttu-id="302ae-2212">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="302ae-2212">ausstellungsdatum</span></span>
- <span data-ttu-id="302ae-2213">Ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="302ae-2213">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="302ae-2214">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2214">Keyword_german_passport_number</span></span>

<span data-ttu-id="302ae-2215">No-Reisepass Nr-Reisepass</span><span class="sxs-lookup"><span data-stu-id="302ae-2215">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="302ae-2216">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="302ae-2216">Keyword_german_passport1</span></span>

<span data-ttu-id="302ae-2217">Reisepass-Nr</span><span class="sxs-lookup"><span data-stu-id="302ae-2217">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="302ae-2218">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="302ae-2218">Keyword_german_passport2</span></span>

<span data-ttu-id="302ae-2219">bnationalit. t</span><span class="sxs-lookup"><span data-stu-id="302ae-2219">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="302ae-2220">Deutsche Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2220">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2221">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2221">Format</span></span>

<span data-ttu-id="302ae-2222">Seit dem 1. November 2010: neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2222">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="302ae-2223">Vom 1. April 1987 bis 31. Oktober 2010:10 Stellen</span><span class="sxs-lookup"><span data-stu-id="302ae-2223">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2224">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2224">Pattern</span></span>

<span data-ttu-id="302ae-2225">Seit 1. November 2010:</span><span class="sxs-lookup"><span data-stu-id="302ae-2225">Since 1 November 2010:</span></span>
- <span data-ttu-id="302ae-2226">Ein Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="302ae-2226">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="302ae-2227">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2227">Eight digits</span></span>

<span data-ttu-id="302ae-2228">Vom 1. April 1987 bis 31. Oktober 2010:</span><span class="sxs-lookup"><span data-stu-id="302ae-2228">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="302ae-2229">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2229">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2230">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2230">Checksum</span></span>

<span data-ttu-id="302ae-2231">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2231">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2232">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2232">Definition</span></span>

<span data-ttu-id="302ae-2233">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2233">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2234">Der reguläre Ausdruck Regex_germany_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2234">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2235">Ein Schlüsselwort aus Keyword_germany_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2235">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2236">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2236">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="302ae-2237">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="302ae-2237">Keyword_germany_id_card</span></span>

- <span data-ttu-id="302ae-2238">Identity Card</span><span class="sxs-lookup"><span data-stu-id="302ae-2238">Identity Card</span></span>
- <span data-ttu-id="302ae-2239">ID</span><span class="sxs-lookup"><span data-stu-id="302ae-2239">ID</span></span>
- <span data-ttu-id="302ae-2240">Identifikations</span><span class="sxs-lookup"><span data-stu-id="302ae-2240">Identification</span></span>
- <span data-ttu-id="302ae-2241">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="302ae-2241">Personalausweis</span></span>
- <span data-ttu-id="302ae-2242">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2242">Identifizierungsnummer</span></span>
- <span data-ttu-id="302ae-2243">Ausweis</span><span class="sxs-lookup"><span data-stu-id="302ae-2243">Ausweis</span></span>
- <span data-ttu-id="302ae-2244">Identifikation</span><span class="sxs-lookup"><span data-stu-id="302ae-2244">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="302ae-2245">Griechenland – Personalausweis</span><span class="sxs-lookup"><span data-stu-id="302ae-2245">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2246">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2246">Format</span></span>

<span data-ttu-id="302ae-2247">Kombination von 7-8 Buchstaben und Zahlen plus einem Gedankenstrich</span><span class="sxs-lookup"><span data-stu-id="302ae-2247">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2248">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2248">Pattern</span></span>

<span data-ttu-id="302ae-2249">Sieben Buchstaben und Zahlen (altes Format):</span><span class="sxs-lookup"><span data-stu-id="302ae-2249">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="302ae-2250">Ein Buchstabe (jeder Buchstabe des griechischen Alphabets) </span><span class="sxs-lookup"><span data-stu-id="302ae-2250">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="302ae-2251">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-2251">A dash</span></span> 
- <span data-ttu-id="302ae-2252">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2252">Six digits</span></span>

<span data-ttu-id="302ae-2253">Acht Buchstaben und Zahlen (neues Format):</span><span class="sxs-lookup"><span data-stu-id="302ae-2253">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="302ae-2254">Zwei Buchstaben, deren Großbuchstabe sowohl im griechischen als auch lateinischen Alphabet (ABEZHIKMNOPTYX) vorkommt </span><span class="sxs-lookup"><span data-stu-id="302ae-2254">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="302ae-2255">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-2255">A dash</span></span> 
- <span data-ttu-id="302ae-2256">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2256">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2257">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2257">Checksum</span></span>

<span data-ttu-id="302ae-2258">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2258">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2259">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2259">Definition</span></span>

<span data-ttu-id="302ae-2260">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2260">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2261">Der reguläre Ausdruck Regex_greece_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2261">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2262">Ein Schlüsselwort aus Keyword_greece_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2262">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2263">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2263">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="302ae-2264">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="302ae-2264">Keyword_greece_id_card</span></span>

- <span data-ttu-id="302ae-2265">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="302ae-2265">Greek identity Card</span></span>
- <span data-ttu-id="302ae-2266">Tautotita</span><span class="sxs-lookup"><span data-stu-id="302ae-2266">Tautotita</span></span>
- <span data-ttu-id="302ae-2267">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="302ae-2267">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="302ae-2268">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="302ae-2268">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="302ae-2269">Hongkong (HKID) - Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2269">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2270">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2270">Format</span></span>

<span data-ttu-id="302ae-2271">Kombination aus 8-9Buchstaben und Zahlen sowie optionale Klammern um das letzte Zeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-2271">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2272">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2272">Pattern</span></span>

<span data-ttu-id="302ae-2273">Kombination aus Buchstaben 8-9 Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="302ae-2273">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="302ae-2274">1-2 Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="302ae-2274">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="302ae-2275">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2275">Six digits</span></span> 
- <span data-ttu-id="302ae-2276">Das letzte Zeichen (eine Ziffer oder der Buchstabe A), bei dem es sich um die Prüfziffer handelt, die optional in Klammern eingeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="302ae-2276">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2277">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2277">Checksum</span></span>

<span data-ttu-id="302ae-2278">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2278">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2279">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2279">Definition</span></span>

<span data-ttu-id="302ae-2280">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2281">Die Funktion Func_hong_kong_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2281">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2282">Ein Schlüsselwort aus Keyword_hong_kong_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2282">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="302ae-2283">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2283">The checksum passes.</span></span>

<span data-ttu-id="302ae-2284">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2284">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2285">Die Funktion Func_hong_kong_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2285">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2286">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2286">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2287">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2287">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="302ae-2288">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="302ae-2288">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="302ae-2289">Hongkong-Identitätskarte</span><span class="sxs-lookup"><span data-stu-id="302ae-2289">hong kong identity card</span></span>
- <span data-ttu-id="302ae-2290">HKIDC</span><span class="sxs-lookup"><span data-stu-id="302ae-2290">HKIDC</span></span>
- <span data-ttu-id="302ae-2291">id card</span><span class="sxs-lookup"><span data-stu-id="302ae-2291">id card</span></span>
- <span data-ttu-id="302ae-2292">identity card</span><span class="sxs-lookup"><span data-stu-id="302ae-2292">identity card</span></span>
- <span data-ttu-id="302ae-2293">HK-Identitätskarte</span><span class="sxs-lookup"><span data-stu-id="302ae-2293">hk identity card</span></span>
- <span data-ttu-id="302ae-2294">Hongkong-ID</span><span class="sxs-lookup"><span data-stu-id="302ae-2294">hong kong id</span></span>
- <span data-ttu-id="302ae-2295">香港身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-2295">香港身份證</span></span>
- <span data-ttu-id="302ae-2296">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-2296">香港永久性居民身份證</span></span>
- <span data-ttu-id="302ae-2297">身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-2297">身份證</span></span>
- <span data-ttu-id="302ae-2298">身份証</span><span class="sxs-lookup"><span data-stu-id="302ae-2298">身份証</span></span>
- <span data-ttu-id="302ae-2299">身分證</span><span class="sxs-lookup"><span data-stu-id="302ae-2299">身分證</span></span>
- <span data-ttu-id="302ae-2300">身分証</span><span class="sxs-lookup"><span data-stu-id="302ae-2300">身分証</span></span>
- <span data-ttu-id="302ae-2301">香港身份証</span><span class="sxs-lookup"><span data-stu-id="302ae-2301">香港身份証</span></span>
- <span data-ttu-id="302ae-2302">香港身分證</span><span class="sxs-lookup"><span data-stu-id="302ae-2302">香港身分證</span></span>
- <span data-ttu-id="302ae-2303">香港身分証</span><span class="sxs-lookup"><span data-stu-id="302ae-2303">香港身分証</span></span>
- <span data-ttu-id="302ae-2304">香港身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-2304">香港身份證</span></span>
- <span data-ttu-id="302ae-2305">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-2305">香港居民身份證</span></span>
- <span data-ttu-id="302ae-2306">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="302ae-2306">香港居民身份証</span></span>
- <span data-ttu-id="302ae-2307">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="302ae-2307">香港居民身分證</span></span>
- <span data-ttu-id="302ae-2308">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="302ae-2308">香港居民身分証</span></span>
- <span data-ttu-id="302ae-2309">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="302ae-2309">香港永久性居民身份証</span></span>
- <span data-ttu-id="302ae-2310">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="302ae-2310">香港永久性居民身分證</span></span>
- <span data-ttu-id="302ae-2311">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="302ae-2311">香港永久性居民身分証</span></span>
- <span data-ttu-id="302ae-2312">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-2312">香港永久性居民身份證</span></span>
- <span data-ttu-id="302ae-2313">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-2313">香港非永久性居民身份證</span></span>
- <span data-ttu-id="302ae-2314">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="302ae-2314">香港非永久性居民身份証</span></span>
- <span data-ttu-id="302ae-2315">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="302ae-2315">香港非永久性居民身分證</span></span>
- <span data-ttu-id="302ae-2316">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="302ae-2316">香港非永久性居民身分証</span></span>
- <span data-ttu-id="302ae-2317">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-2317">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="302ae-2318">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="302ae-2318">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="302ae-2319">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="302ae-2319">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="302ae-2320">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="302ae-2320">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="302ae-2321">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-2321">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="302ae-2322">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="302ae-2322">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="302ae-2323">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="302ae-2323">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="302ae-2324">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="302ae-2324">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="302ae-2325">Indien – Permanente Kontonummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2325">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2326">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2326">Format</span></span>

<span data-ttu-id="302ae-2327">10 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2327">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2328">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2328">Pattern</span></span>

<span data-ttu-id="302ae-2329">10 Buchstaben oder Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-2329">10 letters or digits:</span></span>
- <span data-ttu-id="302ae-2330">Fünf Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="302ae-2330">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="302ae-2331">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2331">Four digits</span></span> 
- <span data-ttu-id="302ae-2332">Ein Buchstabe, der eine alphabetische Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="302ae-2332">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2333">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2333">Checksum</span></span>

<span data-ttu-id="302ae-2334">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2334">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2335">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2335">Definition</span></span>

<span data-ttu-id="302ae-2336">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2336">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2337">Der reguläre Ausdruck Regex_india_permanent_account_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2337">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2338">Ein Schlüsselwort aus Keyword_india_permanent_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2338">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="302ae-2339">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2339">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2340">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2340">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="302ae-2341">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2341">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="302ae-2342">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2342">Permanent Account Number</span></span> 
- <span data-ttu-id="302ae-2343">SCHWENKEN</span><span class="sxs-lookup"><span data-stu-id="302ae-2343">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="302ae-2344">Indien - Eindeutige Identifikationsnummer (Aadhaar)</span><span class="sxs-lookup"><span data-stu-id="302ae-2344">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2345">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2345">Format</span></span>

<span data-ttu-id="302ae-2346">12 Ziffern mit optionalen Leerzeichen oder Bindestrichen</span><span class="sxs-lookup"><span data-stu-id="302ae-2346">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2347">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2347">Pattern</span></span>

<span data-ttu-id="302ae-2348">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-2348">12 digits:</span></span>
- <span data-ttu-id="302ae-2349">Vier Ziffern </span><span class="sxs-lookup"><span data-stu-id="302ae-2349">Four digits</span></span> 
- <span data-ttu-id="302ae-2350">Eine optionales Leerzeichen oder ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-2350">An optional space or dash</span></span> 
- <span data-ttu-id="302ae-2351">Vier Ziffern </span><span class="sxs-lookup"><span data-stu-id="302ae-2351">Four digits</span></span> 
- <span data-ttu-id="302ae-2352">Eine optionales Leerzeichen oder ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-2352">An optional space or dash</span></span> 
- <span data-ttu-id="302ae-2353">Die letzte Ziffer, die eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="302ae-2353">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2354">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2354">Checksum</span></span>

<span data-ttu-id="302ae-2355">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2355">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2356">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2356">Definition</span></span>

<span data-ttu-id="302ae-2357">Eine DLP-Richtlinie ist 85% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: die Funktion Func_india_aadhaar findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2357">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="302ae-2358">Ein Schlüsselwort aus Keyword_india_aadhar wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2358">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="302ae-2359">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2359">The checksum passes.</span></span>
<span data-ttu-id="302ae-2360">Eine DLP-Richtlinie ist 75% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: die Funktion Func_india_aadhaar findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="302ae-2361">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2361">The checksum passes.</span></span>
<span data-ttu-id="302ae-2362"><!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="302ae-2362"></span></span>

### <a name="keywords"></a><span data-ttu-id="302ae-2363">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2363">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="302ae-2364">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="302ae-2364">Keyword_india_aadhar</span></span>
- <span data-ttu-id="302ae-2365">Aadhar</span><span class="sxs-lookup"><span data-stu-id="302ae-2365">Aadhar</span></span>
- <span data-ttu-id="302ae-2366">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="302ae-2366">Aadhaar</span></span>
- <span data-ttu-id="302ae-2367">UID</span><span class="sxs-lookup"><span data-stu-id="302ae-2367">UID</span></span>
- <span data-ttu-id="302ae-2368">आधार</span><span class="sxs-lookup"><span data-stu-id="302ae-2368">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="302ae-2369">Indonesien – Perosonalausweisnummer (KTP)</span><span class="sxs-lookup"><span data-stu-id="302ae-2369">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2370">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2370">Format</span></span>

<span data-ttu-id="302ae-2371">16 Ziffern mit optionalen Punkten</span><span class="sxs-lookup"><span data-stu-id="302ae-2371">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2372">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2372">Pattern</span></span>

<span data-ttu-id="302ae-2373">16 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-2373">16 digits:</span></span>
- <span data-ttu-id="302ae-2374">Zweistelliger Provinzcode </span><span class="sxs-lookup"><span data-stu-id="302ae-2374">Two-digit province code</span></span> 
- <span data-ttu-id="302ae-2375">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="302ae-2375">A period (optional)</span></span> 
- <span data-ttu-id="302ae-2376">Zweistelliger Regency- oder Stadtcode </span><span class="sxs-lookup"><span data-stu-id="302ae-2376">Two-digit regency or city code</span></span> 
- <span data-ttu-id="302ae-2377">Zweistelliger Subdistrict-Code </span><span class="sxs-lookup"><span data-stu-id="302ae-2377">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="302ae-2378">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="302ae-2378">A period (optional)</span></span> 
- <span data-ttu-id="302ae-2379">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="302ae-2379">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="302ae-2380">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="302ae-2380">A period (optional)</span></span> 
- <span data-ttu-id="302ae-2381">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2381">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2382">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2382">Checksum</span></span>

<span data-ttu-id="302ae-2383">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2383">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2384">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2384">Definition</span></span>

<span data-ttu-id="302ae-2385">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2386">Der reguläre Ausdruck Regex_indonesia_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2386">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2387">Ein Schlüsselwort aus Keyword_indonesia_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2387">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="302ae-2388">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2388">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2389">Der reguläre Ausdruck Regex_indonesia_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2389">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2390">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2390">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="302ae-2391">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="302ae-2391">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="302ae-2392">KTP</span><span class="sxs-lookup"><span data-stu-id="302ae-2392">KTP</span></span>
- <span data-ttu-id="302ae-2393">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="302ae-2393">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="302ae-2394">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="302ae-2394">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="302ae-2395">International Banking Account Number (IBAN)</span><span class="sxs-lookup"><span data-stu-id="302ae-2395">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2396">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2396">Format</span></span>

<span data-ttu-id="302ae-2397">Ländercode (zwei Buchstaben) plus Prüfziffern (zwei Ziffern) plus BBAN-Nummer (bis zu 30 Zeichen)</span><span class="sxs-lookup"><span data-stu-id="302ae-2397">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2398">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2398">Pattern</span></span>

<span data-ttu-id="302ae-2399">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="302ae-2399">Pattern must include all of the following:</span></span>

- <span data-ttu-id="302ae-2400">Ländercode aus zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="302ae-2400">Two-letter country code</span></span>
- <span data-ttu-id="302ae-2401">Zwei Prüfziffern (gefolgt von einem optionalen Leerzeichen)</span><span class="sxs-lookup"><span data-stu-id="302ae-2401">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="302ae-2402">1-7 Gruppen von vier Buchstaben oder Ziffern (können durch Leerzeichengetrennt werden)</span><span class="sxs-lookup"><span data-stu-id="302ae-2402">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="302ae-2403">1 bis 3 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2403">1-3 letters or digits</span></span>

<span data-ttu-id="302ae-2404">Das Format für jedes Land ist geringfügig unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="302ae-2404">The format for each country is slightly different.</span></span> <span data-ttu-id="302ae-2405">Der Typ der vertraulichen IBAN-Informationen umfasst diese 60 Länder:</span><span class="sxs-lookup"><span data-stu-id="302ae-2405">The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="302ae-2406">AD, AE, Al, at, AZ, BA, be, BG, BH, ch, CR, CY, CZ, de, DK, Do, EE, es, fi, FO, Fr, GB, ge, GI, GL, GR, HR, HU, IE, IL, is, IT, kW, KZ, LB, Li, LU , NL, No, PL, PT, RO, RS, Sa, SE, Si, SK, SM, TN, TR, VG</span><span class="sxs-lookup"><span data-stu-id="302ae-2406">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2407">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2407">Checksum</span></span>

<span data-ttu-id="302ae-2408">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2408">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2409">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2409">Definition</span></span>

<span data-ttu-id="302ae-2410">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2410">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2411">Die Funktion Func_iban findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2411">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2412">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2412">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2413">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2413">Keywords</span></span>

<span data-ttu-id="302ae-2414">None</span><span class="sxs-lookup"><span data-stu-id="302ae-2414">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="302ae-2415">IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="302ae-2415">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2416">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2416">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="302ae-2417">IPv4</span><span class="sxs-lookup"><span data-stu-id="302ae-2417">IPv4:</span></span>
<span data-ttu-id="302ae-2418">Komplexes Muster, das formatierte (Punkte) und unformatierte (keine Punkte) Versionen der IPv4-Adressen angibt</span><span class="sxs-lookup"><span data-stu-id="302ae-2418">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="302ae-2419">IPv6</span><span class="sxs-lookup"><span data-stu-id="302ae-2419">IPv6:</span></span>
<span data-ttu-id="302ae-2420"> Komplexes Muster, das formatierte IPv6-Nummern angibt (schließt Doppelpunkte ein)</span><span class="sxs-lookup"><span data-stu-id="302ae-2420">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2421">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2421">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2422">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2422">Checksum</span></span>

<span data-ttu-id="302ae-2423">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2423">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2424">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2424">Definition</span></span>

<span data-ttu-id="302ae-2425">Für IPv6 ist eine DLP-Richtlinie zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2425">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2426">Der reguläre Ausdruck Regex_ipv6_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2426">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2427">Es wurde kein Schlüsselwort aus Keyword_ipaddress gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2427">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="302ae-2428">Für IPv4 ist eine DLP-Richtlinie zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2428">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2429">Der reguläre Ausdruck Regex_ipv4_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2429">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2430">Ein Schlüsselwort aus Keyword_ipaddress wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2430">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="302ae-2431">Für IPv6 ist eine DLP-Richtlinie zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2431">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2432">Der reguläre Ausdruck Regex_ipv6_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2432">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2433">Es wurde kein Schlüsselwort aus Keyword_ipaddress gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2433">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2434">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2434">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="302ae-2435">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="302ae-2435">Keyword_ipaddress</span></span>

- <span data-ttu-id="302ae-2436">IP (bei diesem Schlüsselwort wird die Groß-/Kleinschreibung unterschieden)</span><span class="sxs-lookup"><span data-stu-id="302ae-2436">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="302ae-2437">ip address</span><span class="sxs-lookup"><span data-stu-id="302ae-2437">ip address</span></span> 
- <span data-ttu-id="302ae-2438">IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="302ae-2438">ip addresses</span></span>
- <span data-ttu-id="302ae-2439">internet protocol</span><span class="sxs-lookup"><span data-stu-id="302ae-2439">internet protocol</span></span>
- <span data-ttu-id="302ae-2440">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="302ae-2440">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="302ae-2441">Internationale Klassifikation von Krankheiten (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="302ae-2441">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2442">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2442">Format</span></span>

<span data-ttu-id="302ae-2443">Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="302ae-2443">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2444">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2444">Pattern</span></span>

<span data-ttu-id="302ae-2445">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="302ae-2445">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2446">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2446">Checksum</span></span>

<span data-ttu-id="302ae-2447">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2447">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2448">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2448">Definition</span></span>

<span data-ttu-id="302ae-2449">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2449">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2450">Ein Schlüsselwort aus Dictionary_icd_10_cm wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2450">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="302ae-2451">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2451">Keywords</span></span>

<span data-ttu-id="302ae-2452">Ein beliebiger Begriff aus dem Dictionary_icd_10_cm-Stichwort Wörterbuch, das auf der [internationalen Klassifikation der Krankheiten, der zehnTen Revision, der klinischen Modifikation (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604)basiert.</span><span class="sxs-lookup"><span data-stu-id="302ae-2452">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="302ae-2453">Dieser Typ sucht nur nach dem Begriff, nicht nach den Versicherungs Codes.</span><span class="sxs-lookup"><span data-stu-id="302ae-2453">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="302ae-2454">Internationale Klassifikation von Krankheiten (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="302ae-2454">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2455">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2455">Format</span></span>

<span data-ttu-id="302ae-2456">Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="302ae-2456">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2457">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2457">Pattern</span></span>

<span data-ttu-id="302ae-2458">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="302ae-2458">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2459">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2459">Checksum</span></span>

<span data-ttu-id="302ae-2460">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2460">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2461">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2461">Definition</span></span>

<span data-ttu-id="302ae-2462">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2462">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2463">Ein Schlüsselwort aus Dictionary_icd_9_cm wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2463">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2464">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2464">Keywords</span></span>

<span data-ttu-id="302ae-2465">Ein beliebiger Begriff aus dem Dictionary_icd_9_cm-Stichwort Wörterbuch, das auf der [internationalen Klassifikation der Krankheiten, der neunTen Revision, der klinischen Modifikation (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605)basiert.</span><span class="sxs-lookup"><span data-stu-id="302ae-2465">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="302ae-2466">Dieser Typ sucht nur nach dem Begriff, nicht nach den Versicherungs Codes.</span><span class="sxs-lookup"><span data-stu-id="302ae-2466">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="302ae-2467">Irland – Personal Public Service-Nummer (PPS)</span><span class="sxs-lookup"><span data-stu-id="302ae-2467">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2468">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2468">Format</span></span>

<span data-ttu-id="302ae-2469">Altes Format (bis 31. Dez 2012):</span><span class="sxs-lookup"><span data-stu-id="302ae-2469">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="302ae-2470">Sieben Ziffern, gefolgt von 1-2 Buchstaben </span><span class="sxs-lookup"><span data-stu-id="302ae-2470">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="302ae-2471">Neues Format (1 Jan 2013 und nachher):</span><span class="sxs-lookup"><span data-stu-id="302ae-2471">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="302ae-2472">Sieben Ziffern, gefolgt von zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="302ae-2472">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2473">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2473">Pattern</span></span>

<span data-ttu-id="302ae-2474">Altes Format (bis 31. Dez 2012):</span><span class="sxs-lookup"><span data-stu-id="302ae-2474">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="302ae-2475">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="302ae-2475">Seven digits</span></span> 
- <span data-ttu-id="302ae-2476">1-2 Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="302ae-2476">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="302ae-2477">Neues Format (1 Jan 2013 und nachher):</span><span class="sxs-lookup"><span data-stu-id="302ae-2477">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="302ae-2478">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="302ae-2478">Seven digits</span></span> 
- <span data-ttu-id="302ae-2479">Ein Buchstabe (Groß-/Kleinschreibung irrelevant), wobei es sich um eine alphabetische Prüfziffer handelt </span><span class="sxs-lookup"><span data-stu-id="302ae-2479">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="302ae-2480">Die Buchstaben "A" oder "H" (Groß-/Kleinschreibung irrelevant)</span><span class="sxs-lookup"><span data-stu-id="302ae-2480">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2481">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2481">Checksum</span></span>

<span data-ttu-id="302ae-2482">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2482">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2483">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2483">Definition</span></span>

<span data-ttu-id="302ae-2484">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2484">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2485">Die Funktion Func_ireland_pps sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2485">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2486">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="302ae-2486">One of the following is true:</span></span>
    - <span data-ttu-id="302ae-2487">Ein Schlüsselwort aus Keyword_ireland_pps wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2487">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="302ae-2488">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="302ae-2488">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="302ae-2489">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2489">The checksum passes.</span></span>

<span data-ttu-id="302ae-2490">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2490">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2491">Die Funktion Func_ireland_pps sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2491">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2492">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2492">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2493">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2493">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="302ae-2494">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="302ae-2494">Keyword_ireland_pps</span></span>

- <span data-ttu-id="302ae-2495">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2495">Personal Public Service Number</span></span> 
- <span data-ttu-id="302ae-2496">PPS Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2496">PPS Number</span></span> 
- <span data-ttu-id="302ae-2497">PPS Num</span><span class="sxs-lookup"><span data-stu-id="302ae-2497">PPS Num</span></span> 
- <span data-ttu-id="302ae-2498">PPS No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2498">PPS No.</span></span> 
- <span data-ttu-id="302ae-2499">PPS #</span><span class="sxs-lookup"><span data-stu-id="302ae-2499">PPS #</span></span> 
- <span data-ttu-id="302ae-2500">PPS</span><span class="sxs-lookup"><span data-stu-id="302ae-2500">PPS#</span></span> 
- <span data-ttu-id="302ae-2501">PPSN</span><span class="sxs-lookup"><span data-stu-id="302ae-2501">PPSN</span></span> 
- <span data-ttu-id="302ae-2502">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="302ae-2502">Public Services Card</span></span> 
- <span data-ttu-id="302ae-2503">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="302ae-2503">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="302ae-2504">Uimh.</span><span class="sxs-lookup"><span data-stu-id="302ae-2504">Uimh.</span></span> <span data-ttu-id="302ae-2505">PSP</span><span class="sxs-lookup"><span data-stu-id="302ae-2505">PSP</span></span> 
- <span data-ttu-id="302ae-2506">PSP</span><span class="sxs-lookup"><span data-stu-id="302ae-2506">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="302ae-2507">Israelische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2507">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2508">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2508">Format</span></span>

<span data-ttu-id="302ae-2509">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2509">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2510">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2510">Pattern</span></span>

<span data-ttu-id="302ae-2511">Formatiert</span><span class="sxs-lookup"><span data-stu-id="302ae-2511">Formatted:</span></span>
- <span data-ttu-id="302ae-2512">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2512">Two digits</span></span> 
- <span data-ttu-id="302ae-2513">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-2513">A dash</span></span> 
- <span data-ttu-id="302ae-2514">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2514">Three digits</span></span> 
- <span data-ttu-id="302ae-2515">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-2515">A dash</span></span> 
- <span data-ttu-id="302ae-2516">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2516">Eight digits</span></span>

<span data-ttu-id="302ae-2517">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="302ae-2517">Unformatted:</span></span>
- <span data-ttu-id="302ae-2518">	13 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2518">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2519">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2519">Checksum</span></span>

<span data-ttu-id="302ae-2520">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2520">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2521">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2521">Definition</span></span>

<span data-ttu-id="302ae-2522">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2522">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2523">Der reguläre Ausdruck Regex_israel_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2523">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2524">Ein Schlüsselwort aus Keyword_israel_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2524">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2525">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2525">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="302ae-2526">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2526">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="302ae-2527">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2527">Bank Account Number</span></span> 
- <span data-ttu-id="302ae-2528">Bank Account</span><span class="sxs-lookup"><span data-stu-id="302ae-2528">Bank Account</span></span> 
- <span data-ttu-id="302ae-2529">Account Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2529">Account Number</span></span> 
- <span data-ttu-id="302ae-2530">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="302ae-2530">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="302ae-2531">Israelische Ausweis-ID</span><span class="sxs-lookup"><span data-stu-id="302ae-2531">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2532">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2532">Format</span></span>

<span data-ttu-id="302ae-2533">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2533">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2534">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2534">Pattern</span></span>

<span data-ttu-id="302ae-2535">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2535">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2536">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2536">Checksum</span></span>

<span data-ttu-id="302ae-2537">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2537">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2538">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2538">Definition</span></span>

<span data-ttu-id="302ae-2539">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2540">Die Funktion Func_israeli_national_id_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2540">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2541">Ein Schlüsselwort aus Keyword_Israel_National_ID wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2541">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="302ae-2542">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2542">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2543">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2543">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="302ae-2544">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="302ae-2544">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="302ae-2545">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="302ae-2545">מספר זהות</span></span> 
- <span data-ttu-id="302ae-2546">National ID Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2546">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="302ae-2547">Italienische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2547">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2548">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2548">Format</span></span>

<span data-ttu-id="302ae-2549">Eine Kombination von 10 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2549">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2550">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2550">Pattern</span></span>

- <span data-ttu-id="302ae-2551">Eine Kombination aus 10 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-2551">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="302ae-2552">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="302ae-2552">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="302ae-2553">Der Buchstabe „A“ oder „W“ (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="302ae-2553">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="302ae-2554">Sieben Buchstaben (ohne Beachtung der Groß-/Kleinschreibung), Ziffern oder der Unterstrich</span><span class="sxs-lookup"><span data-stu-id="302ae-2554">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="302ae-2555">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="302ae-2555">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2556">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2556">Checksum</span></span>

<span data-ttu-id="302ae-2557">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2557">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2558">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2558">Definition</span></span>

<span data-ttu-id="302ae-2559">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2559">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2560">Der reguläre Ausdruck Regex_italy_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2560">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2561">Ein Schlüsselwort aus Keyword_italy_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2561">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2562">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2562">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="302ae-2563">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2563">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="302ae-2564">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="302ae-2564">numero di patente di guida</span></span> 
- <span data-ttu-id="302ae-2565">patente di guida</span><span class="sxs-lookup"><span data-stu-id="302ae-2565">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="302ae-2566">Japanische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2566">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2567">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2567">Format</span></span>

<span data-ttu-id="302ae-2568">Sieben oder acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2568">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2569">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2569">Pattern</span></span>

<span data-ttu-id="302ae-2570">Bankkontonummer:</span><span class="sxs-lookup"><span data-stu-id="302ae-2570">Bank account number:</span></span>
- <span data-ttu-id="302ae-2571">Sieben oder acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2571">Seven or eight digits</span></span>
- <span data-ttu-id="302ae-2572">Niederlassungscode der Bank:</span><span class="sxs-lookup"><span data-stu-id="302ae-2572">Bank account branch code:</span></span>
- <span data-ttu-id="302ae-2573">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2573">Four digits</span></span> 
- <span data-ttu-id="302ae-2574">Ein Leerzeichen oder ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="302ae-2574">A space or dash (optional)</span></span> 
- <span data-ttu-id="302ae-2575">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2575">Three digits</span></span>

<span data-ttu-id="302ae-2576">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2576">Checksum</span></span>

<span data-ttu-id="302ae-2577">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2577">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2578">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2578">Definition</span></span>

<span data-ttu-id="302ae-2579">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2580">Die Funktion Func_jp_bank_account findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2580">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2581">Ein Schlüsselwort aus Keyword_jp_bank_account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2581">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="302ae-2582">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="302ae-2582">One of the following is true:</span></span>
- <span data-ttu-id="302ae-2583">Die Funktion Func_jp_bank_account_branch_code findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2583">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2584">Ein Schlüsselwort aus Keyword_jp_bank_branch_code wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2584">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="302ae-2585">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2585">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2586">Die Funktion Func_jp_bank_account findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2586">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2587">Ein Schlüsselwort aus Keyword_jp_bank_account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2587">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2588">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2588">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="302ae-2589">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="302ae-2589">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="302ae-2590">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2590">Checking Account Number</span></span> 
- <span data-ttu-id="302ae-2591">Checking Account</span><span class="sxs-lookup"><span data-stu-id="302ae-2591">Checking Account</span></span> 
- <span data-ttu-id="302ae-2592">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="302ae-2592">Checking Account #</span></span> 
- <span data-ttu-id="302ae-2593">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2593">Checking Acct Number</span></span> 
- <span data-ttu-id="302ae-2594">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="302ae-2594">Checking Acct #</span></span> 
- <span data-ttu-id="302ae-2595">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2595">Checking Acct No.</span></span> 
- <span data-ttu-id="302ae-2596">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2596">Checking Account No.</span></span> 
- <span data-ttu-id="302ae-2597">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2597">Bank Account Number</span></span> 
- <span data-ttu-id="302ae-2598">Bank Account</span><span class="sxs-lookup"><span data-stu-id="302ae-2598">Bank Account</span></span> 
- <span data-ttu-id="302ae-2599">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="302ae-2599">Bank Account #</span></span> 
- <span data-ttu-id="302ae-2600">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2600">Bank Acct Number</span></span> 
- <span data-ttu-id="302ae-2601">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="302ae-2601">Bank Acct #</span></span> 
- <span data-ttu-id="302ae-2602">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2602">Bank Acct No.</span></span> 
- <span data-ttu-id="302ae-2603">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2603">Bank Account No.</span></span> 
- <span data-ttu-id="302ae-2604">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2604">Savings Account Number</span></span> 
- <span data-ttu-id="302ae-2605">Savings Account</span><span class="sxs-lookup"><span data-stu-id="302ae-2605">Savings Account</span></span> 
- <span data-ttu-id="302ae-2606">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="302ae-2606">Savings Account #</span></span> 
- <span data-ttu-id="302ae-2607">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2607">Savings Acct Number</span></span> 
- <span data-ttu-id="302ae-2608">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="302ae-2608">Savings Acct #</span></span> 
- <span data-ttu-id="302ae-2609">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2609">Savings Acct No.</span></span> 
- <span data-ttu-id="302ae-2610">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2610">Savings Account No.</span></span> 
- <span data-ttu-id="302ae-2611">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2611">Debit Account Number</span></span> 
- <span data-ttu-id="302ae-2612">Debit Account</span><span class="sxs-lookup"><span data-stu-id="302ae-2612">Debit Account</span></span> 
- <span data-ttu-id="302ae-2613">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="302ae-2613">Debit Account #</span></span> 
- <span data-ttu-id="302ae-2614">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2614">Debit Acct Number</span></span> 
- <span data-ttu-id="302ae-2615">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="302ae-2615">Debit Acct #</span></span> 
- <span data-ttu-id="302ae-2616">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2616">Debit Acct No.</span></span> 
- <span data-ttu-id="302ae-2617">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2617">Debit Account No.</span></span> 
- <span data-ttu-id="302ae-2618">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="302ae-2618">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="302ae-2619">#アカウントの確認. 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="302ae-2619">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="302ae-2620">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="302ae-2620">＃勘定の確認</span></span> 
- <span data-ttu-id="302ae-2621">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="302ae-2621">勘定番号の確認</span></span> 
- <span data-ttu-id="302ae-2622">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="302ae-2622">口座番号の確認</span></span> 
- <span data-ttu-id="302ae-2623">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2623">銀行口座番号</span></span> 
- <span data-ttu-id="302ae-2624">銀行口座</span><span class="sxs-lookup"><span data-stu-id="302ae-2624">銀行口座</span></span> 
- <span data-ttu-id="302ae-2625">銀行口座 #</span><span class="sxs-lookup"><span data-stu-id="302ae-2625">銀行口座＃</span></span> 
- <span data-ttu-id="302ae-2626">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2626">銀行の勘定番号</span></span> 
- <span data-ttu-id="302ae-2627">銀行のacct #</span><span class="sxs-lookup"><span data-stu-id="302ae-2627">銀行のacct＃</span></span> 
- <span data-ttu-id="302ae-2628">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="302ae-2628">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="302ae-2629">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2629">銀行口座番号</span></span>
- <span data-ttu-id="302ae-2630">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2630">普通預金口座番号</span></span> 
- <span data-ttu-id="302ae-2631">預金口座</span><span class="sxs-lookup"><span data-stu-id="302ae-2631">預金口座</span></span> 
- <span data-ttu-id="302ae-2632">貯蓄口座 #</span><span class="sxs-lookup"><span data-stu-id="302ae-2632">貯蓄口座＃</span></span> 
- <span data-ttu-id="302ae-2633">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="302ae-2633">貯蓄勘定の数</span></span> 
- <span data-ttu-id="302ae-2634">貯蓄勘定 #</span><span class="sxs-lookup"><span data-stu-id="302ae-2634">貯蓄勘定＃</span></span> 
- <span data-ttu-id="302ae-2635">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2635">貯蓄勘定番号</span></span> 
- <span data-ttu-id="302ae-2636">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2636">普通預金口座番号</span></span> 
- <span data-ttu-id="302ae-2637">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2637">引き落とし口座番号</span></span> 
- <span data-ttu-id="302ae-2638">口座番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2638">口座番号</span></span> 
- <span data-ttu-id="302ae-2639">口座番号 #</span><span class="sxs-lookup"><span data-stu-id="302ae-2639">口座番号＃</span></span> 
- <span data-ttu-id="302ae-2640">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2640">デビットのacct番号</span></span> 
- <span data-ttu-id="302ae-2641">デビット勘定 #</span><span class="sxs-lookup"><span data-stu-id="302ae-2641">デビット勘定＃</span></span> 
- <span data-ttu-id="302ae-2642">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2642">デビットACCTの番号</span></span> 
- <span data-ttu-id="302ae-2643">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2643">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="302ae-2644">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="302ae-2644">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="302ae-2645">Otemachi</span><span class="sxs-lookup"><span data-stu-id="302ae-2645">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="302ae-2646">Japanische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2646">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2647">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2647">Format</span></span>

<span data-ttu-id="302ae-2648">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2648">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2649">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2649">Pattern</span></span>

<span data-ttu-id="302ae-2650">12 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2650">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2651">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2651">Checksum</span></span>

<span data-ttu-id="302ae-2652">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2652">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2653">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2653">Definition</span></span>

<span data-ttu-id="302ae-2654">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2654">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2655">Die Funktion Func_jp_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2655">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2656">Ein Schlüsselwort aus Keyword_jp_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2656">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2657">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2657">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="302ae-2658">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2658">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="302ae-2659">DL</span><span class="sxs-lookup"><span data-stu-id="302ae-2659">dl#</span></span> 
- <span data-ttu-id="302ae-2660">DL</span><span class="sxs-lookup"><span data-stu-id="302ae-2660">DL＃</span></span> 
- <span data-ttu-id="302ae-2661">DLS</span><span class="sxs-lookup"><span data-stu-id="302ae-2661">dls#</span></span> 
- <span data-ttu-id="302ae-2662">DLS</span><span class="sxs-lookup"><span data-stu-id="302ae-2662">DLS＃</span></span> 
- <span data-ttu-id="302ae-2663">driver license</span><span class="sxs-lookup"><span data-stu-id="302ae-2663">driver license</span></span> 
- <span data-ttu-id="302ae-2664">driver licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-2664">driver licenses</span></span> 
- <span data-ttu-id="302ae-2665">drivers license</span><span class="sxs-lookup"><span data-stu-id="302ae-2665">drivers license</span></span> 
- <span data-ttu-id="302ae-2666">driver's license</span><span class="sxs-lookup"><span data-stu-id="302ae-2666">driver's license</span></span> 
- <span data-ttu-id="302ae-2667">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-2667">drivers licenses</span></span> 
- <span data-ttu-id="302ae-2668">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-2668">driver's licenses</span></span> 
- <span data-ttu-id="302ae-2669">driving licence</span><span class="sxs-lookup"><span data-stu-id="302ae-2669">driving licence</span></span> 
- <span data-ttu-id="302ae-2670">lic</span><span class="sxs-lookup"><span data-stu-id="302ae-2670">lic#</span></span> 
- <span data-ttu-id="302ae-2671">LIC</span><span class="sxs-lookup"><span data-stu-id="302ae-2671">LIC＃</span></span> 
- <span data-ttu-id="302ae-2672">LiCS</span><span class="sxs-lookup"><span data-stu-id="302ae-2672">lics#</span></span> 
- <span data-ttu-id="302ae-2673">state id</span><span class="sxs-lookup"><span data-stu-id="302ae-2673">state id</span></span> 
- <span data-ttu-id="302ae-2674">state identification</span><span class="sxs-lookup"><span data-stu-id="302ae-2674">state identification</span></span> 
- <span data-ttu-id="302ae-2675">state identification number</span><span class="sxs-lookup"><span data-stu-id="302ae-2675">state identification number</span></span> 
- <span data-ttu-id="302ae-2676">低所得国 #</span><span class="sxs-lookup"><span data-stu-id="302ae-2676">低所得国＃</span></span> 
- <span data-ttu-id="302ae-2677">免許証</span><span class="sxs-lookup"><span data-stu-id="302ae-2677">免許証</span></span> 
- <span data-ttu-id="302ae-2678">状態ID</span><span class="sxs-lookup"><span data-stu-id="302ae-2678">状態ID</span></span>
- <span data-ttu-id="302ae-2679">状態の識別</span><span class="sxs-lookup"><span data-stu-id="302ae-2679">状態の識別</span></span> 
- <span data-ttu-id="302ae-2680">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2680">状態の識別番号</span></span> 
- <span data-ttu-id="302ae-2681">運転免許</span><span class="sxs-lookup"><span data-stu-id="302ae-2681">運転免許</span></span> 
- <span data-ttu-id="302ae-2682">運転免許証</span><span class="sxs-lookup"><span data-stu-id="302ae-2682">運転免許証</span></span> 
- <span data-ttu-id="302ae-2683">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2683">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="302ae-2684">Japanische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2684">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2685">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2685">Format</span></span>

<span data-ttu-id="302ae-2686">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2686">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2687">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2687">Pattern</span></span>

<span data-ttu-id="302ae-2688">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2688">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2689">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2689">Checksum</span></span>

<span data-ttu-id="302ae-2690">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2690">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2691">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2691">Definition</span></span>

<span data-ttu-id="302ae-2692">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2692">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2693">Die Funktion Func_jp_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2693">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2694">Ein Schlüsselwort aus Keyword_jp_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2694">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2695">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2695">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="302ae-2696">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="302ae-2696">Keyword_jp_passport</span></span>

- <span data-ttu-id="302ae-2697">パスポート</span><span class="sxs-lookup"><span data-stu-id="302ae-2697">パスポート</span></span> 
- <span data-ttu-id="302ae-2698">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2698">パスポート番号</span></span> 
- <span data-ttu-id="302ae-2699">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="302ae-2699">パスポートのNum</span></span> 
- <span data-ttu-id="302ae-2700">パスポート #</span><span class="sxs-lookup"><span data-stu-id="302ae-2700">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="302ae-2701">Japanische Einwohnerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2701">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2702">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2702">Format</span></span>

<span data-ttu-id="302ae-2703">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2703">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2704">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2704">Pattern</span></span>

<span data-ttu-id="302ae-2705">11 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2705">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2706">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2706">Checksum</span></span>

<span data-ttu-id="302ae-2707">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2707">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2708">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2708">Definition</span></span>

<span data-ttu-id="302ae-2709">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2709">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2710">Die Funktion Func_jp_resident_registration_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2710">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2711">Ein Schlüsselwort aus Keyword_jp_resident_registration_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2711">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2712">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2712">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="302ae-2713">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2713">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="302ae-2714">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2714">Resident Registration Number</span></span>
- <span data-ttu-id="302ae-2715">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2715">Resident Register Number</span></span> 
- <span data-ttu-id="302ae-2716">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2716">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="302ae-2717">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2717">Resident Registration No.</span></span> 
- <span data-ttu-id="302ae-2718">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2718">Resident Register No.</span></span> 
- <span data-ttu-id="302ae-2719">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2719">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="302ae-2720">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2720">Basic Resident Register No.</span></span> 
- <span data-ttu-id="302ae-2721">住民登録番号, 登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="302ae-2721">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="302ae-2722">住民基本登録番号, 登録番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2722">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="302ae-2723">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="302ae-2723">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="302ae-2724">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2724">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="302ae-2725">Japanische Sozialversicherungsnummer (SIN)</span><span class="sxs-lookup"><span data-stu-id="302ae-2725">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2726">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2726">Format</span></span>

<span data-ttu-id="302ae-2727">7-12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2727">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2728">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2728">Pattern</span></span>

<span data-ttu-id="302ae-2729">7 bis 12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-2729">7-12 digits:</span></span>
- <span data-ttu-id="302ae-2730">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2730">Four digits</span></span> 
- <span data-ttu-id="302ae-2731">Ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="302ae-2731">A hyphen (optional)</span></span> 
- <span data-ttu-id="302ae-2732">Sechs Ziffern oder</span><span class="sxs-lookup"><span data-stu-id="302ae-2732">Six digits OR</span></span>
- <span data-ttu-id="302ae-2733">7-12 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2733">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2734">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2734">Checksum</span></span>

<span data-ttu-id="302ae-2735">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2735">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2736">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2736">Definition</span></span>

<span data-ttu-id="302ae-2737">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2737">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2738">Die Funktion Func_jp_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2738">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2739">Ein Schlüsselwort aus Keyword_jp_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2739">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="302ae-2740">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2740">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2741">Die Funktion Func_jp_sin_pre_1997 findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2741">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2742">Ein Schlüsselwort aus Keyword_jp_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2742">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2743">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2743">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="302ae-2744">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="302ae-2744">Keyword_jp_sin</span></span>

- <span data-ttu-id="302ae-2745">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="302ae-2745">Social Insurance No.</span></span> 
- <span data-ttu-id="302ae-2746">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="302ae-2746">Social Insurance Num</span></span> 
- <span data-ttu-id="302ae-2747">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2747">Social Insurance Number</span></span> 
- <span data-ttu-id="302ae-2748">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="302ae-2748">社会保険のテンキー</span></span> 
- <span data-ttu-id="302ae-2749">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2749">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="302ae-2750">Nummer der japanischen Residenzkarte</span><span class="sxs-lookup"><span data-stu-id="302ae-2750">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2751">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2751">Format</span></span>

<span data-ttu-id="302ae-2752">12 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2752">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2753">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2753">Pattern</span></span>

<span data-ttu-id="302ae-2754">12 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-2754">12 letters and digits:</span></span>
- <span data-ttu-id="302ae-2755">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="302ae-2755">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="302ae-2756">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2756">Eight digits</span></span> 
- <span data-ttu-id="302ae-2757">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="302ae-2757">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2758">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2758">Checksum</span></span>

<span data-ttu-id="302ae-2759">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2759">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2760">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2760">Definition</span></span>

<span data-ttu-id="302ae-2761">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2761">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2762">Der reguläre Ausdruck Regex_jp_residence_card_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2762">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2763">Ein Schlüsselwort aus Keyword_jp_residence_card_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2763">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2764">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2764">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="302ae-2765">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2765">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="302ae-2766">Nummer der Residenzkarte</span><span class="sxs-lookup"><span data-stu-id="302ae-2766">Residence card number</span></span>
- <span data-ttu-id="302ae-2767">Aufenthaltskarte Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2767">Residence card no</span></span>
- <span data-ttu-id="302ae-2768">Residenzkarte #</span><span class="sxs-lookup"><span data-stu-id="302ae-2768">Residence card #</span></span>
- <span data-ttu-id="302ae-2769">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="302ae-2769">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="302ae-2770">Malaysia -ID-Kartennummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2770">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2771">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2771">Format</span></span>

<span data-ttu-id="302ae-2772">12 Ziffern mit optionalen Bindestrichen</span><span class="sxs-lookup"><span data-stu-id="302ae-2772">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2773">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2773">Pattern</span></span>

<span data-ttu-id="302ae-2774">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-2774">12 digits:</span></span>
- <span data-ttu-id="302ae-2775">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="302ae-2775">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="302ae-2776">Ein Bindestrich (optional) </span><span class="sxs-lookup"><span data-stu-id="302ae-2776">A dash (optional)</span></span> 
- <span data-ttu-id="302ae-2777">Zwei Buchstaben als Code für den Geburtsort </span><span class="sxs-lookup"><span data-stu-id="302ae-2777">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="302ae-2778">Ein Bindestrich (optional) </span><span class="sxs-lookup"><span data-stu-id="302ae-2778">A dash (optional)</span></span> 
- <span data-ttu-id="302ae-2779">Drei beliebige Ziffern </span><span class="sxs-lookup"><span data-stu-id="302ae-2779">Three random digits</span></span> 
- <span data-ttu-id="302ae-2780">Einstelliger Code für das Geschlecht</span><span class="sxs-lookup"><span data-stu-id="302ae-2780">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2781">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2781">Checksum</span></span>

<span data-ttu-id="302ae-2782">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2782">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2783">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2783">Definition</span></span>

<span data-ttu-id="302ae-2784">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2785">Der reguläre Ausdruck Regex_malaysia_id_card_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2785">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2786">Ein Schlüsselwort aus Keyword_malaysia_id_card_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2786">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2787">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2787">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="302ae-2788">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2788">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="302ae-2789">digitale Anwendungs Karte</span><span class="sxs-lookup"><span data-stu-id="302ae-2789">digital application card</span></span>
- <span data-ttu-id="302ae-2790">i/c</span><span class="sxs-lookup"><span data-stu-id="302ae-2790">i/c</span></span>
- <span data-ttu-id="302ae-2791">i/c Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2791">i/c no</span></span>
- <span data-ttu-id="302ae-2792">IC</span><span class="sxs-lookup"><span data-stu-id="302ae-2792">ic</span></span>
- <span data-ttu-id="302ae-2793">IC Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2793">ic no</span></span>
- <span data-ttu-id="302ae-2794">id card</span><span class="sxs-lookup"><span data-stu-id="302ae-2794">id card</span></span>
- <span data-ttu-id="302ae-2795">Identitätskarte</span><span class="sxs-lookup"><span data-stu-id="302ae-2795">identification Card</span></span>
- <span data-ttu-id="302ae-2796">identity card</span><span class="sxs-lookup"><span data-stu-id="302ae-2796">identity card</span></span>
- <span data-ttu-id="302ae-2797">k/p</span><span class="sxs-lookup"><span data-stu-id="302ae-2797">k/p</span></span>
- <span data-ttu-id="302ae-2798">k/p Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2798">k/p no</span></span>
- <span data-ttu-id="302ae-2799">Kad akuan Diri</span><span class="sxs-lookup"><span data-stu-id="302ae-2799">kad akuan diri</span></span>
- <span data-ttu-id="302ae-2800">Kad aplikasi Digital</span><span class="sxs-lookup"><span data-stu-id="302ae-2800">kad aplikasi digital</span></span>
- <span data-ttu-id="302ae-2801">Kad Einführung in Malaysia</span><span class="sxs-lookup"><span data-stu-id="302ae-2801">kad pengenalan malaysia</span></span>
- <span data-ttu-id="302ae-2802">KP</span><span class="sxs-lookup"><span data-stu-id="302ae-2802">kp</span></span>
- <span data-ttu-id="302ae-2803">KP Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2803">kp no</span></span>
- <span data-ttu-id="302ae-2804">MyKAD</span><span class="sxs-lookup"><span data-stu-id="302ae-2804">mykad</span></span>
- <span data-ttu-id="302ae-2805">mykas</span><span class="sxs-lookup"><span data-stu-id="302ae-2805">mykas</span></span>
- <span data-ttu-id="302ae-2806">mykid</span><span class="sxs-lookup"><span data-stu-id="302ae-2806">mykid</span></span>
- <span data-ttu-id="302ae-2807">mypr</span><span class="sxs-lookup"><span data-stu-id="302ae-2807">mypr</span></span>
- <span data-ttu-id="302ae-2808">mytentera</span><span class="sxs-lookup"><span data-stu-id="302ae-2808">mytentera</span></span>
- <span data-ttu-id="302ae-2809">Malaysia-Identitätskarte</span><span class="sxs-lookup"><span data-stu-id="302ae-2809">malaysia identity card</span></span>
- <span data-ttu-id="302ae-2810">malaysischer Identitätsausweis</span><span class="sxs-lookup"><span data-stu-id="302ae-2810">malaysian identity card</span></span>
- <span data-ttu-id="302ae-2811">NRIC</span><span class="sxs-lookup"><span data-stu-id="302ae-2811">nric</span></span>
- <span data-ttu-id="302ae-2812">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="302ae-2812">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="302ae-2813">Niederlande – Bürgerdienstnummer (BSN)</span><span class="sxs-lookup"><span data-stu-id="302ae-2813">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2814">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2814">Format</span></span>

<span data-ttu-id="302ae-2815">8-9 Ziffern mit optionalen Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-2815">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2816">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2816">Pattern</span></span>

<span data-ttu-id="302ae-2817">8-9 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-2817">8-9 digits:</span></span>
- <span data-ttu-id="302ae-2818">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2818">Three digits</span></span> 
- <span data-ttu-id="302ae-2819">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="302ae-2819">A space (optional)</span></span> 
- <span data-ttu-id="302ae-2820">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2820">Three digits</span></span> 
- <span data-ttu-id="302ae-2821">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="302ae-2821">A space (optional)</span></span> 
- <span data-ttu-id="302ae-2822">2-3 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2822">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2823">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2823">Checksum</span></span>

<span data-ttu-id="302ae-2824">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2824">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2825">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2825">Definition</span></span>

<span data-ttu-id="302ae-2826">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2826">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2827">Die Funktion Func_netherlands_bsn sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2827">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2828">Ein Schlüsselwort aus Keyword_netherlands_bsn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2828">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="302ae-2829">Die Funktion Func_eu_date2 findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="302ae-2829">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="302ae-2830">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2830">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2831">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2831">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="302ae-2832">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="302ae-2832">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="302ae-2833">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="302ae-2833">Citizen service number</span></span> 
- <span data-ttu-id="302ae-2834">BSN</span><span class="sxs-lookup"><span data-stu-id="302ae-2834">BSN</span></span> 
- <span data-ttu-id="302ae-2835">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2835">Burgerservicenummer</span></span> 
- <span data-ttu-id="302ae-2836">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2836">Sofinummer</span></span> 
- <span data-ttu-id="302ae-2837">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2837">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="302ae-2838">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2838">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="302ae-2839">Neuseeländische Gesundheitsministeriumsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2839">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2840">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2840">Format</span></span>

<span data-ttu-id="302ae-2841">Drei Buchstaben, ein Leerzeichen (optional) und vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2841">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2842">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2842">Pattern</span></span>

<span data-ttu-id="302ae-2843">Drei Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) ein Leerzeichen (optional) vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2843">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2844">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2844">Checksum</span></span>

<span data-ttu-id="302ae-2845">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2845">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2846">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2846">Definition</span></span>

<span data-ttu-id="302ae-2847">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2848">Die Funktion Func_new_zealand_ministry_of_health_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2848">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2849">Ein Schlüsselwort aus Keyword_nz_terms wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2849">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="302ae-2850">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2850">The checksum passes.</span></span>

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

<span data-ttu-id="302ae-2851">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2851">Keywords</span></span>

<span data-ttu-id="302ae-2852">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="302ae-2852">Keyword_nz_terms</span></span>

- <span data-ttu-id="302ae-2853">NHI</span><span class="sxs-lookup"><span data-stu-id="302ae-2853">NHI</span></span> 
- <span data-ttu-id="302ae-2854">New Zealand</span><span class="sxs-lookup"><span data-stu-id="302ae-2854">New Zealand</span></span> 
- <span data-ttu-id="302ae-2855">Integrität</span><span class="sxs-lookup"><span data-stu-id="302ae-2855">Health</span></span> 
- <span data-ttu-id="302ae-2856">Flusses zur Gewährung</span><span class="sxs-lookup"><span data-stu-id="302ae-2856">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="302ae-2857">Norwegen – Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2857">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2858">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2858">Format</span></span>

<span data-ttu-id="302ae-2859">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2859">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2860">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2860">Pattern</span></span>

<span data-ttu-id="302ae-2861">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-2861">11 digits:</span></span>
- <span data-ttu-id="302ae-2862">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="302ae-2862">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="302ae-2863">Dreistellige individuelle Zahl </span><span class="sxs-lookup"><span data-stu-id="302ae-2863">Three-digit individual number</span></span> 
- <span data-ttu-id="302ae-2864">Zwei Prüfziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2864">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2865">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2865">Checksum</span></span>

<span data-ttu-id="302ae-2866">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2866">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2867">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2867">Definition</span></span>

<span data-ttu-id="302ae-2868">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2868">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2869">Die Funktion Func_norway_id_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2869">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2870">Ein Schlüsselwort aus Keyword_norway_id_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2870">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="302ae-2871">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2871">The checksum passes.</span></span>
- <span data-ttu-id="302ae-2872">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2872">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2873">Die Funktion Func_norway_id_numbe sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2873">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2874">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2874">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2875">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2875">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="302ae-2876">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2876">Keyword_norway_id_number</span></span>

- <span data-ttu-id="302ae-2877">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="302ae-2877">Personal identification number</span></span>
- <span data-ttu-id="302ae-2878">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2878">Norwegian ID Number</span></span>
- <span data-ttu-id="302ae-2879">ID Number</span><span class="sxs-lookup"><span data-stu-id="302ae-2879">ID Number</span></span>
- <span data-ttu-id="302ae-2880">Identifikations</span><span class="sxs-lookup"><span data-stu-id="302ae-2880">Identification</span></span>
- <span data-ttu-id="302ae-2881">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="302ae-2881">Personnummer</span></span>
- <span data-ttu-id="302ae-2882">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2882">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="302ae-2883">Philippinen – Vereinheitlichte Mehrzweck-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2883">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2884">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2884">Format</span></span>

<span data-ttu-id="302ae-2885">12 Ziffern, durch Bindestriche getrennt</span><span class="sxs-lookup"><span data-stu-id="302ae-2885">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2886">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2886">Pattern</span></span>

<span data-ttu-id="302ae-2887">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-2887">12 digits:</span></span>
- <span data-ttu-id="302ae-2888">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2888">Four digits</span></span> 
- <span data-ttu-id="302ae-2889">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-2889">A hyphen</span></span> 
- <span data-ttu-id="302ae-2890">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="302ae-2890">Seven digits</span></span> 
- <span data-ttu-id="302ae-2891">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-2891">A hyphen</span></span> 
- <span data-ttu-id="302ae-2892">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-2892">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2893">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2893">Checksum</span></span>

<span data-ttu-id="302ae-2894">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2894">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2895">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2895">Definition</span></span>

<span data-ttu-id="302ae-2896">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2896">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2897">Der reguläre Ausdruck Regex_philippines_unified_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2897">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2898">Ein Schlüsselwort aus Keyword_philippines_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2898">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2899">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2899">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="302ae-2900">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="302ae-2900">Keyword_philippines_id</span></span>

- <span data-ttu-id="302ae-2901">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="302ae-2901">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="302ae-2902">UMID</span><span class="sxs-lookup"><span data-stu-id="302ae-2902">UMID</span></span> 
- <span data-ttu-id="302ae-2903">Identity Card</span><span class="sxs-lookup"><span data-stu-id="302ae-2903">Identity Card</span></span> 
- <span data-ttu-id="302ae-2904">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="302ae-2904">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="302ae-2905">Polen Personalausweis</span><span class="sxs-lookup"><span data-stu-id="302ae-2905">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2906">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2906">Format</span></span>

<span data-ttu-id="302ae-2907">Drei Buchstaben und sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2907">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2908">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2908">Pattern</span></span>

<span data-ttu-id="302ae-2909">Drei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2909">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2910">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2910">Checksum</span></span>

<span data-ttu-id="302ae-2911">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2911">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2912">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2912">Definition</span></span>

<span data-ttu-id="302ae-2913">Eine DLP-Richtlinie ist 75% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: die Funktion Func_polish_national_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2913">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="302ae-2914">Ein Schlüsselwort aus Keyword_polish_national_id_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2914">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="302ae-2915">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2915">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2916">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2916">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="302ae-2917">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2917">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="302ae-2918">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="302ae-2918">Dowód osobisty</span></span>
- <span data-ttu-id="302ae-2919">Numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="302ae-2919">Numer dowodu osobistego</span></span>
- <span data-ttu-id="302ae-2920">Nazwa i Numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="302ae-2920">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="302ae-2921">Nazwa i Nr dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="302ae-2921">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="302ae-2922">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="302ae-2922">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="302ae-2923">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="302ae-2923">Dowód Tożsamości</span></span>
- <span data-ttu-id="302ae-2924">Dow.</span><span class="sxs-lookup"><span data-stu-id="302ae-2924">dow.</span></span> <span data-ttu-id="302ae-2925">OS.</span><span class="sxs-lookup"><span data-stu-id="302ae-2925">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="302ae-2926">Polnische ID-Karte (PESEL)</span><span class="sxs-lookup"><span data-stu-id="302ae-2926">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2927">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2927">Format</span></span>

<span data-ttu-id="302ae-2928">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2928">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2929">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2929">Pattern</span></span>

<span data-ttu-id="302ae-2930">11 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2930">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2931">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2931">Checksum</span></span>

<span data-ttu-id="302ae-2932">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2932">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2933">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2933">Definition</span></span>

<span data-ttu-id="302ae-2934">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2934">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2935">Die Funktion Func_pesel_identification_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2935">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2936">Ein Schlüsselwort aus Keyword_pesel_identification_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2936">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="302ae-2937">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2937">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2938">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2938">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="302ae-2939">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2939">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="302ae-2940">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="302ae-2940">Nr PESEL</span></span>
- <span data-ttu-id="302ae-2941">PESEL</span><span class="sxs-lookup"><span data-stu-id="302ae-2941">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="302ae-2942">Polen Reisepass</span><span class="sxs-lookup"><span data-stu-id="302ae-2942">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2943">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2943">Format</span></span>

<span data-ttu-id="302ae-2944">Zwei Buchstaben und sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2944">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2945">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2945">Pattern</span></span>

<span data-ttu-id="302ae-2946">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2946">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2947">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2947">Checksum</span></span>

<span data-ttu-id="302ae-2948">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-2948">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2949">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2949">Definition</span></span>

<span data-ttu-id="302ae-2950">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2950">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2951">Die Funktion Func_polish_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2951">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2952">Ein Schlüsselwort aus Keyword_polish_national_id_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2952">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="302ae-2953">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-2953">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2954">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2954">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="302ae-2955">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="302ae-2955">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="302ae-2956">Numer paszportu</span><span class="sxs-lookup"><span data-stu-id="302ae-2956">Numer paszportu</span></span>
- <span data-ttu-id="302ae-2957">Nr.</span><span class="sxs-lookup"><span data-stu-id="302ae-2957">Nr.</span></span> <span data-ttu-id="302ae-2958">Paszportu</span><span class="sxs-lookup"><span data-stu-id="302ae-2958">Paszportu</span></span>
- <span data-ttu-id="302ae-2959">Paszport</span><span class="sxs-lookup"><span data-stu-id="302ae-2959">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="302ae-2960">Portugal – Bürgerkartennummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2960">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2961">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2961">Format</span></span>

<span data-ttu-id="302ae-2962">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2962">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2963">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2963">Pattern</span></span>

<span data-ttu-id="302ae-2964">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2964">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2965">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2965">Checksum</span></span>

<span data-ttu-id="302ae-2966">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2966">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2967">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2967">Definition</span></span>

<span data-ttu-id="302ae-2968">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2969">Der reguläre Ausdruck Regex_portugal_citizen_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2969">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2970">Ein Schlüsselwort aus Keyword_portugal_citizen_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2970">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-2971">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2971">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="302ae-2972">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="302ae-2972">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="302ae-2973">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="302ae-2973">Citizen Card</span></span>
- <span data-ttu-id="302ae-2974">National ID Card</span><span class="sxs-lookup"><span data-stu-id="302ae-2974">National ID Card</span></span>
- <span data-ttu-id="302ae-2975">CC</span><span class="sxs-lookup"><span data-stu-id="302ae-2975">CC</span></span>
- <span data-ttu-id="302ae-2976">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="302ae-2976">Cartão de Cidadão</span></span>
- <span data-ttu-id="302ae-2977">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="302ae-2977">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="302ae-2978">Saudi-Arabische Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-2978">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2979">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2979">Format</span></span>

<span data-ttu-id="302ae-2980">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2980">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2981">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2981">Pattern</span></span>

<span data-ttu-id="302ae-2982">10 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2982">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-2983">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-2983">Checksum</span></span>

<span data-ttu-id="302ae-2984">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-2984">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-2985">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-2985">Definition</span></span>

<span data-ttu-id="302ae-2986">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-2986">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-2987">Der reguläre Ausdruck Regex_saudi_arabia_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-2987">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-2988">Ein Schlüsselwort aus Keyword_saudi_arabia_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-2988">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-2989">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-2989">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="302ae-2990">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="302ae-2990">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="302ae-2991">Identification Card</span><span class="sxs-lookup"><span data-stu-id="302ae-2991">Identification Card</span></span> 
- <span data-ttu-id="302ae-2992">I card number</span><span class="sxs-lookup"><span data-stu-id="302ae-2992">I card number</span></span> 
- <span data-ttu-id="302ae-2993">ID number</span><span class="sxs-lookup"><span data-stu-id="302ae-2993">ID number</span></span> 
- <span data-ttu-id="302ae-2994">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="302ae-2994">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="302ae-2995">Singapur – National Registration Identity Card-Nummer (NRIC)</span><span class="sxs-lookup"><span data-stu-id="302ae-2995">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-2996">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-2996">Format</span></span>

<span data-ttu-id="302ae-2997">Neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-2997">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-2998">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-2998">Pattern</span></span>

- <span data-ttu-id="302ae-2999">Neun Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-2999">Nine letters and digits:</span></span>
- <span data-ttu-id="302ae-3000">Die Buchstaben "F", "G", "S" oder "T" (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="302ae-3000">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="302ae-3001">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="302ae-3001">Seven digits</span></span> 
- <span data-ttu-id="302ae-3002">Eine alphabetische Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-3002">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3003">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3003">Checksum</span></span>

<span data-ttu-id="302ae-3004">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-3004">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3005">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3005">Definition</span></span>

<span data-ttu-id="302ae-3006">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3006">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3007">Der reguläre Ausdruck Regex_singapore_nric findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3007">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3008">Ein Schlüsselwort aus Keyword_singapore_nric wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3008">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="302ae-3009">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-3009">The checksum passes.</span></span>

<span data-ttu-id="302ae-3010">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3010">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3011">Der reguläre Ausdruck Regex_singapore_nric findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3011">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3012">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-3012">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-3013">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3013">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="302ae-3014">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="302ae-3014">Keyword_singapore_nric</span></span>

- <span data-ttu-id="302ae-3015">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="302ae-3015">National Registration Identity Card</span></span> 
- <span data-ttu-id="302ae-3016">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3016">Identity Card Number</span></span> 
- <span data-ttu-id="302ae-3017">NRIC</span><span class="sxs-lookup"><span data-stu-id="302ae-3017">NRIC</span></span> 
- <span data-ttu-id="302ae-3018">IC</span><span class="sxs-lookup"><span data-stu-id="302ae-3018">IC</span></span> 
- <span data-ttu-id="302ae-3019">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3019">Foreign Identification Number</span></span> 
- <span data-ttu-id="302ae-3020">FIN</span><span class="sxs-lookup"><span data-stu-id="302ae-3020">FIN</span></span> 
- <span data-ttu-id="302ae-3021">身份证</span><span class="sxs-lookup"><span data-stu-id="302ae-3021">身份证</span></span> 
- <span data-ttu-id="302ae-3022">身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-3022">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="302ae-3023">Südafrika – Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-3023">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3024">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3024">Format</span></span>

<span data-ttu-id="302ae-3025">13 Ziffern, die Leerzeichen enthalten können</span><span class="sxs-lookup"><span data-stu-id="302ae-3025">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3026">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3026">Pattern</span></span>

<span data-ttu-id="302ae-3027">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-3027">13 digits:</span></span>
- <span data-ttu-id="302ae-3028">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="302ae-3028">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="302ae-3029">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3029">Four digits</span></span> 
- <span data-ttu-id="302ae-3030">Ein einstelliger Citizenship-Indikator </span><span class="sxs-lookup"><span data-stu-id="302ae-3030">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="302ae-3031">Die Ziffer "8" oder "9" </span><span class="sxs-lookup"><span data-stu-id="302ae-3031">The digit "8" or "9"</span></span> 
- <span data-ttu-id="302ae-3032">Eine Ziffer als Prüfsummenziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-3032">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3033">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3033">Checksum</span></span>

<span data-ttu-id="302ae-3034">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-3034">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3035">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3035">Definition</span></span>

<span data-ttu-id="302ae-3036">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3036">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3037">Die Funktion Func_south_africa_identification_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3037">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3038">Ein Schlüsselwort aus Keyword_south_africa_identification_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3038">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="302ae-3039">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-3039">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3040">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3040">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="302ae-3041">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="302ae-3041">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="302ae-3042">Identity card</span><span class="sxs-lookup"><span data-stu-id="302ae-3042">Identity card</span></span>
- <span data-ttu-id="302ae-3043">ID</span><span class="sxs-lookup"><span data-stu-id="302ae-3043">ID</span></span>
- <span data-ttu-id="302ae-3044">Identifikations</span><span class="sxs-lookup"><span data-stu-id="302ae-3044">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="302ae-3045">Südkorea – Einwohnerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-3045">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3046">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3046">Format</span></span>

<span data-ttu-id="302ae-3047">13 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="302ae-3047">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3048">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3048">Pattern</span></span>

<span data-ttu-id="302ae-3049">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-3049">13 digits:</span></span>
- <span data-ttu-id="302ae-3050">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="302ae-3050">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="302ae-3051">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="302ae-3051">A hyphen</span></span> 
- <span data-ttu-id="302ae-3052">Eine Ziffer, die durch das Jahrhundert und das Geschlecht bestimmt wird </span><span class="sxs-lookup"><span data-stu-id="302ae-3052">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="302ae-3053">Vierstelliger Code für die Geburtsregion </span><span class="sxs-lookup"><span data-stu-id="302ae-3053">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="302ae-3054">Eine Ziffer, um Personen zu unterscheiden, für die die vorhergehenden Zahlen identisch sind </span><span class="sxs-lookup"><span data-stu-id="302ae-3054">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="302ae-3055">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-3055">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3056">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3056">Checksum</span></span>

<span data-ttu-id="302ae-3057">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-3057">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3058">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3058">Definition</span></span>

<span data-ttu-id="302ae-3059">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3059">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3060">Die Funktion Func_south_korea_resident_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3060">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3061">Ein Schlüsselwort aus Keyword_south_korea_resident_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3061">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="302ae-3062">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-3062">The checksum passes.</span></span>

<span data-ttu-id="302ae-3063">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3063">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3064">Die Funktion Func_south_korea_resident_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3064">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3065">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-3065">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-3066">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3066">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="302ae-3067">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="302ae-3067">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="302ae-3068">National ID card</span><span class="sxs-lookup"><span data-stu-id="302ae-3068">National ID card</span></span> 
- <span data-ttu-id="302ae-3069">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3069">Citizen's Registration Number</span></span> 
- <span data-ttu-id="302ae-3070">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="302ae-3070">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="302ae-3071">RRN</span><span class="sxs-lookup"><span data-stu-id="302ae-3071">RRN</span></span> 
- <span data-ttu-id="302ae-3072">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="302ae-3072">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="302ae-3073">Spanische Sozialversicherungsnummer (SSN)</span><span class="sxs-lookup"><span data-stu-id="302ae-3073">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3074">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3074">Format</span></span>

<span data-ttu-id="302ae-3075">11-12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3075">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3076">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3076">Pattern</span></span>

<span data-ttu-id="302ae-3077">11-12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-3077">11-12 digits:</span></span>
- <span data-ttu-id="302ae-3078">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3078">Two digits</span></span> 
- <span data-ttu-id="302ae-3079">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="302ae-3079">A forward slash (optional)</span></span> 
- <span data-ttu-id="302ae-3080">7 bis 8 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3080">7-8 digits</span></span> 
- <span data-ttu-id="302ae-3081">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="302ae-3081">A forward slash (optional)</span></span> 
- <span data-ttu-id="302ae-3082">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3082">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3083">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3083">Checksum</span></span>

<span data-ttu-id="302ae-3084">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-3084">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3085">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3085">Definition</span></span>

<span data-ttu-id="302ae-3086">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3086">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3087">Die Funktion Func_spanish_social_security_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3087">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3088">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-3088">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3089">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3089">Keywords</span></span>

<span data-ttu-id="302ae-3090">None</span><span class="sxs-lookup"><span data-stu-id="302ae-3090">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="302ae-3091">SQL Server-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="302ae-3091">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3092">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3092">Format</span></span>

<span data-ttu-id="302ae-3093">Die Zeichenfolge "Benutzer-ID", "Benutzer-ID", "UID" oder "UserId" gefolgt von den Zeichen und Zeichenfolgen, die im folgenden Muster erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3093">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3094">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3094">Pattern</span></span>

- <span data-ttu-id="302ae-3095">Die Zeichenfolge "Benutzer-ID", "Benutzer-ID", "UID" oder "UserId"</span><span class="sxs-lookup"><span data-stu-id="302ae-3095">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="302ae-3096">Eine beliebige Kombination von zwischen 1-200 Buchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-3096">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="302ae-3097">Die Zeichenfolge "Password" oder "pwd", wobei "pwd" keinem Kleinbuchstaben vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="302ae-3097">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="302ae-3098">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-3098">An equal sign (=)</span></span>
- <span data-ttu-id="302ae-3099">Ein beliebiges Zeichen, das kein Dollarzeichen ($), Prozentzeichen (%), größer als Symbol (>), at-Zeichen (@), Anführungszeichen ("), Semikolon (;), linke geschweifte Klammer ([) oder linke eckige Klammer ({)</span><span class="sxs-lookup"><span data-stu-id="302ae-3099">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="302ae-3100">Eine beliebige Kombination von 7-128 Zeichen, die kein Semikolon (;), Schrägstrich (/) oder Anführungszeichen (") sind.</span><span class="sxs-lookup"><span data-stu-id="302ae-3100">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="302ae-3101">Ein Semikolon (;) oder Anführungszeichen (")</span><span class="sxs-lookup"><span data-stu-id="302ae-3101">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3102">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3102">Checksum</span></span>

<span data-ttu-id="302ae-3103">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3103">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3104">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3104">Definition</span></span>

<span data-ttu-id="302ae-3105">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3105">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3106">Der reguläre Ausdruck CEP_Regex_SQLServerConnectionString findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3106">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3107">Ein Schlüsselwort aus CEP_GlobalFilter wurde **nicht** gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3107">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="302ae-3108">Der reguläre Ausdruck CEP_PasswordPlaceHolder findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3108">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3109">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3109">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!---SQL Server Connection String>
<Entity id="e76b6205-d3cb-46f2-bd63-c90153f2f97d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_SQLServerConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_GlobalFilter" />
            <Match idRef="CEP_PasswordPlaceHolder" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3110">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3110">Keywords</span></span>

#### <a name="cepglobalfilter"></a><span data-ttu-id="302ae-3111">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="302ae-3111">CEP_GlobalFilter</span></span>

- <span data-ttu-id="302ae-3112">Some-Password</span><span class="sxs-lookup"><span data-stu-id="302ae-3112">some-password</span></span>
- <span data-ttu-id="302ae-3113">somepassword</span><span class="sxs-lookup"><span data-stu-id="302ae-3113">somepassword</span></span>
- <span data-ttu-id="302ae-3114">secretPassword</span><span class="sxs-lookup"><span data-stu-id="302ae-3114">secretPassword</span></span>
- <span data-ttu-id="302ae-3115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="302ae-3115">sample</span></span>

#### <a name="ceppasswordplaceholder"></a><span data-ttu-id="302ae-3116">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="302ae-3116">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="302ae-3117">(Beachten Sie, dass dieser vertrauliche Informationstyp diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Schlüsselwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="302ae-3117">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="302ae-3118">Password oder PWD gefolgt von 0-2 Leerzeichen, einem Gleichheits Signal (=), 0-2 Leerzeichen und einem Sternchen (\*)--oder--</span><span class="sxs-lookup"><span data-stu-id="302ae-3118">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="302ae-3119">Password oder PWD gefolgt von:</span><span class="sxs-lookup"><span data-stu-id="302ae-3119">Password or pwd followed by:</span></span>
    - <span data-ttu-id="302ae-3120">Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="302ae-3120">Equal sign (=)</span></span>
    - <span data-ttu-id="302ae-3121">Kleiner als Symbol (<)</span><span class="sxs-lookup"><span data-stu-id="302ae-3121">Less than symbol (<)</span></span>
    - <span data-ttu-id="302ae-3122">Eine beliebige Kombination von 1-200 Zeichen mit groß-oder Kleinbuchstaben, Ziffern, einem Sternchen (\*), Bindestrich (-), Unterstreichung (_) oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-3122">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="302ae-3123">Größer als-Symbol (>)</span><span class="sxs-lookup"><span data-stu-id="302ae-3123">Greater than symbol (>)</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="302ae-3124">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="302ae-3124">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="302ae-3125">(Beachten Sie, dass dieser vertrauliche Informationstyp diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Schlüsselwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="302ae-3125">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="302ae-3126">contoso</span><span class="sxs-lookup"><span data-stu-id="302ae-3126">contoso</span></span>
- <span data-ttu-id="302ae-3127">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="302ae-3127">fabrikam</span></span>
- <span data-ttu-id="302ae-3128">Northwind</span><span class="sxs-lookup"><span data-stu-id="302ae-3128">northwind</span></span>
- <span data-ttu-id="302ae-3129">Sandbox</span><span class="sxs-lookup"><span data-stu-id="302ae-3129">sandbox</span></span>
- <span data-ttu-id="302ae-3130">OneBox</span><span class="sxs-lookup"><span data-stu-id="302ae-3130">onebox</span></span>
- <span data-ttu-id="302ae-3131">localhost</span><span class="sxs-lookup"><span data-stu-id="302ae-3131">localhost</span></span>
- <span data-ttu-id="302ae-3132">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="302ae-3132">127.0.0.1</span></span>
- <span data-ttu-id="302ae-3133">testacs. <!--no-hyperlink-->com</span><span class="sxs-lookup"><span data-stu-id="302ae-3133">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="302ae-3134">s-int.<!--no-hyperlink-->net</span><span class="sxs-lookup"><span data-stu-id="302ae-3134">s-int.<!--no-hyperlink-->net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="302ae-3135">Schwedische Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-3135">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3136">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3136">Format</span></span>

<span data-ttu-id="302ae-3137">10 oder 12 Ziffern und ein optionales Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-3137">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3138">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3138">Pattern</span></span>

<span data-ttu-id="302ae-3139">10 oder 12 Ziffern und ein optionals Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="302ae-3139">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="302ae-3140">2 bis 4 Ziffern (optional)</span><span class="sxs-lookup"><span data-stu-id="302ae-3140">2-4 digits (optional)</span></span> 
- <span data-ttu-id="302ae-3141">Sechs Ziffern im Datumsformat JJMMTT</span><span class="sxs-lookup"><span data-stu-id="302ae-3141">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="302ae-3142">Trennzeichen „-“ oder „+“ (optional) und</span><span class="sxs-lookup"><span data-stu-id="302ae-3142">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="302ae-3143">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3143">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3144">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3144">Checksum</span></span>

<span data-ttu-id="302ae-3145">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-3145">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3146">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3146">Definition</span></span>

<span data-ttu-id="302ae-3147">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3147">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3148">Die Funktion Func_swedish_national_identifier findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3148">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3149">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-3149">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3150">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3150">Keywords</span></span>

<span data-ttu-id="302ae-3151">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3151">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="302ae-3152">Schwedische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-3152">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3153">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3153">Format</span></span>

<span data-ttu-id="302ae-3154">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3154">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3155">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3155">Pattern</span></span>

<span data-ttu-id="302ae-3156">Acht aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3156">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3157">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3157">Checksum</span></span>

<span data-ttu-id="302ae-3158">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3158">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3159">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3159">Definition</span></span>

<span data-ttu-id="302ae-3160">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3160">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3161">Der reguläre Ausdruck Regex_sweden_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3161">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3162">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="302ae-3162">One of the following is true:</span></span>
    - <span data-ttu-id="302ae-3163">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3163">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="302ae-3164">Ein Schlüsselwort aus Keyword_sweden_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3164">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-3165">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3165">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="302ae-3166">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="302ae-3166">Keyword_sweden_passport</span></span>

- <span data-ttu-id="302ae-3167">visa requirements</span><span class="sxs-lookup"><span data-stu-id="302ae-3167">visa requirements</span></span> 
- <span data-ttu-id="302ae-3168">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="302ae-3168">Alien Registration Card</span></span> 
- <span data-ttu-id="302ae-3169">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="302ae-3169">Schengen visas</span></span> 
- <span data-ttu-id="302ae-3170">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="302ae-3170">Schengen visa</span></span> 
- <span data-ttu-id="302ae-3171">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="302ae-3171">Visa Processing</span></span> 
- <span data-ttu-id="302ae-3172">Visa Type</span><span class="sxs-lookup"><span data-stu-id="302ae-3172">Visa Type</span></span> 
- <span data-ttu-id="302ae-3173">Single Entry</span><span class="sxs-lookup"><span data-stu-id="302ae-3173">Single Entry</span></span> 
- <span data-ttu-id="302ae-3174">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="302ae-3174">Multiple Entry</span></span> 
- <span data-ttu-id="302ae-3175">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="302ae-3175">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="302ae-3176">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="302ae-3176">Keyword_passport</span></span>

- <span data-ttu-id="302ae-3177">Passport Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3177">Passport Number</span></span> 
- <span data-ttu-id="302ae-3178">Passport No</span><span class="sxs-lookup"><span data-stu-id="302ae-3178">Passport No</span></span> 
- <span data-ttu-id="302ae-3179">Passport#</span><span class="sxs-lookup"><span data-stu-id="302ae-3179">Passport #</span></span> 
- <span data-ttu-id="302ae-3180">Pass</span><span class="sxs-lookup"><span data-stu-id="302ae-3180">Passport#</span></span> 
- <span data-ttu-id="302ae-3181">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="302ae-3181">PassportID</span></span> 
- <span data-ttu-id="302ae-3182">Passportno</span><span class="sxs-lookup"><span data-stu-id="302ae-3182">Passportno</span></span> 
- <span data-ttu-id="302ae-3183">passportnumber</span><span class="sxs-lookup"><span data-stu-id="302ae-3183">passportnumber</span></span> 
- <span data-ttu-id="302ae-3184">パスポート</span><span class="sxs-lookup"><span data-stu-id="302ae-3184">パスポート</span></span> 
- <span data-ttu-id="302ae-3185">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="302ae-3185">パスポート番号</span></span> 
- <span data-ttu-id="302ae-3186">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="302ae-3186">パスポートのNum</span></span> 
- <span data-ttu-id="302ae-3187">パスポート #</span><span class="sxs-lookup"><span data-stu-id="302ae-3187">パスポート＃</span></span> 
- <span data-ttu-id="302ae-3188">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="302ae-3188">Numéro de passeport</span></span> 
- <span data-ttu-id="302ae-3189">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="302ae-3189">Passeport n °</span></span> 
- <span data-ttu-id="302ae-3190">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="302ae-3190">Passeport Non</span></span> 
- <span data-ttu-id="302ae-3191">Passeport#</span><span class="sxs-lookup"><span data-stu-id="302ae-3191">Passeport #</span></span> 
- <span data-ttu-id="302ae-3192">Passeport</span><span class="sxs-lookup"><span data-stu-id="302ae-3192">Passeport#</span></span> 
- <span data-ttu-id="302ae-3193">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="302ae-3193">PasseportNon</span></span> 
- <span data-ttu-id="302ae-3194">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="302ae-3194">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="302ae-3195">SWIFT-Code</span><span class="sxs-lookup"><span data-stu-id="302ae-3195">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3196">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3196">Format</span></span>

<span data-ttu-id="302ae-3197">Vier Buchstaben, gefolgt von 5-31 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3197">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3198">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3198">Pattern</span></span>

<span data-ttu-id="302ae-3199">Vier Buchstaben, gefolgt von 5 bis 31 Buchstaben oder Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-3199">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="302ae-3200">Vier Buchstaben für den Bankcode (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="302ae-3200">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="302ae-3201">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-3201">An optional space</span></span> 
- <span data-ttu-id="302ae-3202">4 bis 28 Buchstaben oder Ziffern (BBAN, Basic Bank Account Number)</span><span class="sxs-lookup"><span data-stu-id="302ae-3202">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="302ae-3203">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-3203">An optional space</span></span> 
- <span data-ttu-id="302ae-3204">1 bis 3 Buchstaben oder Ziffern (Rest des BBAN)</span><span class="sxs-lookup"><span data-stu-id="302ae-3204">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3205">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3205">Checksum</span></span>

<span data-ttu-id="302ae-3206">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3206">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3207">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3207">Definition</span></span>

<span data-ttu-id="302ae-3208">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3208">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3209">Der reguläre Ausdruck Regex_swift findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3209">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3210">Ein Schlüsselwort aus Keyword_swift wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3210">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3211">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3211">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="302ae-3212">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="302ae-3212">Keyword_swift</span></span>

- <span data-ttu-id="302ae-3213">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="302ae-3213">international organization for standardization 9362</span></span> 
- <span data-ttu-id="302ae-3214">iso 9362</span><span class="sxs-lookup"><span data-stu-id="302ae-3214">iso 9362</span></span> 
- <span data-ttu-id="302ae-3215">ISO9362</span><span class="sxs-lookup"><span data-stu-id="302ae-3215">iso9362</span></span> 
- <span data-ttu-id="302ae-3216">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="302ae-3216">swift\#</span></span> 
- <span data-ttu-id="302ae-3217">Swiftcode</span><span class="sxs-lookup"><span data-stu-id="302ae-3217">swiftcode</span></span> 
- <span data-ttu-id="302ae-3218">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="302ae-3218">swiftnumber</span></span> 
- <span data-ttu-id="302ae-3219">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="302ae-3219">swiftroutingnumber</span></span> 
- <span data-ttu-id="302ae-3220">swift code</span><span class="sxs-lookup"><span data-stu-id="302ae-3220">swift code</span></span> 
- <span data-ttu-id="302ae-3221">swift number #</span><span class="sxs-lookup"><span data-stu-id="302ae-3221">swift number #</span></span> 
- <span data-ttu-id="302ae-3222">swift routing number</span><span class="sxs-lookup"><span data-stu-id="302ae-3222">swift routing number</span></span> 
- <span data-ttu-id="302ae-3223">bic number</span><span class="sxs-lookup"><span data-stu-id="302ae-3223">bic number</span></span> 
- <span data-ttu-id="302ae-3224">bic code</span><span class="sxs-lookup"><span data-stu-id="302ae-3224">bic code</span></span> 
- <span data-ttu-id="302ae-3225">BIC\#</span><span class="sxs-lookup"><span data-stu-id="302ae-3225">bic \#</span></span> 
- <span data-ttu-id="302ae-3226">BIC\#</span><span class="sxs-lookup"><span data-stu-id="302ae-3226">bic\#</span></span> 
- <span data-ttu-id="302ae-3227">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="302ae-3227">bank identifier code</span></span> 
- <span data-ttu-id="302ae-3228">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="302ae-3228">標準化9362</span></span> 
- <span data-ttu-id="302ae-3229">迅速 #</span><span class="sxs-lookup"><span data-stu-id="302ae-3229">迅速＃</span></span> 
- <span data-ttu-id="302ae-3230">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="302ae-3230">SWIFTコード</span></span> 
- <span data-ttu-id="302ae-3231">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="302ae-3231">SWIFT番号</span></span> 
- <span data-ttu-id="302ae-3232">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="302ae-3232">迅速なルーティング番号</span></span> 
- <span data-ttu-id="302ae-3233">BIC番号</span><span class="sxs-lookup"><span data-stu-id="302ae-3233">BIC番号</span></span> 
- <span data-ttu-id="302ae-3234">BICコード</span><span class="sxs-lookup"><span data-stu-id="302ae-3234">BICコード</span></span> 
- <span data-ttu-id="302ae-3235">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="302ae-3235">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="302ae-3236">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="302ae-3236">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="302ae-3237">rapide\#</span><span class="sxs-lookup"><span data-stu-id="302ae-3237">rapide \#</span></span> 
- <span data-ttu-id="302ae-3238">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="302ae-3238">code SWIFT</span></span> 
- <span data-ttu-id="302ae-3239">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="302ae-3239">le numéro de swift</span></span> 
- <span data-ttu-id="302ae-3240">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="302ae-3240">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="302ae-3241">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="302ae-3241">le numéro BIC</span></span> 
- <span data-ttu-id="302ae-3242">\#BIC</span><span class="sxs-lookup"><span data-stu-id="302ae-3242">\# BIC</span></span> 
- <span data-ttu-id="302ae-3243">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="302ae-3243">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="302ae-3244">Taiwanesicher Personalausweis</span><span class="sxs-lookup"><span data-stu-id="302ae-3244">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3245">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3245">Format</span></span>

<span data-ttu-id="302ae-3246">Ein Buchstabe (auf Englisch) gefolgt von neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3246">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3247">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3247">Pattern</span></span>

<span data-ttu-id="302ae-3248">Ein Buchstabe (Englisch), gefolgt von neun Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-3248">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="302ae-3249">Ein Buchstabe (Englisch, Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="302ae-3249">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="302ae-3250">Die Ziffer 1 oder 2</span><span class="sxs-lookup"><span data-stu-id="302ae-3250">The digit "1" or "2"</span></span> 
- <span data-ttu-id="302ae-3251">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3251">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3252">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3252">Checksum</span></span>

<span data-ttu-id="302ae-3253">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-3253">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3254">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3254">Definition</span></span>

<span data-ttu-id="302ae-3255">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3255">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3256">Die Funktion Func_taiwanese_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3256">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3257">Ein Schlüsselwort aus Keyword_taiwanese_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3257">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="302ae-3258">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-3258">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3259">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3259">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="302ae-3260">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="302ae-3260">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="302ae-3261">身份證字號</span><span class="sxs-lookup"><span data-stu-id="302ae-3261">身份證字號</span></span> 
- <span data-ttu-id="302ae-3262">身份證</span><span class="sxs-lookup"><span data-stu-id="302ae-3262">身份證</span></span> 
- <span data-ttu-id="302ae-3263">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="302ae-3263">身份證號碼</span></span> 
- <span data-ttu-id="302ae-3264">身份證號</span><span class="sxs-lookup"><span data-stu-id="302ae-3264">身份證號</span></span> 
- <span data-ttu-id="302ae-3265">身分證字號</span><span class="sxs-lookup"><span data-stu-id="302ae-3265">身分證字號</span></span> 
- <span data-ttu-id="302ae-3266">身分證</span><span class="sxs-lookup"><span data-stu-id="302ae-3266">身分證</span></span> 
- <span data-ttu-id="302ae-3267">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="302ae-3267">身分證號碼</span></span> 
- <span data-ttu-id="302ae-3268">身份證號</span><span class="sxs-lookup"><span data-stu-id="302ae-3268">身份證號</span></span> 
- <span data-ttu-id="302ae-3269">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="302ae-3269">身分證統一編號</span></span> 
- <span data-ttu-id="302ae-3270">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="302ae-3270">國民身分證統一編號</span></span> 
- <span data-ttu-id="302ae-3271">簽名</span><span class="sxs-lookup"><span data-stu-id="302ae-3271">簽名</span></span> 
- <span data-ttu-id="302ae-3272">蓋章</span><span class="sxs-lookup"><span data-stu-id="302ae-3272">蓋章</span></span> 
- <span data-ttu-id="302ae-3273">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="302ae-3273">簽名或蓋章</span></span> 
- <span data-ttu-id="302ae-3274">簽章</span><span class="sxs-lookup"><span data-stu-id="302ae-3274">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="302ae-3275">	Taiwan – Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-3275">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3276">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3276">Format</span></span>

- <span data-ttu-id="302ae-3277">Biometrische Passnummer: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3277">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="302ae-3278">Nicht-biometrische Passnummer: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3278">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3279">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3279">Pattern</span></span>
<span data-ttu-id="302ae-3280">Biometrische Passnummer:</span><span class="sxs-lookup"><span data-stu-id="302ae-3280">Biometric passport number:</span></span>
- <span data-ttu-id="302ae-3281">Die Ziffer "3" </span><span class="sxs-lookup"><span data-stu-id="302ae-3281">The digit "3"</span></span> 
- <span data-ttu-id="302ae-3282">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3282">Eight digits</span></span>

<span data-ttu-id="302ae-3283">Nicht-biometrische Passport-Nummer:</span><span class="sxs-lookup"><span data-stu-id="302ae-3283">Non-biometric passport number:</span></span>
- <span data-ttu-id="302ae-3284">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3284">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3285">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3285">Checksum</span></span>

<span data-ttu-id="302ae-3286">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3287">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3287">Definition</span></span>

<span data-ttu-id="302ae-3288">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3289">Der reguläre Ausdruck Regex_taiwan_passport findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3289">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3290">Ein Schlüsselwort aus Keyword_taiwan_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3290">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3291">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3291">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="302ae-3292">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="302ae-3292">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="302ae-3293">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="302ae-3293">ROC passport number</span></span> 
- <span data-ttu-id="302ae-3294">Passport number</span><span class="sxs-lookup"><span data-stu-id="302ae-3294">Passport number</span></span> 
- <span data-ttu-id="302ae-3295">Passport no</span><span class="sxs-lookup"><span data-stu-id="302ae-3295">Passport no</span></span> 
- <span data-ttu-id="302ae-3296">Passport Num</span><span class="sxs-lookup"><span data-stu-id="302ae-3296">Passport Num</span></span> 
- <span data-ttu-id="302ae-3297">Passport #</span><span class="sxs-lookup"><span data-stu-id="302ae-3297">Passport #</span></span> 
- <span data-ttu-id="302ae-3298">护照</span><span class="sxs-lookup"><span data-stu-id="302ae-3298">护照</span></span> 
- <span data-ttu-id="302ae-3299">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="302ae-3299">中華民國護照</span></span> 
- <span data-ttu-id="302ae-3300">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="302ae-3300">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="302ae-3301">Taiwan – Einwohnerzertifikatsnummer (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="302ae-3301">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3302">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3302">Format</span></span>

<span data-ttu-id="302ae-3303">10 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3303">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3304">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3304">Pattern</span></span>

<span data-ttu-id="302ae-3305">10 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-3305">10 letters and digits:</span></span>
- <span data-ttu-id="302ae-3306">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="302ae-3306">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="302ae-3307">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3307">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3308">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3308">Checksum</span></span>

<span data-ttu-id="302ae-3309">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3309">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3310">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3310">Definition</span></span>

<span data-ttu-id="302ae-3311">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3311">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3312">Der reguläre Ausdruck Regex_taiwan_resident_certificate findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3312">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3313">Ein Schlüsselwort aus Keyword_taiwan_resident_certificate wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3313">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3314">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3314">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="302ae-3315">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="302ae-3315">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="302ae-3316">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="302ae-3316">Resident Certificate</span></span> 
- <span data-ttu-id="302ae-3317">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="302ae-3317">Resident Cert</span></span> 
- <span data-ttu-id="302ae-3318">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="302ae-3318">Resident Cert.</span></span> 
- <span data-ttu-id="302ae-3319">Identification card</span><span class="sxs-lookup"><span data-stu-id="302ae-3319">Identification card</span></span> 
- <span data-ttu-id="302ae-3320">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="302ae-3320">Alien Resident Certificate</span></span> 
- <span data-ttu-id="302ae-3321">Bogens</span><span class="sxs-lookup"><span data-stu-id="302ae-3321">ARC</span></span> 
- <span data-ttu-id="302ae-3322">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="302ae-3322">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="302ae-3323">TARC</span><span class="sxs-lookup"><span data-stu-id="302ae-3323">TARC</span></span> 
- <span data-ttu-id="302ae-3324">居留證</span><span class="sxs-lookup"><span data-stu-id="302ae-3324">居留證</span></span> 
- <span data-ttu-id="302ae-3325">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="302ae-3325">外僑居留證</span></span> 
- <span data-ttu-id="302ae-3326">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="302ae-3326">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="302ae-3327">Thai-Populations Identifizierungs Code</span><span class="sxs-lookup"><span data-stu-id="302ae-3327">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3328">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3328">Format</span></span>

<span data-ttu-id="302ae-3329">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3329">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3330">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3330">Pattern</span></span>

<span data-ttu-id="302ae-3331">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-3331">13 digits:</span></span>
- <span data-ttu-id="302ae-3332">Die erste Ziffer ist 0 oder 9.</span><span class="sxs-lookup"><span data-stu-id="302ae-3332">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="302ae-3333">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3333">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3334">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3334">Checksum</span></span>

<span data-ttu-id="302ae-3335">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-3335">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3336">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3336">Definition</span></span>

<span data-ttu-id="302ae-3337">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3337">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3338">Die Funktion Func_Thai_Citizen_Id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3338">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3339">Ein Schlüsselwort aus Keyword_Thai_Citizen_Id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3339">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="302ae-3340">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3340">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3341">Die Funktion Func_Thai_Citizen_Id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3341">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

```
<!-- Thai Citizen ID -->
-<Entity id="44ca9e86-ead7-4c5d-884a-e2eaa401515e" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
      <Match idRef="Keyword_Thai_Citizen_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3342">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3342">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="302ae-3343">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="302ae-3343">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="302ae-3344">ID Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3344">ID Number</span></span>
- <span data-ttu-id="302ae-3345">IdentifikationsNummer</span><span class="sxs-lookup"><span data-stu-id="302ae-3345">Identification Number</span></span>
- <span data-ttu-id="302ae-3346">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="302ae-3346">บัตรประชาชน</span></span>
- <span data-ttu-id="302ae-3347">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="302ae-3347">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="302ae-3348">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="302ae-3348">บัตรประชาชน</span></span>
- <span data-ttu-id="302ae-3349">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="302ae-3349">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="302ae-3350">Türkische nationale IdentifikationsNummer</span><span class="sxs-lookup"><span data-stu-id="302ae-3350">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3351">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3351">Format</span></span>

<span data-ttu-id="302ae-3352">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3352">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3353">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3353">Pattern</span></span>

<span data-ttu-id="302ae-3354">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3354">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3355">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3355">Checksum</span></span>

<span data-ttu-id="302ae-3356">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-3356">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3357">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3357">Definition</span></span>

<span data-ttu-id="302ae-3358">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3358">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3359">Die Funktion Func_Turkish_National_Id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3359">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3360">Ein Schlüsselwort aus Keyword_Turkish_National_Id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3360">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="302ae-3361">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3361">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3362">Die Funktion Func_Turkish_National_Id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3362">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

```
<!-- Turkish National Identity -->
-<Entity id="fb621f20-3876-4cfc-acec-8c8e73ca32c7" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Turkish_National_Id"/>
      <Match idRef="Keyword_Turkish_National_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Turkish_National_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3363">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3363">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="302ae-3364">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="302ae-3364">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="302ae-3365">TC KİMLİK Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3365">TC Kimlik No</span></span>
- <span data-ttu-id="302ae-3366">TC KİMLİK numarası</span><span class="sxs-lookup"><span data-stu-id="302ae-3366">TC Kimlik numarası</span></span>
- <span data-ttu-id="302ae-3367">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="302ae-3367">Vatandaşlık numarası</span></span>
- <span data-ttu-id="302ae-3368">Vatandaşlık Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3368">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="302ae-p141">Britische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3371">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3371">Format</span></span>

<span data-ttu-id="302ae-3372">Kombination aus 18 Buchstaben und Ziffern im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3372">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3373">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3373">Pattern</span></span>

<span data-ttu-id="302ae-3374">18 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="302ae-3374">18 letters and digits:</span></span>
- <span data-ttu-id="302ae-3375">Fünf Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) oder die Ziffer 9 anstelle eines Buchstabens</span><span class="sxs-lookup"><span data-stu-id="302ae-3375">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="302ae-3376">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-3376">One digit</span></span> 
- <span data-ttu-id="302ae-3377">Fünf Ziffern im Datumsformat TTMMJ für das Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="302ae-3377">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="302ae-3378">Zwei Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) oder die Ziffer 9 anstelle eines Buchstabens</span><span class="sxs-lookup"><span data-stu-id="302ae-3378">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="302ae-3379">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3379">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3380">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3380">Checksum</span></span>

<span data-ttu-id="302ae-3381">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-3381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3382">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3382">Definition</span></span>

<span data-ttu-id="302ae-3383">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3383">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3384">Die Funktion Func_uk_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3384">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3385">Ein Schlüsselwort aus Keyword_uk_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3385">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="302ae-3386">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-3386">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3387">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3387">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="302ae-3388">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="302ae-3388">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="302ae-3389">DVLA</span><span class="sxs-lookup"><span data-stu-id="302ae-3389">DVLA</span></span> 
- <span data-ttu-id="302ae-3390">light vans</span><span class="sxs-lookup"><span data-stu-id="302ae-3390">light vans</span></span> 
- <span data-ttu-id="302ae-3391">Quads entwickelt</span><span class="sxs-lookup"><span data-stu-id="302ae-3391">quadbikes</span></span> 
- <span data-ttu-id="302ae-3392">motor cars</span><span class="sxs-lookup"><span data-stu-id="302ae-3392">motor cars</span></span> 
- <span data-ttu-id="302ae-3393">125cc</span><span class="sxs-lookup"><span data-stu-id="302ae-3393">125cc</span></span> 
- <span data-ttu-id="302ae-3394">Beiwagen</span><span class="sxs-lookup"><span data-stu-id="302ae-3394">sidecar</span></span> 
- <span data-ttu-id="302ae-3395">Dreiräder</span><span class="sxs-lookup"><span data-stu-id="302ae-3395">tricycles</span></span> 
- <span data-ttu-id="302ae-3396">Motorrad</span><span class="sxs-lookup"><span data-stu-id="302ae-3396">motorcycles</span></span> 
- <span data-ttu-id="302ae-3397">photocard licence</span><span class="sxs-lookup"><span data-stu-id="302ae-3397">photocard licence</span></span> 
- <span data-ttu-id="302ae-3398">learner drivers</span><span class="sxs-lookup"><span data-stu-id="302ae-3398">learner drivers</span></span> 
- <span data-ttu-id="302ae-3399">licence holder</span><span class="sxs-lookup"><span data-stu-id="302ae-3399">licence holder</span></span> 
- <span data-ttu-id="302ae-3400">licence holders</span><span class="sxs-lookup"><span data-stu-id="302ae-3400">licence holders</span></span> 
- <span data-ttu-id="302ae-3401">driving licences</span><span class="sxs-lookup"><span data-stu-id="302ae-3401">driving licences</span></span> 
- <span data-ttu-id="302ae-3402">driving licence</span><span class="sxs-lookup"><span data-stu-id="302ae-3402">driving licence</span></span> 
- <span data-ttu-id="302ae-3403">dual control car</span><span class="sxs-lookup"><span data-stu-id="302ae-3403">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="302ae-p142">Britische Wählerverzeichnisnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3406">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3406">Format</span></span>

<span data-ttu-id="302ae-3407">Zwei Buchstaben gefolgt von 1-4 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3407">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3408">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3408">Pattern</span></span>

<span data-ttu-id="302ae-3409">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von 1-4 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3409">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3410">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3410">Checksum</span></span>

<span data-ttu-id="302ae-3411">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3411">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3412">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3412">Definition</span></span>

<span data-ttu-id="302ae-3413">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3413">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3414">Der reguläre Ausdruck Regex_uk_electoral findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3414">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3415">Ein Schlüsselwort aus Keyword_uk_electoral wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3415">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-3416">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3416">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="302ae-3417">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="302ae-3417">Keyword_uk_electoral</span></span>

- <span data-ttu-id="302ae-3418">council nomination</span><span class="sxs-lookup"><span data-stu-id="302ae-3418">council nomination</span></span> 
- <span data-ttu-id="302ae-3419">nomination form</span><span class="sxs-lookup"><span data-stu-id="302ae-3419">nomination form</span></span> 
- <span data-ttu-id="302ae-3420">electoral register</span><span class="sxs-lookup"><span data-stu-id="302ae-3420">electoral register</span></span> 
- <span data-ttu-id="302ae-3421">electoral roll</span><span class="sxs-lookup"><span data-stu-id="302ae-3421">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="302ae-p143">Britische National Health Service-Nummer</span><span class="sxs-lookup"><span data-stu-id="302ae-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3424">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3424">Format</span></span>

<span data-ttu-id="302ae-3425">10-17 Ziffern, durch Leerzeichen getrennt</span><span class="sxs-lookup"><span data-stu-id="302ae-3425">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3426">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3426">Pattern</span></span>

<span data-ttu-id="302ae-3427">10 bis 17 Stellen:</span><span class="sxs-lookup"><span data-stu-id="302ae-3427">10-17 digits:</span></span>
- <span data-ttu-id="302ae-3428">3 oder 10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3428">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="302ae-3429">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-3429">A space</span></span> 
- <span data-ttu-id="302ae-3430">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3430">Three digits</span></span> 
- <span data-ttu-id="302ae-3431">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="302ae-3431">A space</span></span> 
- <span data-ttu-id="302ae-3432">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3432">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3433">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3433">Checksum</span></span>

<span data-ttu-id="302ae-3434">Ja</span><span class="sxs-lookup"><span data-stu-id="302ae-3434">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3435">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3435">Definition</span></span>

<span data-ttu-id="302ae-3436">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3436">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3437">Die Funktion Func_uk_nhs_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3437">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3438">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="302ae-3438">One of the following is true:</span></span>
    - <span data-ttu-id="302ae-3439">Ein Schlüsselwort aus Keyword_uk_nhs_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3439">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="302ae-3440">Ein Schlüsselwort aus Keyword_uk_nhs_number1 wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3440">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="302ae-3441">Ein Schlüsselwort aus Keyword_uk_nhs_number_dob wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3441">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="302ae-3442">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="302ae-3442">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-3443">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3443">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="302ae-3444">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="302ae-3444">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="302ae-3445">national health service</span><span class="sxs-lookup"><span data-stu-id="302ae-3445">national health service</span></span> 
- <span data-ttu-id="302ae-3446">NHS</span><span class="sxs-lookup"><span data-stu-id="302ae-3446">nhs</span></span> 
- <span data-ttu-id="302ae-3447">health services authority</span><span class="sxs-lookup"><span data-stu-id="302ae-3447">health services authority</span></span> 
- <span data-ttu-id="302ae-3448">health authority</span><span class="sxs-lookup"><span data-stu-id="302ae-3448">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="302ae-3449">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="302ae-3449">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="302ae-3450">patient id</span><span class="sxs-lookup"><span data-stu-id="302ae-3450">patient id</span></span> 
- <span data-ttu-id="302ae-3451">patient identification</span><span class="sxs-lookup"><span data-stu-id="302ae-3451">patient identification</span></span> 
- <span data-ttu-id="302ae-3452">patient no</span><span class="sxs-lookup"><span data-stu-id="302ae-3452">patient no</span></span> 
- <span data-ttu-id="302ae-3453">patient number</span><span class="sxs-lookup"><span data-stu-id="302ae-3453">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="302ae-3454">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="302ae-3454">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="302ae-3455">GP</span><span class="sxs-lookup"><span data-stu-id="302ae-3455">GP</span></span> 
- <span data-ttu-id="302ae-3456">DOB</span><span class="sxs-lookup"><span data-stu-id="302ae-3456">DOB</span></span> 
- <span data-ttu-id="302ae-3457">D. O. B</span><span class="sxs-lookup"><span data-stu-id="302ae-3457">D.O.B</span></span> 
- <span data-ttu-id="302ae-3458">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="302ae-3458">Date of Birth</span></span> 
- <span data-ttu-id="302ae-3459">Birth Date</span><span class="sxs-lookup"><span data-stu-id="302ae-3459">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="302ae-p144">Britische nationale Versicherungsnummer (NINO)</span><span class="sxs-lookup"><span data-stu-id="302ae-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3462">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3462">Format</span></span>

<span data-ttu-id="302ae-3463">7 Zeichen oder 9 Zeichen voneinander getrennt durch Leerzeichen oder Bindestriche</span><span class="sxs-lookup"><span data-stu-id="302ae-3463">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3464">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3464">Pattern</span></span>

<span data-ttu-id="302ae-3465">Zwei mögliche Muster:</span><span class="sxs-lookup"><span data-stu-id="302ae-3465">Two possible patterns:</span></span>

- <span data-ttu-id="302ae-3466">Zwei Buchstaben (gültige NINOs verwenden nur bestimmte Zeichen in diesem Präfix, die dieses Muster validiert; Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="302ae-3466">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="302ae-3467">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3467">Six digits</span></span>
- <span data-ttu-id="302ae-3468">Entweder "A", "B", "C" oder "'D" (wie das Präfix, nur bestimmte Zeichen sind im Suffix zulässig; Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="302ae-3468">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="302ae-3469">ODER</span><span class="sxs-lookup"><span data-stu-id="302ae-3469">OR</span></span>

- <span data-ttu-id="302ae-3470">Zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="302ae-3470">Two letters</span></span>
- <span data-ttu-id="302ae-3471">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-3471">A space or dash</span></span>
- <span data-ttu-id="302ae-3472">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3472">Two digits</span></span>
- <span data-ttu-id="302ae-3473">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-3473">A space or dash</span></span>
- <span data-ttu-id="302ae-3474">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3474">Two digits</span></span>
- <span data-ttu-id="302ae-3475">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-3475">A space or dash</span></span>
- <span data-ttu-id="302ae-3476">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3476">Two digits</span></span>
- <span data-ttu-id="302ae-3477">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-3477">A space or dash</span></span>
- <span data-ttu-id="302ae-3478">Entweder "A", "B", "C" oder "'D"</span><span class="sxs-lookup"><span data-stu-id="302ae-3478">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3479">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3479">Checksum</span></span>

<span data-ttu-id="302ae-3480">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3480">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3481">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3481">Definition</span></span>

<span data-ttu-id="302ae-3482">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3482">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3483">Die Funktion Func_uk_nino findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3483">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3484">Ein Schlüsselwort aus Keyword_uk_nino wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3484">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="302ae-3485">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3485">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3486">Die Funktion Func_uk_nino findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3486">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3487">Es wurde kein Schlüsselwort aus Keyword_uk_nino gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3487">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-3488">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3488">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="302ae-3489">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="302ae-3489">Keyword_uk_nino</span></span>

- <span data-ttu-id="302ae-3490">national insurance number</span><span class="sxs-lookup"><span data-stu-id="302ae-3490">national insurance number</span></span> 
- <span data-ttu-id="302ae-3491">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="302ae-3491">national insurance contributions</span></span> 
- <span data-ttu-id="302ae-3492">protection act</span><span class="sxs-lookup"><span data-stu-id="302ae-3492">protection act</span></span> 
- <span data-ttu-id="302ae-3493">Versicherung</span><span class="sxs-lookup"><span data-stu-id="302ae-3493">insurance</span></span> 
- <span data-ttu-id="302ae-3494">social security number</span><span class="sxs-lookup"><span data-stu-id="302ae-3494">social security number</span></span> 
- <span data-ttu-id="302ae-3495">insurance application</span><span class="sxs-lookup"><span data-stu-id="302ae-3495">insurance application</span></span> 
- <span data-ttu-id="302ae-3496">medical application</span><span class="sxs-lookup"><span data-stu-id="302ae-3496">medical application</span></span> 
- <span data-ttu-id="302ae-3497">social insurance</span><span class="sxs-lookup"><span data-stu-id="302ae-3497">social insurance</span></span> 
- <span data-ttu-id="302ae-3498">medical attention</span><span class="sxs-lookup"><span data-stu-id="302ae-3498">medical attention</span></span> 
- <span data-ttu-id="302ae-3499">social security</span><span class="sxs-lookup"><span data-stu-id="302ae-3499">social security</span></span> 
- <span data-ttu-id="302ae-3500">great britain</span><span class="sxs-lookup"><span data-stu-id="302ae-3500">great britain</span></span> 
- <span data-ttu-id="302ae-3501">Versicherung</span><span class="sxs-lookup"><span data-stu-id="302ae-3501">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="302ae-p145">US-amerikanische/britische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3504">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3504">Format</span></span>

<span data-ttu-id="302ae-3505">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3505">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3506">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3506">Pattern</span></span>

<span data-ttu-id="302ae-3507">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3507">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3508">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3508">Checksum</span></span>

<span data-ttu-id="302ae-3509">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3509">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3510">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3510">Definition</span></span>

<span data-ttu-id="302ae-3511">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3511">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3512">Die Funktion Func_usa_uk_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3512">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3513">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3513">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3514">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3514">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="302ae-3515">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="302ae-3515">Keyword_passport</span></span>

- <span data-ttu-id="302ae-3516">Passport Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3516">Passport Number</span></span> 
- <span data-ttu-id="302ae-3517">Passport No</span><span class="sxs-lookup"><span data-stu-id="302ae-3517">Passport No</span></span> 
- <span data-ttu-id="302ae-3518">Passport#</span><span class="sxs-lookup"><span data-stu-id="302ae-3518">Passport #</span></span> 
- <span data-ttu-id="302ae-3519">Pass</span><span class="sxs-lookup"><span data-stu-id="302ae-3519">Passport#</span></span> 
- <span data-ttu-id="302ae-3520">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="302ae-3520">PassportID</span></span> 
- <span data-ttu-id="302ae-3521">Passportno</span><span class="sxs-lookup"><span data-stu-id="302ae-3521">Passportno</span></span> 
- <span data-ttu-id="302ae-3522">passportnumber</span><span class="sxs-lookup"><span data-stu-id="302ae-3522">passportnumber</span></span> 
- <span data-ttu-id="302ae-3523">パスポート</span><span class="sxs-lookup"><span data-stu-id="302ae-3523">パスポート</span></span> 
- <span data-ttu-id="302ae-3524">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="302ae-3524">パスポート番号</span></span> 
- <span data-ttu-id="302ae-3525">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="302ae-3525">パスポートのNum</span></span> 
- <span data-ttu-id="302ae-3526">パスポート #</span><span class="sxs-lookup"><span data-stu-id="302ae-3526">パスポート＃</span></span> 
- <span data-ttu-id="302ae-3527">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="302ae-3527">Numéro de passeport</span></span> 
- <span data-ttu-id="302ae-3528">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="302ae-3528">Passeport n °</span></span> 
- <span data-ttu-id="302ae-3529">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="302ae-3529">Passeport Non</span></span> 
- <span data-ttu-id="302ae-3530">Passeport#</span><span class="sxs-lookup"><span data-stu-id="302ae-3530">Passeport #</span></span> 
- <span data-ttu-id="302ae-3531">Passeport</span><span class="sxs-lookup"><span data-stu-id="302ae-3531">Passeport#</span></span> 
- <span data-ttu-id="302ae-3532">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="302ae-3532">PasseportNon</span></span> 
- <span data-ttu-id="302ae-3533">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="302ae-3533">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="302ae-3534">US-Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="302ae-3534">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3535">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3535">Format</span></span>

<span data-ttu-id="302ae-3536">8-17 Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3536">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3537">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3537">Pattern</span></span>

<span data-ttu-id="302ae-3538">8-17 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3538">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3539">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3539">Checksum</span></span>

<span data-ttu-id="302ae-3540">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3540">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3541">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3541">Definition</span></span>

<span data-ttu-id="302ae-3542">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3542">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3543">Der reguläre Ausdruck Regex_usa_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3543">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3544">Ein Schlüsselwort aus Keyword_usa_Bank_Account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3544">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="302ae-3545">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3545">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="302ae-3546">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="302ae-3546">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="302ae-3547">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3547">Checking Account Number</span></span> 
- <span data-ttu-id="302ae-3548">Checking Account</span><span class="sxs-lookup"><span data-stu-id="302ae-3548">Checking Account</span></span> 
- <span data-ttu-id="302ae-3549">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="302ae-3549">Checking Account #</span></span> 
- <span data-ttu-id="302ae-3550">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3550">Checking Acct Number</span></span> 
- <span data-ttu-id="302ae-3551">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="302ae-3551">Checking Acct #</span></span> 
- <span data-ttu-id="302ae-3552">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="302ae-3552">Checking Acct No.</span></span> 
- <span data-ttu-id="302ae-3553">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="302ae-3553">Checking Account No.</span></span> 
- <span data-ttu-id="302ae-3554">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3554">Bank Account Number</span></span> 
- <span data-ttu-id="302ae-3555">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="302ae-3555">Bank Account #</span></span> 
- <span data-ttu-id="302ae-3556">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3556">Bank Acct Number</span></span> 
- <span data-ttu-id="302ae-3557">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="302ae-3557">Bank Acct #</span></span> 
- <span data-ttu-id="302ae-3558">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="302ae-3558">Bank Acct No.</span></span> 
- <span data-ttu-id="302ae-3559">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="302ae-3559">Bank Account No.</span></span> 
- <span data-ttu-id="302ae-3560">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3560">Savings Account Number</span></span> 
- <span data-ttu-id="302ae-3561">Savings Account</span><span class="sxs-lookup"><span data-stu-id="302ae-3561">Savings Account.</span></span> 
- <span data-ttu-id="302ae-3562">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="302ae-3562">Savings Account #</span></span> 
- <span data-ttu-id="302ae-3563">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3563">Savings Acct Number</span></span> 
- <span data-ttu-id="302ae-3564">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="302ae-3564">Savings Acct #</span></span> 
- <span data-ttu-id="302ae-3565">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="302ae-3565">Savings Acct No.</span></span> 
- <span data-ttu-id="302ae-3566">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="302ae-3566">Savings Account No.</span></span> 
- <span data-ttu-id="302ae-3567">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3567">Debit Account Number</span></span> 
- <span data-ttu-id="302ae-3568">Debit Account</span><span class="sxs-lookup"><span data-stu-id="302ae-3568">Debit Account</span></span> 
- <span data-ttu-id="302ae-3569">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="302ae-3569">Debit Account #</span></span> 
- <span data-ttu-id="302ae-3570">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="302ae-3570">Debit Acct Number</span></span> 
- <span data-ttu-id="302ae-3571">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="302ae-3571">Debit Acct #</span></span> 
- <span data-ttu-id="302ae-3572">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="302ae-3572">Debit Acct No.</span></span> 
- <span data-ttu-id="302ae-3573">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="302ae-3573">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="302ae-3574">US-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-3574">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3575">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3575">Format</span></span>

<span data-ttu-id="302ae-3576">Abhängig vom Bundesstaat</span><span class="sxs-lookup"><span data-stu-id="302ae-3576">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3577">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3577">Pattern</span></span>

<span data-ttu-id="302ae-3578">Abhängig vom Bundesstaat – am Beispiel für New York:</span><span class="sxs-lookup"><span data-stu-id="302ae-3578">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="302ae-3579">Neun Ziffern, die wie DDD DDD DDD formatiert sind, stimmen überein.</span><span class="sxs-lookup"><span data-stu-id="302ae-3579">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="302ae-3580">Neun Ziffern wie ddddddddd werden nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3580">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3581">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3581">Checksum</span></span>

<span data-ttu-id="302ae-3582">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3582">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3583">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3583">Definition</span></span>

<span data-ttu-id="302ae-3584">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3585">Die Funktion Func_new_york_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3585">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3586">Ein Schlüsselwort aus Keyword_[state_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3586">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="302ae-3587">Ein Schlüsselwort aus Keyword_us_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3587">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="302ae-3588">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3588">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3589">Die Funktion Func_new_york_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3589">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3590">Ein Schlüsselwort aus Keyword_[state_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3590">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="302ae-3591">Ein Schlüsselwort aus Keyword_us_drivers_license_abbreviations wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3591">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="302ae-3592">Es wurde kein Schlüsselwort aus Keyword_us_drivers_license gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3592">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-3593">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3593">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="302ae-3594">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="302ae-3594">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="302ae-3595">DL</span><span class="sxs-lookup"><span data-stu-id="302ae-3595">DL</span></span> 
- <span data-ttu-id="302ae-3596">DLS</span><span class="sxs-lookup"><span data-stu-id="302ae-3596">DLS</span></span> 
- <span data-ttu-id="302ae-3597">CDL</span><span class="sxs-lookup"><span data-stu-id="302ae-3597">CDL</span></span> 
- <span data-ttu-id="302ae-3598">CDLS</span><span class="sxs-lookup"><span data-stu-id="302ae-3598">CDLS</span></span> 
- <span data-ttu-id="302ae-3599">ID</span><span class="sxs-lookup"><span data-stu-id="302ae-3599">ID</span></span> 
- <span data-ttu-id="302ae-3600">IDs</span><span class="sxs-lookup"><span data-stu-id="302ae-3600">IDs</span></span> 
- <span data-ttu-id="302ae-3601">DL</span><span class="sxs-lookup"><span data-stu-id="302ae-3601">DL#</span></span> 
- <span data-ttu-id="302ae-3602">DLS</span><span class="sxs-lookup"><span data-stu-id="302ae-3602">DLS#</span></span> 
- <span data-ttu-id="302ae-3603">CDL</span><span class="sxs-lookup"><span data-stu-id="302ae-3603">CDL#</span></span> 
- <span data-ttu-id="302ae-3604">CDLS</span><span class="sxs-lookup"><span data-stu-id="302ae-3604">CDLS#</span></span> 
- <span data-ttu-id="302ae-3605">ID</span><span class="sxs-lookup"><span data-stu-id="302ae-3605">ID#</span></span>
- <span data-ttu-id="302ae-3606">IDs</span><span class="sxs-lookup"><span data-stu-id="302ae-3606">IDs#</span></span> 
- <span data-ttu-id="302ae-3607">ID number</span><span class="sxs-lookup"><span data-stu-id="302ae-3607">ID number</span></span> 
- <span data-ttu-id="302ae-3608">ID numbers</span><span class="sxs-lookup"><span data-stu-id="302ae-3608">ID numbers</span></span> 
- <span data-ttu-id="302ae-3609">LIC</span><span class="sxs-lookup"><span data-stu-id="302ae-3609">LIC</span></span> 
- <span data-ttu-id="302ae-3610">LIC</span><span class="sxs-lookup"><span data-stu-id="302ae-3610">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="302ae-3611">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="302ae-3611">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="302ae-3612">DriverLic</span><span class="sxs-lookup"><span data-stu-id="302ae-3612">DriverLic</span></span> 
- <span data-ttu-id="302ae-3613">DriverLics</span><span class="sxs-lookup"><span data-stu-id="302ae-3613">DriverLics</span></span> 
- <span data-ttu-id="302ae-3614">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="302ae-3614">DriverLicense</span></span> 
- <span data-ttu-id="302ae-3615">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="302ae-3615">DriverLicenses</span></span> 
- <span data-ttu-id="302ae-3616">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-3616">Driver Lic</span></span> 
- <span data-ttu-id="302ae-3617">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-3617">Driver Lics</span></span> 
- <span data-ttu-id="302ae-3618">Driver License</span><span class="sxs-lookup"><span data-stu-id="302ae-3618">Driver License</span></span> 
- <span data-ttu-id="302ae-3619">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-3619">Driver Licenses</span></span> 
- <span data-ttu-id="302ae-3620">DriversLic</span><span class="sxs-lookup"><span data-stu-id="302ae-3620">DriversLic</span></span> 
- <span data-ttu-id="302ae-3621">DriversLics</span><span class="sxs-lookup"><span data-stu-id="302ae-3621">DriversLics</span></span> 
- <span data-ttu-id="302ae-3622">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="302ae-3622">DriversLicense</span></span> 
- <span data-ttu-id="302ae-3623">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="302ae-3623">DriversLicenses</span></span> 
- <span data-ttu-id="302ae-3624">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-3624">Drivers Lic</span></span> 
- <span data-ttu-id="302ae-3625">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-3625">Drivers Lics</span></span> 
- <span data-ttu-id="302ae-3626">Drivers License</span><span class="sxs-lookup"><span data-stu-id="302ae-3626">Drivers License</span></span> 
- <span data-ttu-id="302ae-3627">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-3627">Drivers Licenses</span></span> 
- <span data-ttu-id="302ae-3628">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-3628">Driver'Lic</span></span> 
- <span data-ttu-id="302ae-3629">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-3629">Driver'Lics</span></span> 
- <span data-ttu-id="302ae-3630">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="302ae-3630">Driver'License</span></span> 
- <span data-ttu-id="302ae-3631">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-3631">Driver'Licenses</span></span> 
- <span data-ttu-id="302ae-3632">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-3632">Driver' Lic</span></span> 
- <span data-ttu-id="302ae-3633">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-3633">Driver' Lics</span></span> 
- <span data-ttu-id="302ae-3634">Driver' License</span><span class="sxs-lookup"><span data-stu-id="302ae-3634">Driver' License</span></span> 
- <span data-ttu-id="302ae-3635">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-3635">Driver' Licenses</span></span>
- <span data-ttu-id="302ae-3636">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="302ae-3636">Driver'sLic</span></span> 
- <span data-ttu-id="302ae-3637">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="302ae-3637">Driver'sLics</span></span> 
- <span data-ttu-id="302ae-3638">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="302ae-3638">Driver'sLicense</span></span> 
- <span data-ttu-id="302ae-3639">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="302ae-3639">Driver'sLicenses</span></span> 
- <span data-ttu-id="302ae-3640">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="302ae-3640">Driver's Lic</span></span> 
- <span data-ttu-id="302ae-3641">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="302ae-3641">Driver's Lics</span></span> 
- <span data-ttu-id="302ae-3642">Driver's License</span><span class="sxs-lookup"><span data-stu-id="302ae-3642">Driver's License</span></span> 
- <span data-ttu-id="302ae-3643">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-3643">Driver's Licenses</span></span> 
- <span data-ttu-id="302ae-3644">identification number</span><span class="sxs-lookup"><span data-stu-id="302ae-3644">identification number</span></span> 
- <span data-ttu-id="302ae-3645">identification numbers</span><span class="sxs-lookup"><span data-stu-id="302ae-3645">identification numbers</span></span> 
- <span data-ttu-id="302ae-3646">identification#</span><span class="sxs-lookup"><span data-stu-id="302ae-3646">identification #</span></span> 
- <span data-ttu-id="302ae-3647">id card</span><span class="sxs-lookup"><span data-stu-id="302ae-3647">id card</span></span> 
- <span data-ttu-id="302ae-3648">id cards</span><span class="sxs-lookup"><span data-stu-id="302ae-3648">id cards</span></span> 
- <span data-ttu-id="302ae-3649">identification card</span><span class="sxs-lookup"><span data-stu-id="302ae-3649">identification card</span></span> 
- <span data-ttu-id="302ae-3650">identification cards</span><span class="sxs-lookup"><span data-stu-id="302ae-3650">identification cards</span></span> 
- <span data-ttu-id="302ae-3651">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="302ae-3651">DriverLic#</span></span> 
- <span data-ttu-id="302ae-3652">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="302ae-3652">DriverLics#</span></span> 
- <span data-ttu-id="302ae-3653">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="302ae-3653">DriverLicense#</span></span> 
- <span data-ttu-id="302ae-3654">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="302ae-3654">DriverLicenses#</span></span> 
- <span data-ttu-id="302ae-3655">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-3655">Driver Lic#</span></span> 
- <span data-ttu-id="302ae-3656">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-3656">Driver Lics#</span></span> 
- <span data-ttu-id="302ae-3657">Driver License#</span><span class="sxs-lookup"><span data-stu-id="302ae-3657">Driver License#</span></span> 
- <span data-ttu-id="302ae-3658">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-3658">Driver Licenses#</span></span> 
- <span data-ttu-id="302ae-3659">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="302ae-3659">DriversLic#</span></span> 
- <span data-ttu-id="302ae-3660">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="302ae-3660">DriversLics#</span></span> 
- <span data-ttu-id="302ae-3661">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="302ae-3661">DriversLicense#</span></span> 
- <span data-ttu-id="302ae-3662">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="302ae-3662">DriversLicenses#</span></span> 
- <span data-ttu-id="302ae-3663">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-3663">Drivers Lic#</span></span> 
- <span data-ttu-id="302ae-3664">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-3664">Drivers Lics#</span></span> 
- <span data-ttu-id="302ae-3665">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="302ae-3665">Drivers License#</span></span> 
- <span data-ttu-id="302ae-3666">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-3666">Drivers Licenses#</span></span> 
- <span data-ttu-id="302ae-3667">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="302ae-3667">Driver'Lic#</span></span> 
- <span data-ttu-id="302ae-3668">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="302ae-3668">Driver'Lics#</span></span> 
- <span data-ttu-id="302ae-3669">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="302ae-3669">Driver'License#</span></span> 
- <span data-ttu-id="302ae-3670">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="302ae-3670">Driver'Licenses#</span></span> 
- <span data-ttu-id="302ae-3671">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-3671">Driver' Lic#</span></span> 
- <span data-ttu-id="302ae-3672">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-3672">Driver' Lics#</span></span> 
- <span data-ttu-id="302ae-3673">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="302ae-3673">Driver' License#</span></span> 
- <span data-ttu-id="302ae-3674">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-3674">Driver' Licenses#</span></span> 
- <span data-ttu-id="302ae-3675">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="302ae-3675">Driver'sLic#</span></span> 
- <span data-ttu-id="302ae-3676">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="302ae-3676">Driver'sLics#</span></span> 
- <span data-ttu-id="302ae-3677">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="302ae-3677">Driver'sLicense#</span></span> 
- <span data-ttu-id="302ae-3678">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="302ae-3678">Driver'sLicenses#</span></span> 
- <span data-ttu-id="302ae-3679">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="302ae-3679">Driver's Lic#</span></span> 
- <span data-ttu-id="302ae-3680">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="302ae-3680">Driver's Lics#</span></span> 
- <span data-ttu-id="302ae-3681">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="302ae-3681">Driver's License#</span></span> 
- <span data-ttu-id="302ae-3682">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="302ae-3682">Driver's Licenses#</span></span> 
- <span data-ttu-id="302ae-3683">id card#</span><span class="sxs-lookup"><span data-stu-id="302ae-3683">id card#</span></span> 
- <span data-ttu-id="302ae-3684">id cards#</span><span class="sxs-lookup"><span data-stu-id="302ae-3684">id cards#</span></span> 
- <span data-ttu-id="302ae-3685">identification card#</span><span class="sxs-lookup"><span data-stu-id="302ae-3685">identification card#</span></span> 
- <span data-ttu-id="302ae-3686">identification cards#</span><span class="sxs-lookup"><span data-stu-id="302ae-3686">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="302ae-3687">Keyword_ [state_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="302ae-3687">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="302ae-3688">Abkürzung für Bundesstaat (z. B. „NY“)</span><span class="sxs-lookup"><span data-stu-id="302ae-3688">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="302ae-3689">Name des Bundesstaats (z. B. „New York“)</span><span class="sxs-lookup"><span data-stu-id="302ae-3689">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="302ae-3690">US-Steueridentifikationsnummer (ITIN)</span><span class="sxs-lookup"><span data-stu-id="302ae-3690">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3691">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3691">Format</span></span>

<span data-ttu-id="302ae-3692">Neun Ziffern, die mit "9" beginnen und "7" oder "8" als vierte Ziffer enthalten, optional mit Leerzeichen oder Bindestrichen formatiert</span><span class="sxs-lookup"><span data-stu-id="302ae-3692">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3693">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3693">Pattern</span></span>

<span data-ttu-id="302ae-3694">Formatiert</span><span class="sxs-lookup"><span data-stu-id="302ae-3694">Formatted:</span></span>
- <span data-ttu-id="302ae-3695">Die Ziffer 9</span><span class="sxs-lookup"><span data-stu-id="302ae-3695">The digit "9"</span></span> 
- <span data-ttu-id="302ae-3696">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3696">Two digits</span></span> 
- <span data-ttu-id="302ae-3697">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-3697">A space or dash</span></span> 
- <span data-ttu-id="302ae-3698">Eine 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="302ae-3698">A "7" or "8"</span></span> 
- <span data-ttu-id="302ae-3699">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="302ae-3699">A digit</span></span> 
- <span data-ttu-id="302ae-3700">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="302ae-3700">A space, or dash</span></span> 
- <span data-ttu-id="302ae-3701">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3701">Four digits</span></span>

<span data-ttu-id="302ae-3702">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="302ae-3702">Unformatted:</span></span>
- <span data-ttu-id="302ae-3703">Die Ziffer 9</span><span class="sxs-lookup"><span data-stu-id="302ae-3703">The digit "9"</span></span> 
- <span data-ttu-id="302ae-3704">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3704">Two digits</span></span> 
- <span data-ttu-id="302ae-3705">Eine 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="302ae-3705">A "7" or "8"</span></span> 
- <span data-ttu-id="302ae-3706">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="302ae-3706">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3707">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3707">Checksum</span></span>

<span data-ttu-id="302ae-3708">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3708">No</span></span>

### <a name="definition"></a><span data-ttu-id="302ae-3709">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3709">Definition</span></span>

<span data-ttu-id="302ae-3710">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3710">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3711">Die Funktion Func_formatted_itin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3711">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3712">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="302ae-3712">At least one of the following is true:</span></span>
    - <span data-ttu-id="302ae-3713">Ein Schlüsselwort aus Keyword_itin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3713">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="302ae-3714">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="302ae-3714">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="302ae-3715">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="302ae-3715">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="302ae-3716">Ein Schlüsselwort aus Keyword_itin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3716">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="302ae-3717">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3717">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3718">Die Funktion Func_unformatted_itin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3718">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3719">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="302ae-3719">At least one of the following is true:</span></span>
    - <span data-ttu-id="302ae-3720">Ein Schlüsselwort aus Keyword_itin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3720">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="302ae-3721">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="302ae-3721">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="302ae-3722">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="302ae-3722">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-3723">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3723">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="302ae-3724">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="302ae-3724">Keyword_itin</span></span>

- <span data-ttu-id="302ae-3725">Steuer</span><span class="sxs-lookup"><span data-stu-id="302ae-3725">taxpayer</span></span> 
- <span data-ttu-id="302ae-3726">tax id</span><span class="sxs-lookup"><span data-stu-id="302ae-3726">tax id</span></span> 
- <span data-ttu-id="302ae-3727">tax identification</span><span class="sxs-lookup"><span data-stu-id="302ae-3727">tax identification</span></span> 
- <span data-ttu-id="302ae-3728">Itin</span><span class="sxs-lookup"><span data-stu-id="302ae-3728">itin</span></span> 
- <span data-ttu-id="302ae-3729">SSN</span><span class="sxs-lookup"><span data-stu-id="302ae-3729">ssn</span></span> 
- <span data-ttu-id="302ae-3730">Zinn</span><span class="sxs-lookup"><span data-stu-id="302ae-3730">tin</span></span> 
- <span data-ttu-id="302ae-3731">social security</span><span class="sxs-lookup"><span data-stu-id="302ae-3731">social security</span></span> 
- <span data-ttu-id="302ae-3732">tax payer</span><span class="sxs-lookup"><span data-stu-id="302ae-3732">tax payer</span></span> 
- <span data-ttu-id="302ae-3733">itins</span><span class="sxs-lookup"><span data-stu-id="302ae-3733">itins</span></span> 
- <span data-ttu-id="302ae-3734">getaxit</span><span class="sxs-lookup"><span data-stu-id="302ae-3734">taxid</span></span> 
- <span data-ttu-id="302ae-3735">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="302ae-3735">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="302ae-3736">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="302ae-3736">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="302ae-3737">License</span><span class="sxs-lookup"><span data-stu-id="302ae-3737">License</span></span> 
- <span data-ttu-id="302ae-3738">DL</span><span class="sxs-lookup"><span data-stu-id="302ae-3738">DL</span></span> 
- <span data-ttu-id="302ae-3739">DOB</span><span class="sxs-lookup"><span data-stu-id="302ae-3739">DOB</span></span> 
- <span data-ttu-id="302ae-3740">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="302ae-3740">Birthdate</span></span> 
- <span data-ttu-id="302ae-3741">Geburtstag</span><span class="sxs-lookup"><span data-stu-id="302ae-3741">Birthday</span></span> 
- <span data-ttu-id="302ae-3742">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="302ae-3742">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="302ae-3743">US-Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="302ae-3743">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="302ae-3744">Format</span><span class="sxs-lookup"><span data-stu-id="302ae-3744">Format</span></span>

<span data-ttu-id="302ae-3745">9 Ziffern in formatiertem oder unformatiertem Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3745">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="302ae-3746">Wenn vor Mitte 2011 ausgegeben wird, hat eine SSN eine starke Formatierung, bei der bestimmte Teile der Nummer in bestimmte Bereiche eingehen müssen, um gültig zu sein (es gibt jedoch keine Prüfsumme).</span><span class="sxs-lookup"><span data-stu-id="302ae-3746">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="302ae-3747">Muster</span><span class="sxs-lookup"><span data-stu-id="302ae-3747">Pattern</span></span>

<span data-ttu-id="302ae-3748">Vier Funktionen suchen nach SSNs in vier verschiedenen Mustern:</span><span class="sxs-lookup"><span data-stu-id="302ae-3748">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="302ae-3749">Func_ssn findet SSNs mit einer starken Formatierung vor 2011, die mit Bindestrichen oder Leerzeichen (DDD-DD-dddd oder DDD DD dddd) formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="302ae-3749">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="302ae-3750">Func_unformatted_ssn findet SSNs mit einer starken Formatierung vor 2011, die unformatiert sind, als neun aufeinanderfolgende Ziffern (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="302ae-3750">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="302ae-3751">Func_randomized_formatted_ssn findet Post-2011 SSNs, die mit Bindestrichen oder Leerzeichen (DDD-DD-dddd oder DDD DD dddd) formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="302ae-3751">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="302ae-3752">Func_randomized_unformatted_ssn findet Post-2011 SSNs, die unformatiert sind, als neun aufeinanderfolgende Ziffern (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="302ae-3752">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="302ae-3753">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="302ae-3753">Checksum</span></span>

<span data-ttu-id="302ae-3754">Nein</span><span class="sxs-lookup"><span data-stu-id="302ae-3754">No</span></span>


### <a name="definition"></a><span data-ttu-id="302ae-3755">Definition</span><span class="sxs-lookup"><span data-stu-id="302ae-3755">Definition</span></span>

<span data-ttu-id="302ae-3756">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3756">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3757">Die Funktion Func_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3757">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3758">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3758">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="302ae-3759">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3759">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3760">Die Funktion Func_unformatted_ssn sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3760">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3761">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3761">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="302ae-3762">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3762">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3763">Die Funktion Func_randomized_formatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3763">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3764">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3764">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="302ae-3765">Die Funktion Func_ssn findet keine Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3765">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="302ae-3766">Eine DLP-Richtlinie ist zu 55 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="302ae-3766">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="302ae-3767">Die Funktion Func_randomized_unformatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3767">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="302ae-3768">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="302ae-3768">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="302ae-3769">Die Funktion Func_unformatted_ssn findet keine Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="302ae-3769">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="302ae-3770">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="302ae-3770">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="302ae-3771">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="302ae-3771">Keyword_ssn</span></span>

- <span data-ttu-id="302ae-3772">Social Security</span><span class="sxs-lookup"><span data-stu-id="302ae-3772">Social Security</span></span> 
- <span data-ttu-id="302ae-3773">Social Security#</span><span class="sxs-lookup"><span data-stu-id="302ae-3773">Social Security#</span></span> 
- <span data-ttu-id="302ae-3774">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="302ae-3774">Soc Sec</span></span> 
- <span data-ttu-id="302ae-3775">SSN</span><span class="sxs-lookup"><span data-stu-id="302ae-3775">SSN</span></span> 
- <span data-ttu-id="302ae-3776">SSNS</span><span class="sxs-lookup"><span data-stu-id="302ae-3776">SSNS</span></span> 
- <span data-ttu-id="302ae-3777">SSN</span><span class="sxs-lookup"><span data-stu-id="302ae-3777">SSN#</span></span> 
- <span data-ttu-id="302ae-3778">SS</span><span class="sxs-lookup"><span data-stu-id="302ae-3778">SS#</span></span> 
- <span data-ttu-id="302ae-3779">SSID</span><span class="sxs-lookup"><span data-stu-id="302ae-3779">SSID</span></span> 
   

