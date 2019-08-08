---
title: Wonach die Typen von vertraulichen Informationen suchen
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 05/20/2019
audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: Die Verhinderung von Datenverlust (Data Loss &amp; Prevention, DLP) im Office 365 Security Compliance Center umfasst 80 Typen für vertrauliche Informationen, die Sie in ihren DLP-Richtlinien verwenden können. Dieses Thema enthält eine Liste aller dieser vertraulichen Informationstypen und zeigt, was eine DLP-Richtlinie sucht, wenn sie den jeweiligen Typen erkennt.
ms.openlocfilehash: 7f5c879b35f77ef142b8c45965357715f577832e
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230379"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="e5c57-104">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="e5c57-104">What the sensitive information types look for</span></span>

<span data-ttu-id="e5c57-105">Die Verhinderung von Datenverlust (Data Loss &amp; Prevention, DLP) im Office 365 Security Compliance Center umfasst viele Arten von vertraulichen Informationen, die Sie in ihren DLP-Richtlinien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e5c57-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="e5c57-106">Dieses Thema enthält eine Liste aller dieser vertraulichen Informationstypen und zeigt, was eine DLP-Richtlinie sucht, wenn sie den jeweiligen Typen erkennt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="e5c57-107">Ein vertraulicher Informationstyp wird durch ein Muster definiert, das durch einen regulären Ausdruck oder eine Funktion identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e5c57-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="e5c57-108">Darüber hinaus können auch belegende Hinweise wie Schlüsselwörter oder Prüfsummen zum Identifizieren eines Typs vertraulicher Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="e5c57-109">Beim Auswertungsprozess können auch die Zuverlässigkeitsstufe und die Näherung herangezogen werden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="e5c57-110">ABA Routing Number (US-Bankleitzahl)</span><span class="sxs-lookup"><span data-stu-id="e5c57-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-111">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-111">Format</span></span>

<span data-ttu-id="e5c57-112">9 Ziffern in formatiertem oder unformatiertem Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-113">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-113">Pattern</span></span>

<span data-ttu-id="e5c57-114">Formatiert</span><span class="sxs-lookup"><span data-stu-id="e5c57-114">Formatted:</span></span>
- <span data-ttu-id="e5c57-115">Vier Ziffern, beginnend mit 0, 1, 2, 3, 6, 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="e5c57-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="e5c57-116">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-116">A hyphen</span></span>
- <span data-ttu-id="e5c57-117">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-117">Four digits</span></span>
- <span data-ttu-id="e5c57-118">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-118">A hyphen</span></span>
- <span data-ttu-id="e5c57-119">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-119">A digit</span></span>

<span data-ttu-id="e5c57-120">Unformatiert: 9 aufeinanderfolgende Ziffern, beginnend mit 0, 1, 2, 3, 6, 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="e5c57-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="e5c57-121">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-121">Checksum</span></span>

<span data-ttu-id="e5c57-122">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-123">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-123">Definition</span></span>

<span data-ttu-id="e5c57-124">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-125">Die Funktion Func_aba_routing findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-126">Ein Schlüsselwort aus Keyword_ABA_Routing wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="e5c57-127">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-127">Keywords</span></span>

#### <a name="keyword_aba_routing"></a><span data-ttu-id="e5c57-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="e5c57-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="e5c57-129">ABA</span><span class="sxs-lookup"><span data-stu-id="e5c57-129">aba</span></span>
- <span data-ttu-id="e5c57-130">aba #</span><span class="sxs-lookup"><span data-stu-id="e5c57-130">aba #</span></span>
- <span data-ttu-id="e5c57-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="e5c57-131">aba routing #</span></span>
- <span data-ttu-id="e5c57-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="e5c57-132">aba routing number</span></span>
- <span data-ttu-id="e5c57-133">ABA #</span><span class="sxs-lookup"><span data-stu-id="e5c57-133">aba#</span></span>
- <span data-ttu-id="e5c57-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="e5c57-134">abarouting#</span></span>
- <span data-ttu-id="e5c57-135">aba number</span><span class="sxs-lookup"><span data-stu-id="e5c57-135">aba number</span></span>
- <span data-ttu-id="e5c57-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-136">abaroutingnumber</span></span>
- <span data-ttu-id="e5c57-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="e5c57-137">american bank association routing #</span></span>
- <span data-ttu-id="e5c57-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="e5c57-138">american bank association routing number</span></span>
- <span data-ttu-id="e5c57-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="e5c57-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="e5c57-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="e5c57-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="e5c57-141">bank routing number</span></span>
- <span data-ttu-id="e5c57-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="e5c57-142">bankrouting#</span></span>
- <span data-ttu-id="e5c57-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-143">bankroutingnumber</span></span>
- <span data-ttu-id="e5c57-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="e5c57-144">routing transit number</span></span>
- <span data-ttu-id="e5c57-145">RTN</span><span class="sxs-lookup"><span data-stu-id="e5c57-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="e5c57-146">Argentina National Identity (DNI) Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-147">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-147">Format</span></span>

<span data-ttu-id="e5c57-148">Acht Ziffern, durch Punkte getrennt</span><span class="sxs-lookup"><span data-stu-id="e5c57-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-149">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-149">Pattern</span></span>

<span data-ttu-id="e5c57-150">Acht Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-150">Eight digits:</span></span>
- <span data-ttu-id="e5c57-151">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-151">Two digits</span></span>
- <span data-ttu-id="e5c57-152">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="e5c57-152">A period</span></span>
- <span data-ttu-id="e5c57-153">Drei Ziffern </span><span class="sxs-lookup"><span data-stu-id="e5c57-153">Three digits</span></span>
- <span data-ttu-id="e5c57-154">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="e5c57-154">A period</span></span>
- <span data-ttu-id="e5c57-155">Drei Ziffern </span><span class="sxs-lookup"><span data-stu-id="e5c57-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-156">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-156">Checksum</span></span>

<span data-ttu-id="e5c57-157">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-158">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-158">Definition</span></span>

<span data-ttu-id="e5c57-159">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-160">Der reguläre Ausdruck Regex_argentina_national_id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-161">Ein Schlüsselwort aus Keyword_argentina_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-162">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-162">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="e5c57-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="e5c57-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="e5c57-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="e5c57-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="e5c57-165">Identität</span><span class="sxs-lookup"><span data-stu-id="e5c57-165">Identity</span></span> 
- <span data-ttu-id="e5c57-166">Identification National Identity Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="e5c57-167">DNI</span><span class="sxs-lookup"><span data-stu-id="e5c57-167">DNI</span></span> 
- <span data-ttu-id="e5c57-168">Nic-nationales Personenregister</span><span class="sxs-lookup"><span data-stu-id="e5c57-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="e5c57-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="e5c57-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="e5c57-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="e5c57-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="e5c57-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="e5c57-171">Identidad</span></span> 
- <span data-ttu-id="e5c57-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="e5c57-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="e5c57-173">Australische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-174">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-174">Format</span></span>

<span data-ttu-id="e5c57-175">6-10 Stellen mit oder ohne Bankfilialnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-176">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-176">Pattern</span></span>

<span data-ttu-id="e5c57-177">Kontonummer hat 6-10 Stellen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="e5c57-178">Australische Bankleitzahl:</span><span class="sxs-lookup"><span data-stu-id="e5c57-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="e5c57-179">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-179">Three digits</span></span> 
- <span data-ttu-id="e5c57-180">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-180">A hyphen</span></span> 
- <span data-ttu-id="e5c57-181">Drei Stellen</span><span class="sxs-lookup"><span data-stu-id="e5c57-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-182">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-182">Checksum</span></span>

<span data-ttu-id="e5c57-183">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-184">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-184">Definition</span></span>

<span data-ttu-id="e5c57-185">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-186">Der reguläre Ausdruck Regex_australia_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="e5c57-187">Ein Schlüsselwort aus Keyword_australia_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="e5c57-188">Der reguläre Ausdruck Regex_australia_bank_account_number_bsb findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="e5c57-189">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-190">Der reguläre Ausdruck Regex_australia_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="e5c57-191">Ein Schlüsselwort aus Keyword_australia_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-192">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-192">Keywords</span></span>

#### <a name="keyword_australia_bank_account_number"></a><span data-ttu-id="e5c57-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="e5c57-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="e5c57-194">swift bank code</span></span>
- <span data-ttu-id="e5c57-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="e5c57-195">correspondent bank</span></span>
- <span data-ttu-id="e5c57-196">base currency</span><span class="sxs-lookup"><span data-stu-id="e5c57-196">base currency</span></span>
- <span data-ttu-id="e5c57-197">usa account</span><span class="sxs-lookup"><span data-stu-id="e5c57-197">usa account</span></span>
- <span data-ttu-id="e5c57-198">holder address</span><span class="sxs-lookup"><span data-stu-id="e5c57-198">holder address</span></span>
- <span data-ttu-id="e5c57-199">bank address</span><span class="sxs-lookup"><span data-stu-id="e5c57-199">bank address</span></span>
- <span data-ttu-id="e5c57-200">information account</span><span class="sxs-lookup"><span data-stu-id="e5c57-200">information account</span></span>
- <span data-ttu-id="e5c57-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="e5c57-201">fund transfers</span></span>
- <span data-ttu-id="e5c57-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="e5c57-202">bank charges</span></span>
- <span data-ttu-id="e5c57-203">bank details</span><span class="sxs-lookup"><span data-stu-id="e5c57-203">bank details</span></span>
- <span data-ttu-id="e5c57-204">banking information</span><span class="sxs-lookup"><span data-stu-id="e5c57-204">banking information</span></span>
- <span data-ttu-id="e5c57-205">full names</span><span class="sxs-lookup"><span data-stu-id="e5c57-205">full names</span></span>
- <span data-ttu-id="e5c57-206">IAEO</span><span class="sxs-lookup"><span data-stu-id="e5c57-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="e5c57-207">Australische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-208">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-208">Format</span></span>

<span data-ttu-id="e5c57-209">Neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-210">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-210">Pattern</span></span>

<span data-ttu-id="e5c57-211">Neun Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="e5c57-212">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="e5c57-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-213">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-213">Two digits</span></span> 
- <span data-ttu-id="e5c57-214">Fünf Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="e5c57-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="e5c57-215">ODER</span><span class="sxs-lookup"><span data-stu-id="e5c57-215">OR</span></span>

- <span data-ttu-id="e5c57-216">1-2 optionale Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="e5c57-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-217">4 bis 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-217">4-9 digits</span></span>

<span data-ttu-id="e5c57-218">ODER</span><span class="sxs-lookup"><span data-stu-id="e5c57-218">OR</span></span>

- <span data-ttu-id="e5c57-219">Neun Ziffern oder Buchstaben (Groß-/Kleinschreibung irrelevant)</span><span class="sxs-lookup"><span data-stu-id="e5c57-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-220">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-220">Checksum</span></span>

<span data-ttu-id="e5c57-221">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-222">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-222">Definition</span></span>

<span data-ttu-id="e5c57-223">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-224">Der reguläre Ausdruck Regex_australia_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-225">Ein Schlüsselwort aus Keyword_australia_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="e5c57-226">Es wurde kein Schlüsselwort aus Keyword_australia_drivers_license_number_exclusions gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-227">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-227">Keywords</span></span>

#### <a name="keyword_australia_drivers_license_number"></a><span data-ttu-id="e5c57-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="e5c57-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="e5c57-229">international driving permits</span></span>
- <span data-ttu-id="e5c57-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="e5c57-230">australian automobile association</span></span>
- <span data-ttu-id="e5c57-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="e5c57-231">international driving permit</span></span>
- <span data-ttu-id="e5c57-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="e5c57-232">DriverLicence</span></span>
- <span data-ttu-id="e5c57-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="e5c57-233">DriverLicences</span></span>
- <span data-ttu-id="e5c57-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-234">Driver Lic</span></span>
- <span data-ttu-id="e5c57-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-235">Driver Licence</span></span>
- <span data-ttu-id="e5c57-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-236">Driver Licences</span></span>
- <span data-ttu-id="e5c57-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="e5c57-237">DriversLic</span></span>
- <span data-ttu-id="e5c57-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="e5c57-238">DriversLicence</span></span>
- <span data-ttu-id="e5c57-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="e5c57-239">DriversLicences</span></span>
- <span data-ttu-id="e5c57-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-240">Drivers Lic</span></span>
- <span data-ttu-id="e5c57-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-241">Drivers Lics</span></span>
- <span data-ttu-id="e5c57-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-242">Drivers Licence</span></span>
- <span data-ttu-id="e5c57-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-243">Drivers Licences</span></span>
- <span data-ttu-id="e5c57-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-244">Driver'Lic</span></span>
- <span data-ttu-id="e5c57-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-245">Driver'Lics</span></span>
- <span data-ttu-id="e5c57-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-246">Driver'Licence</span></span>
- <span data-ttu-id="e5c57-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-247">Driver'Licences</span></span>
- <span data-ttu-id="e5c57-248">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-248">Driver' Lic</span></span>
- <span data-ttu-id="e5c57-249">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-249">Driver' Lics</span></span>
- <span data-ttu-id="e5c57-250">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-250">Driver' Licence</span></span>
- <span data-ttu-id="e5c57-251">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-251">Driver' Licences</span></span>
- <span data-ttu-id="e5c57-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="e5c57-252">Driver'sLic</span></span>
- <span data-ttu-id="e5c57-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="e5c57-253">Driver'sLics</span></span>
- <span data-ttu-id="e5c57-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="e5c57-254">Driver'sLicence</span></span>
- <span data-ttu-id="e5c57-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="e5c57-255">Driver'sLicences</span></span>
- <span data-ttu-id="e5c57-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-256">Driver's Lic</span></span>
- <span data-ttu-id="e5c57-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-257">Driver's Lics</span></span>
- <span data-ttu-id="e5c57-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-258">Driver's Licence</span></span>
- <span data-ttu-id="e5c57-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-259">Driver's Licences</span></span>
- <span data-ttu-id="e5c57-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-260">DriverLic#</span></span>
- <span data-ttu-id="e5c57-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-261">DriverLics#</span></span>
- <span data-ttu-id="e5c57-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="e5c57-262">DriverLicence#</span></span>
- <span data-ttu-id="e5c57-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="e5c57-263">DriverLicences#</span></span>
- <span data-ttu-id="e5c57-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-264">Driver Lic#</span></span>
- <span data-ttu-id="e5c57-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-265">Driver Lics#</span></span>
- <span data-ttu-id="e5c57-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="e5c57-266">Driver Licence#</span></span>
- <span data-ttu-id="e5c57-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="e5c57-267">Driver Licences#</span></span>
- <span data-ttu-id="e5c57-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-268">DriversLic#</span></span>
- <span data-ttu-id="e5c57-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-269">DriversLics#</span></span>
- <span data-ttu-id="e5c57-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="e5c57-270">DriversLicence#</span></span>
- <span data-ttu-id="e5c57-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="e5c57-271">DriversLicences#</span></span>
- <span data-ttu-id="e5c57-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-272">Drivers Lic#</span></span>
- <span data-ttu-id="e5c57-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-273">Drivers Lics#</span></span>
- <span data-ttu-id="e5c57-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="e5c57-274">Drivers Licence#</span></span>
- <span data-ttu-id="e5c57-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="e5c57-275">Drivers Licences#</span></span>
- <span data-ttu-id="e5c57-276">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-276">Driver'Lic#</span></span>
- <span data-ttu-id="e5c57-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-277">Driver'Lics#</span></span>
- <span data-ttu-id="e5c57-278">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="e5c57-278">Driver'Licence#</span></span>
- <span data-ttu-id="e5c57-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="e5c57-279">Driver'Licences#</span></span>
- <span data-ttu-id="e5c57-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-280">Driver' Lic#</span></span>
- <span data-ttu-id="e5c57-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-281">Driver' Lics#</span></span>
- <span data-ttu-id="e5c57-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="e5c57-282">Driver' Licence#</span></span>
- <span data-ttu-id="e5c57-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="e5c57-283">Driver' Licences#</span></span>
- <span data-ttu-id="e5c57-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-284">Driver'sLic#</span></span>
- <span data-ttu-id="e5c57-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-285">Driver'sLics#</span></span>
- <span data-ttu-id="e5c57-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="e5c57-286">Driver'sLicence#</span></span>
- <span data-ttu-id="e5c57-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="e5c57-287">Driver'sLicences#</span></span>
- <span data-ttu-id="e5c57-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-288">Driver's Lic#</span></span>
- <span data-ttu-id="e5c57-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-289">Driver's Lics#</span></span>
- <span data-ttu-id="e5c57-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="e5c57-290">Driver's Licence#</span></span>
- <span data-ttu-id="e5c57-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="e5c57-291">Driver's Licences#</span></span> 

#### <a name="keyword_australia_drivers_license_number_exclusions"></a><span data-ttu-id="e5c57-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="e5c57-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="e5c57-293">aaa</span><span class="sxs-lookup"><span data-stu-id="e5c57-293">aaa</span></span>
- <span data-ttu-id="e5c57-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="e5c57-294">DriverLicense</span></span>
- <span data-ttu-id="e5c57-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-295">DriverLicenses</span></span>
- <span data-ttu-id="e5c57-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="e5c57-296">Driver License</span></span>
- <span data-ttu-id="e5c57-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-297">Driver Licenses</span></span>
- <span data-ttu-id="e5c57-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="e5c57-298">DriversLicense</span></span>
- <span data-ttu-id="e5c57-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-299">DriversLicenses</span></span>
- <span data-ttu-id="e5c57-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="e5c57-300">Drivers License</span></span>
- <span data-ttu-id="e5c57-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-301">Drivers Licenses</span></span>
- <span data-ttu-id="e5c57-302">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="e5c57-302">Driver'License</span></span>
- <span data-ttu-id="e5c57-303">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-303">Driver'Licenses</span></span>
- <span data-ttu-id="e5c57-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="e5c57-304">Driver' License</span></span>
- <span data-ttu-id="e5c57-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-305">Driver' Licenses</span></span>
- <span data-ttu-id="e5c57-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="e5c57-306">Driver'sLicense</span></span>
- <span data-ttu-id="e5c57-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-307">Driver'sLicenses</span></span>
- <span data-ttu-id="e5c57-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="e5c57-308">Driver's License</span></span>
- <span data-ttu-id="e5c57-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-309">Driver's Licenses</span></span>
- <span data-ttu-id="e5c57-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="e5c57-310">DriverLicense#</span></span>
- <span data-ttu-id="e5c57-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-311">DriverLicenses#</span></span>
- <span data-ttu-id="e5c57-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-312">Driver License#</span></span>
- <span data-ttu-id="e5c57-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-313">Driver Licenses#</span></span>
- <span data-ttu-id="e5c57-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="e5c57-314">DriversLicense#</span></span>
- <span data-ttu-id="e5c57-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-315">DriversLicenses#</span></span>
- <span data-ttu-id="e5c57-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-316">Drivers License#</span></span>
- <span data-ttu-id="e5c57-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-317">Drivers Licenses#</span></span>
- <span data-ttu-id="e5c57-318">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="e5c57-318">Driver'License#</span></span>
- <span data-ttu-id="e5c57-319">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-319">Driver'Licenses#</span></span>
- <span data-ttu-id="e5c57-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-320">Driver' License#</span></span>
- <span data-ttu-id="e5c57-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-321">Driver' Licenses#</span></span>
- <span data-ttu-id="e5c57-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="e5c57-322">Driver'sLicense#</span></span>
- <span data-ttu-id="e5c57-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="e5c57-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-324">Driver's License#</span></span>
- <span data-ttu-id="e5c57-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="e5c57-326">Australische Medical Account-Nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-327">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-327">Format</span></span>

<span data-ttu-id="e5c57-328">10-11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-329">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-329">Pattern</span></span>

<span data-ttu-id="e5c57-330">10-11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-330">10-11 digits:</span></span>
- <span data-ttu-id="e5c57-331">Erste Ziffer im Bereich von 2-6</span><span class="sxs-lookup"><span data-stu-id="e5c57-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="e5c57-332">Neunte Ziffer ist eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="e5c57-333">Zehnte Ziffer ist die Ausgabeziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="e5c57-334">Elfte Ziffer (optional) ist die Einzelziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-335">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-335">Checksum</span></span>

<span data-ttu-id="e5c57-336">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-337">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-337">Definition</span></span>

<span data-ttu-id="e5c57-338">Eine DLP-Richtlinie ist zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-339">Die Funktion Func_australian_medical_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-340">Ein Schlüsselwort aus Keyword_Australia_Medical_Account_Number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="e5c57-341">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-341">The checksum passes.</span></span>

<span data-ttu-id="e5c57-342">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-343">Die Funktion Func_australian_medical_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-344">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-345">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-345">Keywords</span></span>

#### <a name="keyword_australia_medical_account_number"></a><span data-ttu-id="e5c57-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="e5c57-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="e5c57-347">bank account details</span></span>
- <span data-ttu-id="e5c57-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="e5c57-348">medicare payments</span></span>
- <span data-ttu-id="e5c57-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="e5c57-349">mortgage account</span></span>
- <span data-ttu-id="e5c57-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="e5c57-350">bank payments</span></span>
- <span data-ttu-id="e5c57-351">information branch</span><span class="sxs-lookup"><span data-stu-id="e5c57-351">information branch</span></span>
- <span data-ttu-id="e5c57-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="e5c57-352">credit card loan</span></span>
- <span data-ttu-id="e5c57-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="e5c57-353">department of human services</span></span>
- <span data-ttu-id="e5c57-354">local service</span><span class="sxs-lookup"><span data-stu-id="e5c57-354">local service</span></span>
- <span data-ttu-id="e5c57-355">Medicare</span><span class="sxs-lookup"><span data-stu-id="e5c57-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="e5c57-356">Australische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-357">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-357">Format</span></span>

<span data-ttu-id="e5c57-358">Ein Buchstabe gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-359">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-359">Pattern</span></span>

<span data-ttu-id="e5c57-360">Ein Buchstabe (Groß-/Kleinschreibung irrelevant) gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-361">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-361">Checksum</span></span>

<span data-ttu-id="e5c57-362">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-363">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-363">Definition</span></span>

<span data-ttu-id="e5c57-364">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-365">Der reguläre Ausdruck Regex_australia_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-366">Ein Schlüsselwort aus Keyword_passport oder Keyword_australia_passport_number wird gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-367">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-367">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="e5c57-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="e5c57-368">Keyword_passport</span></span>

- <span data-ttu-id="e5c57-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-369">Passport Number</span></span>
- <span data-ttu-id="e5c57-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="e5c57-370">Passport No</span></span>
- <span data-ttu-id="e5c57-371">Passport#</span><span class="sxs-lookup"><span data-stu-id="e5c57-371">Passport #</span></span>
- <span data-ttu-id="e5c57-372">Pass #</span><span class="sxs-lookup"><span data-stu-id="e5c57-372">Passport#</span></span>
- <span data-ttu-id="e5c57-373">Passport-Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-373">PassportID</span></span>
- <span data-ttu-id="e5c57-374">Passportno</span><span class="sxs-lookup"><span data-stu-id="e5c57-374">Passportno</span></span>
- <span data-ttu-id="e5c57-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-375">passportnumber</span></span>
- <span data-ttu-id="e5c57-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="e5c57-376">パスポート</span></span>
- <span data-ttu-id="e5c57-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-377">パスポート番号</span></span>
- <span data-ttu-id="e5c57-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="e5c57-378">パスポートのNum</span></span>
- <span data-ttu-id="e5c57-379">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-379">パスポート ＃</span></span> 
- <span data-ttu-id="e5c57-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="e5c57-380">Numéro de passeport</span></span>
- <span data-ttu-id="e5c57-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="e5c57-381">Passeport n °</span></span>
- <span data-ttu-id="e5c57-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="e5c57-382">Passeport Non</span></span>
- <span data-ttu-id="e5c57-383">Passeport#</span><span class="sxs-lookup"><span data-stu-id="e5c57-383">Passeport #</span></span>
- <span data-ttu-id="e5c57-384">Passeport #</span><span class="sxs-lookup"><span data-stu-id="e5c57-384">Passeport#</span></span>
- <span data-ttu-id="e5c57-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="e5c57-385">PasseportNon</span></span>
- <span data-ttu-id="e5c57-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="e5c57-386">Passeportn °</span></span>

#### <a name="keyword_australia_passport_number"></a><span data-ttu-id="e5c57-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="e5c57-388">Pass</span><span class="sxs-lookup"><span data-stu-id="e5c57-388">passport</span></span>
- <span data-ttu-id="e5c57-389">passport details</span><span class="sxs-lookup"><span data-stu-id="e5c57-389">passport details</span></span>
- <span data-ttu-id="e5c57-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="e5c57-390">immigration and citizenship</span></span>
- <span data-ttu-id="e5c57-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="e5c57-391">commonwealth of australia</span></span>
- <span data-ttu-id="e5c57-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="e5c57-392">department of immigration</span></span>
- <span data-ttu-id="e5c57-393">residential address</span><span class="sxs-lookup"><span data-stu-id="e5c57-393">residential address</span></span>
- <span data-ttu-id="e5c57-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="e5c57-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="e5c57-395">Visa</span><span class="sxs-lookup"><span data-stu-id="e5c57-395">visa</span></span>
- <span data-ttu-id="e5c57-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="e5c57-396">national identity card</span></span>
- <span data-ttu-id="e5c57-397">passport number</span><span class="sxs-lookup"><span data-stu-id="e5c57-397">passport number</span></span>
- <span data-ttu-id="e5c57-398">travel document</span><span class="sxs-lookup"><span data-stu-id="e5c57-398">travel document</span></span>
- <span data-ttu-id="e5c57-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="e5c57-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="e5c57-400">Australische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-401">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-401">Format</span></span>

<span data-ttu-id="e5c57-402">8-9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-403">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-403">Pattern</span></span>

<span data-ttu-id="e5c57-404">8 bis 9 Ziffern, die in der Regel wie folgt mit Leerzeichen dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="e5c57-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="e5c57-405">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-405">Three digits</span></span> 
- <span data-ttu-id="e5c57-406">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-406">An optional space</span></span> 
- <span data-ttu-id="e5c57-407">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-407">Three digits</span></span> 
- <span data-ttu-id="e5c57-408">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-408">An optional space</span></span> 
- <span data-ttu-id="e5c57-409">2 bis 3 Ziffern, wobei die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="e5c57-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-410">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-410">Checksum</span></span>

<span data-ttu-id="e5c57-411">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-412">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-412">Definition</span></span>

<span data-ttu-id="e5c57-413">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-414">Die Funktion Func_australian_tax_file_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-415">Es wurde kein Schlüsselwort aus Keyword_Australia_Tax_File_Number oder Keyword_number_exclusions gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="e5c57-416">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-416">The checksum passes.</span></span>

```
   <!-- Australia Tax File Number -->
    <Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Match idRef="Keyword_Australia_Tax_File_Number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_number_exclusions" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-417">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-417">Keywords</span></span>

#### <a name="keyword_australia_tax_file_number"></a><span data-ttu-id="e5c57-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="e5c57-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="e5c57-419">australian business number</span></span>
- <span data-ttu-id="e5c57-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="e5c57-420">marginal tax rate</span></span>
- <span data-ttu-id="e5c57-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="e5c57-421">medicare levy</span></span>
- <span data-ttu-id="e5c57-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="e5c57-422">portfolio number</span></span>
- <span data-ttu-id="e5c57-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="e5c57-423">service veterans</span></span>
- <span data-ttu-id="e5c57-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="e5c57-424">withholding tax</span></span>
- <span data-ttu-id="e5c57-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="e5c57-425">individual tax return</span></span>
- <span data-ttu-id="e5c57-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="e5c57-426">tax file number</span></span>

#### <a name="keyword_number_exclusions"></a><span data-ttu-id="e5c57-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="e5c57-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="e5c57-428">00000000</span><span class="sxs-lookup"><span data-stu-id="e5c57-428">00000000</span></span>
- <span data-ttu-id="e5c57-429">11111111</span><span class="sxs-lookup"><span data-stu-id="e5c57-429">11111111</span></span>
- <span data-ttu-id="e5c57-430">22222222</span><span class="sxs-lookup"><span data-stu-id="e5c57-430">22222222</span></span>
- <span data-ttu-id="e5c57-431">33333333</span><span class="sxs-lookup"><span data-stu-id="e5c57-431">33333333</span></span>
- <span data-ttu-id="e5c57-432">44444444</span><span class="sxs-lookup"><span data-stu-id="e5c57-432">44444444</span></span>
- <span data-ttu-id="e5c57-433">55555555</span><span class="sxs-lookup"><span data-stu-id="e5c57-433">55555555</span></span>
- <span data-ttu-id="e5c57-434">66666666</span><span class="sxs-lookup"><span data-stu-id="e5c57-434">66666666</span></span>
- <span data-ttu-id="e5c57-435">77777777</span><span class="sxs-lookup"><span data-stu-id="e5c57-435">77777777</span></span>
- <span data-ttu-id="e5c57-436">88888888</span><span class="sxs-lookup"><span data-stu-id="e5c57-436">88888888</span></span>
- <span data-ttu-id="e5c57-437">99999999</span><span class="sxs-lookup"><span data-stu-id="e5c57-437">99999999</span></span>
- <span data-ttu-id="e5c57-438">000000000</span><span class="sxs-lookup"><span data-stu-id="e5c57-438">000000000</span></span>
- <span data-ttu-id="e5c57-439">111111111</span><span class="sxs-lookup"><span data-stu-id="e5c57-439">111111111</span></span>
- <span data-ttu-id="e5c57-440">222222222</span><span class="sxs-lookup"><span data-stu-id="e5c57-440">222222222</span></span>
- <span data-ttu-id="e5c57-441">333333333</span><span class="sxs-lookup"><span data-stu-id="e5c57-441">333333333</span></span>
- <span data-ttu-id="e5c57-442">444444444</span><span class="sxs-lookup"><span data-stu-id="e5c57-442">444444444</span></span>
- <span data-ttu-id="e5c57-443">555555555</span><span class="sxs-lookup"><span data-stu-id="e5c57-443">555555555</span></span>
- <span data-ttu-id="e5c57-444">666666666</span><span class="sxs-lookup"><span data-stu-id="e5c57-444">666666666</span></span>
- <span data-ttu-id="e5c57-445">777777777</span><span class="sxs-lookup"><span data-stu-id="e5c57-445">777777777</span></span>
- <span data-ttu-id="e5c57-446">888888888</span><span class="sxs-lookup"><span data-stu-id="e5c57-446">888888888</span></span>
- <span data-ttu-id="e5c57-447">999999999</span><span class="sxs-lookup"><span data-stu-id="e5c57-447">999999999</span></span>
- <span data-ttu-id="e5c57-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="e5c57-448">0000000000</span></span>
- <span data-ttu-id="e5c57-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="e5c57-449">1111111111</span></span>
- <span data-ttu-id="e5c57-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="e5c57-450">2222222222</span></span>
- <span data-ttu-id="e5c57-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="e5c57-451">3333333333</span></span>
- <span data-ttu-id="e5c57-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="e5c57-452">4444444444</span></span>
- <span data-ttu-id="e5c57-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="e5c57-453">5555555555</span></span>
- <span data-ttu-id="e5c57-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="e5c57-454">6666666666</span></span>
- <span data-ttu-id="e5c57-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="e5c57-455">7777777777</span></span>
- <span data-ttu-id="e5c57-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="e5c57-456">8888888888</span></span>
- <span data-ttu-id="e5c57-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="e5c57-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="e5c57-458">Azure DocumentDB-Authentifizierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="e5c57-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-459">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-459">Format</span></span>

<span data-ttu-id="e5c57-460">Die Zeichenfolge "DocumentDb" gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-461">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-461">Pattern</span></span>

- <span data-ttu-id="e5c57-462">Die Zeichenfolge "DocumentDb"</span><span class="sxs-lookup"><span data-stu-id="e5c57-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="e5c57-463">Eine beliebige Kombination von zwischen 3-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="e5c57-464">Ein größer als-Symbol (#a0), ein Gleichheitszeichen (=), ein Anführungszeichen (") oder ein Apostroph (')</span><span class="sxs-lookup"><span data-stu-id="e5c57-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="e5c57-465">Eine beliebige Kombination von 86 unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="e5c57-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="e5c57-466">Zwei Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-467">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-467">Checksum</span></span>

<span data-ttu-id="e5c57-468">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-469">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-469">Definition</span></span>

<span data-ttu-id="e5c57-470">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-471">Der reguläre Ausdruck CEP_Regex_AzureDocumentDBAuthKey sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-472">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-473">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-473">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="e5c57-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="e5c57-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="e5c57-475">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="e5c57-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="e5c57-476">contoso</span><span class="sxs-lookup"><span data-stu-id="e5c57-476">contoso</span></span>
- <span data-ttu-id="e5c57-477">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e5c57-477">fabrikam</span></span>
- <span data-ttu-id="e5c57-478">Northwind</span><span class="sxs-lookup"><span data-stu-id="e5c57-478">northwind</span></span>
- <span data-ttu-id="e5c57-479">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="e5c57-479">sandbox</span></span>
- <span data-ttu-id="e5c57-480">OneBox</span><span class="sxs-lookup"><span data-stu-id="e5c57-480">onebox</span></span>
- <span data-ttu-id="e5c57-481">localhost</span><span class="sxs-lookup"><span data-stu-id="e5c57-481">localhost</span></span>
- <span data-ttu-id="e5c57-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="e5c57-482">127.0.0.1</span></span>
- <span data-ttu-id="e5c57-483">testacs.</span><span class="sxs-lookup"><span data-stu-id="e5c57-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-484">com</span><span class="sxs-lookup"><span data-stu-id="e5c57-484">com</span></span>
- <span data-ttu-id="e5c57-485">s-int.</span><span class="sxs-lookup"><span data-stu-id="e5c57-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-486">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="e5c57-487">Azure IaaS-Datenbankverbindungszeichenfolge und Azure SQL-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e5c57-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-488">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-488">Format</span></span>

<span data-ttu-id="e5c57-489">Die Zeichenfolge "Server", "Server" oder "Datenquelle", gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten, einschließlich der Zeichenfolge "cloudapp. Azure" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e5c57-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-490">com "oder" cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c57-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-491">NET "oder" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="e5c57-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-492">NET "und die Zeichenfolge" Password "oder" Password "oder" pwd ".</span><span class="sxs-lookup"><span data-stu-id="e5c57-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-493">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-493">Pattern</span></span>

- <span data-ttu-id="e5c57-494">Die Zeichenfolge "Server", "Server" oder "Datenquelle"</span><span class="sxs-lookup"><span data-stu-id="e5c57-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="e5c57-495">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-496">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-496">An equal sign (=)</span></span>
- <span data-ttu-id="e5c57-497">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-498">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="e5c57-499">Die Zeichenfolge "cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c57-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-500">com "," cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c57-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-501">NET "oder" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="e5c57-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-502">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-502">net"</span></span>
- <span data-ttu-id="e5c57-503">Eine beliebige Kombination von zwischen 1-300 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="e5c57-504">Die Zeichenfolge "Password", "Password" oder "pwd"</span><span class="sxs-lookup"><span data-stu-id="e5c57-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="e5c57-505">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-506">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-506">An equal sign (=)</span></span>
- <span data-ttu-id="e5c57-507">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-508">Ein oder mehrere Zeichen, bei denen es sich nicht um ein Semikolon handelt (;), Anführungszeichen (") oder Apostroph (')</span><span class="sxs-lookup"><span data-stu-id="e5c57-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="e5c57-509">Ein Semikolon (;), Anführungszeichen (") oder Apostroph (')</span><span class="sxs-lookup"><span data-stu-id="e5c57-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-510">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-510">Checksum</span></span>

<span data-ttu-id="e5c57-511">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-512">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-512">Definition</span></span>

<span data-ttu-id="e5c57-513">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-514">Der reguläre Ausdruck CEP_Regex_AzureConnectionString sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-515">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-516">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-516">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="e5c57-517">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="e5c57-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="e5c57-518">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="e5c57-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="e5c57-519">contoso</span><span class="sxs-lookup"><span data-stu-id="e5c57-519">contoso</span></span>
- <span data-ttu-id="e5c57-520">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e5c57-520">fabrikam</span></span>
- <span data-ttu-id="e5c57-521">Northwind</span><span class="sxs-lookup"><span data-stu-id="e5c57-521">northwind</span></span>
- <span data-ttu-id="e5c57-522">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="e5c57-522">sandbox</span></span>
- <span data-ttu-id="e5c57-523">OneBox</span><span class="sxs-lookup"><span data-stu-id="e5c57-523">onebox</span></span>
- <span data-ttu-id="e5c57-524">localhost</span><span class="sxs-lookup"><span data-stu-id="e5c57-524">localhost</span></span>
- <span data-ttu-id="e5c57-525">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="e5c57-525">127.0.0.1</span></span>
- <span data-ttu-id="e5c57-526">testacs.</span><span class="sxs-lookup"><span data-stu-id="e5c57-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-527">com</span><span class="sxs-lookup"><span data-stu-id="e5c57-527">com</span></span>
- <span data-ttu-id="e5c57-528">s-int.</span><span class="sxs-lookup"><span data-stu-id="e5c57-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-529">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="e5c57-530">Azurey-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e5c57-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-531">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-531">Format</span></span>

<span data-ttu-id="e5c57-532">Die Zeichenfolge "Hostname" gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten beschrieben sind, einschließlich der Zeichenfolgen "Azure-Devices".</span><span class="sxs-lookup"><span data-stu-id="e5c57-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-533">NET "und" SharedAccessKey ".</span><span class="sxs-lookup"><span data-stu-id="e5c57-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-534">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-534">Pattern</span></span>

- <span data-ttu-id="e5c57-535">Die Zeichenfolge "Hostname"</span><span class="sxs-lookup"><span data-stu-id="e5c57-535">The string "HostName"</span></span>
- <span data-ttu-id="e5c57-536">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-537">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-537">An equal sign (=)</span></span>
- <span data-ttu-id="e5c57-538">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-539">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="e5c57-540">Die Zeichenfolge "Azure-Devices.</span><span class="sxs-lookup"><span data-stu-id="e5c57-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-541">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-541">net"</span></span>
- <span data-ttu-id="e5c57-542">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="e5c57-543">Die Zeichenfolge "SharedAccessKey"</span><span class="sxs-lookup"><span data-stu-id="e5c57-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="e5c57-544">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-545">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-545">An equal sign (=)</span></span>
- <span data-ttu-id="e5c57-546">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-547">Eine beliebige Kombination von 43 unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="e5c57-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="e5c57-548">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-549">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-549">Checksum</span></span>

<span data-ttu-id="e5c57-550">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-551">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-551">Definition</span></span>

<span data-ttu-id="e5c57-552">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-553">Der reguläre Ausdruck CEP_Regex_AzureIoTConnectionString sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-554">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-555">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-555">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="e5c57-556">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="e5c57-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="e5c57-557">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="e5c57-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="e5c57-558">contoso</span><span class="sxs-lookup"><span data-stu-id="e5c57-558">contoso</span></span>
- <span data-ttu-id="e5c57-559">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e5c57-559">fabrikam</span></span>
- <span data-ttu-id="e5c57-560">Northwind</span><span class="sxs-lookup"><span data-stu-id="e5c57-560">northwind</span></span>
- <span data-ttu-id="e5c57-561">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="e5c57-561">sandbox</span></span>
- <span data-ttu-id="e5c57-562">OneBox</span><span class="sxs-lookup"><span data-stu-id="e5c57-562">onebox</span></span>
- <span data-ttu-id="e5c57-563">localhost</span><span class="sxs-lookup"><span data-stu-id="e5c57-563">localhost</span></span>
- <span data-ttu-id="e5c57-564">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="e5c57-564">127.0.0.1</span></span>
- <span data-ttu-id="e5c57-565">testacs.</span><span class="sxs-lookup"><span data-stu-id="e5c57-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-566">com</span><span class="sxs-lookup"><span data-stu-id="e5c57-566">com</span></span>
- <span data-ttu-id="e5c57-567">s-int.</span><span class="sxs-lookup"><span data-stu-id="e5c57-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-568">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="e5c57-569">Kennwort für Azure-Veröffentlichungseinstellung</span><span class="sxs-lookup"><span data-stu-id="e5c57-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-570">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-570">Format</span></span>

<span data-ttu-id="e5c57-571">Die Zeichenfolge "benutzerkwt =" gefolgt von einer alphanumerischen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e5c57-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-572">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-572">Pattern</span></span>

- <span data-ttu-id="e5c57-573">Die Zeichenfolge "benutzerkwt ="</span><span class="sxs-lookup"><span data-stu-id="e5c57-573">The string "userpwd="</span></span>
- <span data-ttu-id="e5c57-574">Eine beliebige Kombination von 60 Kleinbuchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="e5c57-575">Ein Anführungszeichen (")</span><span class="sxs-lookup"><span data-stu-id="e5c57-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-576">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-576">Checksum</span></span>

<span data-ttu-id="e5c57-577">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-578">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-578">Definition</span></span>

<span data-ttu-id="e5c57-579">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-580">Der reguläre Ausdruck CEP_Regex_AzurePublishSettingPasswords sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-581">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


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

### <a name="keywords"></a><span data-ttu-id="e5c57-582">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-582">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="e5c57-583">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="e5c57-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="e5c57-584">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="e5c57-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="e5c57-585">contoso</span><span class="sxs-lookup"><span data-stu-id="e5c57-585">contoso</span></span>
- <span data-ttu-id="e5c57-586">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e5c57-586">fabrikam</span></span>
- <span data-ttu-id="e5c57-587">Northwind</span><span class="sxs-lookup"><span data-stu-id="e5c57-587">northwind</span></span>
- <span data-ttu-id="e5c57-588">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="e5c57-588">sandbox</span></span>
- <span data-ttu-id="e5c57-589">OneBox</span><span class="sxs-lookup"><span data-stu-id="e5c57-589">onebox</span></span>
- <span data-ttu-id="e5c57-590">localhost</span><span class="sxs-lookup"><span data-stu-id="e5c57-590">localhost</span></span>
- <span data-ttu-id="e5c57-591">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="e5c57-591">127.0.0.1</span></span>
- <span data-ttu-id="e5c57-592">testacs.</span><span class="sxs-lookup"><span data-stu-id="e5c57-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-593">com</span><span class="sxs-lookup"><span data-stu-id="e5c57-593">com</span></span>
- <span data-ttu-id="e5c57-594">s-int.</span><span class="sxs-lookup"><span data-stu-id="e5c57-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-595">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="e5c57-596">Azure-Zeichenfolgen-Cache-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e5c57-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-597">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-597">Format</span></span>

<span data-ttu-id="e5c57-598">Die Zeichenfolge "" Codestring. Cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="e5c57-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-599">NET ", gefolgt von den Zeichen und Zeichenfolgen, die im folgenden Muster dargestellt werden, einschließlich der Zeichenfolge" Password "oder" pwd ".</span><span class="sxs-lookup"><span data-stu-id="e5c57-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-600">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-600">Pattern</span></span>

- <span data-ttu-id="e5c57-601">Die Zeichenfolge "" Codestring. Cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="e5c57-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-602">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-602">net"</span></span>
- <span data-ttu-id="e5c57-603">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="e5c57-604">Die Zeichenfolge "Password" oder "pwd"</span><span class="sxs-lookup"><span data-stu-id="e5c57-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="e5c57-605">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-606">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-606">An equal sign (=)</span></span>
- <span data-ttu-id="e5c57-607">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-608">Eine beliebige Kombination von 43 Zeichen mit unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="e5c57-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="e5c57-609">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-610">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-610">Checksum</span></span>

<span data-ttu-id="e5c57-611">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-612">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-612">Definition</span></span>

<span data-ttu-id="e5c57-613">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-614">Der reguläre Ausdruck CEP_Regex_AzureRedisCacheConnectionString sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="e5c57-615">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-616">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-616">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="e5c57-617">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="e5c57-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="e5c57-618">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="e5c57-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="e5c57-619">contoso</span><span class="sxs-lookup"><span data-stu-id="e5c57-619">contoso</span></span>
- <span data-ttu-id="e5c57-620">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e5c57-620">fabrikam</span></span>
- <span data-ttu-id="e5c57-621">Northwind</span><span class="sxs-lookup"><span data-stu-id="e5c57-621">northwind</span></span>
- <span data-ttu-id="e5c57-622">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="e5c57-622">sandbox</span></span>
- <span data-ttu-id="e5c57-623">OneBox</span><span class="sxs-lookup"><span data-stu-id="e5c57-623">onebox</span></span>
- <span data-ttu-id="e5c57-624">localhost</span><span class="sxs-lookup"><span data-stu-id="e5c57-624">localhost</span></span>
- <span data-ttu-id="e5c57-625">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="e5c57-625">127.0.0.1</span></span>
- <span data-ttu-id="e5c57-626">testacs.</span><span class="sxs-lookup"><span data-stu-id="e5c57-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-627">com</span><span class="sxs-lookup"><span data-stu-id="e5c57-627">com</span></span>
- <span data-ttu-id="e5c57-628">s-int.</span><span class="sxs-lookup"><span data-stu-id="e5c57-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-629">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="e5c57-630">Azure-SAS</span><span class="sxs-lookup"><span data-stu-id="e5c57-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-631">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-631">Format</span></span>

<span data-ttu-id="e5c57-632">Die Zeichenfolge "SIG" gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-633">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-633">Pattern</span></span>

- <span data-ttu-id="e5c57-634">Die Zeichenfolge "SIG"</span><span class="sxs-lookup"><span data-stu-id="e5c57-634">The string "sig"</span></span>
- <span data-ttu-id="e5c57-635">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-636">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-636">An equal sign (=)</span></span>
- <span data-ttu-id="e5c57-637">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-638">Eine beliebige Kombination von zwischen 43-53 Zeichen, die klein-oder Großbuchstaben, Ziffern oder das Prozentzeichen (%)</span><span class="sxs-lookup"><span data-stu-id="e5c57-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="e5c57-639">Die Zeichenfolge "% 3D"</span><span class="sxs-lookup"><span data-stu-id="e5c57-639">The string "%3d"</span></span>
- <span data-ttu-id="e5c57-640">Ein beliebiges Zeichen, das kein niedriger oder groß geschriebener Buchstabe, eine Ziffer oder ein Prozentzeichen ist (%)</span><span class="sxs-lookup"><span data-stu-id="e5c57-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-641">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-641">Checksum</span></span>

<span data-ttu-id="e5c57-642">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-643">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-643">Definition</span></span>

<span data-ttu-id="e5c57-644">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-645">Der reguläre Ausdruck CEP_Regex_AzureSAS sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="e5c57-646">Azure Service Bus-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e5c57-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-647">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-647">Format</span></span>

<span data-ttu-id="e5c57-648">Die Zeichenfolge "Endpoint" gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten, einschließlich der Zeichenfolgen "ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="e5c57-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-649">NET "und" SharedAccesKey ".</span><span class="sxs-lookup"><span data-stu-id="e5c57-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-650">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-650">Pattern</span></span>

- <span data-ttu-id="e5c57-651">Die Zeichenfolge "Endpoint"</span><span class="sxs-lookup"><span data-stu-id="e5c57-651">The string "EndPoint"</span></span>
- <span data-ttu-id="e5c57-652">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-653">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-653">An equal sign (=)</span></span>
- <span data-ttu-id="e5c57-654">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-655">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="e5c57-656">Die Zeichenfolge "ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="e5c57-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-657">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-657">net"</span></span>
- <span data-ttu-id="e5c57-658">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="e5c57-659">Die Zeichenfolge "SharedAccessKey"</span><span class="sxs-lookup"><span data-stu-id="e5c57-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="e5c57-660">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-661">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-661">An equal sign (=)</span></span>
- <span data-ttu-id="e5c57-662">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-663">Eine beliebige Kombination von 43 Zeichen mit unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="e5c57-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="e5c57-664">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-665">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-665">Checksum</span></span>

<span data-ttu-id="e5c57-666">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-667">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-667">Definition</span></span>

<span data-ttu-id="e5c57-668">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-669">Der reguläre Ausdruck CEP_Regex_AzureServiceBusConnectionString sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="e5c57-670">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-671">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-671">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="e5c57-672">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="e5c57-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="e5c57-673">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="e5c57-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="e5c57-674">contoso</span><span class="sxs-lookup"><span data-stu-id="e5c57-674">contoso</span></span>
- <span data-ttu-id="e5c57-675">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e5c57-675">fabrikam</span></span>
- <span data-ttu-id="e5c57-676">Northwind</span><span class="sxs-lookup"><span data-stu-id="e5c57-676">northwind</span></span>
- <span data-ttu-id="e5c57-677">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="e5c57-677">sandbox</span></span>
- <span data-ttu-id="e5c57-678">OneBox</span><span class="sxs-lookup"><span data-stu-id="e5c57-678">onebox</span></span>
- <span data-ttu-id="e5c57-679">localhost</span><span class="sxs-lookup"><span data-stu-id="e5c57-679">localhost</span></span>
- <span data-ttu-id="e5c57-680">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="e5c57-680">127.0.0.1</span></span>
- <span data-ttu-id="e5c57-681">testacs.</span><span class="sxs-lookup"><span data-stu-id="e5c57-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-682">com</span><span class="sxs-lookup"><span data-stu-id="e5c57-682">com</span></span>
- <span data-ttu-id="e5c57-683">s-int.</span><span class="sxs-lookup"><span data-stu-id="e5c57-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-684">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="e5c57-685">Azure Storage-Kontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="e5c57-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-686">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-686">Format</span></span>

<span data-ttu-id="e5c57-687">Die Zeichenfolge "DefaultEndpointsProtocol", gefolgt von den Zeichen und Zeichenfolgen, die in dem Muster unten, einschließlich der Zeichenfolge "AccountKey", dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-688">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-688">Pattern</span></span>

- <span data-ttu-id="e5c57-689">Die Zeichenfolge "DefaultEndpointsProtocol"</span><span class="sxs-lookup"><span data-stu-id="e5c57-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="e5c57-690">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-691">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-691">An equal sign (=)</span></span>
- <span data-ttu-id="e5c57-692">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-693">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="e5c57-694">Die Zeichenfolge "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="e5c57-694">The string "AccountKey"</span></span>
- <span data-ttu-id="e5c57-695">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-696">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-696">An equal sign (=)</span></span>
- <span data-ttu-id="e5c57-697">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="e5c57-698">Eine beliebige Kombination von 86 Zeichen mit unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="e5c57-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="e5c57-699">Zwei Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-700">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-700">Checksum</span></span>

<span data-ttu-id="e5c57-701">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-702">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-702">Definition</span></span>

<span data-ttu-id="e5c57-703">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-704">Der reguläre Ausdruck CEP_Regex_AzureStorageAccountKey sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-705">Der reguläre Ausdruck CEP_AzureEmulatorStorageAccountFilter findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-706">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-707">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-707">Keywords</span></span>

#### <a name="cep_azureemulatorstorageaccountfilter"></a><span data-ttu-id="e5c57-708">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="e5c57-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="e5c57-709">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="e5c57-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="e5c57-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="e5c57-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="e5c57-711">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="e5c57-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="e5c57-712">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="e5c57-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="e5c57-713">contoso</span><span class="sxs-lookup"><span data-stu-id="e5c57-713">contoso</span></span>
- <span data-ttu-id="e5c57-714">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e5c57-714">fabrikam</span></span>
- <span data-ttu-id="e5c57-715">Northwind</span><span class="sxs-lookup"><span data-stu-id="e5c57-715">northwind</span></span>
- <span data-ttu-id="e5c57-716">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="e5c57-716">sandbox</span></span>
- <span data-ttu-id="e5c57-717">OneBox</span><span class="sxs-lookup"><span data-stu-id="e5c57-717">onebox</span></span>
- <span data-ttu-id="e5c57-718">localhost</span><span class="sxs-lookup"><span data-stu-id="e5c57-718">localhost</span></span>
- <span data-ttu-id="e5c57-719">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="e5c57-719">127.0.0.1</span></span>
- <span data-ttu-id="e5c57-720">testacs.</span><span class="sxs-lookup"><span data-stu-id="e5c57-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-721">com</span><span class="sxs-lookup"><span data-stu-id="e5c57-721">com</span></span>
- <span data-ttu-id="e5c57-722">s-int.</span><span class="sxs-lookup"><span data-stu-id="e5c57-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-723">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="e5c57-724">Azure Storage-Kontoschlüssel (generisch)</span><span class="sxs-lookup"><span data-stu-id="e5c57-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-725">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-725">Format</span></span>

<span data-ttu-id="e5c57-726">Eine beliebige Kombination von 86 unter-oder Großbuchstaben, Ziffern, den Schrägstrich (/) oder Pluszeichen (+), vorangestellt oder gefolgt von den im Muster unten beschriebenen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-727">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-727">Pattern</span></span>

- <span data-ttu-id="e5c57-728">0-1 des größer als-Symbols (#a0), Apostroph ('), Gleichheitszeichen (=), Anführungszeichen (") oder Nummernzeichen (#)</span><span class="sxs-lookup"><span data-stu-id="e5c57-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="e5c57-729">Eine beliebige Kombination von 86 Zeichen mit unter-oder Großbuchstaben, Ziffern, dem Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="e5c57-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="e5c57-730">Zwei Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="e5c57-731">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-731">Checksum</span></span>

<span data-ttu-id="e5c57-732">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-733">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-733">Definition</span></span>

<span data-ttu-id="e5c57-734">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-735">Der reguläre Ausdruck CEP_Regex_AzureStorageAccountKeyGeneric sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="e5c57-736">Belgien – Nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-737">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-737">Format</span></span>

<span data-ttu-id="e5c57-738">11 Ziffern plus Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-739">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-739">Pattern</span></span>

<span data-ttu-id="e5c57-740">11 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="e5c57-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="e5c57-741">Sechs Ziffern und zwei Punkte im Format JJ.MM.TT für das Geburtsdatum </span><span class="sxs-lookup"><span data-stu-id="e5c57-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="e5c57-742">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-742">A hyphen</span></span> 
- <span data-ttu-id="e5c57-743">Drei aufeinander folgende Ziffern (ungerade für Männer, gerade für Frauen) </span><span class="sxs-lookup"><span data-stu-id="e5c57-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="e5c57-744">Ein Punkt</span><span class="sxs-lookup"><span data-stu-id="e5c57-744">A period</span></span> 
- <span data-ttu-id="e5c57-745">Zwei Ziffern als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-746">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-746">Checksum</span></span>

<span data-ttu-id="e5c57-747">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-748">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-748">Definition</span></span>

<span data-ttu-id="e5c57-749">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-750">Die Funktion Func_belgium_national_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-751">Ein Schlüsselwort aus Keyword_belgium_national_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="e5c57-752">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-752">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-753">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-753">Keywords</span></span>

#### <a name="keyword_belgium_national_number"></a><span data-ttu-id="e5c57-754">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="e5c57-755">Identität</span><span class="sxs-lookup"><span data-stu-id="e5c57-755">Identity</span></span>
- <span data-ttu-id="e5c57-756">Registrierung</span><span class="sxs-lookup"><span data-stu-id="e5c57-756">Registration</span></span>
- <span data-ttu-id="e5c57-757">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="e5c57-757">Identification</span></span> 
- <span data-ttu-id="e5c57-758">ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-758">ID</span></span> 
- <span data-ttu-id="e5c57-759">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="e5c57-759">Identiteitskaart</span></span>
- <span data-ttu-id="e5c57-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-760">Registratie nummer</span></span> 
- <span data-ttu-id="e5c57-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-761">Identificatie nummer</span></span> 
- <span data-ttu-id="e5c57-762">Identiteit</span><span class="sxs-lookup"><span data-stu-id="e5c57-762">Identiteit</span></span>
- <span data-ttu-id="e5c57-763">Registratie</span><span class="sxs-lookup"><span data-stu-id="e5c57-763">Registratie</span></span>
- <span data-ttu-id="e5c57-764">Identificatie</span><span class="sxs-lookup"><span data-stu-id="e5c57-764">Identificatie</span></span> 
- <span data-ttu-id="e5c57-765">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="e5c57-765">Carte d’identité</span></span> 
- <span data-ttu-id="e5c57-766">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="e5c57-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="e5c57-767">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="e5c57-767">numéro d'identification</span></span>
- <span data-ttu-id="e5c57-768">identité</span><span class="sxs-lookup"><span data-stu-id="e5c57-768">identité</span></span> 
- <span data-ttu-id="e5c57-769">Inschrift</span><span class="sxs-lookup"><span data-stu-id="e5c57-769">inscription</span></span> 
- <span data-ttu-id="e5c57-770">Identifikation</span><span class="sxs-lookup"><span data-stu-id="e5c57-770">Identifikation</span></span>
- <span data-ttu-id="e5c57-771">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="e5c57-771">Identifizierung</span></span>
- <span data-ttu-id="e5c57-772">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-772">Identifikationsnummer</span></span>
- <span data-ttu-id="e5c57-773">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-773">Personalausweis</span></span>
- <span data-ttu-id="e5c57-774">Registrierung</span><span class="sxs-lookup"><span data-stu-id="e5c57-774">Registrierung</span></span>
- <span data-ttu-id="e5c57-775">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="e5c57-776">Brazil CPF Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-777">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-777">Format</span></span>

<span data-ttu-id="e5c57-778">11 Ziffern, die eine Prüfziffer umfassen und die formatiert oder unformatiert sein können</span><span class="sxs-lookup"><span data-stu-id="e5c57-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-779">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-779">Pattern</span></span>

<span data-ttu-id="e5c57-780">Formatiert</span><span class="sxs-lookup"><span data-stu-id="e5c57-780">Formatted:</span></span>
- <span data-ttu-id="e5c57-781">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-781">Three digits</span></span> 
- <span data-ttu-id="e5c57-782">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="e5c57-782">A period</span></span> 
- <span data-ttu-id="e5c57-783">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-783">Three digits</span></span> 
- <span data-ttu-id="e5c57-784">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="e5c57-784">A period</span></span> 
- <span data-ttu-id="e5c57-785">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-785">Three digits</span></span> 
- <span data-ttu-id="e5c57-786">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-786">A hyphen</span></span> 
- <span data-ttu-id="e5c57-787">Zwei Ziffern, die Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="e5c57-787">Two digits which are check digits</span></span>

<span data-ttu-id="e5c57-788">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="e5c57-788">Unformatted:</span></span>
- <span data-ttu-id="e5c57-789">11 Ziffern, wobei die letzten beiden Ziffern Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="e5c57-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-790">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-790">Checksum</span></span>

<span data-ttu-id="e5c57-791">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-792">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-792">Definition</span></span>

<span data-ttu-id="e5c57-793">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-794">Die Funktion Func_brazil_cpf findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-795">Ein Schlüsselwort aus Keyword_brazil_cpf wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="e5c57-796">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-796">The checksum passes.</span></span>

<span data-ttu-id="e5c57-797">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-798">Die Funktion Func_brazil_cpf findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-799">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-799">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-800">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-800">Keywords</span></span>

#### <a name="keyword_brazil_cpf"></a><span data-ttu-id="e5c57-801">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="e5c57-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="e5c57-802">CPF</span><span class="sxs-lookup"><span data-stu-id="e5c57-802">CPF</span></span>
- <span data-ttu-id="e5c57-803">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="e5c57-803">Identification</span></span>
- <span data-ttu-id="e5c57-804">Registrierung</span><span class="sxs-lookup"><span data-stu-id="e5c57-804">Registration</span></span>
- <span data-ttu-id="e5c57-805">Umsatz</span><span class="sxs-lookup"><span data-stu-id="e5c57-805">Revenue</span></span>
- <span data-ttu-id="e5c57-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="e5c57-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="e5c57-807">Imposto</span><span class="sxs-lookup"><span data-stu-id="e5c57-807">Imposto</span></span> 
- <span data-ttu-id="e5c57-808">Identificação</span><span class="sxs-lookup"><span data-stu-id="e5c57-808">Identificação</span></span> 
- <span data-ttu-id="e5c57-809">Inscrição</span><span class="sxs-lookup"><span data-stu-id="e5c57-809">Inscrição</span></span> 
- <span data-ttu-id="e5c57-810">Receita</span><span class="sxs-lookup"><span data-stu-id="e5c57-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="e5c57-811">Brasilien – Juristische Personennummer (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="e5c57-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-812">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-812">Format</span></span>

<span data-ttu-id="e5c57-813">14 Ziffern, die eine Registrierungsnummer, eine Zweignummer und Prüfnziffern sowie Trennzeichen umfassen</span><span class="sxs-lookup"><span data-stu-id="e5c57-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-814">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-814">Pattern</span></span>
<span data-ttu-id="e5c57-815">14 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="e5c57-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="e5c57-816">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-816">Two digits</span></span> 
- <span data-ttu-id="e5c57-817">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="e5c57-817">A period</span></span> 
- <span data-ttu-id="e5c57-818">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-818">Three digits</span></span> 
- <span data-ttu-id="e5c57-819">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="e5c57-819">A period</span></span> 
- <span data-ttu-id="e5c57-820">Drei Ziffern (diese ersten acht Ziffern sind die Registrierungsnummer) </span><span class="sxs-lookup"><span data-stu-id="e5c57-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="e5c57-821">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-821">A forward slash</span></span> 
- <span data-ttu-id="e5c57-822">Vierstellige Zweignummer </span><span class="sxs-lookup"><span data-stu-id="e5c57-822">Four-digit branch number</span></span> 
- <span data-ttu-id="e5c57-823">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-823">A hyphen</span></span> 
- <span data-ttu-id="e5c57-824">Zwei Ziffern, die Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="e5c57-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-825">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-825">Checksum</span></span>

<span data-ttu-id="e5c57-826">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-827">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-827">Definition</span></span>

<span data-ttu-id="e5c57-828">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-829">Die Funktion Func_brazil_cnpj findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-830">Ein Schlüsselwort aus Keyword_brazil_cnpj wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="e5c57-831">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-831">The checksum passes.</span></span>

<span data-ttu-id="e5c57-832">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-833">Die Funktion Func_brazil_cnpj findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-834">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-834">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-835">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-835">Keywords</span></span>

#### <a name="keyword_brazil_cnpj"></a><span data-ttu-id="e5c57-836">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="e5c57-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="e5c57-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="e5c57-837">CNPJ</span></span> 
- <span data-ttu-id="e5c57-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="e5c57-838">CNPJ/MF</span></span> 
- <span data-ttu-id="e5c57-839">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="e5c57-839">CNPJ-MF</span></span> 
- <span data-ttu-id="e5c57-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="e5c57-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="e5c57-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="e5c57-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="e5c57-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="e5c57-842">Legal entity</span></span> 
- <span data-ttu-id="e5c57-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="e5c57-843">Legal entities</span></span> 
- <span data-ttu-id="e5c57-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="e5c57-844">Registration Status</span></span> 
- <span data-ttu-id="e5c57-845">Business</span><span class="sxs-lookup"><span data-stu-id="e5c57-845">Business</span></span> 
- <span data-ttu-id="e5c57-846">Company</span><span class="sxs-lookup"><span data-stu-id="e5c57-846">Company</span></span>
- <span data-ttu-id="e5c57-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="e5c57-847">CNPJ</span></span> 
- <span data-ttu-id="e5c57-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="e5c57-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="e5c57-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="e5c57-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="e5c57-850">CGC</span><span class="sxs-lookup"><span data-stu-id="e5c57-850">CGC</span></span> 
- <span data-ttu-id="e5c57-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="e5c57-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="e5c57-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="e5c57-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="e5c57-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="e5c57-853">Situação cadastral</span></span> 
- <span data-ttu-id="e5c57-854">Inscrição</span><span class="sxs-lookup"><span data-stu-id="e5c57-854">Inscrição</span></span> 
- <span data-ttu-id="e5c57-855">Empresa</span><span class="sxs-lookup"><span data-stu-id="e5c57-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="e5c57-856">	Brasilien – Personalausweis (RG)</span><span class="sxs-lookup"><span data-stu-id="e5c57-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-857">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-857">Format</span></span>

<span data-ttu-id="e5c57-858">Registro Geral (altes Format): neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="e5c57-859">Registro de Identidade (RIC) (neues Format): 11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-860">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-860">Pattern</span></span>

<span data-ttu-id="e5c57-861">Registro Geral (altes Format):</span><span class="sxs-lookup"><span data-stu-id="e5c57-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="e5c57-862">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-862">Two digits</span></span> 
- <span data-ttu-id="e5c57-863">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="e5c57-863">A period</span></span> 
- <span data-ttu-id="e5c57-864">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-864">Three digits</span></span> 
- <span data-ttu-id="e5c57-865">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="e5c57-865">A period</span></span> 
- <span data-ttu-id="e5c57-866">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-866">Three digits</span></span> 
- <span data-ttu-id="e5c57-867">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-867">A hyphen</span></span> 
- <span data-ttu-id="e5c57-868">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-868">One digit which is a check digit</span></span>

<span data-ttu-id="e5c57-869">Registro de Identidade (RIC) (neues Format):</span><span class="sxs-lookup"><span data-stu-id="e5c57-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="e5c57-870">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-870">10 digits</span></span> 
- <span data-ttu-id="e5c57-871">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-871">A hyphen</span></span> 
- <span data-ttu-id="e5c57-872">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-873">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-873">Checksum</span></span>

<span data-ttu-id="e5c57-874">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-875">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-875">Definition</span></span>

<span data-ttu-id="e5c57-876">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-877">Die Funktion Func_brazil_rg findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-878">Ein Schlüsselwort aus Keyword_brazil_rg wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="e5c57-879">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-879">The checksum passes.</span></span>

<span data-ttu-id="e5c57-880">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-881">Die Funktion Func_brazil_rg findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-882">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-882">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-883">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-883">Keywords</span></span>

#### <a name="keyword_brazil_rg"></a><span data-ttu-id="e5c57-884">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="e5c57-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="e5c57-885">Cédula de identidade Personalausweis National ID número de rregistro Registro de Iidentidade Registro Geral RG (bei diesem Schlüsselwort wird die Groß-/Kleinschreibung beachtet) RIC (bei diesem Schlüsselwort wird die Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="e5c57-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="e5c57-886">Kanadische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-887">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-887">Format</span></span>

<span data-ttu-id="e5c57-888">Sieben oder zwölf Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-889">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-889">Pattern</span></span>

<span data-ttu-id="e5c57-890">Eine kanadische Kontonummer umfasst sieben oder zwölf Ziffern.</span><span class="sxs-lookup"><span data-stu-id="e5c57-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="e5c57-891">Eine kanadische Bankkontonummer setzt sich wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="e5c57-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="e5c57-892">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-892">Five digits</span></span> 
- <span data-ttu-id="e5c57-893">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-893">A hyphen</span></span> 
- <span data-ttu-id="e5c57-894">Drei Ziffern oder</span><span class="sxs-lookup"><span data-stu-id="e5c57-894">Three digits OR</span></span>
- <span data-ttu-id="e5c57-895">Eine 0 (null) </span><span class="sxs-lookup"><span data-stu-id="e5c57-895">A zero "0"</span></span> 
- <span data-ttu-id="e5c57-896">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-897">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-897">Checksum</span></span>

<span data-ttu-id="e5c57-898">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-899">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-899">Definition</span></span>

<span data-ttu-id="e5c57-900">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-901">Der reguläre Ausdruck Regex_canada_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-902">Ein Schlüsselwort aus Keyword_canada_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="e5c57-903">Der reguläre Ausdruck Regex_canada_bank_account_transit_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="e5c57-904">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-905">Der reguläre Ausdruck Regex_canada_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-906">Ein Schlüsselwort aus Keyword_canada_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-907">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-907">Keywords</span></span>

#### <a name="keyword_canada_bank_account_number"></a><span data-ttu-id="e5c57-908">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="e5c57-909">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="e5c57-909">canada savings bonds</span></span>
- <span data-ttu-id="e5c57-910">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="e5c57-910">canada revenue agency</span></span>
- <span data-ttu-id="e5c57-911">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="e5c57-911">canadian financial institution</span></span>
- <span data-ttu-id="e5c57-912">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="e5c57-912">direct deposit form</span></span>
- <span data-ttu-id="e5c57-913">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="e5c57-913">canadian citizen</span></span>
- <span data-ttu-id="e5c57-914">legal representative</span><span class="sxs-lookup"><span data-stu-id="e5c57-914">legal representative</span></span>
- <span data-ttu-id="e5c57-915">notary public</span><span class="sxs-lookup"><span data-stu-id="e5c57-915">notary public</span></span>
- <span data-ttu-id="e5c57-916">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="e5c57-916">commissioner for oaths</span></span>
- <span data-ttu-id="e5c57-917">child care benefit</span><span class="sxs-lookup"><span data-stu-id="e5c57-917">child care benefit</span></span>
- <span data-ttu-id="e5c57-918">universal child care</span><span class="sxs-lookup"><span data-stu-id="e5c57-918">universal child care</span></span>
- <span data-ttu-id="e5c57-919">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="e5c57-919">canada child tax benefit</span></span>
- <span data-ttu-id="e5c57-920">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="e5c57-920">income tax benefit</span></span>
- <span data-ttu-id="e5c57-921">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="e5c57-921">harmonized sales tax</span></span>
- <span data-ttu-id="e5c57-922">social insurance number</span><span class="sxs-lookup"><span data-stu-id="e5c57-922">social insurance number</span></span>
- <span data-ttu-id="e5c57-923">income tax refund</span><span class="sxs-lookup"><span data-stu-id="e5c57-923">income tax refund</span></span>
- <span data-ttu-id="e5c57-924">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="e5c57-924">child tax benefit</span></span>
- <span data-ttu-id="e5c57-925">territorial payments</span><span class="sxs-lookup"><span data-stu-id="e5c57-925">territorial payments</span></span>
- <span data-ttu-id="e5c57-926">institution number</span><span class="sxs-lookup"><span data-stu-id="e5c57-926">institution number</span></span>
- <span data-ttu-id="e5c57-927">deposit request</span><span class="sxs-lookup"><span data-stu-id="e5c57-927">deposit request</span></span>
- <span data-ttu-id="e5c57-928">banking information</span><span class="sxs-lookup"><span data-stu-id="e5c57-928">banking information</span></span>
- <span data-ttu-id="e5c57-929">direct deposit</span><span class="sxs-lookup"><span data-stu-id="e5c57-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="e5c57-930">Kanadische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-931">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-931">Format</span></span>

<span data-ttu-id="e5c57-932">Variiert je nach Provinz</span><span class="sxs-lookup"><span data-stu-id="e5c57-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-933">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-933">Pattern</span></span>

<span data-ttu-id="e5c57-934">Verschiedene Muster in Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec und Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="e5c57-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-935">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-935">Checksum</span></span>

<span data-ttu-id="e5c57-936">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-937">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-937">Definition</span></span>

<span data-ttu-id="e5c57-938">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-939">Die Funktion Func_[province_name]_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-940">Ein Schlüsselwort aus Keyword_[province_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="e5c57-941">Ein Schlüsselwort aus Keyword_canada_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-942">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-942">Keywords</span></span>

#### <a name="keyword_province_name_drivers_license_name"></a><span data-ttu-id="e5c57-943">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="e5c57-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="e5c57-944">Die Abkürzung für die Provinz, z. B. AB</span><span class="sxs-lookup"><span data-stu-id="e5c57-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="e5c57-945">Der Name der Provinz, beispielsweise „Alberta“</span><span class="sxs-lookup"><span data-stu-id="e5c57-945">The province name, for example Alberta</span></span>

#### <a name="keyword_canada_drivers_license"></a><span data-ttu-id="e5c57-946">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="e5c57-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="e5c57-947">DL</span><span class="sxs-lookup"><span data-stu-id="e5c57-947">DL</span></span>
- <span data-ttu-id="e5c57-948">DLS</span><span class="sxs-lookup"><span data-stu-id="e5c57-948">DLS</span></span>
- <span data-ttu-id="e5c57-949">CDL</span><span class="sxs-lookup"><span data-stu-id="e5c57-949">CDL</span></span>
- <span data-ttu-id="e5c57-950">CDLS</span><span class="sxs-lookup"><span data-stu-id="e5c57-950">CDLS</span></span>
- <span data-ttu-id="e5c57-951">DriverLic</span><span class="sxs-lookup"><span data-stu-id="e5c57-951">DriverLic</span></span>
- <span data-ttu-id="e5c57-952">DriverLics</span><span class="sxs-lookup"><span data-stu-id="e5c57-952">DriverLics</span></span>
- <span data-ttu-id="e5c57-953">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="e5c57-953">DriverLicense</span></span>
- <span data-ttu-id="e5c57-954">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-954">DriverLicenses</span></span>
- <span data-ttu-id="e5c57-955">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="e5c57-955">DriverLicence</span></span>
- <span data-ttu-id="e5c57-956">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="e5c57-956">DriverLicences</span></span>
- <span data-ttu-id="e5c57-957">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-957">Driver Lic</span></span>
- <span data-ttu-id="e5c57-958">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-958">Driver Lics</span></span>
- <span data-ttu-id="e5c57-959">Driver License</span><span class="sxs-lookup"><span data-stu-id="e5c57-959">Driver License</span></span>
- <span data-ttu-id="e5c57-960">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-960">Driver Licenses</span></span>
- <span data-ttu-id="e5c57-961">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-961">Driver Licence</span></span>
- <span data-ttu-id="e5c57-962">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-962">Driver Licences</span></span>
- <span data-ttu-id="e5c57-963">DriversLic</span><span class="sxs-lookup"><span data-stu-id="e5c57-963">DriversLic</span></span>
- <span data-ttu-id="e5c57-964">DriversLics</span><span class="sxs-lookup"><span data-stu-id="e5c57-964">DriversLics</span></span>
- <span data-ttu-id="e5c57-965">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="e5c57-965">DriversLicence</span></span>
- <span data-ttu-id="e5c57-966">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="e5c57-966">DriversLicences</span></span>
- <span data-ttu-id="e5c57-967">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="e5c57-967">DriversLicense</span></span>
- <span data-ttu-id="e5c57-968">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-968">DriversLicenses</span></span>
- <span data-ttu-id="e5c57-969">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-969">Drivers Lic</span></span>
- <span data-ttu-id="e5c57-970">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-970">Drivers Lics</span></span>
- <span data-ttu-id="e5c57-971">Drivers License</span><span class="sxs-lookup"><span data-stu-id="e5c57-971">Drivers License</span></span>
- <span data-ttu-id="e5c57-972">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-972">Drivers Licenses</span></span>
- <span data-ttu-id="e5c57-973">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-973">Drivers Licence</span></span>
- <span data-ttu-id="e5c57-974">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-974">Drivers Licences</span></span>
- <span data-ttu-id="e5c57-975">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-975">Driver'Lic</span></span>
- <span data-ttu-id="e5c57-976">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-976">Driver'Lics</span></span>
- <span data-ttu-id="e5c57-977">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="e5c57-977">Driver'License</span></span>
- <span data-ttu-id="e5c57-978">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-978">Driver'Licenses</span></span>
- <span data-ttu-id="e5c57-979">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-979">Driver'Licence</span></span>
- <span data-ttu-id="e5c57-980">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-980">Driver'Licences</span></span>
- <span data-ttu-id="e5c57-981">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-981">Driver' Lic</span></span>
- <span data-ttu-id="e5c57-982">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-982">Driver' Lics</span></span>
- <span data-ttu-id="e5c57-983">Driver' License</span><span class="sxs-lookup"><span data-stu-id="e5c57-983">Driver' License</span></span>
- <span data-ttu-id="e5c57-984">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-984">Driver' Licenses</span></span>
- <span data-ttu-id="e5c57-985">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-985">Driver' Licence</span></span>
- <span data-ttu-id="e5c57-986">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-986">Driver' Licences</span></span>
- <span data-ttu-id="e5c57-987">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="e5c57-987">Driver'sLic</span></span>
- <span data-ttu-id="e5c57-988">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="e5c57-988">Driver'sLics</span></span>
- <span data-ttu-id="e5c57-989">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="e5c57-989">Driver'sLicense</span></span>
- <span data-ttu-id="e5c57-990">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-990">Driver'sLicenses</span></span>
- <span data-ttu-id="e5c57-991">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="e5c57-991">Driver'sLicence</span></span>
- <span data-ttu-id="e5c57-992">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="e5c57-992">Driver'sLicences</span></span>
- <span data-ttu-id="e5c57-993">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-993">Driver's Lic</span></span>
- <span data-ttu-id="e5c57-994">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-994">Driver's Lics</span></span>
- <span data-ttu-id="e5c57-995">Driver's License</span><span class="sxs-lookup"><span data-stu-id="e5c57-995">Driver's License</span></span>
- <span data-ttu-id="e5c57-996">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-996">Driver's Licenses</span></span>
- <span data-ttu-id="e5c57-997">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-997">Driver's Licence</span></span>
- <span data-ttu-id="e5c57-998">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-998">Driver's Licences</span></span>
- <span data-ttu-id="e5c57-999">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="e5c57-999">Permis de Conduire</span></span>
- <span data-ttu-id="e5c57-1000">id</span><span class="sxs-lookup"><span data-stu-id="e5c57-1000">id</span></span>
- <span data-ttu-id="e5c57-1001">ids</span><span class="sxs-lookup"><span data-stu-id="e5c57-1001">ids</span></span>
- <span data-ttu-id="e5c57-1002">idcard number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1002">idcard number</span></span>
- <span data-ttu-id="e5c57-1003">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="e5c57-1003">idcard numbers</span></span>
- <span data-ttu-id="e5c57-1004">idcard #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1004">idcard #</span></span>
- <span data-ttu-id="e5c57-1005">idcard #s</span><span class="sxs-lookup"><span data-stu-id="e5c57-1005">idcard #s</span></span>
- <span data-ttu-id="e5c57-1006">idcard card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1006">idcard card</span></span>
- <span data-ttu-id="e5c57-1007">idcard cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1007">idcard cards</span></span>
- <span data-ttu-id="e5c57-1008">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-1008">idcard</span></span>
- <span data-ttu-id="e5c57-1009">identification number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1009">identification number</span></span>
- <span data-ttu-id="e5c57-1010">identification numbers</span><span class="sxs-lookup"><span data-stu-id="e5c57-1010">identification numbers</span></span>
- <span data-ttu-id="e5c57-1011">identification #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1011">identification #</span></span>
- <span data-ttu-id="e5c57-1012">identification #s</span><span class="sxs-lookup"><span data-stu-id="e5c57-1012">identification #s</span></span>
- <span data-ttu-id="e5c57-1013">identification card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1013">identification card</span></span>
- <span data-ttu-id="e5c57-1014">identification cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1014">identification cards</span></span>
- <span data-ttu-id="e5c57-1015">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="e5c57-1015">identification</span></span> 
- <span data-ttu-id="e5c57-1016">DL #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1016">DL#</span></span>
- <span data-ttu-id="e5c57-1017">DLS #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1017">DLS#</span></span> 
- <span data-ttu-id="e5c57-1018">CDL #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1018">CDL#</span></span> 
- <span data-ttu-id="e5c57-1019">CDLS #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1019">CDLS#</span></span> 
- <span data-ttu-id="e5c57-1020">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1020">DriverLic#</span></span> 
- <span data-ttu-id="e5c57-1021">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1021">DriverLics#</span></span> 
- <span data-ttu-id="e5c57-1022">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1022">DriverLicense#</span></span> 
- <span data-ttu-id="e5c57-1023">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="e5c57-1024">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1024">DriverLicence#</span></span> 
- <span data-ttu-id="e5c57-1025">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1025">DriverLicences#</span></span> 
- <span data-ttu-id="e5c57-1026">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1026">Driver Lic#</span></span>
- <span data-ttu-id="e5c57-1027">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1027">Driver Lics#</span></span> 
- <span data-ttu-id="e5c57-1028">Driver License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1028">Driver License#</span></span> 
- <span data-ttu-id="e5c57-1029">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="e5c57-1030">Driver License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1030">Driver License#</span></span> 
- <span data-ttu-id="e5c57-1031">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1031">Driver Licences#</span></span> 
- <span data-ttu-id="e5c57-1032">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1032">DriversLic#</span></span> 
- <span data-ttu-id="e5c57-1033">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1033">DriversLics#</span></span> 
- <span data-ttu-id="e5c57-1034">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1034">DriversLicense#</span></span> 
- <span data-ttu-id="e5c57-1035">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="e5c57-1036">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1036">DriversLicence#</span></span> 
- <span data-ttu-id="e5c57-1037">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1037">DriversLicences#</span></span> 
- <span data-ttu-id="e5c57-1038">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="e5c57-1039">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="e5c57-1040">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1040">Drivers License#</span></span> 
- <span data-ttu-id="e5c57-1041">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="e5c57-1042">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="e5c57-1043">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="e5c57-1044">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="e5c57-1045">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="e5c57-1046">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1046">Driver'License#</span></span> 
- <span data-ttu-id="e5c57-1047">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="e5c57-1048">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="e5c57-1049">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="e5c57-1050">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="e5c57-1051">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="e5c57-1052">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1052">Driver' License#</span></span> 
- <span data-ttu-id="e5c57-1053">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="e5c57-1054">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="e5c57-1055">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="e5c57-1056">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="e5c57-1057">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="e5c57-1058">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="e5c57-1059">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="e5c57-1060">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="e5c57-1061">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="e5c57-1062">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="e5c57-1063">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="e5c57-1064">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1064">Driver's License#</span></span> 
- <span data-ttu-id="e5c57-1065">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="e5c57-1066">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="e5c57-1067">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="e5c57-1068">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="e5c57-1069">ID #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1069">id#</span></span> 
- <span data-ttu-id="e5c57-1070">IDs #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1070">ids#</span></span> 
- <span data-ttu-id="e5c57-1071">idcard card#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1071">idcard card#</span></span> 
- <span data-ttu-id="e5c57-1072">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1072">idcard cards#</span></span> 
- <span data-ttu-id="e5c57-1073">Personalausweis #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1073">idcard#</span></span> 
- <span data-ttu-id="e5c57-1074">identification card#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1074">identification card#</span></span> 
- <span data-ttu-id="e5c57-1075">identification cards#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1075">identification cards#</span></span> 
- <span data-ttu-id="e5c57-1076">Identifizierung #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="e5c57-1077">Kanadische Health Service-Nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1078">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1078">Format</span></span>

<span data-ttu-id="e5c57-1079">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1080">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1080">Pattern</span></span>

<span data-ttu-id="e5c57-1081">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1082">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1082">Checksum</span></span>

<span data-ttu-id="e5c57-1083">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1084">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1084">Definition</span></span>

<span data-ttu-id="e5c57-1085">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1086">Der reguläre Ausdruck Regex_canada_health_service_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1087">Ein Schlüsselwort aus Keyword_canada_health_service_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-1088">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1088">Keywords</span></span>

#### <a name="keyword_canada_health_service_number"></a><span data-ttu-id="e5c57-1089">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="e5c57-1090">personal health number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1090">personal health number</span></span>
- <span data-ttu-id="e5c57-1091">patient information</span><span class="sxs-lookup"><span data-stu-id="e5c57-1091">patient information</span></span>
- <span data-ttu-id="e5c57-1092">health services</span><span class="sxs-lookup"><span data-stu-id="e5c57-1092">health services</span></span>
- <span data-ttu-id="e5c57-1093">speciality services</span><span class="sxs-lookup"><span data-stu-id="e5c57-1093">speciality services</span></span>
- <span data-ttu-id="e5c57-1094">automobile accident</span><span class="sxs-lookup"><span data-stu-id="e5c57-1094">automobile accident</span></span>
- <span data-ttu-id="e5c57-1095">patient hospital</span><span class="sxs-lookup"><span data-stu-id="e5c57-1095">patient hospital</span></span>
- <span data-ttu-id="e5c57-1096">Psychiater</span><span class="sxs-lookup"><span data-stu-id="e5c57-1096">psychiatrist</span></span>
- <span data-ttu-id="e5c57-1097">workers compensation</span><span class="sxs-lookup"><span data-stu-id="e5c57-1097">workers compensation</span></span>
- <span data-ttu-id="e5c57-1098">Disability</span><span class="sxs-lookup"><span data-stu-id="e5c57-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="e5c57-1099">Kanadische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1100">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1100">Format</span></span>

<span data-ttu-id="e5c57-1101">Zwei Großbuchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1102">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1102">Pattern</span></span>

<span data-ttu-id="e5c57-1103">Zwei Großbuchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1104">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1104">Checksum</span></span>

<span data-ttu-id="e5c57-1105">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1106">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1106">Definition</span></span>

<span data-ttu-id="e5c57-1107">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1108">Der reguläre Ausdruck Regex_canada_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1109">Ein Schlüsselwort aus Keyword_canada_passport_number oder Keyword_passport wird gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-1110">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1110">Keywords</span></span>

#### <a name="keyword_canada_passport_number"></a><span data-ttu-id="e5c57-1111">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="e5c57-1112">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="e5c57-1112">canadian citizenship</span></span>
- <span data-ttu-id="e5c57-1113">canadian passport</span><span class="sxs-lookup"><span data-stu-id="e5c57-1113">canadian passport</span></span>
- <span data-ttu-id="e5c57-1114">passport application</span><span class="sxs-lookup"><span data-stu-id="e5c57-1114">passport application</span></span>
- <span data-ttu-id="e5c57-1115">passport photos</span><span class="sxs-lookup"><span data-stu-id="e5c57-1115">passport photos</span></span>
- <span data-ttu-id="e5c57-1116">certified translator</span><span class="sxs-lookup"><span data-stu-id="e5c57-1116">certified translator</span></span>
- <span data-ttu-id="e5c57-1117">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="e5c57-1117">canadian citizens</span></span>
- <span data-ttu-id="e5c57-1118">processing times</span><span class="sxs-lookup"><span data-stu-id="e5c57-1118">processing times</span></span>
- <span data-ttu-id="e5c57-1119">renewal application</span><span class="sxs-lookup"><span data-stu-id="e5c57-1119">renewal application</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="e5c57-1120">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="e5c57-1120">Keyword_passport</span></span>

- <span data-ttu-id="e5c57-1121">Passport Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1121">Passport Number</span></span>
- <span data-ttu-id="e5c57-1122">Passport No</span><span class="sxs-lookup"><span data-stu-id="e5c57-1122">Passport No</span></span>
- <span data-ttu-id="e5c57-1123">Passport#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1123">Passport #</span></span>
- <span data-ttu-id="e5c57-1124">Pass #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1124">Passport#</span></span>
- <span data-ttu-id="e5c57-1125">Passport-Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-1125">PassportID</span></span>
- <span data-ttu-id="e5c57-1126">Passportno</span><span class="sxs-lookup"><span data-stu-id="e5c57-1126">Passportno</span></span>
- <span data-ttu-id="e5c57-1127">passportnumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-1127">passportnumber</span></span>
- <span data-ttu-id="e5c57-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="e5c57-1128">パスポート</span></span>
- <span data-ttu-id="e5c57-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-1129">パスポート番号</span></span>
- <span data-ttu-id="e5c57-1130">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="e5c57-1130">パスポートのNum</span></span>
- <span data-ttu-id="e5c57-1131">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-1131">パスポート＃</span></span>
- <span data-ttu-id="e5c57-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="e5c57-1132">Numéro de passeport</span></span>
- <span data-ttu-id="e5c57-1133">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="e5c57-1133">Passeport n °</span></span>
- <span data-ttu-id="e5c57-1134">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="e5c57-1134">Passeport Non</span></span>
- <span data-ttu-id="e5c57-1135">Passeport#</span><span class="sxs-lookup"><span data-stu-id="e5c57-1135">Passeport #</span></span>
- <span data-ttu-id="e5c57-1136">Passeport #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1136">Passeport#</span></span>
- <span data-ttu-id="e5c57-1137">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="e5c57-1137">PasseportNon</span></span>
- <span data-ttu-id="e5c57-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="e5c57-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="e5c57-1139">Kanadische Personal Health Identification-Nummer (PHIN)</span><span class="sxs-lookup"><span data-stu-id="e5c57-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1140">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1140">Format</span></span>

<span data-ttu-id="e5c57-1141">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1142">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1142">Pattern</span></span>

<span data-ttu-id="e5c57-1143">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1144">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1144">Checksum</span></span>

<span data-ttu-id="e5c57-1145">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1146">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1146">Definition</span></span>

<span data-ttu-id="e5c57-1147">Eine DLP-Richtlinie ist 75% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: der reguläre Ausdruck Regex_canada_phin findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="e5c57-1148">Mindestens zwei Schlüsselwörter aus Keyword_canada_phin oder Keyword_canada_provinces werden gefunden..</span><span class="sxs-lookup"><span data-stu-id="e5c57-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-1149">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1149">Keywords</span></span>

#### <a name="keyword_canada_phin"></a><span data-ttu-id="e5c57-1150">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="e5c57-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="e5c57-1151">social insurance number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1151">social insurance number</span></span>
- <span data-ttu-id="e5c57-1152">health information act</span><span class="sxs-lookup"><span data-stu-id="e5c57-1152">health information act</span></span>
- <span data-ttu-id="e5c57-1153">income tax information</span><span class="sxs-lookup"><span data-stu-id="e5c57-1153">income tax information</span></span>
- <span data-ttu-id="e5c57-1154">manitoba health</span><span class="sxs-lookup"><span data-stu-id="e5c57-1154">manitoba health</span></span>
- <span data-ttu-id="e5c57-1155">health registration</span><span class="sxs-lookup"><span data-stu-id="e5c57-1155">health registration</span></span>
- <span data-ttu-id="e5c57-1156">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="e5c57-1156">prescription purchases</span></span>
- <span data-ttu-id="e5c57-1157">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="e5c57-1157">benefit eligibility</span></span>
- <span data-ttu-id="e5c57-1158">personal health</span><span class="sxs-lookup"><span data-stu-id="e5c57-1158">personal health</span></span>
- <span data-ttu-id="e5c57-1159">power of attorney</span><span class="sxs-lookup"><span data-stu-id="e5c57-1159">power of attorney</span></span>
- <span data-ttu-id="e5c57-1160">registration number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1160">registration number</span></span>
- <span data-ttu-id="e5c57-1161">personal health number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1161">personal health number</span></span>
- <span data-ttu-id="e5c57-1162">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="e5c57-1162">practitioner referral</span></span>
- <span data-ttu-id="e5c57-1163">wellness professional</span><span class="sxs-lookup"><span data-stu-id="e5c57-1163">wellness professional</span></span>
- <span data-ttu-id="e5c57-1164">patient referral</span><span class="sxs-lookup"><span data-stu-id="e5c57-1164">patient referral</span></span>
- <span data-ttu-id="e5c57-1165">health and wellness</span><span class="sxs-lookup"><span data-stu-id="e5c57-1165">health and wellness</span></span>

#### <a name="keyword_canada_provinces"></a><span data-ttu-id="e5c57-1166">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="e5c57-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="e5c57-1167">Nunavut</span><span class="sxs-lookup"><span data-stu-id="e5c57-1167">Nunavut</span></span>
- <span data-ttu-id="e5c57-1168">Quebec</span><span class="sxs-lookup"><span data-stu-id="e5c57-1168">Quebec</span></span>
- <span data-ttu-id="e5c57-1169">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="e5c57-1169">Northwest Territories</span></span>
- <span data-ttu-id="e5c57-1170">Ontario</span><span class="sxs-lookup"><span data-stu-id="e5c57-1170">Ontario</span></span>
- <span data-ttu-id="e5c57-1171">British Columbia</span><span class="sxs-lookup"><span data-stu-id="e5c57-1171">British Columbia</span></span>
- <span data-ttu-id="e5c57-1172">Alberta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1172">Alberta</span></span>
- <span data-ttu-id="e5c57-1173">Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="e5c57-1173">Saskatchewan</span></span>
- <span data-ttu-id="e5c57-1174">Manitoba</span><span class="sxs-lookup"><span data-stu-id="e5c57-1174">Manitoba</span></span>
- <span data-ttu-id="e5c57-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="e5c57-1175">Yukon</span></span>
- <span data-ttu-id="e5c57-1176">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="e5c57-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="e5c57-1177">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="e5c57-1177">New Brunswick</span></span>
- <span data-ttu-id="e5c57-1178">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="e5c57-1178">Nova Scotia</span></span>
- <span data-ttu-id="e5c57-1179">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="e5c57-1179">Prince Edward Island</span></span>
- <span data-ttu-id="e5c57-1180">Kanada</span><span class="sxs-lookup"><span data-stu-id="e5c57-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="e5c57-1181">Kanadische Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1182">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1182">Format</span></span>

<span data-ttu-id="e5c57-1183">Neun Ziffern mit optionalen Bindestrichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1184">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1184">Pattern</span></span>

<span data-ttu-id="e5c57-1185">Formatiert</span><span class="sxs-lookup"><span data-stu-id="e5c57-1185">Formatted:</span></span>
- <span data-ttu-id="e5c57-1186">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1186">Three digits</span></span> 
- <span data-ttu-id="e5c57-1187">Ein Bindestrich oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-1187">A hyphen or space</span></span> 
- <span data-ttu-id="e5c57-1188">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1188">Three digits</span></span> 
- <span data-ttu-id="e5c57-1189">Ein Bindestrich oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-1189">A hyphen or space</span></span> 
- <span data-ttu-id="e5c57-1190">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1190">Three digits</span></span>

<span data-ttu-id="e5c57-1191">Unformatiert: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1192">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1192">Checksum</span></span>

<span data-ttu-id="e5c57-1193">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1194">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1194">Definition</span></span>

<span data-ttu-id="e5c57-1195">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1196">Die Funktion Func_canadian_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1197">Mindestens zwei dieser eine beliebige Kombination der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="e5c57-1198">Ein Schlüsselwort aus Keyword_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="e5c57-1199">Ein Schlüsselwort aus Keyword_sin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="e5c57-1200">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="e5c57-1201">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1201">The checksum passes.</span></span>

<span data-ttu-id="e5c57-1202">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1203">Die Funktion Func_unformatted_canadian_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1204">Ein Schlüsselwort aus Keyword_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="e5c57-1205">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1205">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-1206">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1206">Keywords</span></span>

#### <a name="keyword_sin"></a><span data-ttu-id="e5c57-1207">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="e5c57-1207">Keyword_sin</span></span>

- <span data-ttu-id="e5c57-1208">sin</span><span class="sxs-lookup"><span data-stu-id="e5c57-1208">sin</span></span> 
- <span data-ttu-id="e5c57-1209">social insurance</span><span class="sxs-lookup"><span data-stu-id="e5c57-1209">social insurance</span></span> 
- <span data-ttu-id="e5c57-1210">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="e5c57-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="e5c57-1211">Todsünden</span><span class="sxs-lookup"><span data-stu-id="e5c57-1211">sins</span></span> 
- <span data-ttu-id="e5c57-1212">SSN</span><span class="sxs-lookup"><span data-stu-id="e5c57-1212">ssn</span></span> 
- <span data-ttu-id="e5c57-1213">Sozialversicherungsnummern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1213">ssns</span></span> 
- <span data-ttu-id="e5c57-1214">social security</span><span class="sxs-lookup"><span data-stu-id="e5c57-1214">social security</span></span> 
- <span data-ttu-id="e5c57-1215">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="e5c57-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="e5c57-1216">national identification number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1216">national identification number</span></span> 
- <span data-ttu-id="e5c57-1217">national id</span><span class="sxs-lookup"><span data-stu-id="e5c57-1217">national id</span></span> 
- <span data-ttu-id="e5c57-1218">Sin #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1218">sin#</span></span> 
- <span data-ttu-id="e5c57-1219">soc ins</span><span class="sxs-lookup"><span data-stu-id="e5c57-1219">soc ins</span></span> 
- <span data-ttu-id="e5c57-1220">social ins</span><span class="sxs-lookup"><span data-stu-id="e5c57-1220">social ins</span></span> 

#### <a name="keyword_sin_collaborative"></a><span data-ttu-id="e5c57-1221">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="e5c57-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="e5c57-1222">driver's license</span><span class="sxs-lookup"><span data-stu-id="e5c57-1222">driver's license</span></span> 
- <span data-ttu-id="e5c57-1223">drivers license</span><span class="sxs-lookup"><span data-stu-id="e5c57-1223">drivers license</span></span> 
- <span data-ttu-id="e5c57-1224">driver's licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-1224">driver's licence</span></span> 
- <span data-ttu-id="e5c57-1225">drivers licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-1225">drivers licence</span></span> 
- <span data-ttu-id="e5c57-1226">DOB</span><span class="sxs-lookup"><span data-stu-id="e5c57-1226">DOB</span></span> 
- <span data-ttu-id="e5c57-1227">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-1227">Birthdate</span></span> 
- <span data-ttu-id="e5c57-1228">Geburtstag</span><span class="sxs-lookup"><span data-stu-id="e5c57-1228">Birthday</span></span> 
- <span data-ttu-id="e5c57-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="e5c57-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="e5c57-1230">	Chile Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1231">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1231">Format</span></span>

<span data-ttu-id="e5c57-1232">7-8 Ziffern Plus Trennzeichen für eine Prüfziffer oder einen Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e5c57-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1233">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1233">Pattern</span></span>

<span data-ttu-id="e5c57-1234">7-8 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="e5c57-1235">1-2 Ziffern </span><span class="sxs-lookup"><span data-stu-id="e5c57-1235">1-2 digits</span></span> 
- <span data-ttu-id="e5c57-1236">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="e5c57-1236">A period</span></span> 
- <span data-ttu-id="e5c57-1237">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1237">Three digits</span></span> 
- <span data-ttu-id="e5c57-1238">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="e5c57-1238">A period</span></span> 
- <span data-ttu-id="e5c57-1239">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1239">Three digits</span></span> 
- <span data-ttu-id="e5c57-1240">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-1240">A dash</span></span> 
- <span data-ttu-id="e5c57-1241">Eine Ziffer oder ein Buchstabe (Groß-/Kleinschreibung nicht unterschieden), die bzw. der eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="e5c57-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1242">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1242">Checksum</span></span>

<span data-ttu-id="e5c57-1243">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1244">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1244">Definition</span></span>

<span data-ttu-id="e5c57-1245">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1246">Die Funktion Func_chile_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1247">Ein Schlüsselwort aus Keyword_chile_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="e5c57-1248">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1248">The checksum passes.</span></span>

<span data-ttu-id="e5c57-1249">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1250">Die Funktion Func_chile_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1251">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1251">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-1252">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1252">Keywords</span></span>

#### <a name="keyword_chile_id_card"></a><span data-ttu-id="e5c57-1253">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="e5c57-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1254">National Identification Number</span></span> 
- <span data-ttu-id="e5c57-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1255">Identity card</span></span> 
- <span data-ttu-id="e5c57-1256">ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-1256">ID</span></span> 
- <span data-ttu-id="e5c57-1257">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="e5c57-1257">Identification</span></span> 
- <span data-ttu-id="e5c57-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="e5c57-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="e5c57-1259">Ausführen</span><span class="sxs-lookup"><span data-stu-id="e5c57-1259">RUN</span></span> 
- <span data-ttu-id="e5c57-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="e5c57-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="e5c57-1261">Rut</span><span class="sxs-lookup"><span data-stu-id="e5c57-1261">RUT</span></span> 
- <span data-ttu-id="e5c57-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="e5c57-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="e5c57-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="e5c57-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="e5c57-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="e5c57-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="e5c57-1265">Identificación</span><span class="sxs-lookup"><span data-stu-id="e5c57-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="e5c57-1266">	China (PRC) – Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1267">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1267">Format</span></span>

<span data-ttu-id="e5c57-1268">18 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1269">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1269">Pattern</span></span>

<span data-ttu-id="e5c57-1270">18 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1270">18 digits:</span></span>
- <span data-ttu-id="e5c57-1271">Sechs Ziffern, die einen Adresscode angeben </span><span class="sxs-lookup"><span data-stu-id="e5c57-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="e5c57-1272">Acht Ziffern im Fomat JJJJMMTT, wobei es sich um das Geburtsdatum handelt </span><span class="sxs-lookup"><span data-stu-id="e5c57-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="e5c57-1273">Drei Ziffern, die ein Reihenfolgencode sind </span><span class="sxs-lookup"><span data-stu-id="e5c57-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="e5c57-1274">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1275">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1275">Checksum</span></span>

<span data-ttu-id="e5c57-1276">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1277">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1277">Definition</span></span>

<span data-ttu-id="e5c57-1278">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1279">Die Funktion Func_china_resident_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1280">Ein Schlüsselwort aus Keyword_china_resident_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="e5c57-1281">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1281">The checksum passes.</span></span>

<span data-ttu-id="e5c57-1282">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1283">Die Funktion Func_china_resident_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1284">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1284">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-1285">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1285">Keywords</span></span>

### <a name="keyword_china_resident_id"></a><span data-ttu-id="e5c57-1286">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="e5c57-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="e5c57-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="e5c57-1288">PRC</span><span class="sxs-lookup"><span data-stu-id="e5c57-1288">PRC</span></span> 
- <span data-ttu-id="e5c57-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1289">National Identification Card</span></span> 
- <span data-ttu-id="e5c57-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="e5c57-1290">身份证</span></span> 
- <span data-ttu-id="e5c57-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="e5c57-1291">居民 身份证</span></span> 
- <span data-ttu-id="e5c57-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="e5c57-1292">居民身份证</span></span> 
- <span data-ttu-id="e5c57-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="e5c57-1293">鉴定</span></span> 
- <span data-ttu-id="e5c57-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="e5c57-1294">身分證</span></span> 
- <span data-ttu-id="e5c57-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-1295">居民 身份證</span></span>
- <span data-ttu-id="e5c57-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="e5c57-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="e5c57-1297">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1298">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1298">Format</span></span>

<span data-ttu-id="e5c57-1299">16 Ziffern, die formatiert oder unformatiert (dddddddddddddddd) sein können und den Luhn-Test bestehen müssen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1299">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1300">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1300">Pattern</span></span>

<span data-ttu-id="e5c57-1301">Sehr komplexe und robuste Muster, die Karten aller wichtigen Marken weltweit, einschließlich Visa, MasterCard, Discover-Karte, JCB, American Express, Geschenkgutscheine und Restaurantkarten erkennen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1302">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1302">Checksum</span></span>

<span data-ttu-id="e5c57-1303">Ja, die Luhn-Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1304">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1304">Definition</span></span>

<span data-ttu-id="e5c57-1305">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1306">Die Funktion Func_credit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1307">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1307">One of the following is true:</span></span>
    - <span data-ttu-id="e5c57-1308">Ein Schlüsselwort aus Keyword_cc_verification wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="e5c57-1309">Ein Schlüsselwort aus Keyword_cc_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="e5c57-1310">Die Funktion Func_expiration_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="e5c57-1311">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1311">The checksum passes.</span></span>

<span data-ttu-id="e5c57-1312">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1313">Die Funktion Func_credit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1314">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1314">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-1315">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1315">Keywords</span></span>

#### <a name="keyword_cc_verification"></a><span data-ttu-id="e5c57-1316">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="e5c57-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="e5c57-1317">card verification</span><span class="sxs-lookup"><span data-stu-id="e5c57-1317">card verification</span></span>
- <span data-ttu-id="e5c57-1318">card identification number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1318">card identification number</span></span>
- <span data-ttu-id="e5c57-1319">CVN</span><span class="sxs-lookup"><span data-stu-id="e5c57-1319">cvn</span></span>
- <span data-ttu-id="e5c57-1320">cid</span><span class="sxs-lookup"><span data-stu-id="e5c57-1320">cid</span></span>
- <span data-ttu-id="e5c57-1321">CVC2</span><span class="sxs-lookup"><span data-stu-id="e5c57-1321">cvc2</span></span>
- <span data-ttu-id="e5c57-1322">CVV2</span><span class="sxs-lookup"><span data-stu-id="e5c57-1322">cvv2</span></span>
- <span data-ttu-id="e5c57-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="e5c57-1323">pin block</span></span>
- <span data-ttu-id="e5c57-1324">security code</span><span class="sxs-lookup"><span data-stu-id="e5c57-1324">security code</span></span>
- <span data-ttu-id="e5c57-1325">security number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1325">security number</span></span>
- <span data-ttu-id="e5c57-1326">security no</span><span class="sxs-lookup"><span data-stu-id="e5c57-1326">security no</span></span>
- <span data-ttu-id="e5c57-1327">issue number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1327">issue number</span></span>
- <span data-ttu-id="e5c57-1328">issue no</span><span class="sxs-lookup"><span data-stu-id="e5c57-1328">issue no</span></span>
- <span data-ttu-id="e5c57-1329">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1329">cryptogramme</span></span>
- <span data-ttu-id="e5c57-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="e5c57-1330">numéro de sécurité</span></span>
- <span data-ttu-id="e5c57-1331">numero de securite</span><span class="sxs-lookup"><span data-stu-id="e5c57-1331">numero de securite</span></span>
- <span data-ttu-id="e5c57-1332">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="e5c57-1333">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="e5c57-1334">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1334">prüfziffer</span></span>
- <span data-ttu-id="e5c57-1335">prufziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1335">prufziffer</span></span>
- <span data-ttu-id="e5c57-1336">Sicherheitskode</span><span class="sxs-lookup"><span data-stu-id="e5c57-1336">sicherheits Kode</span></span>
- <span data-ttu-id="e5c57-1337">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="e5c57-1337">sicherheitscode</span></span>
- <span data-ttu-id="e5c57-1338">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="e5c57-1339">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-1339">verfalldatum</span></span>
- <span data-ttu-id="e5c57-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="e5c57-1340">codice di verifica</span></span>
- <span data-ttu-id="e5c57-1341">COD.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1341">cod.</span></span> <span data-ttu-id="e5c57-1342">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1342">sicurezza</span></span>
- <span data-ttu-id="e5c57-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1343">cod sicurezza</span></span>
- <span data-ttu-id="e5c57-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="e5c57-1344">n autorizzazione</span></span>
- <span data-ttu-id="e5c57-1345">Código</span><span class="sxs-lookup"><span data-stu-id="e5c57-1345">código</span></span>
- <span data-ttu-id="e5c57-1346">codigo</span><span class="sxs-lookup"><span data-stu-id="e5c57-1346">codigo</span></span>
- <span data-ttu-id="e5c57-1347">COD.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1347">cod.</span></span> <span data-ttu-id="e5c57-1348">SEG</span><span class="sxs-lookup"><span data-stu-id="e5c57-1348">seg</span></span>
- <span data-ttu-id="e5c57-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="e5c57-1349">cod seg</span></span>
- <span data-ttu-id="e5c57-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1350">código de segurança</span></span>
- <span data-ttu-id="e5c57-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1351">codigo de seguranca</span></span>
- <span data-ttu-id="e5c57-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1352">codigo de segurança</span></span>
- <span data-ttu-id="e5c57-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1353">código de seguranca</span></span>
- <span data-ttu-id="e5c57-1354">cód.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1354">cód.</span></span> <span data-ttu-id="e5c57-1355">Segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1355">segurança</span></span>
- <span data-ttu-id="e5c57-1356">COD.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1356">cod.</span></span> <span data-ttu-id="e5c57-1357">Seguranca COD.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1357">seguranca cod.</span></span> <span data-ttu-id="e5c57-1358">Segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1358">segurança</span></span>
- <span data-ttu-id="e5c57-1359">cód.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1359">cód.</span></span> <span data-ttu-id="e5c57-1360">seguranca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1360">seguranca</span></span>
- <span data-ttu-id="e5c57-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1361">cód segurança</span></span>
- <span data-ttu-id="e5c57-1362">COD Seguranca COD Segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="e5c57-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1363">cód seguranca</span></span>
- <span data-ttu-id="e5c57-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="e5c57-1364">número de verificação</span></span>
- <span data-ttu-id="e5c57-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1365">numero de verificacao</span></span>
- <span data-ttu-id="e5c57-1366">Ablauf</span><span class="sxs-lookup"><span data-stu-id="e5c57-1366">ablauf</span></span>
- <span data-ttu-id="e5c57-1367">Gültig bis</span><span class="sxs-lookup"><span data-stu-id="e5c57-1367">gültig bis</span></span>
- <span data-ttu-id="e5c57-1368">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="e5c57-1369">Gultig bis</span><span class="sxs-lookup"><span data-stu-id="e5c57-1369">gultig bis</span></span>
- <span data-ttu-id="e5c57-1370">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="e5c57-1371">scadenza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1371">scadenza</span></span>
- <span data-ttu-id="e5c57-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="e5c57-1372">data scad</span></span>
- <span data-ttu-id="e5c57-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="e5c57-1373">fecha de expiracion</span></span>
- <span data-ttu-id="e5c57-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="e5c57-1374">fecha de venc</span></span>
- <span data-ttu-id="e5c57-1375">vencimiento</span><span class="sxs-lookup"><span data-stu-id="e5c57-1375">vencimiento</span></span>
- <span data-ttu-id="e5c57-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1376">válido hasta</span></span>
- <span data-ttu-id="e5c57-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1377">valido hasta</span></span>
- <span data-ttu-id="e5c57-1378">VTO</span><span class="sxs-lookup"><span data-stu-id="e5c57-1378">vto</span></span>
- <span data-ttu-id="e5c57-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="e5c57-1379">data de expiração</span></span>
- <span data-ttu-id="e5c57-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1380">data de expiracao</span></span>
- <span data-ttu-id="e5c57-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="e5c57-1381">data em que expira</span></span>
- <span data-ttu-id="e5c57-1382">validade</span><span class="sxs-lookup"><span data-stu-id="e5c57-1382">validade</span></span>
- <span data-ttu-id="e5c57-1383">Valor</span><span class="sxs-lookup"><span data-stu-id="e5c57-1383">valor</span></span>
- <span data-ttu-id="e5c57-1384">vencimento</span><span class="sxs-lookup"><span data-stu-id="e5c57-1384">vencimento</span></span>
- <span data-ttu-id="e5c57-1385">Venc</span><span class="sxs-lookup"><span data-stu-id="e5c57-1385">Venc</span></span> 

#### <a name="keyword_cc_name"></a><span data-ttu-id="e5c57-1386">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="e5c57-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="e5c57-1387">Amex</span><span class="sxs-lookup"><span data-stu-id="e5c57-1387">amex</span></span>
- <span data-ttu-id="e5c57-1388">american express</span><span class="sxs-lookup"><span data-stu-id="e5c57-1388">american express</span></span>
- <span data-ttu-id="e5c57-1389">AmericanExpress</span><span class="sxs-lookup"><span data-stu-id="e5c57-1389">americanexpress</span></span>
- <span data-ttu-id="e5c57-1390">Visa</span><span class="sxs-lookup"><span data-stu-id="e5c57-1390">Visa</span></span>
- <span data-ttu-id="e5c57-1391">MasterCard</span><span class="sxs-lookup"><span data-stu-id="e5c57-1391">mastercard</span></span>
- <span data-ttu-id="e5c57-1392">master card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1392">master card</span></span>
- <span data-ttu-id="e5c57-1393">Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="e5c57-1393">mc</span></span> 
- <span data-ttu-id="e5c57-1394">MasterCards gesichert</span><span class="sxs-lookup"><span data-stu-id="e5c57-1394">mastercards</span></span>
- <span data-ttu-id="e5c57-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1395">master cards</span></span>
- <span data-ttu-id="e5c57-1396">diner's Club</span><span class="sxs-lookup"><span data-stu-id="e5c57-1396">diner's Club</span></span>
- <span data-ttu-id="e5c57-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="e5c57-1397">diners club</span></span>
- <span data-ttu-id="e5c57-1398">DinersClub</span><span class="sxs-lookup"><span data-stu-id="e5c57-1398">dinersclub</span></span>
- <span data-ttu-id="e5c57-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1399">discover card</span></span>
- <span data-ttu-id="e5c57-1400">discovercard</span><span class="sxs-lookup"><span data-stu-id="e5c57-1400">discovercard</span></span>
- <span data-ttu-id="e5c57-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1401">discover cards</span></span>
- <span data-ttu-id="e5c57-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="e5c57-1402">JCB</span></span>
- <span data-ttu-id="e5c57-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="e5c57-1403">japanese card bureau</span></span>
- <span data-ttu-id="e5c57-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="e5c57-1404">carte blanche</span></span>
- <span data-ttu-id="e5c57-1405">CarteBlanche</span><span class="sxs-lookup"><span data-stu-id="e5c57-1405">carteblanche</span></span>
- <span data-ttu-id="e5c57-1406">credit card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1406">credit card</span></span>
- <span data-ttu-id="e5c57-1407">CC #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1407">cc#</span></span>
- <span data-ttu-id="e5c57-1408">cc #:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1408">cc#:</span></span>
- <span data-ttu-id="e5c57-1409">expiration date</span><span class="sxs-lookup"><span data-stu-id="e5c57-1409">expiration date</span></span>
- <span data-ttu-id="e5c57-1410">exp date</span><span class="sxs-lookup"><span data-stu-id="e5c57-1410">exp date</span></span>
- <span data-ttu-id="e5c57-1411">expiry date</span><span class="sxs-lookup"><span data-stu-id="e5c57-1411">expiry date</span></span>
- <span data-ttu-id="e5c57-1412">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="e5c57-1412">date d’expiration</span></span>
- <span data-ttu-id="e5c57-1413">date d'exp</span><span class="sxs-lookup"><span data-stu-id="e5c57-1413">date d'exp</span></span>
- <span data-ttu-id="e5c57-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="e5c57-1414">date expiration</span></span>
- <span data-ttu-id="e5c57-1415">bank card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1415">bank card</span></span>
- <span data-ttu-id="e5c57-1416">Bankcard</span><span class="sxs-lookup"><span data-stu-id="e5c57-1416">bankcard</span></span>
- <span data-ttu-id="e5c57-1417">card number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1417">card number</span></span>
- <span data-ttu-id="e5c57-1418">card num</span><span class="sxs-lookup"><span data-stu-id="e5c57-1418">card num</span></span>
- <span data-ttu-id="e5c57-1419">cardNumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-1419">cardnumber</span></span>
- <span data-ttu-id="e5c57-1420">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="e5c57-1420">cardnumbers</span></span>
- <span data-ttu-id="e5c57-1421">card numbers</span><span class="sxs-lookup"><span data-stu-id="e5c57-1421">card numbers</span></span>
- <span data-ttu-id="e5c57-1422">CreditCard</span><span class="sxs-lookup"><span data-stu-id="e5c57-1422">creditcard</span></span>
- <span data-ttu-id="e5c57-1423">credit cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1423">credit cards</span></span>
- <span data-ttu-id="e5c57-1424">creditCards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1424">creditcards</span></span>
- <span data-ttu-id="e5c57-1425">Angaben</span><span class="sxs-lookup"><span data-stu-id="e5c57-1425">ccn</span></span>
- <span data-ttu-id="e5c57-1426">card holder</span><span class="sxs-lookup"><span data-stu-id="e5c57-1426">card holder</span></span>
- <span data-ttu-id="e5c57-1427">Inhaber</span><span class="sxs-lookup"><span data-stu-id="e5c57-1427">cardholder</span></span>
- <span data-ttu-id="e5c57-1428">card holders</span><span class="sxs-lookup"><span data-stu-id="e5c57-1428">card holders</span></span>
- <span data-ttu-id="e5c57-1429">Inhaber</span><span class="sxs-lookup"><span data-stu-id="e5c57-1429">cardholders</span></span>
- <span data-ttu-id="e5c57-1430">check card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1430">check card</span></span>
- <span data-ttu-id="e5c57-1431">checkcard</span><span class="sxs-lookup"><span data-stu-id="e5c57-1431">checkcard</span></span>
- <span data-ttu-id="e5c57-1432">check cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1432">check cards</span></span>
- <span data-ttu-id="e5c57-1433">checkcards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1433">checkcards</span></span>
- <span data-ttu-id="e5c57-1434">debit card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1434">debit card</span></span>
- <span data-ttu-id="e5c57-1435">Debitkarte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1435">debitcard</span></span>
- <span data-ttu-id="e5c57-1436">debit cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1436">debit cards</span></span>
- <span data-ttu-id="e5c57-1437">debitcards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1437">debitcards</span></span>
- <span data-ttu-id="e5c57-1438">atm card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1438">atm card</span></span>
- <span data-ttu-id="e5c57-1439">atmcard</span><span class="sxs-lookup"><span data-stu-id="e5c57-1439">atmcard</span></span>
- <span data-ttu-id="e5c57-1440">atm cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1440">atm cards</span></span>
- <span data-ttu-id="e5c57-1441">atmcards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1441">atmcards</span></span>
- <span data-ttu-id="e5c57-1442">enroute</span><span class="sxs-lookup"><span data-stu-id="e5c57-1442">enroute</span></span>
- <span data-ttu-id="e5c57-1443">en route</span><span class="sxs-lookup"><span data-stu-id="e5c57-1443">en route</span></span>
- <span data-ttu-id="e5c57-1444">card type</span><span class="sxs-lookup"><span data-stu-id="e5c57-1444">card type</span></span>
- <span data-ttu-id="e5c57-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="e5c57-1445">carte bancaire</span></span>
- <span data-ttu-id="e5c57-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="e5c57-1446">carte de crédit</span></span>
- <span data-ttu-id="e5c57-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="e5c57-1447">carte de credit</span></span>
- <span data-ttu-id="e5c57-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1448">numéro de carte</span></span>
- <span data-ttu-id="e5c57-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1449">numero de carte</span></span>
- <span data-ttu-id="e5c57-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1450">nº de la carte</span></span>
- <span data-ttu-id="e5c57-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1451">nº de carte</span></span>
- <span data-ttu-id="e5c57-1452">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1452">kreditkarte</span></span>
- <span data-ttu-id="e5c57-1453">Karte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1453">karte</span></span>
- <span data-ttu-id="e5c57-1454">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="e5c57-1454">karteninhaber</span></span>
- <span data-ttu-id="e5c57-1455">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="e5c57-1455">karteninhabers</span></span>
- <span data-ttu-id="e5c57-1456">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="e5c57-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="e5c57-1457">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="e5c57-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="e5c57-1458">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="e5c57-1458">kreditkartentyp</span></span>
- <span data-ttu-id="e5c57-1459">eigentümername</span><span class="sxs-lookup"><span data-stu-id="e5c57-1459">eigentümername</span></span>
- <span data-ttu-id="e5c57-1460">kartennr</span><span class="sxs-lookup"><span data-stu-id="e5c57-1460">kartennr</span></span> 
- <span data-ttu-id="e5c57-1461">kartennummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1461">kartennummer</span></span>
- <span data-ttu-id="e5c57-1462">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1462">kreditkartennummer</span></span>
- <span data-ttu-id="e5c57-1463">Kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="e5c57-1464">carta di credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1464">carta di credito</span></span>
- <span data-ttu-id="e5c57-1465">carta credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1465">carta credito</span></span>
- <span data-ttu-id="e5c57-1466">Carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1466">carta</span></span>
- <span data-ttu-id="e5c57-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1467">n carta</span></span>
- <span data-ttu-id="e5c57-1468">Nr.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1468">nr.</span></span> <span data-ttu-id="e5c57-1469">Carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1469">carta</span></span>
- <span data-ttu-id="e5c57-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1470">nr carta</span></span>
- <span data-ttu-id="e5c57-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1471">numero carta</span></span>
- <span data-ttu-id="e5c57-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1472">numero della carta</span></span>
- <span data-ttu-id="e5c57-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1473">numero di carta</span></span>
- <span data-ttu-id="e5c57-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1474">tarjeta credito</span></span>
- <span data-ttu-id="e5c57-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1475">tarjeta de credito</span></span>
- <span data-ttu-id="e5c57-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1476">tarjeta crédito</span></span>
- <span data-ttu-id="e5c57-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="e5c57-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="e5c57-1478">tarjeta de atm</span></span>
- <span data-ttu-id="e5c57-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="e5c57-1479">tarjeta atm</span></span>
- <span data-ttu-id="e5c57-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1480">tarjeta debito</span></span>
- <span data-ttu-id="e5c57-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1481">tarjeta de debito</span></span>
- <span data-ttu-id="e5c57-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1482">tarjeta débito</span></span>
- <span data-ttu-id="e5c57-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1483">tarjeta de débito</span></span>
- <span data-ttu-id="e5c57-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1484">nº de tarjeta</span></span>
- <span data-ttu-id="e5c57-1485">Nein.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1485">no.</span></span> <span data-ttu-id="e5c57-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1486">de tarjeta</span></span>
- <span data-ttu-id="e5c57-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1487">no de tarjeta</span></span>
- <span data-ttu-id="e5c57-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1488">numero de tarjeta</span></span>
- <span data-ttu-id="e5c57-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1489">número de tarjeta</span></span>
- <span data-ttu-id="e5c57-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="e5c57-1490">tarjeta no</span></span>
- <span data-ttu-id="e5c57-1491">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="e5c57-1491">tarjetahabiente</span></span>
- <span data-ttu-id="e5c57-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1492">cartão de crédito</span></span>
- <span data-ttu-id="e5c57-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1493">cartão de credito</span></span>
- <span data-ttu-id="e5c57-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1494">cartao de crédito</span></span>
- <span data-ttu-id="e5c57-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1495">cartao de credito</span></span>
- <span data-ttu-id="e5c57-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1496">cartão de débito</span></span>
- <span data-ttu-id="e5c57-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1497">cartao de débito</span></span>
- <span data-ttu-id="e5c57-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1498">cartão de debito</span></span>
- <span data-ttu-id="e5c57-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1499">cartao de debito</span></span>
- <span data-ttu-id="e5c57-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="e5c57-1500">débito automático</span></span>
- <span data-ttu-id="e5c57-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="e5c57-1501">debito automatico</span></span>
- <span data-ttu-id="e5c57-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1502">número do cartão</span></span>
- <span data-ttu-id="e5c57-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1503">numero do cartão</span></span> 
- <span data-ttu-id="e5c57-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1504">número do cartao</span></span>
- <span data-ttu-id="e5c57-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1505">numero do cartao</span></span>
- <span data-ttu-id="e5c57-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1506">número de cartão</span></span>
- <span data-ttu-id="e5c57-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1507">numero de cartão</span></span>
- <span data-ttu-id="e5c57-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1508">número de cartao</span></span>
- <span data-ttu-id="e5c57-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1509">numero de cartao</span></span>
- <span data-ttu-id="e5c57-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1510">nº do cartão</span></span>
- <span data-ttu-id="e5c57-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1511">nº do cartao</span></span>
- <span data-ttu-id="e5c57-1512">nº.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1512">nº.</span></span> <span data-ttu-id="e5c57-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1513">do cartão</span></span>
- <span data-ttu-id="e5c57-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1514">no do cartão</span></span>
- <span data-ttu-id="e5c57-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1515">no do cartao</span></span>
- <span data-ttu-id="e5c57-1516">Nein.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1516">no.</span></span> <span data-ttu-id="e5c57-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1517">do cartão</span></span>
- <span data-ttu-id="e5c57-1518">Nein.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1518">no.</span></span> <span data-ttu-id="e5c57-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="e5c57-1520">	Kroatien – Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1521">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1521">Format</span></span>

<span data-ttu-id="e5c57-1522">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1523">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1523">Pattern</span></span>

<span data-ttu-id="e5c57-1524">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1525">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1525">Checksum</span></span>

<span data-ttu-id="e5c57-1526">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1527">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1527">Definition</span></span>

<span data-ttu-id="e5c57-1528">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1529">Die Funktion Func_croatia_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1530">Ein Schlüsselwort aus Keyword_croatia_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-1531">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1531">Keywords</span></span>

#### <a name="keyword_croatia_id_card"></a><span data-ttu-id="e5c57-1532">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="e5c57-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1533">Croatian identity card</span></span>
- <span data-ttu-id="e5c57-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="e5c57-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="e5c57-1535">	Croatia Personal Identification (OIB) Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1536">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1536">Format</span></span>

<span data-ttu-id="e5c57-1537">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1538">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1538">Pattern</span></span>

<span data-ttu-id="e5c57-1539">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1539">11 digits:</span></span>
- <span data-ttu-id="e5c57-1540">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1540">10 digits</span></span> 
- <span data-ttu-id="e5c57-1541">Letzte Ziffer ist eine Prüfziffer für den Zweck des internationalen Datenaustauschs, die Buchstaben HR werden vor den elf Ziffern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1542">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1542">Checksum</span></span>

<span data-ttu-id="e5c57-1543">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1544">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1544">Definition</span></span>

<span data-ttu-id="e5c57-1545">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1546">Die Funktion Func_croatia_oib_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1547">Ein Schlüsselwort aus Keyword_croatia_oib_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="e5c57-1548">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1548">The checksum passes.</span></span>

<span data-ttu-id="e5c57-1549">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1550">Die Funktion Func_croatia_oib_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1551">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1551">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-1552">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1552">Keywords</span></span>

#### <a name="keyword_croatia_oib_number"></a><span data-ttu-id="e5c57-1553">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="e5c57-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1554">Personal Identification Number</span></span>
- <span data-ttu-id="e5c57-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="e5c57-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="e5c57-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="e5c57-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="e5c57-1557">Tschechische Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1558">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1558">Format</span></span>

<span data-ttu-id="e5c57-1559">Neun Ziffern mit optionalem Schrägstrich (altes Format) 10 Ziffern mit optionalem Schrägstrich (neues Format)</span><span class="sxs-lookup"><span data-stu-id="e5c57-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1560">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1560">Pattern</span></span>

<span data-ttu-id="e5c57-1561">Neun Ziffern (altes Format):</span><span class="sxs-lookup"><span data-stu-id="e5c57-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="e5c57-1562">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1562">Nine digits</span></span>

<span data-ttu-id="e5c57-1563">ODER</span><span class="sxs-lookup"><span data-stu-id="e5c57-1563">OR</span></span>

- <span data-ttu-id="e5c57-1564">Sechs Ziffern, die das Geburtsdatum darstellen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="e5c57-1565">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-1565">A forward slash</span></span>
- <span data-ttu-id="e5c57-1566">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1566">Three digits</span></span>

<span data-ttu-id="e5c57-1567">10 Ziffern (neues Format):</span><span class="sxs-lookup"><span data-stu-id="e5c57-1567">10 digits (new format):</span></span>
- <span data-ttu-id="e5c57-1568">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1568">10 digits</span></span>

<span data-ttu-id="e5c57-1569">ODER</span><span class="sxs-lookup"><span data-stu-id="e5c57-1569">OR</span></span>

- <span data-ttu-id="e5c57-1570">Sechs Ziffern, die das Geburtsdatum darstellen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="e5c57-1571">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-1571">A forward slash</span></span> 
- <span data-ttu-id="e5c57-1572">Vier Ziffern, wobei die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="e5c57-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1573">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1573">Checksum</span></span>

<span data-ttu-id="e5c57-1574">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1575">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1575">Definition</span></span>

<span data-ttu-id="e5c57-1576">Eine DLP-Richtlinie ist 85% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: die Funktion Func_czech_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="e5c57-1577">Ein Schlüsselwort aus Keyword_czech_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="e5c57-1578">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1578">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="e5c57-1579">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1579">Keywords</span></span>

- <span data-ttu-id="e5c57-1580">Tschechische Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1580">czech personal identity number</span></span>
- <span data-ttu-id="e5c57-1581">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="e5c57-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="e5c57-1582">	Dänemark – Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1583">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1583">Format</span></span>

<span data-ttu-id="e5c57-1584">10 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="e5c57-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1585">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1585">Pattern</span></span>

<span data-ttu-id="e5c57-1586">10 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1586">10 digits:</span></span>
- <span data-ttu-id="e5c57-1587">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="e5c57-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="e5c57-1588">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-1588">A hyphen</span></span> 
- <span data-ttu-id="e5c57-1589">Vier Ziffern, bei denen die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="e5c57-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1590">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1590">Checksum</span></span>

<span data-ttu-id="e5c57-1591">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1592">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1592">Definition</span></span>

<span data-ttu-id="e5c57-1593">Eine DLP-Richtlinie ist 75% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: der reguläre Ausdruck Regex_denmark_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="e5c57-1594">Ein Schlüsselwort aus Keyword_denmark_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="e5c57-1595">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1595">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-1596">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1596">Keywords</span></span>

#### <a name="keyword_denmark_id"></a><span data-ttu-id="e5c57-1597">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="e5c57-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="e5c57-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1598">Personal Identification Number</span></span>
- <span data-ttu-id="e5c57-1599">CPR</span><span class="sxs-lookup"><span data-stu-id="e5c57-1599">CPR</span></span>
- <span data-ttu-id="e5c57-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="e5c57-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="e5c57-1601">Personnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="e5c57-1602">Drug Enforcement Agency (DEA)-Nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1603">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1603">Format</span></span>

<span data-ttu-id="e5c57-1604">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1605">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1605">Pattern</span></span>

<span data-ttu-id="e5c57-1606">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="e5c57-1607">Einen Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) aus der folgenden Gruppe möglicher Buchstaben: abcdefghjklmnprstux, was einem Registrantencode entspricht</span><span class="sxs-lookup"><span data-stu-id="e5c57-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="e5c57-1608">Ein Buchstabe (bei dem die Groß-und Kleinschreibung nicht beachtet wird), der dem ersten Buchstaben des Nachnamens des Registrants entspricht</span><span class="sxs-lookup"><span data-stu-id="e5c57-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="e5c57-1609">Sieben Ziffern, von denen die letzte die Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="e5c57-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1610">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1610">Checksum</span></span>

<span data-ttu-id="e5c57-1611">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1612">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1612">Definition</span></span>

<span data-ttu-id="e5c57-1613">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1614">Die Funktion Func_dea_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1615">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1615">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-1616">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1616">Keywords</span></span>

<span data-ttu-id="e5c57-1617">Keine</span><span class="sxs-lookup"><span data-stu-id="e5c57-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="e5c57-1618">EU Debit Card-Nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1619">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1619">Format</span></span>

<span data-ttu-id="e5c57-1620">16 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1621">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1621">Pattern</span></span>

<span data-ttu-id="e5c57-1622">Sehr komplexes und robustes Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1623">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1623">Checksum</span></span>

<span data-ttu-id="e5c57-1624">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1625">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1625">Definition</span></span>

<span data-ttu-id="e5c57-1626">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1627">Die Funktion Func_eu_debit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1628">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="e5c57-1629">Ein Schlüsselwort aus Keyword_eu_debit_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="e5c57-1630">Ein Schlüsselwort aus Keyword_card_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="e5c57-1631">Ein Schlüsselwort aus Keyword_card_security_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="e5c57-1632">Ein Schlüsselwort aus Keyword_card_expiration_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="e5c57-1633">Die Funktion Func_expiration_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="e5c57-1634">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1634">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-1635">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1635">Keywords</span></span>

#### <a name="keyword_eu_debit_card"></a><span data-ttu-id="e5c57-1636">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="e5c57-1637">account number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1637">account number</span></span> 
- <span data-ttu-id="e5c57-1638">card number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1638">card number</span></span> 
- <span data-ttu-id="e5c57-1639">card no.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1639">card no.</span></span> 
- <span data-ttu-id="e5c57-1640">security number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1640">security number</span></span> 
- <span data-ttu-id="e5c57-1641">CC #</span><span class="sxs-lookup"><span data-stu-id="e5c57-1641">cc#</span></span> 

#### <a name="keyword_card_terms_dict"></a><span data-ttu-id="e5c57-1642">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="e5c57-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="e5c57-1643">acct nbr</span><span class="sxs-lookup"><span data-stu-id="e5c57-1643">acct nbr</span></span> 
- <span data-ttu-id="e5c57-1644">acct num</span><span class="sxs-lookup"><span data-stu-id="e5c57-1644">acct num</span></span> 
- <span data-ttu-id="e5c57-1645">acct no</span><span class="sxs-lookup"><span data-stu-id="e5c57-1645">acct no</span></span> 
- <span data-ttu-id="e5c57-1646">american express</span><span class="sxs-lookup"><span data-stu-id="e5c57-1646">american express</span></span> 
- <span data-ttu-id="e5c57-1647">AmericanExpress</span><span class="sxs-lookup"><span data-stu-id="e5c57-1647">americanexpress</span></span> 
- <span data-ttu-id="e5c57-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="e5c57-1648">americano espresso</span></span> 
- <span data-ttu-id="e5c57-1649">Amex</span><span class="sxs-lookup"><span data-stu-id="e5c57-1649">amex</span></span> 
- <span data-ttu-id="e5c57-1650">atm card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1650">atm card</span></span> 
- <span data-ttu-id="e5c57-1651">atm cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1651">atm cards</span></span> 
- <span data-ttu-id="e5c57-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="e5c57-1652">atm kaart</span></span> 
- <span data-ttu-id="e5c57-1653">atmcard</span><span class="sxs-lookup"><span data-stu-id="e5c57-1653">atmcard</span></span> 
- <span data-ttu-id="e5c57-1654">atmcards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1654">atmcards</span></span> 
- <span data-ttu-id="e5c57-1655">atmkaart</span><span class="sxs-lookup"><span data-stu-id="e5c57-1655">atmkaart</span></span> 
- <span data-ttu-id="e5c57-1656">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="e5c57-1656">atmkaarten</span></span> 
- <span data-ttu-id="e5c57-1657">Bancontact</span><span class="sxs-lookup"><span data-stu-id="e5c57-1657">bancontact</span></span> 
- <span data-ttu-id="e5c57-1658">bank card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1658">bank card</span></span> 
- <span data-ttu-id="e5c57-1659">bankkaart</span><span class="sxs-lookup"><span data-stu-id="e5c57-1659">bankkaart</span></span> 
- <span data-ttu-id="e5c57-1660">card holder</span><span class="sxs-lookup"><span data-stu-id="e5c57-1660">card holder</span></span> 
- <span data-ttu-id="e5c57-1661">card holders</span><span class="sxs-lookup"><span data-stu-id="e5c57-1661">card holders</span></span> 
- <span data-ttu-id="e5c57-1662">card num</span><span class="sxs-lookup"><span data-stu-id="e5c57-1662">card num</span></span> 
- <span data-ttu-id="e5c57-1663">card number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1663">card number</span></span> 
- <span data-ttu-id="e5c57-1664">card numbers</span><span class="sxs-lookup"><span data-stu-id="e5c57-1664">card numbers</span></span> 
- <span data-ttu-id="e5c57-1665">card type</span><span class="sxs-lookup"><span data-stu-id="e5c57-1665">card type</span></span> 
- <span data-ttu-id="e5c57-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="e5c57-1666">cardano numerico</span></span> 
- <span data-ttu-id="e5c57-1667">Inhaber</span><span class="sxs-lookup"><span data-stu-id="e5c57-1667">cardholder</span></span> 
- <span data-ttu-id="e5c57-1668">Inhaber</span><span class="sxs-lookup"><span data-stu-id="e5c57-1668">cardholders</span></span> 
- <span data-ttu-id="e5c57-1669">cardNumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-1669">cardnumber</span></span> 
- <span data-ttu-id="e5c57-1670">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="e5c57-1670">cardnumbers</span></span> 
- <span data-ttu-id="e5c57-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1671">carta bianca</span></span> 
- <span data-ttu-id="e5c57-1672">carta credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1672">carta credito</span></span> 
- <span data-ttu-id="e5c57-1673">carta di credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1673">carta di credito</span></span> 
- <span data-ttu-id="e5c57-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1674">cartao de credito</span></span> 
- <span data-ttu-id="e5c57-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1675">cartao de crédito</span></span> 
- <span data-ttu-id="e5c57-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1676">cartao de debito</span></span> 
- <span data-ttu-id="e5c57-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1677">cartao de débito</span></span> 
- <span data-ttu-id="e5c57-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="e5c57-1678">carte bancaire</span></span> 
- <span data-ttu-id="e5c57-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="e5c57-1679">carte blanche</span></span> 
- <span data-ttu-id="e5c57-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="e5c57-1680">carte bleue</span></span> 
- <span data-ttu-id="e5c57-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="e5c57-1681">carte de credit</span></span> 
- <span data-ttu-id="e5c57-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="e5c57-1682">carte de crédit</span></span> 
- <span data-ttu-id="e5c57-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1683">carte di credito</span></span> 
- <span data-ttu-id="e5c57-1684">CarteBlanche</span><span class="sxs-lookup"><span data-stu-id="e5c57-1684">carteblanche</span></span> 
- <span data-ttu-id="e5c57-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1685">cartão de credito</span></span> 
- <span data-ttu-id="e5c57-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1686">cartão de crédito</span></span> 
- <span data-ttu-id="e5c57-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1687">cartão de debito</span></span> 
- <span data-ttu-id="e5c57-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1688">cartão de débito</span></span> 
- <span data-ttu-id="e5c57-1689">cb</span><span class="sxs-lookup"><span data-stu-id="e5c57-1689">cb</span></span> 
- <span data-ttu-id="e5c57-1690">Angaben</span><span class="sxs-lookup"><span data-stu-id="e5c57-1690">ccn</span></span> 
- <span data-ttu-id="e5c57-1691">check card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1691">check card</span></span> 
- <span data-ttu-id="e5c57-1692">check cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1692">check cards</span></span> 
- <span data-ttu-id="e5c57-1693">checkcard</span><span class="sxs-lookup"><span data-stu-id="e5c57-1693">checkcard</span></span>
- <span data-ttu-id="e5c57-1694">checkcards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1694">checkcards</span></span> 
- <span data-ttu-id="e5c57-1695">chequekaart</span><span class="sxs-lookup"><span data-stu-id="e5c57-1695">chequekaart</span></span> 
- <span data-ttu-id="e5c57-1696">Cirrus</span><span class="sxs-lookup"><span data-stu-id="e5c57-1696">cirrus</span></span> 
- <span data-ttu-id="e5c57-1697">Cirrus-EDC-Maestro</span><span class="sxs-lookup"><span data-stu-id="e5c57-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="e5c57-1698">controlekaart</span><span class="sxs-lookup"><span data-stu-id="e5c57-1698">controlekaart</span></span> 
- <span data-ttu-id="e5c57-1699">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="e5c57-1699">controlekaarten</span></span> 
- <span data-ttu-id="e5c57-1700">credit card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1700">credit card</span></span> 
- <span data-ttu-id="e5c57-1701">credit cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1701">credit cards</span></span> 
- <span data-ttu-id="e5c57-1702">CreditCard</span><span class="sxs-lookup"><span data-stu-id="e5c57-1702">creditcard</span></span> 
- <span data-ttu-id="e5c57-1703">creditCards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1703">creditcards</span></span> 
- <span data-ttu-id="e5c57-1704">debetkaart</span><span class="sxs-lookup"><span data-stu-id="e5c57-1704">debetkaart</span></span> 
- <span data-ttu-id="e5c57-1705">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="e5c57-1705">debetkaarten</span></span> 
- <span data-ttu-id="e5c57-1706">debit card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1706">debit card</span></span> 
- <span data-ttu-id="e5c57-1707">debit cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1707">debit cards</span></span> 
- <span data-ttu-id="e5c57-1708">Debitkarte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1708">debitcard</span></span> 
- <span data-ttu-id="e5c57-1709">debitcards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1709">debitcards</span></span> 
- <span data-ttu-id="e5c57-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="e5c57-1710">debito automatico</span></span> 
- <span data-ttu-id="e5c57-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="e5c57-1711">diners club</span></span> 
- <span data-ttu-id="e5c57-1712">DinersClub</span><span class="sxs-lookup"><span data-stu-id="e5c57-1712">dinersclub</span></span> 
- <span data-ttu-id="e5c57-1713">ermitteln</span><span class="sxs-lookup"><span data-stu-id="e5c57-1713">discover</span></span> 
- <span data-ttu-id="e5c57-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1714">discover card</span></span> 
- <span data-ttu-id="e5c57-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1715">discover cards</span></span> 
- <span data-ttu-id="e5c57-1716">discovercard</span><span class="sxs-lookup"><span data-stu-id="e5c57-1716">discovercard</span></span> 
- <span data-ttu-id="e5c57-1717">discovercards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1717">discovercards</span></span> 
- <span data-ttu-id="e5c57-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="e5c57-1718">débito automático</span></span>
- <span data-ttu-id="e5c57-1719">EDC</span><span class="sxs-lookup"><span data-stu-id="e5c57-1719">edc</span></span> 
- <span data-ttu-id="e5c57-1720">eigentümername</span><span class="sxs-lookup"><span data-stu-id="e5c57-1720">eigentümername</span></span> 
- <span data-ttu-id="e5c57-1721">european debit card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1721">european debit card</span></span> 
- <span data-ttu-id="e5c57-1722">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="e5c57-1722">hoofdkaart</span></span> 
- <span data-ttu-id="e5c57-1723">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="e5c57-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="e5c57-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="e5c57-1724">in viaggio</span></span> 
- <span data-ttu-id="e5c57-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="e5c57-1725">japanese card bureau</span></span> 
- <span data-ttu-id="e5c57-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="e5c57-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="e5c57-1727">JCB</span><span class="sxs-lookup"><span data-stu-id="e5c57-1727">jcb</span></span> 
- <span data-ttu-id="e5c57-1728">Kaart</span><span class="sxs-lookup"><span data-stu-id="e5c57-1728">kaart</span></span> 
- <span data-ttu-id="e5c57-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="e5c57-1729">kaart num</span></span> 
- <span data-ttu-id="e5c57-1730">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="e5c57-1730">kaartaantal</span></span> 
- <span data-ttu-id="e5c57-1731">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="e5c57-1731">kaartaantallen</span></span> 
- <span data-ttu-id="e5c57-1732">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="e5c57-1732">kaarthouder</span></span> 
- <span data-ttu-id="e5c57-1733">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="e5c57-1733">kaarthouders</span></span> 
- <span data-ttu-id="e5c57-1734">Karte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1734">karte</span></span>  
- <span data-ttu-id="e5c57-1735">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="e5c57-1735">karteninhaber</span></span> 
- <span data-ttu-id="e5c57-1736">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="e5c57-1736">karteninhabers</span></span>
- <span data-ttu-id="e5c57-1737">kartennr</span><span class="sxs-lookup"><span data-stu-id="e5c57-1737">kartennr</span></span> 
- <span data-ttu-id="e5c57-1738">kartennummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1738">kartennummer</span></span> 
- <span data-ttu-id="e5c57-1739">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1739">kreditkarte</span></span> 
- <span data-ttu-id="e5c57-1740">Kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="e5c57-1741">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="e5c57-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="e5c57-1742">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="e5c57-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="e5c57-1743">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="e5c57-1744">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="e5c57-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="e5c57-1745">Maestro</span><span class="sxs-lookup"><span data-stu-id="e5c57-1745">maestro</span></span> 
- <span data-ttu-id="e5c57-1746">master card</span><span class="sxs-lookup"><span data-stu-id="e5c57-1746">master card</span></span> 
- <span data-ttu-id="e5c57-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-1747">master cards</span></span> 
- <span data-ttu-id="e5c57-1748">MasterCard</span><span class="sxs-lookup"><span data-stu-id="e5c57-1748">mastercard</span></span> 
- <span data-ttu-id="e5c57-1749">MasterCards gesichert</span><span class="sxs-lookup"><span data-stu-id="e5c57-1749">mastercards</span></span> 
- <span data-ttu-id="e5c57-1750">Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="e5c57-1750">mc</span></span> 
- <span data-ttu-id="e5c57-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="e5c57-1751">mister cash</span></span> 
- <span data-ttu-id="e5c57-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1752">n carta</span></span> 
- <span data-ttu-id="e5c57-1753">Carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1753">carta</span></span> 
- <span data-ttu-id="e5c57-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1754">no de tarjeta</span></span> 
- <span data-ttu-id="e5c57-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1755">no do cartao</span></span> 
- <span data-ttu-id="e5c57-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1756">no do cartão</span></span> 
- <span data-ttu-id="e5c57-1757">Nein.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1757">no.</span></span> <span data-ttu-id="e5c57-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1758">de tarjeta</span></span> 
- <span data-ttu-id="e5c57-1759">Nein.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1759">no.</span></span> <span data-ttu-id="e5c57-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1760">do cartao</span></span> 
- <span data-ttu-id="e5c57-1761">Nein.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1761">no.</span></span> <span data-ttu-id="e5c57-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1762">do cartão</span></span> 
- <span data-ttu-id="e5c57-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1763">nr carta</span></span> 
- <span data-ttu-id="e5c57-1764">Nr.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1764">nr.</span></span> <span data-ttu-id="e5c57-1765">Carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1765">carta</span></span> 
- <span data-ttu-id="e5c57-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="e5c57-1766">numeri di scheda</span></span> 
- <span data-ttu-id="e5c57-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1767">numero carta</span></span> 
- <span data-ttu-id="e5c57-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1768">numero de cartao</span></span> 
- <span data-ttu-id="e5c57-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1769">numero de carte</span></span> 
- <span data-ttu-id="e5c57-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1770">numero de cartão</span></span> 
- <span data-ttu-id="e5c57-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1771">numero de tarjeta</span></span>
- <span data-ttu-id="e5c57-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1772">numero della carta</span></span> 
- <span data-ttu-id="e5c57-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1773">numero di carta</span></span> 
- <span data-ttu-id="e5c57-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="e5c57-1774">numero di scheda</span></span> 
- <span data-ttu-id="e5c57-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1775">numero do cartao</span></span> 
- <span data-ttu-id="e5c57-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1776">numero do cartão</span></span> 
- <span data-ttu-id="e5c57-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1777">numéro de carte</span></span> 
- <span data-ttu-id="e5c57-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1778">nº carta</span></span> 
- <span data-ttu-id="e5c57-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1779">nº de carte</span></span> 
- <span data-ttu-id="e5c57-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="e5c57-1780">nº de la carte</span></span> 
- <span data-ttu-id="e5c57-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="e5c57-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1782">nº do cartao</span></span> 
- <span data-ttu-id="e5c57-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1783">nº do cartão</span></span> 
- <span data-ttu-id="e5c57-1784">nº.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1784">nº.</span></span> <span data-ttu-id="e5c57-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1785">do cartão</span></span> 
- <span data-ttu-id="e5c57-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1786">número de cartao</span></span> 
- <span data-ttu-id="e5c57-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="e5c57-1787">número de cartão</span></span> 
- <span data-ttu-id="e5c57-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1788">número de tarjeta</span></span> 
- <span data-ttu-id="e5c57-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1789">número do cartao</span></span> 
- <span data-ttu-id="e5c57-1790">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="e5c57-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="e5c57-1791">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="e5c57-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="e5c57-1792">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="e5c57-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="e5c57-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1793">scheda della banca</span></span> 
- <span data-ttu-id="e5c57-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="e5c57-1794">scheda di controllo</span></span> 
- <span data-ttu-id="e5c57-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1795">scheda di debito</span></span> 
- <span data-ttu-id="e5c57-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="e5c57-1796">scheda matrice</span></span> 
- <span data-ttu-id="e5c57-1797">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="e5c57-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="e5c57-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="e5c57-1798">schede di controllo</span></span> 
- <span data-ttu-id="e5c57-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1799">schede di debito</span></span> 
- <span data-ttu-id="e5c57-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="e5c57-1800">schede matrici</span></span> 
- <span data-ttu-id="e5c57-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="e5c57-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="e5c57-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="e5c57-1802">scoprono le schede</span></span> 
- <span data-ttu-id="e5c57-1803">Solo</span><span class="sxs-lookup"><span data-stu-id="e5c57-1803">solo</span></span> 
- <span data-ttu-id="e5c57-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="e5c57-1804">supporti di scheda</span></span> 
- <span data-ttu-id="e5c57-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="e5c57-1805">supporto di scheda</span></span> 
- <span data-ttu-id="e5c57-1806">Schalter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1806">switch</span></span> 
- <span data-ttu-id="e5c57-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="e5c57-1807">tarjeta atm</span></span> 
- <span data-ttu-id="e5c57-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1808">tarjeta credito</span></span> 
- <span data-ttu-id="e5c57-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="e5c57-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="e5c57-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="e5c57-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="e5c57-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="e5c57-1812">tarjeta debito</span></span> 
- <span data-ttu-id="e5c57-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="e5c57-1813">tarjeta no</span></span>
- <span data-ttu-id="e5c57-1814">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="e5c57-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="e5c57-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="e5c57-1815">tipo della scheda</span></span> 
- <span data-ttu-id="e5c57-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="e5c57-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="e5c57-1817">Scheda</span><span class="sxs-lookup"><span data-stu-id="e5c57-1817">scheda</span></span> 
- <span data-ttu-id="e5c57-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="e5c57-1818">v pay</span></span> 
- <span data-ttu-id="e5c57-1819">v-Pay</span><span class="sxs-lookup"><span data-stu-id="e5c57-1819">v-pay</span></span> 
- <span data-ttu-id="e5c57-1820">Visa</span><span class="sxs-lookup"><span data-stu-id="e5c57-1820">visa</span></span> 
- <span data-ttu-id="e5c57-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="e5c57-1821">visa plus</span></span> 
- <span data-ttu-id="e5c57-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="e5c57-1822">visa electron</span></span> 
- <span data-ttu-id="e5c57-1823">Visto</span><span class="sxs-lookup"><span data-stu-id="e5c57-1823">visto</span></span> 
- <span data-ttu-id="e5c57-1824">Visum</span><span class="sxs-lookup"><span data-stu-id="e5c57-1824">visum</span></span> 
- <span data-ttu-id="e5c57-1825">vpay</span><span class="sxs-lookup"><span data-stu-id="e5c57-1825">vpay</span></span>   

#### <a name="keyword_card_security_terms_dict"></a><span data-ttu-id="e5c57-1826">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="e5c57-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="e5c57-1827">card identification number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1827">card identification number</span></span>
- <span data-ttu-id="e5c57-1828">card verification</span><span class="sxs-lookup"><span data-stu-id="e5c57-1828">card verification</span></span> 
- <span data-ttu-id="e5c57-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="e5c57-1829">cardi la verifica</span></span> 
- <span data-ttu-id="e5c57-1830">cid</span><span class="sxs-lookup"><span data-stu-id="e5c57-1830">cid</span></span> 
- <span data-ttu-id="e5c57-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="e5c57-1831">cod seg</span></span> 
- <span data-ttu-id="e5c57-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1832">cod seguranca</span></span> 
- <span data-ttu-id="e5c57-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1833">cod segurança</span></span> 
- <span data-ttu-id="e5c57-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1834">cod sicurezza</span></span> 
- <span data-ttu-id="e5c57-1835">COD.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1835">cod.</span></span> <span data-ttu-id="e5c57-1836">SEG</span><span class="sxs-lookup"><span data-stu-id="e5c57-1836">seg</span></span> 
- <span data-ttu-id="e5c57-1837">COD.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1837">cod.</span></span> <span data-ttu-id="e5c57-1838">seguranca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1838">seguranca</span></span> 
- <span data-ttu-id="e5c57-1839">COD.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1839">cod.</span></span> <span data-ttu-id="e5c57-1840">Segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1840">segurança</span></span> 
- <span data-ttu-id="e5c57-1841">COD.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1841">cod.</span></span> <span data-ttu-id="e5c57-1842">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1842">sicurezza</span></span> 
- <span data-ttu-id="e5c57-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="e5c57-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="e5c57-1844">codice di verifica</span></span> 
- <span data-ttu-id="e5c57-1845">codigo</span><span class="sxs-lookup"><span data-stu-id="e5c57-1845">codigo</span></span> 
- <span data-ttu-id="e5c57-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="e5c57-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1847">codigo de segurança</span></span> 
- <span data-ttu-id="e5c57-1848">crittogramma</span><span class="sxs-lookup"><span data-stu-id="e5c57-1848">crittogramma</span></span> 
- <span data-ttu-id="e5c57-1849">Kryptogramm</span><span class="sxs-lookup"><span data-stu-id="e5c57-1849">cryptogram</span></span> 
- <span data-ttu-id="e5c57-1850">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1850">cryptogramme</span></span> 
- <span data-ttu-id="e5c57-1851">CV2</span><span class="sxs-lookup"><span data-stu-id="e5c57-1851">cv2</span></span> 
- <span data-ttu-id="e5c57-1852">CVC</span><span class="sxs-lookup"><span data-stu-id="e5c57-1852">cvc</span></span> 
- <span data-ttu-id="e5c57-1853">CVC2</span><span class="sxs-lookup"><span data-stu-id="e5c57-1853">cvc2</span></span> 
- <span data-ttu-id="e5c57-1854">CVN</span><span class="sxs-lookup"><span data-stu-id="e5c57-1854">cvn</span></span> 
- <span data-ttu-id="e5c57-1855">CVV</span><span class="sxs-lookup"><span data-stu-id="e5c57-1855">cvv</span></span> 
- <span data-ttu-id="e5c57-1856">CVV2</span><span class="sxs-lookup"><span data-stu-id="e5c57-1856">cvv2</span></span> 
- <span data-ttu-id="e5c57-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1857">cód seguranca</span></span> 
- <span data-ttu-id="e5c57-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1858">cód segurança</span></span> 
- <span data-ttu-id="e5c57-1859">cód.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1859">cód.</span></span> <span data-ttu-id="e5c57-1860">seguranca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1860">seguranca</span></span> 
- <span data-ttu-id="e5c57-1861">cód.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1861">cód.</span></span> <span data-ttu-id="e5c57-1862">Segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1862">segurança</span></span> 
- <span data-ttu-id="e5c57-1863">Código</span><span class="sxs-lookup"><span data-stu-id="e5c57-1863">código</span></span> 
- <span data-ttu-id="e5c57-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="e5c57-1864">código de seguranca</span></span> 
- <span data-ttu-id="e5c57-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="e5c57-1865">código de segurança</span></span> 
- <span data-ttu-id="e5c57-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="e5c57-1866">de kaart controle</span></span> 
- <span data-ttu-id="e5c57-1867">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="e5c57-1867">geeft nr uit</span></span> 
- <span data-ttu-id="e5c57-1868">issue no</span><span class="sxs-lookup"><span data-stu-id="e5c57-1868">issue no</span></span> 
- <span data-ttu-id="e5c57-1869">issue number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1869">issue number</span></span> 
- <span data-ttu-id="e5c57-1870">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="e5c57-1871">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="e5c57-1872">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="e5c57-1873">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="e5c57-1873">kwestieaantal</span></span> 
- <span data-ttu-id="e5c57-1874">Nein.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1874">no.</span></span> <span data-ttu-id="e5c57-1875">Dell ' edizione</span><span class="sxs-lookup"><span data-stu-id="e5c57-1875">dell'edizione</span></span> 
- <span data-ttu-id="e5c57-1876">Nein.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1876">no.</span></span> <span data-ttu-id="e5c57-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1877">di sicurezza</span></span> 
- <span data-ttu-id="e5c57-1878">numero de securite</span><span class="sxs-lookup"><span data-stu-id="e5c57-1878">numero de securite</span></span> 
- <span data-ttu-id="e5c57-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1879">numero de verificacao</span></span> 
- <span data-ttu-id="e5c57-1880">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="e5c57-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="e5c57-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="e5c57-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="e5c57-1882">Scheda</span><span class="sxs-lookup"><span data-stu-id="e5c57-1882">scheda</span></span> 
- <span data-ttu-id="e5c57-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="e5c57-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="e5c57-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="e5c57-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="e5c57-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="e5c57-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="e5c57-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="e5c57-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="e5c57-1887">número de verificação</span></span> 
- <span data-ttu-id="e5c57-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="e5c57-1888">perno il blocco</span></span> 
- <span data-ttu-id="e5c57-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="e5c57-1889">pin block</span></span> 
- <span data-ttu-id="e5c57-1890">prufziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1890">prufziffer</span></span> 
- <span data-ttu-id="e5c57-1891">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1891">prüfziffer</span></span> 
- <span data-ttu-id="e5c57-1892">security code</span><span class="sxs-lookup"><span data-stu-id="e5c57-1892">security code</span></span> 
- <span data-ttu-id="e5c57-1893">security no</span><span class="sxs-lookup"><span data-stu-id="e5c57-1893">security no</span></span> 
- <span data-ttu-id="e5c57-1894">security number</span><span class="sxs-lookup"><span data-stu-id="e5c57-1894">security number</span></span> 
- <span data-ttu-id="e5c57-1895">Sicherheitskode</span><span class="sxs-lookup"><span data-stu-id="e5c57-1895">sicherheits kode</span></span> 
- <span data-ttu-id="e5c57-1896">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="e5c57-1896">sicherheitscode</span></span> 
- <span data-ttu-id="e5c57-1897">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="e5c57-1898">speldblok</span><span class="sxs-lookup"><span data-stu-id="e5c57-1898">speldblok</span></span> 
- <span data-ttu-id="e5c57-1899">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-1899">veiligheid nr</span></span> 
- <span data-ttu-id="e5c57-1900">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="e5c57-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="e5c57-1901">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="e5c57-1901">veiligheidscode</span></span> 
- <span data-ttu-id="e5c57-1902">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="e5c57-1903">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-1903">verfalldatum</span></span> 

#### <a name="keyword_card_expiration_terms_dict"></a><span data-ttu-id="e5c57-1904">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="e5c57-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="e5c57-1905">Ablauf</span><span class="sxs-lookup"><span data-stu-id="e5c57-1905">ablauf</span></span> 
- <span data-ttu-id="e5c57-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="e5c57-1906">data de expiracao</span></span> 
- <span data-ttu-id="e5c57-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="e5c57-1907">data de expiração</span></span> 
- <span data-ttu-id="e5c57-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="e5c57-1908">data del exp</span></span> 
- <span data-ttu-id="e5c57-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="e5c57-1909">data di exp</span></span> 
- <span data-ttu-id="e5c57-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1910">data di scadenza</span></span> 
- <span data-ttu-id="e5c57-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="e5c57-1911">data em que expira</span></span> 
- <span data-ttu-id="e5c57-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="e5c57-1912">data scad</span></span> 
- <span data-ttu-id="e5c57-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1913">data scadenza</span></span> 
- <span data-ttu-id="e5c57-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="e5c57-1914">date de validité</span></span> 
- <span data-ttu-id="e5c57-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="e5c57-1915">datum afloop</span></span> 
- <span data-ttu-id="e5c57-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="e5c57-1916">datum van exp</span></span> 
- <span data-ttu-id="e5c57-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="e5c57-1917">de afloop</span></span> 
- <span data-ttu-id="e5c57-1918">Espira</span><span class="sxs-lookup"><span data-stu-id="e5c57-1918">espira</span></span> 
- <span data-ttu-id="e5c57-1919">Espira</span><span class="sxs-lookup"><span data-stu-id="e5c57-1919">espira</span></span> 
- <span data-ttu-id="e5c57-1920">exp date</span><span class="sxs-lookup"><span data-stu-id="e5c57-1920">exp date</span></span> 
- <span data-ttu-id="e5c57-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="e5c57-1921">exp datum</span></span> 
- <span data-ttu-id="e5c57-1922">Ablauf</span><span class="sxs-lookup"><span data-stu-id="e5c57-1922">expiration</span></span> 
- <span data-ttu-id="e5c57-1923">ablaufen</span><span class="sxs-lookup"><span data-stu-id="e5c57-1923">expire</span></span> 
- <span data-ttu-id="e5c57-1924">abläuft</span><span class="sxs-lookup"><span data-stu-id="e5c57-1924">expires</span></span> 
- <span data-ttu-id="e5c57-1925">Ablauf</span><span class="sxs-lookup"><span data-stu-id="e5c57-1925">expiry</span></span> 
- <span data-ttu-id="e5c57-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="e5c57-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="e5c57-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="e5c57-1927">fecha de venc</span></span> 
- <span data-ttu-id="e5c57-1928">Gultig bis</span><span class="sxs-lookup"><span data-stu-id="e5c57-1928">gultig bis</span></span> 
- <span data-ttu-id="e5c57-1929">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="e5c57-1930">Gültig bis</span><span class="sxs-lookup"><span data-stu-id="e5c57-1930">gültig bis</span></span> 
- <span data-ttu-id="e5c57-1931">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="e5c57-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1932">la scadenza</span></span> 
- <span data-ttu-id="e5c57-1933">scadenza</span><span class="sxs-lookup"><span data-stu-id="e5c57-1933">scadenza</span></span> 
- <span data-ttu-id="e5c57-1934">valable</span><span class="sxs-lookup"><span data-stu-id="e5c57-1934">valable</span></span> 
- <span data-ttu-id="e5c57-1935">validade</span><span class="sxs-lookup"><span data-stu-id="e5c57-1935">validade</span></span> 
- <span data-ttu-id="e5c57-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1936">valido hasta</span></span> 
- <span data-ttu-id="e5c57-1937">Valor</span><span class="sxs-lookup"><span data-stu-id="e5c57-1937">valor</span></span> 
- <span data-ttu-id="e5c57-1938">venc</span><span class="sxs-lookup"><span data-stu-id="e5c57-1938">venc</span></span> 
- <span data-ttu-id="e5c57-1939">vencimento</span><span class="sxs-lookup"><span data-stu-id="e5c57-1939">vencimento</span></span> 
- <span data-ttu-id="e5c57-1940">vencimiento</span><span class="sxs-lookup"><span data-stu-id="e5c57-1940">vencimiento</span></span> 
- <span data-ttu-id="e5c57-1941">verloopt</span><span class="sxs-lookup"><span data-stu-id="e5c57-1941">verloopt</span></span> 
- <span data-ttu-id="e5c57-1942">vervaldag</span><span class="sxs-lookup"><span data-stu-id="e5c57-1942">vervaldag</span></span> 
- <span data-ttu-id="e5c57-1943">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-1943">vervaldatum</span></span> 
- <span data-ttu-id="e5c57-1944">VTO</span><span class="sxs-lookup"><span data-stu-id="e5c57-1944">vto</span></span> 
- <span data-ttu-id="e5c57-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="e5c57-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="e5c57-1946">EU-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1946">EU Driver's License Number</span></span>

<span data-ttu-id="e5c57-1947">Weitere Informationen finden Sie unter [EU-Führerscheinnummer vertraulicher Informationstyp](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="e5c57-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="e5c57-1948">EU-nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1948">EU National Identification Number</span></span>

<span data-ttu-id="e5c57-1949">Weitere Informationen finden Sie unter [sensible Informationstypen für die nationale Identifikationsnummer der EU](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="e5c57-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="e5c57-1950">EU-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1950">EU Passport Number</span></span>

<span data-ttu-id="e5c57-1951">Weitere Informationen finden Sie unter [sensible Informationstypen für EU-Passport-Nummern](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="e5c57-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="e5c57-1952">EU-Sozialversicherungsnummer oder gleichwertige ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="e5c57-1953">Weitere Informationen finden Sie unter [EU-Sozialversicherungsnummer oder gleichwertiger ID-Typ für vertrauliche Informationen](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="e5c57-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="e5c57-1954">EU-Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="e5c57-1955">Weitere Informationen finden Sie unter [vertraulicher Informationstyp der EU-Steueridentifikationsnummer](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="e5c57-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="e5c57-1956">Finland National ID (Finnischer Personalausweis)</span><span class="sxs-lookup"><span data-stu-id="e5c57-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1957">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1957">Format</span></span>

<span data-ttu-id="e5c57-1958">Sechs Ziffern plus ein Zeichen, das ein Jahrhundert angibt, plus drei Ziffern plus einer Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1959">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1959">Pattern</span></span>

<span data-ttu-id="e5c57-1960">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="e5c57-1961">Sechs Ziffern im Format TTMMJJ, die ein Geburtsdatum darstellen</span><span class="sxs-lookup"><span data-stu-id="e5c57-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="e5c57-1962">Jahrhundertkennzeichnung (entweder „-“, „+“ oder „a“)</span><span class="sxs-lookup"><span data-stu-id="e5c57-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="e5c57-1963">Dreistellige persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="e5c57-1964">Eine Ziffer oder ein Buchstabe (Groß-/Kleinschreibung irrelevant), die bzw. der eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="e5c57-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1965">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1965">Checksum</span></span>

<span data-ttu-id="e5c57-1966">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1967">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1967">Definition</span></span>

<span data-ttu-id="e5c57-1968">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1969">Die Funktion Func_finnish_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1970">Ein Schlüsselwort aus Keyword_finnish_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="e5c57-1971">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1971">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-1972">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1972">Keywords</span></span>

- <span data-ttu-id="e5c57-1973">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="e5c57-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="e5c57-1974">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="e5c57-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="e5c57-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="e5c57-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="e5c57-1976">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="e5c57-1976">Personbeteckning</span></span>
- <span data-ttu-id="e5c57-1977">Personnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="e5c57-1978">Finnland – Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1978">Finland Passport Number</span></span>

<span data-ttu-id="e5c57-1979">Format Kombination von neun Buchstaben und Ziffern Muster Kombination aus neun Buchstaben und Ziffern: zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet) siebenstellige Prüfsumme keine Definition eine DLP-Richtlinie ist 75% zuversichtlich, dass diese Art von vertraulichen Informationen erkannt wurde, wenn innerhalb eines Proximity of 300 Characters: der reguläre Ausdruck Regex_finland_passport_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1979">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="e5c57-1980">Ein Schlüsselwort aus Keyword_finland_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1980">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
<span data-ttu-id="e5c57-1981"><Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="e5c57-1981"></span></span>
<span data-ttu-id="e5c57-1982">Schlüsselwörter Keyword_finland_passport_number Passport Passi</span><span class="sxs-lookup"><span data-stu-id="e5c57-1982">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="e5c57-1983">Französische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-1983">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-1984">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-1984">Format</span></span>

<span data-ttu-id="e5c57-1985">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-1985">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-1986">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-1986">Pattern</span></span>

<span data-ttu-id="e5c57-1987">12 Ziffern mit Validierung, um ähnliche Muster ( z. B. französische Telefonnummern) auszuschließen</span><span class="sxs-lookup"><span data-stu-id="e5c57-1987">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-1988">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-1988">Checksum</span></span>

<span data-ttu-id="e5c57-1989">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-1989">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-1990">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-1990">Definition</span></span>

<span data-ttu-id="e5c57-1991">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1991">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-1992">Die Funktion Func_french_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1992">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-1993">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="e5c57-1993">At least one of the following is true:</span></span>
- <span data-ttu-id="e5c57-1994">Ein Schlüsselwort aus Keyword_french_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1994">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="e5c57-1995">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="e5c57-1995">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-1996">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-1996">Keywords</span></span>

#### <a name="keyword_french_drivers_license"></a><span data-ttu-id="e5c57-1997">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="e5c57-1997">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="e5c57-1998">drivers licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-1998">drivers licence</span></span>
- <span data-ttu-id="e5c57-1999">drivers license</span><span class="sxs-lookup"><span data-stu-id="e5c57-1999">drivers license</span></span>
- <span data-ttu-id="e5c57-2000">Führerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2000">driving licence</span></span>
- <span data-ttu-id="e5c57-2001">driving license</span><span class="sxs-lookup"><span data-stu-id="e5c57-2001">driving license</span></span>
- <span data-ttu-id="e5c57-2002">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="e5c57-2002">permis de conduire</span></span>
- <span data-ttu-id="e5c57-2003">licence number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2003">licence number</span></span>
- <span data-ttu-id="e5c57-2004">license number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2004">license number</span></span>
- <span data-ttu-id="e5c57-2005">licence numbers</span><span class="sxs-lookup"><span data-stu-id="e5c57-2005">licence numbers</span></span>
- <span data-ttu-id="e5c57-2006">license numbers</span><span class="sxs-lookup"><span data-stu-id="e5c57-2006">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="e5c57-2007">Französische Carte nationale d'identité (CNI)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2007">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2008">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2008">Format</span></span>

<span data-ttu-id="e5c57-2009">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2009">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2010">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2010">Pattern</span></span>

<span data-ttu-id="e5c57-2011">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2011">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2012">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2012">Checksum</span></span>

<span data-ttu-id="e5c57-2013">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2013">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2014">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2014">Definition</span></span>

<span data-ttu-id="e5c57-2015">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2015">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2016">Der reguläre Ausdruck Regex_france_cni findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2016">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2017">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2017">Keywords</span></span>

<span data-ttu-id="e5c57-2018">Keine</span><span class="sxs-lookup"><span data-stu-id="e5c57-2018">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="e5c57-2019">Französische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2019">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2020">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2020">Format</span></span>

<span data-ttu-id="e5c57-2021">Neun Ziffern und Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e5c57-2021">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2022">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2022">Pattern</span></span>

<span data-ttu-id="e5c57-2023">Neun Ziffern und Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2023">Nine digits and letters:</span></span>
- <span data-ttu-id="e5c57-2024">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2024">Two digits</span></span> 
- <span data-ttu-id="e5c57-2025">Zwei Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2025">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-2026">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2026">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2027">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2027">Checksum</span></span>

<span data-ttu-id="e5c57-2028">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2028">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2029">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2029">Definition</span></span>

<span data-ttu-id="e5c57-2030">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2030">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2031">Die Funktion Func_fr_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2031">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2032">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2032">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2033">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2033">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="e5c57-2034">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="e5c57-2034">Keyword_passport</span></span>

- <span data-ttu-id="e5c57-2035">Passport Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2035">Passport Number</span></span>
- <span data-ttu-id="e5c57-2036">Passport No</span><span class="sxs-lookup"><span data-stu-id="e5c57-2036">Passport No</span></span>
- <span data-ttu-id="e5c57-2037">Passport#</span><span class="sxs-lookup"><span data-stu-id="e5c57-2037">Passport #</span></span>
- <span data-ttu-id="e5c57-2038">Pass #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2038">Passport#</span></span>
- <span data-ttu-id="e5c57-2039">Passport-Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2039">PassportID</span></span>
- <span data-ttu-id="e5c57-2040">Passportno</span><span class="sxs-lookup"><span data-stu-id="e5c57-2040">Passportno</span></span>
- <span data-ttu-id="e5c57-2041">passportnumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-2041">passportnumber</span></span>
- <span data-ttu-id="e5c57-2042">パスポート</span><span class="sxs-lookup"><span data-stu-id="e5c57-2042">パスポート</span></span>
- <span data-ttu-id="e5c57-2043">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2043">パスポート番号</span></span>
- <span data-ttu-id="e5c57-2044">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="e5c57-2044">パスポートのNum</span></span>
- <span data-ttu-id="e5c57-2045">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-2045">パスポート ＃</span></span> 
- <span data-ttu-id="e5c57-2046">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="e5c57-2046">Numéro de passeport</span></span>
- <span data-ttu-id="e5c57-2047">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="e5c57-2047">Passeport n °</span></span>
- <span data-ttu-id="e5c57-2048">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="e5c57-2048">Passeport Non</span></span>
- <span data-ttu-id="e5c57-2049">Passeport#</span><span class="sxs-lookup"><span data-stu-id="e5c57-2049">Passeport #</span></span>
- <span data-ttu-id="e5c57-2050">Passeport #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2050">Passeport#</span></span>
- <span data-ttu-id="e5c57-2051">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="e5c57-2051">PasseportNon</span></span>
- <span data-ttu-id="e5c57-2052">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="e5c57-2052">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="e5c57-2053">Französische Sozialversicherungsnummer (INSEE)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2053">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2054">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2054">Format</span></span>

<span data-ttu-id="e5c57-2055">15 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2055">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2056">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2056">Pattern</span></span>

<span data-ttu-id="e5c57-2057">Muss einem von zwei Mustern entsprechen:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2057">Must match one of two patterns:</span></span>
- <span data-ttu-id="e5c57-2058">13 Ziffern, gefolgt von einem Leerzeichen, gefolgt von zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2058">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="e5c57-2059">oder</span><span class="sxs-lookup"><span data-stu-id="e5c57-2059">or</span></span>
- <span data-ttu-id="e5c57-2060">15 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2060">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2061">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2061">Checksum</span></span>

<span data-ttu-id="e5c57-2062">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2062">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2063">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2063">Definition</span></span>

<span data-ttu-id="e5c57-2064">Eine DLP-Richtlinie ist zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2064">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2065">Die Funktion Func_french_insee oder Func_fr_insee sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2065">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2066">Ein Schlüsselwort aus Keyword_fr_insee wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2066">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="e5c57-2067">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2067">The checksum passes.</span></span>

<span data-ttu-id="e5c57-2068">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2068">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2069">Die Funktion Func_french_insee oder Func_fr_insee sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2069">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2070">Es wurde kein Schlüsselwort aus Keyword_fr_insee gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2070">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="e5c57-2071">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2071">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2072">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2072">Keywords</span></span>

#### <a name="keyword_fr_insee"></a><span data-ttu-id="e5c57-2073">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="e5c57-2073">Keyword_fr_insee</span></span>

- <span data-ttu-id="e5c57-2074">INSEE</span><span class="sxs-lookup"><span data-stu-id="e5c57-2074">insee</span></span>
- <span data-ttu-id="e5c57-2075">securité sociale</span><span class="sxs-lookup"><span data-stu-id="e5c57-2075">securité sociale</span></span>
- <span data-ttu-id="e5c57-2076">securite sociale</span><span class="sxs-lookup"><span data-stu-id="e5c57-2076">securite sociale</span></span>
- <span data-ttu-id="e5c57-2077">national id</span><span class="sxs-lookup"><span data-stu-id="e5c57-2077">national id</span></span>
- <span data-ttu-id="e5c57-2078">national identification</span><span class="sxs-lookup"><span data-stu-id="e5c57-2078">national identification</span></span>
- <span data-ttu-id="e5c57-2079">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="e5c57-2079">numéro d'identité</span></span>
- <span data-ttu-id="e5c57-2080">no d'identité</span><span class="sxs-lookup"><span data-stu-id="e5c57-2080">no d'identité</span></span>
- <span data-ttu-id="e5c57-2081">Nein.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2081">no.</span></span> <span data-ttu-id="e5c57-2082">d ' identité</span><span class="sxs-lookup"><span data-stu-id="e5c57-2082">d'identité</span></span>
- <span data-ttu-id="e5c57-2083">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="e5c57-2083">numero d'identite</span></span>
- <span data-ttu-id="e5c57-2084">no d'identite</span><span class="sxs-lookup"><span data-stu-id="e5c57-2084">no d'identite</span></span>
- <span data-ttu-id="e5c57-2085">Nein.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2085">no.</span></span> <span data-ttu-id="e5c57-2086">d'identite</span><span class="sxs-lookup"><span data-stu-id="e5c57-2086">d'identite</span></span>
- <span data-ttu-id="e5c57-2087">social security number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2087">social security number</span></span>
- <span data-ttu-id="e5c57-2088">social security code</span><span class="sxs-lookup"><span data-stu-id="e5c57-2088">social security code</span></span>
- <span data-ttu-id="e5c57-2089">social insurance number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2089">social insurance number</span></span>
- <span data-ttu-id="e5c57-2090">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="e5c57-2090">le numéro d'identification nationale</span></span>
- <span data-ttu-id="e5c57-2091">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="e5c57-2091">d'identité nationale</span></span>
- <span data-ttu-id="e5c57-2092">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e5c57-2092">numéro de sécurité sociale</span></span>
- <span data-ttu-id="e5c57-2093">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e5c57-2093">le code de la sécurité sociale</span></span>
- <span data-ttu-id="e5c57-2094">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="e5c57-2094">numéro d'assurance sociale</span></span>
- <span data-ttu-id="e5c57-2095">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="e5c57-2095">numéro de sécu</span></span>
- <span data-ttu-id="e5c57-2096">code sécu</span><span class="sxs-lookup"><span data-stu-id="e5c57-2096">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="e5c57-2097">Deutsche Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2097">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2098">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2098">Format</span></span>

<span data-ttu-id="e5c57-2099">Kombination von 11 Ziffern und Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e5c57-2099">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2100">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2100">Pattern</span></span>

<span data-ttu-id="e5c57-2101">11 Zahlen und Buchstaben (ohne Beachtung der Groß-/Kleinschreibung):</span><span class="sxs-lookup"><span data-stu-id="e5c57-2101">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="e5c57-2102">Eine Ziffer oder ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="e5c57-2102">A digit or letter</span></span> 
- <span data-ttu-id="e5c57-2103">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2103">Two digits</span></span> 
- <span data-ttu-id="e5c57-2104">Sechs Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e5c57-2104">Six digits or letters</span></span> 
- <span data-ttu-id="e5c57-2105">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2105">A digit</span></span> 
- <span data-ttu-id="e5c57-2106">Eine Ziffer oder ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="e5c57-2106">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2107">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2107">Checksum</span></span>

<span data-ttu-id="e5c57-2108">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2108">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2109">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2109">Definition</span></span>

<span data-ttu-id="e5c57-2110">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2110">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2111">Die Funktion Func_german_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2111">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2112">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2112">At least one of the following is true:</span></span>
    - <span data-ttu-id="e5c57-2113">Ein Schlüsselwort aus Keyword_german_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2113">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="e5c57-2114">Ein Schlüsselwort aus Keyword_german_drivers_license_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2114">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="e5c57-2115">Ein Schlüsselwort aus Keyword_german_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2115">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="e5c57-2116">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2116">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2117">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2117">Keywords</span></span>

#### <a name="keyword_german_drivers_license_number"></a><span data-ttu-id="e5c57-2118">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2118">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="e5c57-2119">Führerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2119">Führerschein</span></span>
- <span data-ttu-id="e5c57-2120">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2120">Fuhrerschein</span></span>
- <span data-ttu-id="e5c57-2121">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2121">Fuehrerschein</span></span>
- <span data-ttu-id="e5c57-2122">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2122">Führerscheinnummer</span></span>
- <span data-ttu-id="e5c57-2123">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2123">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="e5c57-2124">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2124">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="e5c57-2125">Führerschein-</span><span class="sxs-lookup"><span data-stu-id="e5c57-2125">Führerschein-</span></span> 
- <span data-ttu-id="e5c57-2126">Fuhrerschein-</span><span class="sxs-lookup"><span data-stu-id="e5c57-2126">Fuhrerschein-</span></span> 
- <span data-ttu-id="e5c57-2127">Fuehrerschein-</span><span class="sxs-lookup"><span data-stu-id="e5c57-2127">Fuehrerschein-</span></span> 
- <span data-ttu-id="e5c57-2128">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2128">FührerscheinnummerNr</span></span>
- <span data-ttu-id="e5c57-2129">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2129">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="e5c57-2130">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2130">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="e5c57-2131">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2131">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="e5c57-2132">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2132">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="e5c57-2133">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2133">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="e5c57-2134">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2134">Führerschein- Nr</span></span>
- <span data-ttu-id="e5c57-2135">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2135">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="e5c57-2136">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2136">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="e5c57-2137">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2137">Führerschein- Klasse</span></span> 
- <span data-ttu-id="e5c57-2138">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2138">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="e5c57-2139">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2139">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="e5c57-2140">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2140">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="e5c57-2141">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2141">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="e5c57-2142">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2142">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="e5c57-2143">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2143">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="e5c57-2144">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2144">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="e5c57-2145">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2145">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="e5c57-2146">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2146">Führerschein- Nr</span></span> 
- <span data-ttu-id="e5c57-2147">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2147">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="e5c57-2148">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2148">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="e5c57-2149">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2149">Führerschein- Klasse</span></span> 
- <span data-ttu-id="e5c57-2150">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2150">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="e5c57-2151">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2151">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="e5c57-2152">DL</span><span class="sxs-lookup"><span data-stu-id="e5c57-2152">DL</span></span> 
- <span data-ttu-id="e5c57-2153">DLS</span><span class="sxs-lookup"><span data-stu-id="e5c57-2153">DLS</span></span>
- <span data-ttu-id="e5c57-2154">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-2154">Driv Lic</span></span> 
- <span data-ttu-id="e5c57-2155">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="e5c57-2155">Driv Licen</span></span> 
- <span data-ttu-id="e5c57-2156">Driv License</span><span class="sxs-lookup"><span data-stu-id="e5c57-2156">Driv License</span></span>
- <span data-ttu-id="e5c57-2157">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-2157">Driv Licenses</span></span> 
- <span data-ttu-id="e5c57-2158">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-2158">Driv Licence</span></span> 
- <span data-ttu-id="e5c57-2159">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-2159">Driv Licences</span></span> 
- <span data-ttu-id="e5c57-2160">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-2160">Driv Lic</span></span> 
- <span data-ttu-id="e5c57-2161">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="e5c57-2161">Driver Licen</span></span> 
- <span data-ttu-id="e5c57-2162">Driver License</span><span class="sxs-lookup"><span data-stu-id="e5c57-2162">Driver License</span></span> 
- <span data-ttu-id="e5c57-2163">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-2163">Driver Licenses</span></span> 
- <span data-ttu-id="e5c57-2164">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-2164">Driver Licence</span></span> 
- <span data-ttu-id="e5c57-2165">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-2165">Driver Licences</span></span> 
- <span data-ttu-id="e5c57-2166">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-2166">Drivers Lic</span></span> 
- <span data-ttu-id="e5c57-2167">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="e5c57-2167">Drivers Licen</span></span> 
- <span data-ttu-id="e5c57-2168">Drivers License</span><span class="sxs-lookup"><span data-stu-id="e5c57-2168">Drivers License</span></span> 
- <span data-ttu-id="e5c57-2169">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-2169">Drivers Licenses</span></span> 
- <span data-ttu-id="e5c57-2170">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-2170">Drivers Licence</span></span> 
- <span data-ttu-id="e5c57-2171">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-2171">Drivers Licences</span></span> 
- <span data-ttu-id="e5c57-2172">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-2172">Driver's Lic</span></span> 
- <span data-ttu-id="e5c57-2173">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="e5c57-2173">Driver's Licen</span></span> 
- <span data-ttu-id="e5c57-2174">Driver's License</span><span class="sxs-lookup"><span data-stu-id="e5c57-2174">Driver's License</span></span> 
- <span data-ttu-id="e5c57-2175">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-2175">Driver's Licenses</span></span> 
- <span data-ttu-id="e5c57-2176">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-2176">Driver's Licence</span></span> 
- <span data-ttu-id="e5c57-2177">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-2177">Driver's Licences</span></span> 
- <span data-ttu-id="e5c57-2178">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-2178">Driving Lic</span></span> 
- <span data-ttu-id="e5c57-2179">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="e5c57-2179">Driving Licen</span></span> 
- <span data-ttu-id="e5c57-2180">Driving License</span><span class="sxs-lookup"><span data-stu-id="e5c57-2180">Driving License</span></span> 
- <span data-ttu-id="e5c57-2181">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-2181">Driving Licenses</span></span> 
- <span data-ttu-id="e5c57-2182">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-2182">Driving Licence</span></span> 
- <span data-ttu-id="e5c57-2183">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-2183">Driving Licences</span></span>

#### <a name="keyword_german_drivers_license_collaborative"></a><span data-ttu-id="e5c57-2184">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="e5c57-2184">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="e5c57-2185">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2185">Nr-Führerschein</span></span> 
- <span data-ttu-id="e5c57-2186">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2186">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="e5c57-2187">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2187">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="e5c57-2188">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2188">No-Führerschein</span></span> 
- <span data-ttu-id="e5c57-2189">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2189">No-Fuhrerschein</span></span> 
- <span data-ttu-id="e5c57-2190">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2190">No-Fuehrerschein</span></span> 
- <span data-ttu-id="e5c57-2191">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2191">N-Führerschein</span></span> 
- <span data-ttu-id="e5c57-2192">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2192">N-Fuhrerschein</span></span> 
- <span data-ttu-id="e5c57-2193">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2193">N-Fuehrerschein</span></span>
- <span data-ttu-id="e5c57-2194">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2194">Nr-Führerschein</span></span> 
- <span data-ttu-id="e5c57-2195">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2195">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="e5c57-2196">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2196">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="e5c57-2197">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2197">No-Führerschein</span></span> 
- <span data-ttu-id="e5c57-2198">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2198">No-Fuhrerschein</span></span> 
- <span data-ttu-id="e5c57-2199">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2199">No-Fuehrerschein</span></span> 
- <span data-ttu-id="e5c57-2200">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2200">N-Führerschein</span></span> 
- <span data-ttu-id="e5c57-2201">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2201">N-Fuhrerschein</span></span> 
- <span data-ttu-id="e5c57-2202">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2202">N-Fuehrerschein</span></span> 

#### <a name="keyword_german_drivers_license"></a><span data-ttu-id="e5c57-2203">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="e5c57-2203">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="e5c57-2204">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-2204">ausstellungsdatum</span></span>
- <span data-ttu-id="e5c57-2205">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="e5c57-2205">ausstellungsort</span></span>
- <span data-ttu-id="e5c57-2206">Ausstellende Behöde</span><span class="sxs-lookup"><span data-stu-id="e5c57-2206">ausstellende behöde</span></span>
- <span data-ttu-id="e5c57-2207">Ausstellende Behorde</span><span class="sxs-lookup"><span data-stu-id="e5c57-2207">ausstellende behorde</span></span>
- <span data-ttu-id="e5c57-2208">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="e5c57-2208">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="e5c57-2209">Deutsche Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2209">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2210">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2210">Format</span></span>

<span data-ttu-id="e5c57-2211">10 Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e5c57-2211">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2212">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2212">Pattern</span></span>

<span data-ttu-id="e5c57-2213">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2213">Pattern must include all of the following:</span></span>
- <span data-ttu-id="e5c57-2214">Das erste Zeichen ist eine Ziffer oder ein Buchstabe aus dieser Gruppe (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2214">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="e5c57-2215">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2215">Three digits</span></span> 
- <span data-ttu-id="e5c57-2216">Fünf Ziffern oder Buchstaben aus dieser Gruppe (C -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2216">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="e5c57-2217">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2217">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2218">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2218">Checksum</span></span>

<span data-ttu-id="e5c57-2219">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2219">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2220">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2220">Definition</span></span>

<span data-ttu-id="e5c57-2221">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2221">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2222">Die Funktion Func_german_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2222">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2223">Ein Schlüsselwort aus einer der fünf Schlüsselwortlisten wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2223">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="e5c57-2224">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2224">The checksum passes.</span></span>

<span data-ttu-id="e5c57-2225">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2226">Die Funktion Func_german_passport_data findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2226">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2227">Ein Schlüsselwort aus einer der fünf Schlüsselwortlisten wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2227">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="e5c57-2228">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2228">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2229">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2229">Keywords</span></span>

#### <a name="keyword_german_passport"></a><span data-ttu-id="e5c57-2230">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="e5c57-2230">Keyword_german_passport</span></span>

- <span data-ttu-id="e5c57-2231">Reisepass</span><span class="sxs-lookup"><span data-stu-id="e5c57-2231">reisepass</span></span>
- <span data-ttu-id="e5c57-2232">reisepasse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2232">reisepasse</span></span>
- <span data-ttu-id="e5c57-2233">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2233">reisepassnummer</span></span>
- <span data-ttu-id="e5c57-2234">Pass</span><span class="sxs-lookup"><span data-stu-id="e5c57-2234">passport</span></span>
- <span data-ttu-id="e5c57-2235">Pässe</span><span class="sxs-lookup"><span data-stu-id="e5c57-2235">passports</span></span>

#### <a name="keyword_german_passport_collaborative"></a><span data-ttu-id="e5c57-2236">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="e5c57-2236">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="e5c57-2237">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-2237">geburtsdatum</span></span>
- <span data-ttu-id="e5c57-2238">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-2238">ausstellungsdatum</span></span>
- <span data-ttu-id="e5c57-2239">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="e5c57-2239">ausstellungsort</span></span>

#### <a name="keyword_german_passport_number"></a><span data-ttu-id="e5c57-2240">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2240">Keyword_german_passport_number</span></span>

<span data-ttu-id="e5c57-2241">No-Reisepass Nr-Reisepass</span><span class="sxs-lookup"><span data-stu-id="e5c57-2241">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keyword_german_passport1"></a><span data-ttu-id="e5c57-2242">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="e5c57-2242">Keyword_german_passport1</span></span>

<span data-ttu-id="e5c57-2243">Reisepass-Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2243">Reisepass-Nr</span></span>

#### <a name="keyword_german_passport2"></a><span data-ttu-id="e5c57-2244">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="e5c57-2244">Keyword_german_passport2</span></span>

<span data-ttu-id="e5c57-2245">bnationalit. t</span><span class="sxs-lookup"><span data-stu-id="e5c57-2245">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="e5c57-2246">Deutsche Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2246">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2247">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2247">Format</span></span>

<span data-ttu-id="e5c57-2248">Seit dem 1. November 2010: neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2248">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="e5c57-2249">Vom 1. April 1987 bis 31. Oktober 2010:10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2249">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2250">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2250">Pattern</span></span>

<span data-ttu-id="e5c57-2251">Seit 1. November 2010:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2251">Since 1 November 2010:</span></span>
- <span data-ttu-id="e5c57-2252">Ein Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2252">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-2253">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2253">Eight digits</span></span>

<span data-ttu-id="e5c57-2254">Vom 1. April 1987 bis 31. Oktober 2010:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2254">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="e5c57-2255">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2255">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2256">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2256">Checksum</span></span>

<span data-ttu-id="e5c57-2257">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2257">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2258">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2258">Definition</span></span>

<span data-ttu-id="e5c57-2259">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2259">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2260">Der reguläre Ausdruck Regex_germany_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2260">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2261">Ein Schlüsselwort aus Keyword_germany_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2261">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2262">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2262">Keywords</span></span>

#### <a name="keyword_germany_id_card"></a><span data-ttu-id="e5c57-2263">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2263">Keyword_germany_id_card</span></span>

- <span data-ttu-id="e5c57-2264">Identity Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2264">Identity Card</span></span>
- <span data-ttu-id="e5c57-2265">ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-2265">ID</span></span>
- <span data-ttu-id="e5c57-2266">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="e5c57-2266">Identification</span></span>
- <span data-ttu-id="e5c57-2267">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-2267">Personalausweis</span></span>
- <span data-ttu-id="e5c57-2268">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2268">Identifizierungsnummer</span></span>
- <span data-ttu-id="e5c57-2269">Ausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-2269">Ausweis</span></span>
- <span data-ttu-id="e5c57-2270">Identifikation</span><span class="sxs-lookup"><span data-stu-id="e5c57-2270">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="e5c57-2271">Griechenland – Personalausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-2271">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2272">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2272">Format</span></span>

<span data-ttu-id="e5c57-2273">Kombination von 7-8 Buchstaben und Zahlen plus einem Gedankenstrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-2273">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2274">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2274">Pattern</span></span>

<span data-ttu-id="e5c57-2275">Sieben Buchstaben und Zahlen (altes Format):</span><span class="sxs-lookup"><span data-stu-id="e5c57-2275">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="e5c57-2276">Ein Buchstabe (jeder Buchstabe des griechischen Alphabets) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2276">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="e5c57-2277">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-2277">A dash</span></span> 
- <span data-ttu-id="e5c57-2278">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2278">Six digits</span></span>

<span data-ttu-id="e5c57-2279">Acht Buchstaben und Zahlen (neues Format):</span><span class="sxs-lookup"><span data-stu-id="e5c57-2279">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="e5c57-2280">Zwei Buchstaben, deren Großbuchstabe sowohl im griechischen als auch lateinischen Alphabet (ABEZHIKMNOPTYX) vorkommt </span><span class="sxs-lookup"><span data-stu-id="e5c57-2280">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="e5c57-2281">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-2281">A dash</span></span> 
- <span data-ttu-id="e5c57-2282">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2282">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2283">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2283">Checksum</span></span>

<span data-ttu-id="e5c57-2284">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2284">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2285">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2285">Definition</span></span>

<span data-ttu-id="e5c57-2286">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2286">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2287">Der reguläre Ausdruck Regex_greece_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2287">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2288">Ein Schlüsselwort aus Keyword_greece_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2288">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2289">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2289">Keywords</span></span>

#### <a name="keyword_greece_id_card"></a><span data-ttu-id="e5c57-2290">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2290">Keyword_greece_id_card</span></span>

- <span data-ttu-id="e5c57-2291">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2291">Greek identity Card</span></span>
- <span data-ttu-id="e5c57-2292">Tautotita</span><span class="sxs-lookup"><span data-stu-id="e5c57-2292">Tautotita</span></span>
- <span data-ttu-id="e5c57-2293">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="e5c57-2293">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="e5c57-2294">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="e5c57-2294">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="e5c57-2295">Hongkong (HKID) - Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2295">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2296">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2296">Format</span></span>

<span data-ttu-id="e5c57-2297">Kombination aus 8-9Buchstaben und Zahlen sowie optionale Klammern um das letzte Zeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-2297">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2298">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2298">Pattern</span></span>

<span data-ttu-id="e5c57-2299">Kombination aus Buchstaben 8-9 Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2299">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="e5c57-2300">1-2 Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2300">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-2301">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2301">Six digits</span></span> 
- <span data-ttu-id="e5c57-2302">Das letzte Zeichen (eine Ziffer oder der Buchstabe A), bei dem es sich um die Prüfziffer handelt, die optional in Klammern eingeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2302">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2303">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2303">Checksum</span></span>

<span data-ttu-id="e5c57-2304">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2304">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2305">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2305">Definition</span></span>

<span data-ttu-id="e5c57-2306">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2306">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2307">Die Funktion Func_hong_kong_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2307">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2308">Ein Schlüsselwort aus Keyword_hong_kong_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2308">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="e5c57-2309">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2309">The checksum passes.</span></span>

<span data-ttu-id="e5c57-2310">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2310">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2311">Die Funktion Func_hong_kong_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2311">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2312">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2312">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2313">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2313">Keywords</span></span>

#### <a name="keyword_hong_kong_id_card"></a><span data-ttu-id="e5c57-2314">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2314">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="e5c57-2315">Hong Kong Identity Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2315">hong kong identity card</span></span>
- <span data-ttu-id="e5c57-2316">HKIDC</span><span class="sxs-lookup"><span data-stu-id="e5c57-2316">HKIDC</span></span>
- <span data-ttu-id="e5c57-2317">id card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2317">id card</span></span>
- <span data-ttu-id="e5c57-2318">identity card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2318">identity card</span></span>
- <span data-ttu-id="e5c57-2319">HK-Personalausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-2319">hk identity card</span></span>
- <span data-ttu-id="e5c57-2320">Hong Kong-ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-2320">hong kong id</span></span>
- <span data-ttu-id="e5c57-2321">香港身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2321">香港身份證</span></span>
- <span data-ttu-id="e5c57-2322">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2322">香港永久性居民身份證</span></span>
- <span data-ttu-id="e5c57-2323">身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2323">身份證</span></span>
- <span data-ttu-id="e5c57-2324">身份証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2324">身份証</span></span>
- <span data-ttu-id="e5c57-2325">身分證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2325">身分證</span></span>
- <span data-ttu-id="e5c57-2326">身分証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2326">身分証</span></span>
- <span data-ttu-id="e5c57-2327">香港身份証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2327">香港身份証</span></span>
- <span data-ttu-id="e5c57-2328">香港身分證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2328">香港身分證</span></span>
- <span data-ttu-id="e5c57-2329">香港身分証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2329">香港身分証</span></span>
- <span data-ttu-id="e5c57-2330">香港身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2330">香港身份證</span></span>
- <span data-ttu-id="e5c57-2331">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2331">香港居民身份證</span></span>
- <span data-ttu-id="e5c57-2332">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2332">香港居民身份証</span></span>
- <span data-ttu-id="e5c57-2333">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2333">香港居民身分證</span></span>
- <span data-ttu-id="e5c57-2334">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2334">香港居民身分証</span></span>
- <span data-ttu-id="e5c57-2335">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2335">香港永久性居民身份証</span></span>
- <span data-ttu-id="e5c57-2336">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2336">香港永久性居民身分證</span></span>
- <span data-ttu-id="e5c57-2337">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2337">香港永久性居民身分証</span></span>
- <span data-ttu-id="e5c57-2338">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2338">香港永久性居民身份證</span></span>
- <span data-ttu-id="e5c57-2339">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2339">香港非永久性居民身份證</span></span>
- <span data-ttu-id="e5c57-2340">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2340">香港非永久性居民身份証</span></span>
- <span data-ttu-id="e5c57-2341">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2341">香港非永久性居民身分證</span></span>
- <span data-ttu-id="e5c57-2342">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2342">香港非永久性居民身分証</span></span>
- <span data-ttu-id="e5c57-2343">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2343">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="e5c57-2344">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2344">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="e5c57-2345">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2345">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="e5c57-2346">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2346">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="e5c57-2347">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2347">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="e5c57-2348">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2348">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="e5c57-2349">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="e5c57-2349">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="e5c57-2350">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2350">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="e5c57-2351">Indien – Permanente Kontonummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2351">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2352">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2352">Format</span></span>

<span data-ttu-id="e5c57-2353">10 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2353">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2354">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2354">Pattern</span></span>

<span data-ttu-id="e5c57-2355">10 Buchstaben oder Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2355">10 letters or digits:</span></span>
- <span data-ttu-id="e5c57-2356">Fünf Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2356">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-2357">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2357">Four digits</span></span> 
- <span data-ttu-id="e5c57-2358">Ein Buchstabe, der eine alphabetische Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="e5c57-2358">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2359">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2359">Checksum</span></span>

<span data-ttu-id="e5c57-2360">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2360">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2361">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2361">Definition</span></span>

<span data-ttu-id="e5c57-2362">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2362">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2363">Der reguläre Ausdruck Regex_india_permanent_account_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2363">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2364">Ein Schlüsselwort aus Keyword_india_permanent_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2364">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="e5c57-2365">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2365">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2366">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2366">Keywords</span></span>

#### <a name="keyword_india_permanent_account_number"></a><span data-ttu-id="e5c57-2367">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2367">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="e5c57-2368">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2368">Permanent Account Number</span></span> 
- <span data-ttu-id="e5c57-2369">Schwenken</span><span class="sxs-lookup"><span data-stu-id="e5c57-2369">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="e5c57-2370">Indien - Eindeutige Identifikationsnummer (Aadhaar)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2370">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2371">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2371">Format</span></span>

<span data-ttu-id="e5c57-2372">12 Ziffern mit optionalen Leerzeichen oder Bindestrichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-2372">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2373">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2373">Pattern</span></span>

<span data-ttu-id="e5c57-2374">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2374">12 digits:</span></span>
- <span data-ttu-id="e5c57-2375">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2375">Four digits</span></span> 
- <span data-ttu-id="e5c57-2376">Eine optionales Leerzeichen oder ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-2376">An optional space or dash</span></span> 
- <span data-ttu-id="e5c57-2377">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2377">Four digits</span></span> 
- <span data-ttu-id="e5c57-2378">Eine optionales Leerzeichen oder ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-2378">An optional space or dash</span></span> 
- <span data-ttu-id="e5c57-2379">Die letzte Ziffer, die eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="e5c57-2379">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2380">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2380">Checksum</span></span>

<span data-ttu-id="e5c57-2381">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2382">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2382">Definition</span></span>

<span data-ttu-id="e5c57-2383">Eine DLP-Richtlinie ist 85% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: die Funktion Func_india_aadhaar findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2383">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="e5c57-2384">Ein Schlüsselwort aus Keyword_india_aadhar wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2384">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="e5c57-2385">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2385">The checksum passes.</span></span>
<span data-ttu-id="e5c57-2386">Eine DLP-Richtlinie ist 75% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: die Funktion Func_india_aadhaar findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2386">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="e5c57-2387">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2387">The checksum passes.</span></span>
<!-- India Unique Identification (Aadhaar) number -->
<span data-ttu-id="e5c57-2388"><Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="e5c57-2388"></span></span>

### <a name="keywords"></a><span data-ttu-id="e5c57-2389">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2389">Keywords</span></span>
   
#### <a name="keyword_india_aadhar"></a><span data-ttu-id="e5c57-2390">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="e5c57-2390">Keyword_india_aadhar</span></span>
- <span data-ttu-id="e5c57-2391">Aadhar</span><span class="sxs-lookup"><span data-stu-id="e5c57-2391">Aadhar</span></span>
- <span data-ttu-id="e5c57-2392">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="e5c57-2392">Aadhaar</span></span>
- <span data-ttu-id="e5c57-2393">UID</span><span class="sxs-lookup"><span data-stu-id="e5c57-2393">UID</span></span>
- <span data-ttu-id="e5c57-2394">आधार</span><span class="sxs-lookup"><span data-stu-id="e5c57-2394">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="e5c57-2395">Indonesien – Perosonalausweisnummer (KTP)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2395">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2396">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2396">Format</span></span>

<span data-ttu-id="e5c57-2397">16 Ziffern mit optionalen Punkten</span><span class="sxs-lookup"><span data-stu-id="e5c57-2397">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2398">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2398">Pattern</span></span>

<span data-ttu-id="e5c57-2399">16 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2399">16 digits:</span></span>
- <span data-ttu-id="e5c57-2400">Zweistelliger Provinzcode </span><span class="sxs-lookup"><span data-stu-id="e5c57-2400">Two-digit province code</span></span> 
- <span data-ttu-id="e5c57-2401">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2401">A period (optional)</span></span> 
- <span data-ttu-id="e5c57-2402">Zweistelliger Regency- oder Stadtcode </span><span class="sxs-lookup"><span data-stu-id="e5c57-2402">Two-digit regency or city code</span></span> 
- <span data-ttu-id="e5c57-2403">Zweistelliger Subdistrict-Code </span><span class="sxs-lookup"><span data-stu-id="e5c57-2403">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="e5c57-2404">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2404">A period (optional)</span></span> 
- <span data-ttu-id="e5c57-2405">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="e5c57-2405">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="e5c57-2406">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2406">A period (optional)</span></span> 
- <span data-ttu-id="e5c57-2407">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2407">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2408">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2408">Checksum</span></span>

<span data-ttu-id="e5c57-2409">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2409">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2410">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2410">Definition</span></span>

<span data-ttu-id="e5c57-2411">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2412">Der reguläre Ausdruck Regex_indonesia_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2412">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2413">Ein Schlüsselwort aus Keyword_indonesia_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2413">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="e5c57-2414">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2415">Der reguläre Ausdruck Regex_indonesia_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2415">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2416">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2416">Keywords</span></span>
   
#### <a name="keyword_indonesia_id_card"></a><span data-ttu-id="e5c57-2417">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2417">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="e5c57-2418">KTP</span><span class="sxs-lookup"><span data-stu-id="e5c57-2418">KTP</span></span>
- <span data-ttu-id="e5c57-2419">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="e5c57-2419">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="e5c57-2420">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="e5c57-2420">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="e5c57-2421">International Banking Account Number (IBAN)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2421">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2422">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2422">Format</span></span>

<span data-ttu-id="e5c57-2423">Landesvorwahl (zwei Buchstaben) plus Prüfziffern (zwei Ziffern) plus BBAN-Nummer (bis zu 30 Zeichen)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2423">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2424">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2424">Pattern</span></span>

<span data-ttu-id="e5c57-2425">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2425">Pattern must include all of the following:</span></span>

- <span data-ttu-id="e5c57-2426">Landesvorwahl mit zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e5c57-2426">Two-letter country code</span></span>
- <span data-ttu-id="e5c57-2427">Zwei Prüfziffern (gefolgt von einem optionalen Leerzeichen)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2427">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="e5c57-2428">1-7 Gruppen von vier Buchstaben oder Ziffern (können durch Leerzeichengetrennt werden)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2428">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="e5c57-2429">1 bis 3 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2429">1-3 letters or digits</span></span>

<span data-ttu-id="e5c57-2430">Das Format für jedes Land unterscheidet sich geringfügig.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2430">The format for each country is slightly different.</span></span> <span data-ttu-id="e5c57-2431">Der Typ der IBAN-vertraulichen Informationen deckt diese 60 Länder ab:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2431">The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="e5c57-2432">AD, AE, Al, at, AZ, BA, be, BG, BH, ch, CR, CY, CZ, de, DK, Do, EE, es, fi, FO, Fr, GB, ge, GI, GL, GR, HR, HU, IE, IL, is, IT, kW, KZ, LB, Li, lt, LU, LV, MC, MD, me, MK, Mr, MT, mu , NL, No, PL, PT, RO, RS, Sa, SE, Si, SK, SM, TN, TR, VG</span><span class="sxs-lookup"><span data-stu-id="e5c57-2432">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2433">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2433">Checksum</span></span>

<span data-ttu-id="e5c57-2434">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2434">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2435">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2435">Definition</span></span>

<span data-ttu-id="e5c57-2436">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2436">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2437">Die Funktion Func_iban findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2437">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2438">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2438">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2439">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2439">Keywords</span></span>

<span data-ttu-id="e5c57-2440">Keine</span><span class="sxs-lookup"><span data-stu-id="e5c57-2440">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="e5c57-2441">IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="e5c57-2441">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2442">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2442">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="e5c57-2443">IPv4</span><span class="sxs-lookup"><span data-stu-id="e5c57-2443">IPv4:</span></span>
<span data-ttu-id="e5c57-2444">Komplexes Muster, das formatierte (Punkte) und unformatierte (keine Punkte) Versionen der IPv4-Adressen angibt</span><span class="sxs-lookup"><span data-stu-id="e5c57-2444">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="e5c57-2445">IPv6</span><span class="sxs-lookup"><span data-stu-id="e5c57-2445">IPv6:</span></span>
<span data-ttu-id="e5c57-2446"> Komplexes Muster, das formatierte IPv6-Nummern angibt (schließt Doppelpunkte ein)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2446">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2447">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2447">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2448">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2448">Checksum</span></span>

<span data-ttu-id="e5c57-2449">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2449">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2450">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2450">Definition</span></span>

<span data-ttu-id="e5c57-2451">Für IPv6 ist eine DLP-Richtlinie zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2451">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2452">Der reguläre Ausdruck Regex_ipv6_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2452">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2453">Es wurde kein Schlüsselwort aus Keyword_ipaddress gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2453">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="e5c57-2454">Für IPv4 ist eine DLP-Richtlinie zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2454">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2455">Der reguläre Ausdruck Regex_ipv4_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2455">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2456">Ein Schlüsselwort aus Keyword_ipaddress wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2456">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="e5c57-2457">Für IPv6 ist eine DLP-Richtlinie zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2457">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2458">Der reguläre Ausdruck Regex_ipv6_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2458">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2459">Es wurde kein Schlüsselwort aus Keyword_ipaddress gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2459">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2460">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2460">Keywords</span></span>

#### <a name="keyword_ipaddress"></a><span data-ttu-id="e5c57-2461">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="e5c57-2461">Keyword_ipaddress</span></span>

- <span data-ttu-id="e5c57-2462">IP (bei diesem Schlüsselwort wird die Groß-/Kleinschreibung unterschieden)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2462">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="e5c57-2463">ip address</span><span class="sxs-lookup"><span data-stu-id="e5c57-2463">ip address</span></span> 
- <span data-ttu-id="e5c57-2464">IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="e5c57-2464">ip addresses</span></span>
- <span data-ttu-id="e5c57-2465">internet protocol</span><span class="sxs-lookup"><span data-stu-id="e5c57-2465">internet protocol</span></span>
- <span data-ttu-id="e5c57-2466">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="e5c57-2466">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="e5c57-2467">Internationale Klassifikation von Krankheiten (ICD-10-cm)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2467">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2468">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2468">Format</span></span>

<span data-ttu-id="e5c57-2469">Dictionary</span><span class="sxs-lookup"><span data-stu-id="e5c57-2469">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2470">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2470">Pattern</span></span>

<span data-ttu-id="e5c57-2471">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="e5c57-2471">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2472">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2472">Checksum</span></span>

<span data-ttu-id="e5c57-2473">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2473">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2474">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2474">Definition</span></span>

<span data-ttu-id="e5c57-2475">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2475">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2476">Ein Schlüsselwort aus Dictionary_icd_10_cm wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2476">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="e5c57-2477">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2477">Keywords</span></span>

<span data-ttu-id="e5c57-2478">Ein beliebiger Ausdruck aus dem Dictionary_icd_10_cm-Stichwort Wörterbuch, das auf der [internationalen Klassifikation von Krankheiten basiert, zehnte Überarbeitung, klinische Änderung (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="e5c57-2478">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="e5c57-2479">Dieser Typ sucht nur nach dem Begriff, nicht nach den Versicherungs Codes.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2479">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="e5c57-2480">Internationale Klassifikation von Krankheiten (ICD-9-cm)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2480">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2481">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2481">Format</span></span>

<span data-ttu-id="e5c57-2482">Dictionary</span><span class="sxs-lookup"><span data-stu-id="e5c57-2482">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2483">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2483">Pattern</span></span>

<span data-ttu-id="e5c57-2484">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="e5c57-2484">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2485">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2485">Checksum</span></span>

<span data-ttu-id="e5c57-2486">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2486">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2487">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2487">Definition</span></span>

<span data-ttu-id="e5c57-2488">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2488">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2489">Ein Schlüsselwort aus Dictionary_icd_9_cm wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2489">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2490">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2490">Keywords</span></span>

<span data-ttu-id="e5c57-2491">Ein beliebiger Ausdruck aus dem Dictionary_icd_9_cm-Stichwort Wörterbuch, das auf der [internationalen Klassifikation von Krankheiten basiert, neunte Revision, klinische Änderung (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="e5c57-2491">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="e5c57-2492">Dieser Typ sucht nur nach dem Begriff, nicht nach den Versicherungs Codes.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2492">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="e5c57-2493">Irland – Personal Public Service-Nummer (PPS)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2493">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2494">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2494">Format</span></span>

<span data-ttu-id="e5c57-2495">Altes Format (bis 31. Dez. 2012):</span><span class="sxs-lookup"><span data-stu-id="e5c57-2495">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="e5c57-2496">Sieben Ziffern, gefolgt von 1-2 Buchstaben </span><span class="sxs-lookup"><span data-stu-id="e5c57-2496">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="e5c57-2497">Neues Format (1 Jan 2013 und danach):</span><span class="sxs-lookup"><span data-stu-id="e5c57-2497">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="e5c57-2498">Sieben Ziffern, gefolgt von zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e5c57-2498">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2499">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2499">Pattern</span></span>

<span data-ttu-id="e5c57-2500">Altes Format (bis 31. Dez. 2012):</span><span class="sxs-lookup"><span data-stu-id="e5c57-2500">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="e5c57-2501">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="e5c57-2501">Seven digits</span></span> 
- <span data-ttu-id="e5c57-2502">1-2 Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2502">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="e5c57-2503">Neues Format (1 Jan 2013 und danach):</span><span class="sxs-lookup"><span data-stu-id="e5c57-2503">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="e5c57-2504">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="e5c57-2504">Seven digits</span></span> 
- <span data-ttu-id="e5c57-2505">Ein Buchstabe (Groß-/Kleinschreibung irrelevant), wobei es sich um eine alphabetische Prüfziffer handelt </span><span class="sxs-lookup"><span data-stu-id="e5c57-2505">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="e5c57-2506">Die Buchstaben "A" oder "H" (Groß-/Kleinschreibung irrelevant)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2506">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2507">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2507">Checksum</span></span>

<span data-ttu-id="e5c57-2508">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2508">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2509">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2509">Definition</span></span>

<span data-ttu-id="e5c57-2510">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2510">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2511">Die Funktion Func_ireland_pps findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2511">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2512">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2512">One of the following is true:</span></span>
    - <span data-ttu-id="e5c57-2513">Ein Schlüsselwort aus Keyword_ireland_pps wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2513">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="e5c57-2514">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2514">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="e5c57-2515">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2515">The checksum passes.</span></span>

<span data-ttu-id="e5c57-2516">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2516">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2517">Die Funktion Func_ireland_pps findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2517">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2518">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2518">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2519">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2519">Keywords</span></span>

#### <a name="keyword_ireland_pps"></a><span data-ttu-id="e5c57-2520">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="e5c57-2520">Keyword_ireland_pps</span></span>

- <span data-ttu-id="e5c57-2521">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2521">Personal Public Service Number</span></span> 
- <span data-ttu-id="e5c57-2522">PPS Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2522">PPS Number</span></span> 
- <span data-ttu-id="e5c57-2523">PPS Num</span><span class="sxs-lookup"><span data-stu-id="e5c57-2523">PPS Num</span></span> 
- <span data-ttu-id="e5c57-2524">PPS No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2524">PPS No.</span></span> 
- <span data-ttu-id="e5c57-2525">PPS #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2525">PPS #</span></span> 
- <span data-ttu-id="e5c57-2526">PPS #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2526">PPS#</span></span> 
- <span data-ttu-id="e5c57-2527">PPSN</span><span class="sxs-lookup"><span data-stu-id="e5c57-2527">PPSN</span></span> 
- <span data-ttu-id="e5c57-2528">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2528">Public Services Card</span></span> 
- <span data-ttu-id="e5c57-2529">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="e5c57-2529">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="e5c57-2530">Uimh.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2530">Uimh.</span></span> <span data-ttu-id="e5c57-2531">PSP</span><span class="sxs-lookup"><span data-stu-id="e5c57-2531">PSP</span></span> 
- <span data-ttu-id="e5c57-2532">PSP</span><span class="sxs-lookup"><span data-stu-id="e5c57-2532">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="e5c57-2533">Israelische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2533">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2534">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2534">Format</span></span>

<span data-ttu-id="e5c57-2535">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2535">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2536">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2536">Pattern</span></span>

<span data-ttu-id="e5c57-2537">Formatiert</span><span class="sxs-lookup"><span data-stu-id="e5c57-2537">Formatted:</span></span>
- <span data-ttu-id="e5c57-2538">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2538">Two digits</span></span> 
- <span data-ttu-id="e5c57-2539">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-2539">A dash</span></span> 
- <span data-ttu-id="e5c57-2540">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2540">Three digits</span></span> 
- <span data-ttu-id="e5c57-2541">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-2541">A dash</span></span> 
- <span data-ttu-id="e5c57-2542">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2542">Eight digits</span></span>

<span data-ttu-id="e5c57-2543">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="e5c57-2543">Unformatted:</span></span>
- <span data-ttu-id="e5c57-2544">	13 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2544">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2545">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2545">Checksum</span></span>

<span data-ttu-id="e5c57-2546">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2546">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2547">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2547">Definition</span></span>

<span data-ttu-id="e5c57-2548">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2548">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2549">Der reguläre Ausdruck Regex_israel_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2549">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2550">Ein Schlüsselwort aus Keyword_israel_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2550">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2551">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2551">Keywords</span></span>

#### <a name="keyword_israel_bank_account_number"></a><span data-ttu-id="e5c57-2552">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2552">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="e5c57-2553">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2553">Bank Account Number</span></span> 
- <span data-ttu-id="e5c57-2554">Bank Account</span><span class="sxs-lookup"><span data-stu-id="e5c57-2554">Bank Account</span></span> 
- <span data-ttu-id="e5c57-2555">Account Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2555">Account Number</span></span> 
- <span data-ttu-id="e5c57-2556">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="e5c57-2556">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="e5c57-2557">Israelische Ausweis-ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-2557">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2558">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2558">Format</span></span>

<span data-ttu-id="e5c57-2559">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2559">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2560">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2560">Pattern</span></span>

<span data-ttu-id="e5c57-2561">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2561">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2562">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2562">Checksum</span></span>

<span data-ttu-id="e5c57-2563">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2563">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2564">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2564">Definition</span></span>

<span data-ttu-id="e5c57-2565">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2565">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2566">Die Funktion Func_israeli_national_id_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2566">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2567">Ein Schlüsselwort aus Keyword_Israel_National_ID wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2567">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="e5c57-2568">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2568">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2569">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2569">Keywords</span></span>

#### <a name="keyword_israel_national_id"></a><span data-ttu-id="e5c57-2570">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-2570">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="e5c57-2571">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="e5c57-2571">מספר זהות</span></span> 
- <span data-ttu-id="e5c57-2572">National ID Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2572">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="e5c57-2573">Italienische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2573">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2574">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2574">Format</span></span>

<span data-ttu-id="e5c57-2575">Eine Kombination von 10 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2575">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2576">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2576">Pattern</span></span>

- <span data-ttu-id="e5c57-2577">Eine Kombination aus 10 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2577">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="e5c57-2578">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2578">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-2579">Der Buchstabe „A“ oder „W“ (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2579">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-2580">Sieben Buchstaben (ohne Beachtung der Groß-/Kleinschreibung), Ziffern oder der Unterstrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-2580">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="e5c57-2581">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2581">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2582">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2582">Checksum</span></span>

<span data-ttu-id="e5c57-2583">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2583">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2584">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2584">Definition</span></span>

<span data-ttu-id="e5c57-2585">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2585">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2586">Der reguläre Ausdruck Regex_italy_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2586">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2587">Ein Schlüsselwort aus Keyword_italy_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2587">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2588">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2588">Keywords</span></span>

#### <a name="keyword_italy_drivers_license_number"></a><span data-ttu-id="e5c57-2589">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2589">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="e5c57-2590">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="e5c57-2590">numero di patente di guida</span></span> 
- <span data-ttu-id="e5c57-2591">patente di guida</span><span class="sxs-lookup"><span data-stu-id="e5c57-2591">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="e5c57-2592">Japanische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2592">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2593">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2593">Format</span></span>

<span data-ttu-id="e5c57-2594">Sieben oder acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2594">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2595">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2595">Pattern</span></span>

<span data-ttu-id="e5c57-2596">Bankkontonummer:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2596">Bank account number:</span></span>
- <span data-ttu-id="e5c57-2597">Sieben oder acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2597">Seven or eight digits</span></span>
- <span data-ttu-id="e5c57-2598">Niederlassungscode der Bank:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2598">Bank account branch code:</span></span>
- <span data-ttu-id="e5c57-2599">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2599">Four digits</span></span> 
- <span data-ttu-id="e5c57-2600">Ein Leerzeichen oder ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2600">A space or dash (optional)</span></span> 
- <span data-ttu-id="e5c57-2601">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2601">Three digits</span></span>

<span data-ttu-id="e5c57-2602">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2602">Checksum</span></span>

<span data-ttu-id="e5c57-2603">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2603">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2604">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2604">Definition</span></span>

<span data-ttu-id="e5c57-2605">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2605">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2606">Die Funktion Func_jp_bank_account findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2606">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2607">Ein Schlüsselwort aus Keyword_jp_bank_account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2607">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="e5c57-2608">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2608">One of the following is true:</span></span>
- <span data-ttu-id="e5c57-2609">Die Funktion Func_jp_bank_account_branch_code findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2609">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2610">Ein Schlüsselwort aus Keyword_jp_bank_branch_code wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2610">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="e5c57-2611">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2611">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2612">Die Funktion Func_jp_bank_account findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2612">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2613">Ein Schlüsselwort aus Keyword_jp_bank_account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2613">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2614">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2614">Keywords</span></span>

#### <a name="keyword_jp_bank_account"></a><span data-ttu-id="e5c57-2615">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="e5c57-2615">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="e5c57-2616">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2616">Checking Account Number</span></span> 
- <span data-ttu-id="e5c57-2617">Checking Account</span><span class="sxs-lookup"><span data-stu-id="e5c57-2617">Checking Account</span></span> 
- <span data-ttu-id="e5c57-2618">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2618">Checking Account #</span></span> 
- <span data-ttu-id="e5c57-2619">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2619">Checking Acct Number</span></span> 
- <span data-ttu-id="e5c57-2620">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2620">Checking Acct #</span></span> 
- <span data-ttu-id="e5c57-2621">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2621">Checking Acct No.</span></span> 
- <span data-ttu-id="e5c57-2622">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2622">Checking Account No.</span></span> 
- <span data-ttu-id="e5c57-2623">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2623">Bank Account Number</span></span> 
- <span data-ttu-id="e5c57-2624">Bank Account</span><span class="sxs-lookup"><span data-stu-id="e5c57-2624">Bank Account</span></span> 
- <span data-ttu-id="e5c57-2625">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2625">Bank Account #</span></span> 
- <span data-ttu-id="e5c57-2626">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2626">Bank Acct Number</span></span> 
- <span data-ttu-id="e5c57-2627">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2627">Bank Acct #</span></span> 
- <span data-ttu-id="e5c57-2628">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2628">Bank Acct No.</span></span> 
- <span data-ttu-id="e5c57-2629">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2629">Bank Account No.</span></span> 
- <span data-ttu-id="e5c57-2630">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2630">Savings Account Number</span></span> 
- <span data-ttu-id="e5c57-2631">Savings Account</span><span class="sxs-lookup"><span data-stu-id="e5c57-2631">Savings Account</span></span> 
- <span data-ttu-id="e5c57-2632">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2632">Savings Account #</span></span> 
- <span data-ttu-id="e5c57-2633">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2633">Savings Acct Number</span></span> 
- <span data-ttu-id="e5c57-2634">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2634">Savings Acct #</span></span> 
- <span data-ttu-id="e5c57-2635">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2635">Savings Acct No.</span></span> 
- <span data-ttu-id="e5c57-2636">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2636">Savings Account No.</span></span> 
- <span data-ttu-id="e5c57-2637">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2637">Debit Account Number</span></span> 
- <span data-ttu-id="e5c57-2638">Debit Account</span><span class="sxs-lookup"><span data-stu-id="e5c57-2638">Debit Account</span></span> 
- <span data-ttu-id="e5c57-2639">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2639">Debit Account #</span></span> 
- <span data-ttu-id="e5c57-2640">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2640">Debit Acct Number</span></span> 
- <span data-ttu-id="e5c57-2641">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2641">Debit Acct #</span></span> 
- <span data-ttu-id="e5c57-2642">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2642">Debit Acct No.</span></span> 
- <span data-ttu-id="e5c57-2643">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2643">Debit Account No.</span></span> 
- <span data-ttu-id="e5c57-2644">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="e5c57-2644">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="e5c57-2645">#アカウントの確認, 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="e5c57-2645">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="e5c57-2646">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="e5c57-2646">＃勘定の確認</span></span> 
- <span data-ttu-id="e5c57-2647">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="e5c57-2647">勘定番号の確認</span></span> 
- <span data-ttu-id="e5c57-2648">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="e5c57-2648">口座番号の確認</span></span> 
- <span data-ttu-id="e5c57-2649">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2649">銀行口座番号</span></span> 
- <span data-ttu-id="e5c57-2650">銀行口座</span><span class="sxs-lookup"><span data-stu-id="e5c57-2650">銀行口座</span></span> 
- <span data-ttu-id="e5c57-2651">銀行口座＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-2651">銀行口座＃</span></span> 
- <span data-ttu-id="e5c57-2652">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2652">銀行の勘定番号</span></span> 
- <span data-ttu-id="e5c57-2653">銀行のacct＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-2653">銀行のacct＃</span></span> 
- <span data-ttu-id="e5c57-2654">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="e5c57-2654">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="e5c57-2655">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2655">銀行口座番号</span></span>
- <span data-ttu-id="e5c57-2656">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2656">普通預金口座番号</span></span> 
- <span data-ttu-id="e5c57-2657">預金口座</span><span class="sxs-lookup"><span data-stu-id="e5c57-2657">預金口座</span></span> 
- <span data-ttu-id="e5c57-2658">貯蓄口座＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-2658">貯蓄口座＃</span></span> 
- <span data-ttu-id="e5c57-2659">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="e5c57-2659">貯蓄勘定の数</span></span> 
- <span data-ttu-id="e5c57-2660">貯蓄勘定＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-2660">貯蓄勘定＃</span></span> 
- <span data-ttu-id="e5c57-2661">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2661">貯蓄勘定番号</span></span> 
- <span data-ttu-id="e5c57-2662">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2662">普通預金口座番号</span></span> 
- <span data-ttu-id="e5c57-2663">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2663">引き落とし口座番号</span></span> 
- <span data-ttu-id="e5c57-2664">口座番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2664">口座番号</span></span> 
- <span data-ttu-id="e5c57-2665">口座番号＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-2665">口座番号＃</span></span> 
- <span data-ttu-id="e5c57-2666">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2666">デビットのacct番号</span></span> 
- <span data-ttu-id="e5c57-2667">デビット勘定＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-2667">デビット勘定＃</span></span> 
- <span data-ttu-id="e5c57-2668">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2668">デビットACCTの番号</span></span> 
- <span data-ttu-id="e5c57-2669">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2669">デビット口座番号</span></span> 

#### <a name="keyword_jp_bank_branch_code"></a><span data-ttu-id="e5c57-2670">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="e5c57-2670">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="e5c57-2671">Otemachi</span><span class="sxs-lookup"><span data-stu-id="e5c57-2671">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="e5c57-2672">Japanische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2672">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2673">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2673">Format</span></span>

<span data-ttu-id="e5c57-2674">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2674">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2675">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2675">Pattern</span></span>

<span data-ttu-id="e5c57-2676">12 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2676">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2677">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2677">Checksum</span></span>

<span data-ttu-id="e5c57-2678">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2678">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2679">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2679">Definition</span></span>

<span data-ttu-id="e5c57-2680">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2680">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2681">Die Funktion Func_jp_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2681">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2682">Ein Schlüsselwort aus Keyword_jp_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2682">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2683">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2683">Keywords</span></span>

#### <a name="keyword_jp_drivers_license_number"></a><span data-ttu-id="e5c57-2684">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2684">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="e5c57-2685">DL #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2685">dl#</span></span> 
- <span data-ttu-id="e5c57-2686">DL</span><span class="sxs-lookup"><span data-stu-id="e5c57-2686">DL＃</span></span> 
- <span data-ttu-id="e5c57-2687">DLS #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2687">dls#</span></span> 
- <span data-ttu-id="e5c57-2688">DLS</span><span class="sxs-lookup"><span data-stu-id="e5c57-2688">DLS＃</span></span> 
- <span data-ttu-id="e5c57-2689">driver license</span><span class="sxs-lookup"><span data-stu-id="e5c57-2689">driver license</span></span> 
- <span data-ttu-id="e5c57-2690">driver licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-2690">driver licenses</span></span> 
- <span data-ttu-id="e5c57-2691">drivers license</span><span class="sxs-lookup"><span data-stu-id="e5c57-2691">drivers license</span></span> 
- <span data-ttu-id="e5c57-2692">driver's license</span><span class="sxs-lookup"><span data-stu-id="e5c57-2692">driver's license</span></span> 
- <span data-ttu-id="e5c57-2693">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-2693">drivers licenses</span></span> 
- <span data-ttu-id="e5c57-2694">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-2694">driver's licenses</span></span> 
- <span data-ttu-id="e5c57-2695">driving licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-2695">driving licence</span></span> 
- <span data-ttu-id="e5c57-2696">lic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2696">lic#</span></span> 
- <span data-ttu-id="e5c57-2697">LIC</span><span class="sxs-lookup"><span data-stu-id="e5c57-2697">LIC＃</span></span> 
- <span data-ttu-id="e5c57-2698">LiCS #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2698">lics#</span></span> 
- <span data-ttu-id="e5c57-2699">state id</span><span class="sxs-lookup"><span data-stu-id="e5c57-2699">state id</span></span> 
- <span data-ttu-id="e5c57-2700">state identification</span><span class="sxs-lookup"><span data-stu-id="e5c57-2700">state identification</span></span> 
- <span data-ttu-id="e5c57-2701">state identification number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2701">state identification number</span></span> 
- <span data-ttu-id="e5c57-2702">低所得国＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-2702">低所得国＃</span></span> 
- <span data-ttu-id="e5c57-2703">免許証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2703">免許証</span></span> 
- <span data-ttu-id="e5c57-2704">状態ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-2704">状態ID</span></span>
- <span data-ttu-id="e5c57-2705">状態の識別</span><span class="sxs-lookup"><span data-stu-id="e5c57-2705">状態の識別</span></span> 
- <span data-ttu-id="e5c57-2706">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2706">状態の識別番号</span></span> 
- <span data-ttu-id="e5c57-2707">運転免許</span><span class="sxs-lookup"><span data-stu-id="e5c57-2707">運転免許</span></span> 
- <span data-ttu-id="e5c57-2708">運転免許証</span><span class="sxs-lookup"><span data-stu-id="e5c57-2708">運転免許証</span></span> 
- <span data-ttu-id="e5c57-2709">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2709">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="e5c57-2710">Japanische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2710">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2711">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2711">Format</span></span>

<span data-ttu-id="e5c57-2712">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2712">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2713">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2713">Pattern</span></span>

<span data-ttu-id="e5c57-2714">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2714">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2715">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2715">Checksum</span></span>

<span data-ttu-id="e5c57-2716">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2716">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2717">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2717">Definition</span></span>

<span data-ttu-id="e5c57-2718">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2718">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2719">Die Funktion Func_jp_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2719">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2720">Ein Schlüsselwort aus Keyword_jp_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2720">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2721">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2721">Keywords</span></span>

#### <a name="keyword_jp_passport"></a><span data-ttu-id="e5c57-2722">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="e5c57-2722">Keyword_jp_passport</span></span>

- <span data-ttu-id="e5c57-2723">パスポート</span><span class="sxs-lookup"><span data-stu-id="e5c57-2723">パスポート</span></span> 
- <span data-ttu-id="e5c57-2724">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2724">パスポート番号</span></span> 
- <span data-ttu-id="e5c57-2725">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="e5c57-2725">パスポートのNum</span></span> 
- <span data-ttu-id="e5c57-2726">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-2726">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="e5c57-2727">Japanische Einwohnerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2727">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2728">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2728">Format</span></span>

<span data-ttu-id="e5c57-2729">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2729">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2730">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2730">Pattern</span></span>

<span data-ttu-id="e5c57-2731">11 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2731">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2732">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2732">Checksum</span></span>

<span data-ttu-id="e5c57-2733">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2733">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2734">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2734">Definition</span></span>

<span data-ttu-id="e5c57-2735">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2736">Die Funktion Func_jp_resident_registration_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2736">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2737">Ein Schlüsselwort aus Keyword_jp_resident_registration_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2737">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2738">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2738">Keywords</span></span>

#### <a name="keyword_jp_resident_registration_number"></a><span data-ttu-id="e5c57-2739">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2739">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="e5c57-2740">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2740">Resident Registration Number</span></span>
- <span data-ttu-id="e5c57-2741">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2741">Resident Register Number</span></span> 
- <span data-ttu-id="e5c57-2742">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2742">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="e5c57-2743">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2743">Resident Registration No.</span></span> 
- <span data-ttu-id="e5c57-2744">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2744">Resident Register No.</span></span> 
- <span data-ttu-id="e5c57-2745">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2745">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="e5c57-2746">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2746">Basic Resident Register No.</span></span> 
- <span data-ttu-id="e5c57-2747">住民登録番号、登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="e5c57-2747">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="e5c57-2748">住民基本登録番号、登録番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2748">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="e5c57-2749">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="e5c57-2749">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="e5c57-2750">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2750">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="e5c57-2751">Japanische Sozialversicherungsnummer (SIN)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2751">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2752">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2752">Format</span></span>

<span data-ttu-id="e5c57-2753">7-12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2753">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2754">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2754">Pattern</span></span>

<span data-ttu-id="e5c57-2755">7 bis 12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2755">7-12 digits:</span></span>
- <span data-ttu-id="e5c57-2756">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2756">Four digits</span></span> 
- <span data-ttu-id="e5c57-2757">Ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2757">A hyphen (optional)</span></span> 
- <span data-ttu-id="e5c57-2758">Sechs Ziffern oder</span><span class="sxs-lookup"><span data-stu-id="e5c57-2758">Six digits OR</span></span>
- <span data-ttu-id="e5c57-2759">7-12 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2759">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2760">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2760">Checksum</span></span>

<span data-ttu-id="e5c57-2761">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2761">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2762">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2762">Definition</span></span>

<span data-ttu-id="e5c57-2763">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2763">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2764">Die Funktion Func_jp_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2764">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2765">Ein Schlüsselwort aus Keyword_jp_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2765">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="e5c57-2766">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2766">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2767">Die Funktion Func_jp_sin_pre_1997 findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2767">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2768">Ein Schlüsselwort aus Keyword_jp_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2768">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2769">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2769">Keywords</span></span>

#### <a name="keyword_jp_sin"></a><span data-ttu-id="e5c57-2770">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="e5c57-2770">Keyword_jp_sin</span></span>

- <span data-ttu-id="e5c57-2771">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2771">Social Insurance No.</span></span> 
- <span data-ttu-id="e5c57-2772">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="e5c57-2772">Social Insurance Num</span></span> 
- <span data-ttu-id="e5c57-2773">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2773">Social Insurance Number</span></span> 
- <span data-ttu-id="e5c57-2774">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="e5c57-2774">社会保険のテンキー</span></span> 
- <span data-ttu-id="e5c57-2775">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2775">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="e5c57-2776">Japanische Residenz Kartennummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2776">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2777">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2777">Format</span></span>

<span data-ttu-id="e5c57-2778">12 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2778">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2779">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2779">Pattern</span></span>

<span data-ttu-id="e5c57-2780">12 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2780">12 letters and digits:</span></span>
- <span data-ttu-id="e5c57-2781">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2781">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="e5c57-2782">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2782">Eight digits</span></span> 
- <span data-ttu-id="e5c57-2783">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2783">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2784">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2784">Checksum</span></span>

<span data-ttu-id="e5c57-2785">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2785">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2786">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2786">Definition</span></span>

<span data-ttu-id="e5c57-2787">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2787">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2788">Der reguläre Ausdruck Regex_jp_residence_card_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2788">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2789">Ein Schlüsselwort aus Keyword_jp_residence_card_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2789">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2790">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2790">Keywords</span></span>

#### <a name="keyword_jp_residence_card_number"></a><span data-ttu-id="e5c57-2791">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2791">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="e5c57-2792">Wohnsitz Kartennummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2792">Residence card number</span></span>
- <span data-ttu-id="e5c57-2793">Residenzkarte Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2793">Residence card no</span></span>
- <span data-ttu-id="e5c57-2794">Aufenthaltskarte #</span><span class="sxs-lookup"><span data-stu-id="e5c57-2794">Residence card #</span></span>
- <span data-ttu-id="e5c57-2795">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-2795">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="e5c57-2796">Malaysia -ID-Kartennummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2796">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2797">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2797">Format</span></span>

<span data-ttu-id="e5c57-2798">12 Ziffern mit optionalen Bindestrichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-2798">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2799">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2799">Pattern</span></span>

<span data-ttu-id="e5c57-2800">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2800">12 digits:</span></span>
- <span data-ttu-id="e5c57-2801">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="e5c57-2801">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="e5c57-2802">Ein Bindestrich (optional) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2802">A dash (optional)</span></span> 
- <span data-ttu-id="e5c57-2803">Zwei Buchstaben als Code für den Geburtsort </span><span class="sxs-lookup"><span data-stu-id="e5c57-2803">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="e5c57-2804">Ein Bindestrich (optional) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2804">A dash (optional)</span></span> 
- <span data-ttu-id="e5c57-2805">Drei beliebige Ziffern </span><span class="sxs-lookup"><span data-stu-id="e5c57-2805">Three random digits</span></span> 
- <span data-ttu-id="e5c57-2806">Einstelliger Code für das Geschlecht</span><span class="sxs-lookup"><span data-stu-id="e5c57-2806">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2807">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2807">Checksum</span></span>

<span data-ttu-id="e5c57-2808">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2808">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2809">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2809">Definition</span></span>

<span data-ttu-id="e5c57-2810">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2810">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2811">Der reguläre Ausdruck Regex_malaysia_id_card_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2811">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2812">Ein Schlüsselwort aus Keyword_malaysia_id_card_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2812">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2813">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2813">Keywords</span></span>
   
#### <a name="keyword_malaysia_id_card_number"></a><span data-ttu-id="e5c57-2814">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2814">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="e5c57-2815">digitale Anwendungs Karte</span><span class="sxs-lookup"><span data-stu-id="e5c57-2815">digital application card</span></span>
- <span data-ttu-id="e5c57-2816">i/c</span><span class="sxs-lookup"><span data-stu-id="e5c57-2816">i/c</span></span>
- <span data-ttu-id="e5c57-2817">i/c Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2817">i/c no</span></span>
- <span data-ttu-id="e5c57-2818">IK</span><span class="sxs-lookup"><span data-stu-id="e5c57-2818">ic</span></span>
- <span data-ttu-id="e5c57-2819">IC Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2819">ic no</span></span>
- <span data-ttu-id="e5c57-2820">id card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2820">id card</span></span>
- <span data-ttu-id="e5c57-2821">Ausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-2821">identification Card</span></span>
- <span data-ttu-id="e5c57-2822">identity card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2822">identity card</span></span>
- <span data-ttu-id="e5c57-2823">k/p</span><span class="sxs-lookup"><span data-stu-id="e5c57-2823">k/p</span></span>
- <span data-ttu-id="e5c57-2824">k/p Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2824">k/p no</span></span>
- <span data-ttu-id="e5c57-2825">Kad akuan Diri</span><span class="sxs-lookup"><span data-stu-id="e5c57-2825">kad akuan diri</span></span>
- <span data-ttu-id="e5c57-2826">Kad aplikasi Digital</span><span class="sxs-lookup"><span data-stu-id="e5c57-2826">kad aplikasi digital</span></span>
- <span data-ttu-id="e5c57-2827">Kad Einführung in Malaysia</span><span class="sxs-lookup"><span data-stu-id="e5c57-2827">kad pengenalan malaysia</span></span>
- <span data-ttu-id="e5c57-2828">KP</span><span class="sxs-lookup"><span data-stu-id="e5c57-2828">kp</span></span>
- <span data-ttu-id="e5c57-2829">KP Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2829">kp no</span></span>
- <span data-ttu-id="e5c57-2830">MyKAD</span><span class="sxs-lookup"><span data-stu-id="e5c57-2830">mykad</span></span>
- <span data-ttu-id="e5c57-2831">mykas</span><span class="sxs-lookup"><span data-stu-id="e5c57-2831">mykas</span></span>
- <span data-ttu-id="e5c57-2832">mykid</span><span class="sxs-lookup"><span data-stu-id="e5c57-2832">mykid</span></span>
- <span data-ttu-id="e5c57-2833">mypr</span><span class="sxs-lookup"><span data-stu-id="e5c57-2833">mypr</span></span>
- <span data-ttu-id="e5c57-2834">mytentera</span><span class="sxs-lookup"><span data-stu-id="e5c57-2834">mytentera</span></span>
- <span data-ttu-id="e5c57-2835">Malaysia-Personalausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-2835">malaysia identity card</span></span>
- <span data-ttu-id="e5c57-2836">malaysischer Personalausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-2836">malaysian identity card</span></span>
- <span data-ttu-id="e5c57-2837">NRIC</span><span class="sxs-lookup"><span data-stu-id="e5c57-2837">nric</span></span>
- <span data-ttu-id="e5c57-2838">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-2838">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="e5c57-2839">Niederlande – Bürgerdienstnummer (BSN)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2839">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2840">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2840">Format</span></span>

<span data-ttu-id="e5c57-2841">8-9 Ziffern mit optionalen Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-2841">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2842">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2842">Pattern</span></span>

<span data-ttu-id="e5c57-2843">8-9 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2843">8-9 digits:</span></span>
- <span data-ttu-id="e5c57-2844">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2844">Three digits</span></span> 
- <span data-ttu-id="e5c57-2845">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2845">A space (optional)</span></span> 
- <span data-ttu-id="e5c57-2846">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2846">Three digits</span></span> 
- <span data-ttu-id="e5c57-2847">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="e5c57-2847">A space (optional)</span></span> 
- <span data-ttu-id="e5c57-2848">2-3 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2848">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2849">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2849">Checksum</span></span>

<span data-ttu-id="e5c57-2850">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2850">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2851">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2851">Definition</span></span>

<span data-ttu-id="e5c57-2852">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2852">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2853">Die Funktion Func_netherlands_bsn findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2853">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2854">Ein Schlüsselwort aus Keyword_netherlands_bsn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2854">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="e5c57-2855">Die Funktion Func_eu_date2 sucht ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2855">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="e5c57-2856">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2856">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2857">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2857">Keywords</span></span>

#### <a name="keyword_netherlands_bsn"></a><span data-ttu-id="e5c57-2858">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="e5c57-2858">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="e5c57-2859">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2859">Citizen service number</span></span> 
- <span data-ttu-id="e5c57-2860">BSN</span><span class="sxs-lookup"><span data-stu-id="e5c57-2860">BSN</span></span> 
- <span data-ttu-id="e5c57-2861">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2861">Burgerservicenummer</span></span> 
- <span data-ttu-id="e5c57-2862">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2862">Sofinummer</span></span> 
- <span data-ttu-id="e5c57-2863">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2863">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="e5c57-2864">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2864">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="e5c57-2865">Neuseeländische Gesundheitsministeriumsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2865">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2866">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2866">Format</span></span>

<span data-ttu-id="e5c57-2867">Drei Buchstaben, ein Leerzeichen (optional) und vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2867">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2868">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2868">Pattern</span></span>

<span data-ttu-id="e5c57-2869">Drei Buchstaben (Groß-/Kleinschreibung nicht beachtet) ein Leerzeichen (optional) vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2869">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2870">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2870">Checksum</span></span>

<span data-ttu-id="e5c57-2871">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2871">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2872">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2872">Definition</span></span>

<span data-ttu-id="e5c57-2873">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2873">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2874">Die Funktion Func_new_zealand_ministry_of_health_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2874">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2875">Ein Schlüsselwort aus Keyword_nz_terms wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2875">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="e5c57-2876">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2876">The checksum passes.</span></span>

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

<span data-ttu-id="e5c57-2877">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2877">Keywords</span></span>

<span data-ttu-id="e5c57-2878">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="e5c57-2878">Keyword_nz_terms</span></span>

- <span data-ttu-id="e5c57-2879">Nhi</span><span class="sxs-lookup"><span data-stu-id="e5c57-2879">NHI</span></span> 
- <span data-ttu-id="e5c57-2880">New Zealand</span><span class="sxs-lookup"><span data-stu-id="e5c57-2880">New Zealand</span></span> 
- <span data-ttu-id="e5c57-2881">Health</span><span class="sxs-lookup"><span data-stu-id="e5c57-2881">Health</span></span> 
- <span data-ttu-id="e5c57-2882">Behandlung</span><span class="sxs-lookup"><span data-stu-id="e5c57-2882">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="e5c57-2883">Norwegen – Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2883">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2884">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2884">Format</span></span>

<span data-ttu-id="e5c57-2885">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2885">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2886">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2886">Pattern</span></span>

<span data-ttu-id="e5c57-2887">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2887">11 digits:</span></span>
- <span data-ttu-id="e5c57-2888">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="e5c57-2888">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="e5c57-2889">Dreistellige individuelle Zahl </span><span class="sxs-lookup"><span data-stu-id="e5c57-2889">Three-digit individual number</span></span> 
- <span data-ttu-id="e5c57-2890">Zwei Prüfziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2890">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2891">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2891">Checksum</span></span>

<span data-ttu-id="e5c57-2892">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2892">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2893">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2893">Definition</span></span>

<span data-ttu-id="e5c57-2894">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2894">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2895">Die Funktion Func_norway_id_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2895">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2896">Ein Schlüsselwort aus Keyword_norway_id_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2896">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="e5c57-2897">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2897">The checksum passes.</span></span>
- <span data-ttu-id="e5c57-2898">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2898">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2899">Die Funktion Func_norway_id_numbe findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2899">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2900">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2900">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2901">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2901">Keywords</span></span>

#### <a name="keyword_norway_id_number"></a><span data-ttu-id="e5c57-2902">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2902">Keyword_norway_id_number</span></span>

- <span data-ttu-id="e5c57-2903">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2903">Personal identification number</span></span>
- <span data-ttu-id="e5c57-2904">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2904">Norwegian ID Number</span></span>
- <span data-ttu-id="e5c57-2905">ID Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2905">ID Number</span></span>
- <span data-ttu-id="e5c57-2906">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="e5c57-2906">Identification</span></span>
- <span data-ttu-id="e5c57-2907">Personnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2907">Personnummer</span></span>
- <span data-ttu-id="e5c57-2908">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2908">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="e5c57-2909">Philippinen – Vereinheitlichte Mehrzweck-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2909">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2910">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2910">Format</span></span>

<span data-ttu-id="e5c57-2911">12 Ziffern, durch Bindestriche getrennt</span><span class="sxs-lookup"><span data-stu-id="e5c57-2911">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2912">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2912">Pattern</span></span>

<span data-ttu-id="e5c57-2913">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2913">12 digits:</span></span>
- <span data-ttu-id="e5c57-2914">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2914">Four digits</span></span> 
- <span data-ttu-id="e5c57-2915">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-2915">A hyphen</span></span> 
- <span data-ttu-id="e5c57-2916">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="e5c57-2916">Seven digits</span></span> 
- <span data-ttu-id="e5c57-2917">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-2917">A hyphen</span></span> 
- <span data-ttu-id="e5c57-2918">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2918">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2919">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2919">Checksum</span></span>

<span data-ttu-id="e5c57-2920">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2920">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2921">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2921">Definition</span></span>

<span data-ttu-id="e5c57-2922">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2922">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2923">Der reguläre Ausdruck Regex_philippines_unified_id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2923">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2924">Ein Schlüsselwort aus Keyword_philippines_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2924">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2925">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2925">Keywords</span></span>
   
#### <a name="keyword_philippines_id"></a><span data-ttu-id="e5c57-2926">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="e5c57-2926">Keyword_philippines_id</span></span>

- <span data-ttu-id="e5c57-2927">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-2927">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="e5c57-2928">Umid</span><span class="sxs-lookup"><span data-stu-id="e5c57-2928">UMID</span></span> 
- <span data-ttu-id="e5c57-2929">Identity Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2929">Identity Card</span></span> 
- <span data-ttu-id="e5c57-2930">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-2930">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="e5c57-2931">Polen Personalausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-2931">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2932">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2932">Format</span></span>

<span data-ttu-id="e5c57-2933">Drei Buchstaben und sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2933">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2934">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2934">Pattern</span></span>

<span data-ttu-id="e5c57-2935">Drei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2935">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2936">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2936">Checksum</span></span>

<span data-ttu-id="e5c57-2937">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2937">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2938">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2938">Definition</span></span>

<span data-ttu-id="e5c57-2939">Eine DLP-Richtlinie ist 75% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: die Funktion Func_polish_national_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2939">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="e5c57-2940">Ein Schlüsselwort aus Keyword_polish_national_id_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2940">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="e5c57-2941">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2941">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2942">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2942">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="e5c57-2943">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2943">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="e5c57-2944">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="e5c57-2944">Dowód osobisty</span></span>
- <span data-ttu-id="e5c57-2945">Numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="e5c57-2945">Numer dowodu osobistego</span></span>
- <span data-ttu-id="e5c57-2946">Nazwa i Numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="e5c57-2946">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="e5c57-2947">Nazwa i Nr dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="e5c57-2947">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="e5c57-2948">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="e5c57-2948">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="e5c57-2949">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="e5c57-2949">Dowód Tożsamości</span></span>
- <span data-ttu-id="e5c57-2950">Dow.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2950">dow.</span></span> <span data-ttu-id="e5c57-2951">OS.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2951">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="e5c57-2952">Polnische ID-Karte (PESEL)</span><span class="sxs-lookup"><span data-stu-id="e5c57-2952">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2953">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2953">Format</span></span>

<span data-ttu-id="e5c57-2954">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2954">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2955">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2955">Pattern</span></span>

<span data-ttu-id="e5c57-2956">11 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2956">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2957">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2957">Checksum</span></span>

<span data-ttu-id="e5c57-2958">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2958">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2959">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2959">Definition</span></span>

<span data-ttu-id="e5c57-2960">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2960">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2961">Die Funktion Func_pesel_identification_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2961">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2962">Ein Schlüsselwort aus Keyword_pesel_identification_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2962">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="e5c57-2963">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2963">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2964">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2964">Keywords</span></span>

#### <a name="keyword_pesel_identification_number"></a><span data-ttu-id="e5c57-2965">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2965">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="e5c57-2966">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="e5c57-2966">Nr PESEL</span></span>
- <span data-ttu-id="e5c57-2967">PESEL</span><span class="sxs-lookup"><span data-stu-id="e5c57-2967">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="e5c57-2968">Polen Reisepass</span><span class="sxs-lookup"><span data-stu-id="e5c57-2968">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2969">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2969">Format</span></span>

<span data-ttu-id="e5c57-2970">Zwei Buchstaben und sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2970">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2971">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2971">Pattern</span></span>

<span data-ttu-id="e5c57-2972">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2972">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2973">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2973">Checksum</span></span>

<span data-ttu-id="e5c57-2974">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-2974">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2975">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2975">Definition</span></span>

<span data-ttu-id="e5c57-2976">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2976">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2977">Die Funktion Func_polish_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2977">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2978">Ein Schlüsselwort aus Keyword_polish_national_id_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2978">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="e5c57-2979">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2979">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-2980">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2980">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="e5c57-2981">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-2981">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="e5c57-2982">Numer paszportu</span><span class="sxs-lookup"><span data-stu-id="e5c57-2982">Numer paszportu</span></span>
- <span data-ttu-id="e5c57-2983">Nr.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2983">Nr.</span></span> <span data-ttu-id="e5c57-2984">Paszportu</span><span class="sxs-lookup"><span data-stu-id="e5c57-2984">Paszportu</span></span>
- <span data-ttu-id="e5c57-2985">Paszport</span><span class="sxs-lookup"><span data-stu-id="e5c57-2985">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="e5c57-2986">Portugal – Bürgerkartennummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-2986">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-2987">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-2987">Format</span></span>

<span data-ttu-id="e5c57-2988">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2988">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-2989">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-2989">Pattern</span></span>

<span data-ttu-id="e5c57-2990">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-2990">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-2991">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-2991">Checksum</span></span>

<span data-ttu-id="e5c57-2992">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-2992">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-2993">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-2993">Definition</span></span>

<span data-ttu-id="e5c57-2994">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-2994">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-2995">Der reguläre Ausdruck Regex_portugal_citizen_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2995">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-2996">Ein Schlüsselwort aus Keyword_portugal_citizen_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-2996">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-2997">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-2997">Keywords</span></span>

#### <a name="keyword_portugal_citizen_card"></a><span data-ttu-id="e5c57-2998">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2998">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="e5c57-2999">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-2999">Citizen Card</span></span>
- <span data-ttu-id="e5c57-3000">National ID Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-3000">National ID Card</span></span>
- <span data-ttu-id="e5c57-3001">CC</span><span class="sxs-lookup"><span data-stu-id="e5c57-3001">CC</span></span>
- <span data-ttu-id="e5c57-3002">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="e5c57-3002">Cartão de Cidadão</span></span>
- <span data-ttu-id="e5c57-3003">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="e5c57-3003">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="e5c57-3004">Saudi-Arabische Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3004">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3005">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3005">Format</span></span>

<span data-ttu-id="e5c57-3006">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3006">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3007">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3007">Pattern</span></span>

<span data-ttu-id="e5c57-3008">10 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3008">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3009">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3009">Checksum</span></span>

<span data-ttu-id="e5c57-3010">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3010">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3011">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3011">Definition</span></span>

<span data-ttu-id="e5c57-3012">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3012">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3013">Der reguläre Ausdruck Regex_saudi_arabia_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3013">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3014">Ein Schlüsselwort aus Keyword_saudi_arabia_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3014">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3015">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3015">Keywords</span></span>

#### <a name="keyword_saudi_arabia_national_id"></a><span data-ttu-id="e5c57-3016">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="e5c57-3016">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="e5c57-3017">Identification Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-3017">Identification Card</span></span> 
- <span data-ttu-id="e5c57-3018">I card number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3018">I card number</span></span> 
- <span data-ttu-id="e5c57-3019">ID number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3019">ID number</span></span> 
- <span data-ttu-id="e5c57-3020">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="e5c57-3020">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="e5c57-3021">Singapur – National Registration Identity Card-Nummer (NRIC)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3021">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3022">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3022">Format</span></span>

<span data-ttu-id="e5c57-3023">Neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3023">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3024">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3024">Pattern</span></span>

- <span data-ttu-id="e5c57-3025">Neun Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3025">Nine letters and digits:</span></span>
- <span data-ttu-id="e5c57-3026">Die Buchstaben "F", "G", "S" oder "T" (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="e5c57-3026">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-3027">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="e5c57-3027">Seven digits</span></span> 
- <span data-ttu-id="e5c57-3028">Eine alphabetische Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3028">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3029">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3029">Checksum</span></span>

<span data-ttu-id="e5c57-3030">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-3030">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3031">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3031">Definition</span></span>

<span data-ttu-id="e5c57-3032">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3032">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3033">Der reguläre Ausdruck Regex_singapore_nric sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3033">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3034">Ein Schlüsselwort aus Keyword_singapore_nric wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3034">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="e5c57-3035">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3035">The checksum passes.</span></span>

<span data-ttu-id="e5c57-3036">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3036">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3037">Der reguläre Ausdruck Regex_singapore_nric sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3037">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3038">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3038">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3039">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3039">Keywords</span></span>
   
#### <a name="keyword_singapore_nric"></a><span data-ttu-id="e5c57-3040">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="e5c57-3040">Keyword_singapore_nric</span></span>

- <span data-ttu-id="e5c57-3041">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-3041">National Registration Identity Card</span></span> 
- <span data-ttu-id="e5c57-3042">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3042">Identity Card Number</span></span> 
- <span data-ttu-id="e5c57-3043">NRIC</span><span class="sxs-lookup"><span data-stu-id="e5c57-3043">NRIC</span></span> 
- <span data-ttu-id="e5c57-3044">IK</span><span class="sxs-lookup"><span data-stu-id="e5c57-3044">IC</span></span> 
- <span data-ttu-id="e5c57-3045">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3045">Foreign Identification Number</span></span> 
- <span data-ttu-id="e5c57-3046">FIN</span><span class="sxs-lookup"><span data-stu-id="e5c57-3046">FIN</span></span> 
- <span data-ttu-id="e5c57-3047">身份证</span><span class="sxs-lookup"><span data-stu-id="e5c57-3047">身份证</span></span> 
- <span data-ttu-id="e5c57-3048">身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-3048">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="e5c57-3049">Südafrika – Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3049">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3050">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3050">Format</span></span>

<span data-ttu-id="e5c57-3051">13 Ziffern, die Leerzeichen enthalten können</span><span class="sxs-lookup"><span data-stu-id="e5c57-3051">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3052">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3052">Pattern</span></span>

<span data-ttu-id="e5c57-3053">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3053">13 digits:</span></span>
- <span data-ttu-id="e5c57-3054">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="e5c57-3054">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="e5c57-3055">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3055">Four digits</span></span> 
- <span data-ttu-id="e5c57-3056">Ein einstelliger Citizenship-Indikator </span><span class="sxs-lookup"><span data-stu-id="e5c57-3056">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="e5c57-3057">Die Ziffer "8" oder "9" </span><span class="sxs-lookup"><span data-stu-id="e5c57-3057">The digit "8" or "9"</span></span> 
- <span data-ttu-id="e5c57-3058">Eine Ziffer als Prüfsummenziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3058">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3059">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3059">Checksum</span></span>

<span data-ttu-id="e5c57-3060">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3061">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3061">Definition</span></span>

<span data-ttu-id="e5c57-3062">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3063">Die Funktion Func_south_africa_identification_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3063">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3064">Ein Schlüsselwort aus Keyword_south_africa_identification_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3064">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="e5c57-3065">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3065">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-3066">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3066">Keywords</span></span>
   
#### <a name="keyword_south_africa_identification_number"></a><span data-ttu-id="e5c57-3067">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3067">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="e5c57-3068">Identity card</span><span class="sxs-lookup"><span data-stu-id="e5c57-3068">Identity card</span></span>
- <span data-ttu-id="e5c57-3069">ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-3069">ID</span></span>
- <span data-ttu-id="e5c57-3070">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="e5c57-3070">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="e5c57-3071">Südkorea – Einwohnerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3071">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3072">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3072">Format</span></span>

<span data-ttu-id="e5c57-3073">13 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="e5c57-3073">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3074">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3074">Pattern</span></span>

<span data-ttu-id="e5c57-3075">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3075">13 digits:</span></span>
- <span data-ttu-id="e5c57-3076">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="e5c57-3076">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="e5c57-3077">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e5c57-3077">A hyphen</span></span> 
- <span data-ttu-id="e5c57-3078">Eine Ziffer, die durch das Jahrhundert und das Geschlecht bestimmt wird </span><span class="sxs-lookup"><span data-stu-id="e5c57-3078">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="e5c57-3079">Vierstelliger Code für die Geburtsregion </span><span class="sxs-lookup"><span data-stu-id="e5c57-3079">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="e5c57-3080">Eine Ziffer, um Personen zu unterscheiden, für die die vorhergehenden Zahlen identisch sind </span><span class="sxs-lookup"><span data-stu-id="e5c57-3080">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="e5c57-3081">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3081">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3082">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3082">Checksum</span></span>

<span data-ttu-id="e5c57-3083">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-3083">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3084">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3084">Definition</span></span>

<span data-ttu-id="e5c57-3085">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3085">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3086">Die Funktion Func_south_korea_resident_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3086">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3087">Ein Schlüsselwort aus Keyword_south_korea_resident_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3087">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="e5c57-3088">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3088">The checksum passes.</span></span>

<span data-ttu-id="e5c57-3089">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3089">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3090">Die Funktion Func_south_korea_resident_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3090">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3091">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3091">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3092">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3092">Keywords</span></span>
   
#### <a name="keyword_south_korea_resident_number"></a><span data-ttu-id="e5c57-3093">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3093">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="e5c57-3094">National ID card</span><span class="sxs-lookup"><span data-stu-id="e5c57-3094">National ID card</span></span> 
- <span data-ttu-id="e5c57-3095">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3095">Citizen's Registration Number</span></span> 
- <span data-ttu-id="e5c57-3096">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="e5c57-3096">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="e5c57-3097">RRN</span><span class="sxs-lookup"><span data-stu-id="e5c57-3097">RRN</span></span> 
- <span data-ttu-id="e5c57-3098">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="e5c57-3098">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="e5c57-3099">Spanische Sozialversicherungsnummer (SSN)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3099">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3100">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3100">Format</span></span>

<span data-ttu-id="e5c57-3101">11-12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3101">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3102">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3102">Pattern</span></span>

<span data-ttu-id="e5c57-3103">11-12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3103">11-12 digits:</span></span>
- <span data-ttu-id="e5c57-3104">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3104">Two digits</span></span> 
- <span data-ttu-id="e5c57-3105">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3105">A forward slash (optional)</span></span> 
- <span data-ttu-id="e5c57-3106">7 bis 8 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3106">7-8 digits</span></span> 
- <span data-ttu-id="e5c57-3107">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3107">A forward slash (optional)</span></span> 
- <span data-ttu-id="e5c57-3108">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3108">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3109">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3109">Checksum</span></span>

<span data-ttu-id="e5c57-3110">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-3110">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3111">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3111">Definition</span></span>

<span data-ttu-id="e5c57-3112">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3112">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3113">Die Funktion Func_spanish_social_security_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3113">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3114">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3114">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-3115">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3115">Keywords</span></span>

<span data-ttu-id="e5c57-3116">Keine</span><span class="sxs-lookup"><span data-stu-id="e5c57-3116">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="e5c57-3117">SQL Server Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e5c57-3117">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3118">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3118">Format</span></span>

<span data-ttu-id="e5c57-3119">Die Zeichenfolge "Benutzer-ID", "Benutzer-ID", "UID" oder "UserID", gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten dargestellt sind.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3119">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3120">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3120">Pattern</span></span>

- <span data-ttu-id="e5c57-3121">Die Zeichenfolge "Benutzer-ID", "Benutzer-ID", "UID" oder "UserID"</span><span class="sxs-lookup"><span data-stu-id="e5c57-3121">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="e5c57-3122">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-3122">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="e5c57-3123">Die Zeichenfolge "Password" oder "pwd", wobei "pwd" kein Kleinbuchstabe vorangestellt ist</span><span class="sxs-lookup"><span data-stu-id="e5c57-3123">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="e5c57-3124">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3124">An equal sign (=)</span></span>
- <span data-ttu-id="e5c57-3125">Ein beliebiges Zeichen, das kein Dollarzeichen ($), Prozentzeichen (%), größer als das Symbol (#a0), Symbol (@), Anführungszeichen ("), Semikolon (;), linke geschweifte Klammer ([) oder linke Klammer ({) ist.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3125">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="e5c57-3126">Eine beliebige Kombination von 7-128 Zeichen, die kein Semikolon sind (;), Schrägstrich (/) oder Anführungszeichen (")</span><span class="sxs-lookup"><span data-stu-id="e5c57-3126">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="e5c57-3127">Ein Semikolon (;) oder Anführungszeichen (")</span><span class="sxs-lookup"><span data-stu-id="e5c57-3127">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3128">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3128">Checksum</span></span>

<span data-ttu-id="e5c57-3129">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3129">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3130">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3130">Definition</span></span>

<span data-ttu-id="e5c57-3131">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3131">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3132">Der reguläre Ausdruck CEP_Regex_SQLServerConnectionString sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3132">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3133">Ein Schlüsselwort aus CEP_GlobalFilter wurde **nicht** gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3133">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="e5c57-3134">Der reguläre Ausdruck CEP_PasswordPlaceHolder findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3134">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3135">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3135">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3136">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3136">Keywords</span></span>

#### <a name="cep_globalfilter"></a><span data-ttu-id="e5c57-3137">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3137">CEP_GlobalFilter</span></span>

- <span data-ttu-id="e5c57-3138">Einige-Kennwort</span><span class="sxs-lookup"><span data-stu-id="e5c57-3138">some-password</span></span>
- <span data-ttu-id="e5c57-3139">somepassword</span><span class="sxs-lookup"><span data-stu-id="e5c57-3139">somepassword</span></span>
- <span data-ttu-id="e5c57-3140">secretPassword</span><span class="sxs-lookup"><span data-stu-id="e5c57-3140">secretPassword</span></span>
- <span data-ttu-id="e5c57-3141">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e5c57-3141">sample</span></span>

#### <a name="cep_passwordplaceholder"></a><span data-ttu-id="e5c57-3142">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="e5c57-3142">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="e5c57-3143">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3143">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="e5c57-3144">Password oder PWD gefolgt von 0-2 Leerzeichen, ein Gleichheitszeichen (=), 0-2 Leerzeichen und ein Sternchen (\*)--oder--</span><span class="sxs-lookup"><span data-stu-id="e5c57-3144">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="e5c57-3145">Password oder PWD gefolgt von:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3145">Password or pwd followed by:</span></span>
    - <span data-ttu-id="e5c57-3146">Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3146">Equal sign (=)</span></span>
    - <span data-ttu-id="e5c57-3147">Kleiner als-Symbol (#a0)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3147">Less than symbol (<)</span></span>
    - <span data-ttu-id="e5c57-3148">Eine beliebige Kombination von 1-200 Zeichen mit groß-oder Kleinbuchstaben, Ziffern, einem Sternchen (\*), einem Bindestrich (-), einem Unterstrich (_) oder einem Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-3148">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="e5c57-3149">Größer als-Symbol (#a0)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3149">Greater than symbol (>)</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="e5c57-3150">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="e5c57-3150">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="e5c57-3151">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3151">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="e5c57-3152">contoso</span><span class="sxs-lookup"><span data-stu-id="e5c57-3152">contoso</span></span>
- <span data-ttu-id="e5c57-3153">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e5c57-3153">fabrikam</span></span>
- <span data-ttu-id="e5c57-3154">Northwind</span><span class="sxs-lookup"><span data-stu-id="e5c57-3154">northwind</span></span>
- <span data-ttu-id="e5c57-3155">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="e5c57-3155">sandbox</span></span>
- <span data-ttu-id="e5c57-3156">OneBox</span><span class="sxs-lookup"><span data-stu-id="e5c57-3156">onebox</span></span>
- <span data-ttu-id="e5c57-3157">localhost</span><span class="sxs-lookup"><span data-stu-id="e5c57-3157">localhost</span></span>
- <span data-ttu-id="e5c57-3158">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="e5c57-3158">127.0.0.1</span></span>
- <span data-ttu-id="e5c57-3159">testacs.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3159">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-3160">com</span><span class="sxs-lookup"><span data-stu-id="e5c57-3160">com</span></span>
- <span data-ttu-id="e5c57-3161">s-int.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3161">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="e5c57-3162">NET</span><span class="sxs-lookup"><span data-stu-id="e5c57-3162">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="e5c57-3163">Schwedische Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3163">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3164">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3164">Format</span></span>

<span data-ttu-id="e5c57-3165">10 oder 12 Ziffern und ein optionales Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-3165">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3166">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3166">Pattern</span></span>

<span data-ttu-id="e5c57-3167">10 oder 12 Ziffern und ein optionals Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3167">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="e5c57-3168">2 bis 4 Ziffern (optional)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3168">2-4 digits (optional)</span></span> 
- <span data-ttu-id="e5c57-3169">Sechs Ziffern im Datumsformat JJMMTT</span><span class="sxs-lookup"><span data-stu-id="e5c57-3169">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="e5c57-3170">Trennzeichen „-“ oder „+“ (optional) und</span><span class="sxs-lookup"><span data-stu-id="e5c57-3170">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="e5c57-3171">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3171">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3172">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3172">Checksum</span></span>

<span data-ttu-id="e5c57-3173">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-3173">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3174">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3174">Definition</span></span>

<span data-ttu-id="e5c57-3175">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3175">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3176">Die Funktion Func_swedish_national_identifier findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3176">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3177">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3177">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-3178">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3178">Keywords</span></span>

<span data-ttu-id="e5c57-3179">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3179">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="e5c57-3180">Schwedische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3180">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3181">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3181">Format</span></span>

<span data-ttu-id="e5c57-3182">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3182">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3183">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3183">Pattern</span></span>

<span data-ttu-id="e5c57-3184">Acht aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3184">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3185">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3185">Checksum</span></span>

<span data-ttu-id="e5c57-3186">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3186">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3187">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3187">Definition</span></span>

<span data-ttu-id="e5c57-3188">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3188">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3189">Der reguläre Ausdruck Regex_sweden_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3189">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3190">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3190">One of the following is true:</span></span>
    - <span data-ttu-id="e5c57-3191">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3191">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="e5c57-3192">Ein Schlüsselwort aus Keyword_sweden_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3192">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3193">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3193">Keywords</span></span>
   
#### <a name="keyword_sweden_passport"></a><span data-ttu-id="e5c57-3194">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="e5c57-3194">Keyword_sweden_passport</span></span>

- <span data-ttu-id="e5c57-3195">visa requirements</span><span class="sxs-lookup"><span data-stu-id="e5c57-3195">visa requirements</span></span> 
- <span data-ttu-id="e5c57-3196">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="e5c57-3196">Alien Registration Card</span></span> 
- <span data-ttu-id="e5c57-3197">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="e5c57-3197">Schengen visas</span></span> 
- <span data-ttu-id="e5c57-3198">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="e5c57-3198">Schengen visa</span></span> 
- <span data-ttu-id="e5c57-3199">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="e5c57-3199">Visa Processing</span></span> 
- <span data-ttu-id="e5c57-3200">Visa Type</span><span class="sxs-lookup"><span data-stu-id="e5c57-3200">Visa Type</span></span> 
- <span data-ttu-id="e5c57-3201">Single Entry</span><span class="sxs-lookup"><span data-stu-id="e5c57-3201">Single Entry</span></span> 
- <span data-ttu-id="e5c57-3202">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="e5c57-3202">Multiple Entry</span></span> 
- <span data-ttu-id="e5c57-3203">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="e5c57-3203">G3 Processing Fees</span></span> 

#### <a name="keyword_passport"></a><span data-ttu-id="e5c57-3204">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="e5c57-3204">Keyword_passport</span></span>

- <span data-ttu-id="e5c57-3205">Passport Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3205">Passport Number</span></span> 
- <span data-ttu-id="e5c57-3206">Passport No</span><span class="sxs-lookup"><span data-stu-id="e5c57-3206">Passport No</span></span> 
- <span data-ttu-id="e5c57-3207">Passport#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3207">Passport #</span></span> 
- <span data-ttu-id="e5c57-3208">Pass #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3208">Passport#</span></span> 
- <span data-ttu-id="e5c57-3209">Passport-Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-3209">PassportID</span></span> 
- <span data-ttu-id="e5c57-3210">Passportno</span><span class="sxs-lookup"><span data-stu-id="e5c57-3210">Passportno</span></span> 
- <span data-ttu-id="e5c57-3211">passportnumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-3211">passportnumber</span></span> 
- <span data-ttu-id="e5c57-3212">パスポート</span><span class="sxs-lookup"><span data-stu-id="e5c57-3212">パスポート</span></span> 
- <span data-ttu-id="e5c57-3213">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-3213">パスポート番号</span></span> 
- <span data-ttu-id="e5c57-3214">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="e5c57-3214">パスポートのNum</span></span> 
- <span data-ttu-id="e5c57-3215">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-3215">パスポート＃</span></span> 
- <span data-ttu-id="e5c57-3216">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="e5c57-3216">Numéro de passeport</span></span> 
- <span data-ttu-id="e5c57-3217">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="e5c57-3217">Passeport n °</span></span> 
- <span data-ttu-id="e5c57-3218">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="e5c57-3218">Passeport Non</span></span> 
- <span data-ttu-id="e5c57-3219">Passeport#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3219">Passeport #</span></span> 
- <span data-ttu-id="e5c57-3220">Passeport #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3220">Passeport#</span></span> 
- <span data-ttu-id="e5c57-3221">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="e5c57-3221">PasseportNon</span></span> 
- <span data-ttu-id="e5c57-3222">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="e5c57-3222">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="e5c57-3223">SWIFT-Code</span><span class="sxs-lookup"><span data-stu-id="e5c57-3223">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3224">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3224">Format</span></span>

<span data-ttu-id="e5c57-3225">Vier Buchstaben, gefolgt von 5-31 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3225">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3226">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3226">Pattern</span></span>

<span data-ttu-id="e5c57-3227">Vier Buchstaben, gefolgt von 5 bis 31 Buchstaben oder Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3227">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="e5c57-3228">Vier Buchstaben für den Bankcode (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3228">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-3229">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-3229">An optional space</span></span> 
- <span data-ttu-id="e5c57-3230">4 bis 28 Buchstaben oder Ziffern (BBAN, Basic Bank Account Number)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3230">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="e5c57-3231">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-3231">An optional space</span></span> 
- <span data-ttu-id="e5c57-3232">1 bis 3 Buchstaben oder Ziffern (Rest des BBAN)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3232">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3233">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3233">Checksum</span></span>

<span data-ttu-id="e5c57-3234">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3234">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3235">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3235">Definition</span></span>

<span data-ttu-id="e5c57-3236">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3236">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3237">Der reguläre Ausdruck Regex_swift findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3237">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3238">Ein Schlüsselwort aus Keyword_swift wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3238">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-3239">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3239">Keywords</span></span>
   
#### <a name="keyword_swift"></a><span data-ttu-id="e5c57-3240">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="e5c57-3240">Keyword_swift</span></span>

- <span data-ttu-id="e5c57-3241">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="e5c57-3241">international organization for standardization 9362</span></span> 
- <span data-ttu-id="e5c57-3242">iso 9362</span><span class="sxs-lookup"><span data-stu-id="e5c57-3242">iso 9362</span></span> 
- <span data-ttu-id="e5c57-3243">iso9362</span><span class="sxs-lookup"><span data-stu-id="e5c57-3243">iso9362</span></span> 
- <span data-ttu-id="e5c57-3244">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3244">swift\#</span></span> 
- <span data-ttu-id="e5c57-3245">Swiftcode</span><span class="sxs-lookup"><span data-stu-id="e5c57-3245">swiftcode</span></span> 
- <span data-ttu-id="e5c57-3246">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-3246">swiftnumber</span></span> 
- <span data-ttu-id="e5c57-3247">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-3247">swiftroutingnumber</span></span> 
- <span data-ttu-id="e5c57-3248">swift code</span><span class="sxs-lookup"><span data-stu-id="e5c57-3248">swift code</span></span> 
- <span data-ttu-id="e5c57-3249">swift number #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3249">swift number #</span></span> 
- <span data-ttu-id="e5c57-3250">swift routing number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3250">swift routing number</span></span> 
- <span data-ttu-id="e5c57-3251">bic number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3251">bic number</span></span> 
- <span data-ttu-id="e5c57-3252">bic code</span><span class="sxs-lookup"><span data-stu-id="e5c57-3252">bic code</span></span> 
- <span data-ttu-id="e5c57-3253">BIC\#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3253">bic \#</span></span> 
- <span data-ttu-id="e5c57-3254">BIC\#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3254">bic\#</span></span> 
- <span data-ttu-id="e5c57-3255">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="e5c57-3255">bank identifier code</span></span> 
- <span data-ttu-id="e5c57-3256">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="e5c57-3256">標準化9362</span></span> 
- <span data-ttu-id="e5c57-3257">迅速＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-3257">迅速＃</span></span> 
- <span data-ttu-id="e5c57-3258">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="e5c57-3258">SWIFTコード</span></span> 
- <span data-ttu-id="e5c57-3259">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-3259">SWIFT番号</span></span> 
- <span data-ttu-id="e5c57-3260">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-3260">迅速なルーティング番号</span></span> 
- <span data-ttu-id="e5c57-3261">BIC番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-3261">BIC番号</span></span> 
- <span data-ttu-id="e5c57-3262">BICコード</span><span class="sxs-lookup"><span data-stu-id="e5c57-3262">BICコード</span></span> 
- <span data-ttu-id="e5c57-3263">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="e5c57-3263">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="e5c57-3264">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="e5c57-3264">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="e5c57-3265">rapide\#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3265">rapide \#</span></span> 
- <span data-ttu-id="e5c57-3266">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="e5c57-3266">code SWIFT</span></span> 
- <span data-ttu-id="e5c57-3267">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="e5c57-3267">le numéro de swift</span></span> 
- <span data-ttu-id="e5c57-3268">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="e5c57-3268">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="e5c57-3269">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="e5c57-3269">le numéro BIC</span></span> 
- <span data-ttu-id="e5c57-3270">\#BIC</span><span class="sxs-lookup"><span data-stu-id="e5c57-3270">\# BIC</span></span> 
- <span data-ttu-id="e5c57-3271">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="e5c57-3271">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="e5c57-3272">Taiwanesicher Personalausweis</span><span class="sxs-lookup"><span data-stu-id="e5c57-3272">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3273">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3273">Format</span></span>

<span data-ttu-id="e5c57-3274">Ein Buchstabe (auf Englisch) gefolgt von neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3274">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3275">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3275">Pattern</span></span>

<span data-ttu-id="e5c57-3276">Ein Buchstabe (Englisch), gefolgt von neun Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3276">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="e5c57-3277">Ein Buchstabe (Englisch, Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3277">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-3278">Die Ziffer 1 oder 2</span><span class="sxs-lookup"><span data-stu-id="e5c57-3278">The digit "1" or "2"</span></span> 
- <span data-ttu-id="e5c57-3279">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3279">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3280">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3280">Checksum</span></span>

<span data-ttu-id="e5c57-3281">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-3281">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3282">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3282">Definition</span></span>

<span data-ttu-id="e5c57-3283">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3283">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3284">Die Funktion Func_taiwanese_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3284">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3285">Ein Schlüsselwort aus Keyword_taiwanese_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3285">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="e5c57-3286">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3286">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-3287">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3287">Keywords</span></span>

#### <a name="keyword_taiwanese_national_id"></a><span data-ttu-id="e5c57-3288">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="e5c57-3288">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="e5c57-3289">身份證字號</span><span class="sxs-lookup"><span data-stu-id="e5c57-3289">身份證字號</span></span> 
- <span data-ttu-id="e5c57-3290">身份證</span><span class="sxs-lookup"><span data-stu-id="e5c57-3290">身份證</span></span> 
- <span data-ttu-id="e5c57-3291">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="e5c57-3291">身份證號碼</span></span> 
- <span data-ttu-id="e5c57-3292">身份證號</span><span class="sxs-lookup"><span data-stu-id="e5c57-3292">身份證號</span></span> 
- <span data-ttu-id="e5c57-3293">身分證字號</span><span class="sxs-lookup"><span data-stu-id="e5c57-3293">身分證字號</span></span> 
- <span data-ttu-id="e5c57-3294">身分證</span><span class="sxs-lookup"><span data-stu-id="e5c57-3294">身分證</span></span> 
- <span data-ttu-id="e5c57-3295">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="e5c57-3295">身分證號碼</span></span> 
- <span data-ttu-id="e5c57-3296">身份證號</span><span class="sxs-lookup"><span data-stu-id="e5c57-3296">身份證號</span></span> 
- <span data-ttu-id="e5c57-3297">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="e5c57-3297">身分證統一編號</span></span> 
- <span data-ttu-id="e5c57-3298">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="e5c57-3298">國民身分證統一編號</span></span> 
- <span data-ttu-id="e5c57-3299">簽名</span><span class="sxs-lookup"><span data-stu-id="e5c57-3299">簽名</span></span> 
- <span data-ttu-id="e5c57-3300">蓋章</span><span class="sxs-lookup"><span data-stu-id="e5c57-3300">蓋章</span></span> 
- <span data-ttu-id="e5c57-3301">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="e5c57-3301">簽名或蓋章</span></span> 
- <span data-ttu-id="e5c57-3302">簽章</span><span class="sxs-lookup"><span data-stu-id="e5c57-3302">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="e5c57-3303">	Taiwan – Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3303">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3304">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3304">Format</span></span>

- <span data-ttu-id="e5c57-3305">Biometrische Passport-Nummer: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3305">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="e5c57-3306">Nicht biometrische Passport-Nummer: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3306">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3307">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3307">Pattern</span></span>
<span data-ttu-id="e5c57-3308">Biometrische Passnummer:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3308">Biometric passport number:</span></span>
- <span data-ttu-id="e5c57-3309">Die Ziffer "3" </span><span class="sxs-lookup"><span data-stu-id="e5c57-3309">The digit "3"</span></span> 
- <span data-ttu-id="e5c57-3310">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3310">Eight digits</span></span>

<span data-ttu-id="e5c57-3311">Nicht biometrische Passnummer:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3311">Non-biometric passport number:</span></span>
- <span data-ttu-id="e5c57-3312">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3312">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3313">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3313">Checksum</span></span>

<span data-ttu-id="e5c57-3314">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3314">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3315">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3315">Definition</span></span>

<span data-ttu-id="e5c57-3316">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3316">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3317">Der reguläre Ausdruck Regex_taiwan_passport sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3317">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3318">Ein Schlüsselwort aus Keyword_taiwan_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3318">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-3319">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3319">Keywords</span></span>

#### <a name="keyword_taiwan_passport"></a><span data-ttu-id="e5c57-3320">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="e5c57-3320">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="e5c57-3321">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3321">ROC passport number</span></span> 
- <span data-ttu-id="e5c57-3322">Passport number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3322">Passport number</span></span> 
- <span data-ttu-id="e5c57-3323">Passport no</span><span class="sxs-lookup"><span data-stu-id="e5c57-3323">Passport no</span></span> 
- <span data-ttu-id="e5c57-3324">Passport Num</span><span class="sxs-lookup"><span data-stu-id="e5c57-3324">Passport Num</span></span> 
- <span data-ttu-id="e5c57-3325">Passport #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3325">Passport #</span></span> 
- <span data-ttu-id="e5c57-3326">护照</span><span class="sxs-lookup"><span data-stu-id="e5c57-3326">护照</span></span> 
- <span data-ttu-id="e5c57-3327">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="e5c57-3327">中華民國護照</span></span> 
- <span data-ttu-id="e5c57-3328">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="e5c57-3328">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="e5c57-3329">Taiwan – Einwohnerzertifikatsnummer (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3329">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3330">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3330">Format</span></span>

<span data-ttu-id="e5c57-3331">10 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3331">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3332">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3332">Pattern</span></span>

<span data-ttu-id="e5c57-3333">10 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3333">10 letters and digits:</span></span>
- <span data-ttu-id="e5c57-3334">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="e5c57-3334">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="e5c57-3335">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3335">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3336">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3336">Checksum</span></span>

<span data-ttu-id="e5c57-3337">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3337">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3338">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3338">Definition</span></span>

<span data-ttu-id="e5c57-3339">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3339">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3340">Der reguläre Ausdruck Regex_taiwan_resident_certificate sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3340">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3341">Ein Schlüsselwort aus Keyword_taiwan_resident_certificate wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3341">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-3342">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3342">Keywords</span></span>

#### <a name="keyword_taiwan_resident_certificate"></a><span data-ttu-id="e5c57-3343">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="e5c57-3343">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="e5c57-3344">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="e5c57-3344">Resident Certificate</span></span> 
- <span data-ttu-id="e5c57-3345">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="e5c57-3345">Resident Cert</span></span> 
- <span data-ttu-id="e5c57-3346">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3346">Resident Cert.</span></span> 
- <span data-ttu-id="e5c57-3347">Identification card</span><span class="sxs-lookup"><span data-stu-id="e5c57-3347">Identification card</span></span> 
- <span data-ttu-id="e5c57-3348">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="e5c57-3348">Alien Resident Certificate</span></span> 
- <span data-ttu-id="e5c57-3349">Bogens</span><span class="sxs-lookup"><span data-stu-id="e5c57-3349">ARC</span></span> 
- <span data-ttu-id="e5c57-3350">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="e5c57-3350">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="e5c57-3351">TARC</span><span class="sxs-lookup"><span data-stu-id="e5c57-3351">TARC</span></span> 
- <span data-ttu-id="e5c57-3352">居留證</span><span class="sxs-lookup"><span data-stu-id="e5c57-3352">居留證</span></span> 
- <span data-ttu-id="e5c57-3353">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="e5c57-3353">外僑居留證</span></span> 
- <span data-ttu-id="e5c57-3354">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="e5c57-3354">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="e5c57-3355">Thai-Populations Kennzeichnungs Code</span><span class="sxs-lookup"><span data-stu-id="e5c57-3355">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3356">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3356">Format</span></span>

<span data-ttu-id="e5c57-3357">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3357">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3358">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3358">Pattern</span></span>

<span data-ttu-id="e5c57-3359">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3359">13 digits:</span></span>
- <span data-ttu-id="e5c57-3360">Die erste Ziffer ist nicht 0 oder 9.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3360">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="e5c57-3361">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3361">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3362">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3362">Checksum</span></span>

<span data-ttu-id="e5c57-3363">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-3363">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3364">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3364">Definition</span></span>

<span data-ttu-id="e5c57-3365">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3365">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3366">Die Funktion Func_Thai_Citizen_Id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3366">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3367">Ein Schlüsselwort aus Keyword_Thai_Citizen_Id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3367">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="e5c57-3368">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3368">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3369">Die Funktion Func_Thai_Citizen_Id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3369">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3370">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3370">Keywords</span></span>

#### <a name="keyword_thai_citizen_id"></a><span data-ttu-id="e5c57-3371">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="e5c57-3371">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="e5c57-3372">ID Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3372">ID Number</span></span>
- <span data-ttu-id="e5c57-3373">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3373">Identification Number</span></span>
- <span data-ttu-id="e5c57-3374">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="e5c57-3374">บัตรประชาชน</span></span>
- <span data-ttu-id="e5c57-3375">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="e5c57-3375">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="e5c57-3376">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="e5c57-3376">บัตรประชาชน</span></span>
- <span data-ttu-id="e5c57-3377">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="e5c57-3377">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="e5c57-3378">Türkische nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3378">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3379">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3379">Format</span></span>

<span data-ttu-id="e5c57-3380">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3380">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3381">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3381">Pattern</span></span>

<span data-ttu-id="e5c57-3382">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3382">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3383">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3383">Checksum</span></span>

<span data-ttu-id="e5c57-3384">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-3384">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3385">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3385">Definition</span></span>

<span data-ttu-id="e5c57-3386">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3386">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3387">Die Funktion Func_Turkish_National_Id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3387">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3388">Ein Schlüsselwort aus Keyword_Turkish_National_Id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3388">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="e5c57-3389">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3389">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3390">Die Funktion Func_Turkish_National_Id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3390">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3391">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3391">Keywords</span></span>

#### <a name="keyword_turkish_national_id"></a><span data-ttu-id="e5c57-3392">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="e5c57-3392">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="e5c57-3393">TC KİMLİK Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3393">TC Kimlik No</span></span>
- <span data-ttu-id="e5c57-3394">TC KİMLİK numarası</span><span class="sxs-lookup"><span data-stu-id="e5c57-3394">TC Kimlik numarası</span></span>
- <span data-ttu-id="e5c57-3395">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="e5c57-3395">Vatandaşlık numarası</span></span>
- <span data-ttu-id="e5c57-3396">Vatandaşlık Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3396">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="e5c57-p142">Britische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-p142">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3399">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3399">Format</span></span>

<span data-ttu-id="e5c57-3400">Kombination aus 18 Buchstaben und Ziffern im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3400">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3401">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3401">Pattern</span></span>

<span data-ttu-id="e5c57-3402">18 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3402">18 letters and digits:</span></span>
- <span data-ttu-id="e5c57-3403">Fünf Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) oder die Ziffer 9 anstelle eines Buchstabens</span><span class="sxs-lookup"><span data-stu-id="e5c57-3403">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="e5c57-3404">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3404">One digit</span></span> 
- <span data-ttu-id="e5c57-3405">Fünf Ziffern im Datumsformat TTMMJ für das Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-3405">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="e5c57-3406">Zwei Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) oder die Ziffer 9 anstelle eines Buchstabens</span><span class="sxs-lookup"><span data-stu-id="e5c57-3406">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="e5c57-3407">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3407">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3408">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3408">Checksum</span></span>

<span data-ttu-id="e5c57-3409">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-3409">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3410">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3410">Definition</span></span>

<span data-ttu-id="e5c57-3411">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3412">Die Funktion Func_uk_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3412">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3413">Ein Schlüsselwort aus Keyword_uk_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3413">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="e5c57-3414">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3414">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-3415">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3415">Keywords</span></span>

#### <a name="keyword_uk_drivers_license"></a><span data-ttu-id="e5c57-3416">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="e5c57-3416">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="e5c57-3417">DVLA</span><span class="sxs-lookup"><span data-stu-id="e5c57-3417">DVLA</span></span> 
- <span data-ttu-id="e5c57-3418">light vans</span><span class="sxs-lookup"><span data-stu-id="e5c57-3418">light vans</span></span> 
- <span data-ttu-id="e5c57-3419">Quads entwickelt</span><span class="sxs-lookup"><span data-stu-id="e5c57-3419">quadbikes</span></span> 
- <span data-ttu-id="e5c57-3420">motor cars</span><span class="sxs-lookup"><span data-stu-id="e5c57-3420">motor cars</span></span> 
- <span data-ttu-id="e5c57-3421">125cc</span><span class="sxs-lookup"><span data-stu-id="e5c57-3421">125cc</span></span> 
- <span data-ttu-id="e5c57-3422">Beiwagen</span><span class="sxs-lookup"><span data-stu-id="e5c57-3422">sidecar</span></span> 
- <span data-ttu-id="e5c57-3423">Dreiräder</span><span class="sxs-lookup"><span data-stu-id="e5c57-3423">tricycles</span></span> 
- <span data-ttu-id="e5c57-3424">Motorrad</span><span class="sxs-lookup"><span data-stu-id="e5c57-3424">motorcycles</span></span> 
- <span data-ttu-id="e5c57-3425">photocard licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-3425">photocard licence</span></span> 
- <span data-ttu-id="e5c57-3426">learner drivers</span><span class="sxs-lookup"><span data-stu-id="e5c57-3426">learner drivers</span></span> 
- <span data-ttu-id="e5c57-3427">licence holder</span><span class="sxs-lookup"><span data-stu-id="e5c57-3427">licence holder</span></span> 
- <span data-ttu-id="e5c57-3428">licence holders</span><span class="sxs-lookup"><span data-stu-id="e5c57-3428">licence holders</span></span> 
- <span data-ttu-id="e5c57-3429">driving licences</span><span class="sxs-lookup"><span data-stu-id="e5c57-3429">driving licences</span></span> 
- <span data-ttu-id="e5c57-3430">driving licence</span><span class="sxs-lookup"><span data-stu-id="e5c57-3430">driving licence</span></span> 
- <span data-ttu-id="e5c57-3431">dual control car</span><span class="sxs-lookup"><span data-stu-id="e5c57-3431">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="e5c57-p143">Britische Wählerverzeichnisnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-p143">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3434">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3434">Format</span></span>

<span data-ttu-id="e5c57-3435">Zwei Buchstaben gefolgt von 1-4 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3435">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3436">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3436">Pattern</span></span>

<span data-ttu-id="e5c57-3437">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von 1-4 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3437">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3438">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3438">Checksum</span></span>

<span data-ttu-id="e5c57-3439">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3439">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3440">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3440">Definition</span></span>

<span data-ttu-id="e5c57-3441">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3441">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3442">Der reguläre Ausdruck Regex_uk_electoral findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3442">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3443">Ein Schlüsselwort aus Keyword_uk_electoral wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3443">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3444">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3444">Keywords</span></span>

#### <a name="keyword_uk_electoral"></a><span data-ttu-id="e5c57-3445">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="e5c57-3445">Keyword_uk_electoral</span></span>

- <span data-ttu-id="e5c57-3446">council nomination</span><span class="sxs-lookup"><span data-stu-id="e5c57-3446">council nomination</span></span> 
- <span data-ttu-id="e5c57-3447">nomination form</span><span class="sxs-lookup"><span data-stu-id="e5c57-3447">nomination form</span></span> 
- <span data-ttu-id="e5c57-3448">electoral register</span><span class="sxs-lookup"><span data-stu-id="e5c57-3448">electoral register</span></span> 
- <span data-ttu-id="e5c57-3449">electoral roll</span><span class="sxs-lookup"><span data-stu-id="e5c57-3449">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="e5c57-p144">Britische National Health Service-Nummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-p144">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3452">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3452">Format</span></span>

<span data-ttu-id="e5c57-3453">10-17 Ziffern, durch Leerzeichen getrennt</span><span class="sxs-lookup"><span data-stu-id="e5c57-3453">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3454">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3454">Pattern</span></span>

<span data-ttu-id="e5c57-3455">10 bis 17 Stellen:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3455">10-17 digits:</span></span>
- <span data-ttu-id="e5c57-3456">3 oder 10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3456">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="e5c57-3457">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-3457">A space</span></span> 
- <span data-ttu-id="e5c57-3458">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3458">Three digits</span></span> 
- <span data-ttu-id="e5c57-3459">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="e5c57-3459">A space</span></span> 
- <span data-ttu-id="e5c57-3460">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3460">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3461">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3461">Checksum</span></span>

<span data-ttu-id="e5c57-3462">Ja</span><span class="sxs-lookup"><span data-stu-id="e5c57-3462">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3463">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3463">Definition</span></span>

<span data-ttu-id="e5c57-3464">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3464">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3465">Die Funktion Func_uk_nhs_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3465">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3466">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3466">One of the following is true:</span></span>
    - <span data-ttu-id="e5c57-3467">Ein Schlüsselwort aus Keyword_uk_nhs_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3467">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="e5c57-3468">Ein Schlüsselwort aus Keyword_uk_nhs_number1 wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3468">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="e5c57-3469">Ein Schlüsselwort aus Keyword_uk_nhs_number_dob wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3469">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="e5c57-3470">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3470">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3471">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3471">Keywords</span></span>
   
#### <a name="keyword_uk_nhs_number"></a><span data-ttu-id="e5c57-3472">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3472">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="e5c57-3473">national health service</span><span class="sxs-lookup"><span data-stu-id="e5c57-3473">national health service</span></span> 
- <span data-ttu-id="e5c57-3474">NHS</span><span class="sxs-lookup"><span data-stu-id="e5c57-3474">nhs</span></span> 
- <span data-ttu-id="e5c57-3475">health services authority</span><span class="sxs-lookup"><span data-stu-id="e5c57-3475">health services authority</span></span> 
- <span data-ttu-id="e5c57-3476">health authority</span><span class="sxs-lookup"><span data-stu-id="e5c57-3476">health authority</span></span>

#### <a name="keyword_uk_nhs_number1"></a><span data-ttu-id="e5c57-3477">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="e5c57-3477">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="e5c57-3478">patient id</span><span class="sxs-lookup"><span data-stu-id="e5c57-3478">patient id</span></span> 
- <span data-ttu-id="e5c57-3479">patient identification</span><span class="sxs-lookup"><span data-stu-id="e5c57-3479">patient identification</span></span> 
- <span data-ttu-id="e5c57-3480">patient no</span><span class="sxs-lookup"><span data-stu-id="e5c57-3480">patient no</span></span> 
- <span data-ttu-id="e5c57-3481">patient number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3481">patient number</span></span>

#### <a name="keyword_uk_nhs_number_dob"></a><span data-ttu-id="e5c57-3482">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="e5c57-3482">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="e5c57-3483">GP</span><span class="sxs-lookup"><span data-stu-id="e5c57-3483">GP</span></span> 
- <span data-ttu-id="e5c57-3484">DOB</span><span class="sxs-lookup"><span data-stu-id="e5c57-3484">DOB</span></span> 
- <span data-ttu-id="e5c57-3485">D. O. B</span><span class="sxs-lookup"><span data-stu-id="e5c57-3485">D.O.B</span></span> 
- <span data-ttu-id="e5c57-3486">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="e5c57-3486">Date of Birth</span></span> 
- <span data-ttu-id="e5c57-3487">Birth Date</span><span class="sxs-lookup"><span data-stu-id="e5c57-3487">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="e5c57-p145">Britische nationale Versicherungsnummer (NINO)</span><span class="sxs-lookup"><span data-stu-id="e5c57-p145">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3490">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3490">Format</span></span>

<span data-ttu-id="e5c57-3491">7 Zeichen oder 9 Zeichen, getrennt durch Leerzeichen oder Bindestriche</span><span class="sxs-lookup"><span data-stu-id="e5c57-3491">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3492">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3492">Pattern</span></span>

<span data-ttu-id="e5c57-3493">Zwei mögliche Muster:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3493">Two possible patterns:</span></span>

- <span data-ttu-id="e5c57-3494">Zwei Buchstaben (gültige Ninos verwenden nur bestimmte Zeichen in diesem Präfix, die von diesem Muster überprüft werden; Groß-/Kleinschreibung wird nicht berücksichtigt)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3494">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="e5c57-3495">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3495">Six digits</span></span>
- <span data-ttu-id="e5c57-3496">Entweder "A", "B", "C" oder "'d" (wie das Präfix sind nur bestimmte Zeichen im Suffix zulässig; Groß-/Kleinschreibung wird nicht berücksichtigt)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3496">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="e5c57-3497">ODER</span><span class="sxs-lookup"><span data-stu-id="e5c57-3497">OR</span></span>

- <span data-ttu-id="e5c57-3498">Zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e5c57-3498">Two letters</span></span>
- <span data-ttu-id="e5c57-3499">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-3499">A space or dash</span></span>
- <span data-ttu-id="e5c57-3500">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3500">Two digits</span></span>
- <span data-ttu-id="e5c57-3501">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-3501">A space or dash</span></span>
- <span data-ttu-id="e5c57-3502">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3502">Two digits</span></span>
- <span data-ttu-id="e5c57-3503">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-3503">A space or dash</span></span>
- <span data-ttu-id="e5c57-3504">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3504">Two digits</span></span>
- <span data-ttu-id="e5c57-3505">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-3505">A space or dash</span></span>
- <span data-ttu-id="e5c57-3506">Entweder "A", "B", "C" oder "'d"</span><span class="sxs-lookup"><span data-stu-id="e5c57-3506">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3507">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3507">Checksum</span></span>

<span data-ttu-id="e5c57-3508">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3508">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3509">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3509">Definition</span></span>

<span data-ttu-id="e5c57-3510">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3510">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3511">Die Funktion Func_uk_nino findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3511">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3512">Ein Schlüsselwort aus Keyword_uk_nino wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3512">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="e5c57-3513">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3513">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3514">Die Funktion Func_uk_nino findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3514">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3515">Es wurde kein Schlüsselwort aus Keyword_uk_nino gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3515">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3516">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3516">Keywords</span></span>

#### <a name="keyword_uk_nino"></a><span data-ttu-id="e5c57-3517">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="e5c57-3517">Keyword_uk_nino</span></span>

- <span data-ttu-id="e5c57-3518">national insurance number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3518">national insurance number</span></span> 
- <span data-ttu-id="e5c57-3519">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="e5c57-3519">national insurance contributions</span></span> 
- <span data-ttu-id="e5c57-3520">protection act</span><span class="sxs-lookup"><span data-stu-id="e5c57-3520">protection act</span></span> 
- <span data-ttu-id="e5c57-3521">Versicherungs</span><span class="sxs-lookup"><span data-stu-id="e5c57-3521">insurance</span></span> 
- <span data-ttu-id="e5c57-3522">social security number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3522">social security number</span></span> 
- <span data-ttu-id="e5c57-3523">insurance application</span><span class="sxs-lookup"><span data-stu-id="e5c57-3523">insurance application</span></span> 
- <span data-ttu-id="e5c57-3524">medical application</span><span class="sxs-lookup"><span data-stu-id="e5c57-3524">medical application</span></span> 
- <span data-ttu-id="e5c57-3525">social insurance</span><span class="sxs-lookup"><span data-stu-id="e5c57-3525">social insurance</span></span> 
- <span data-ttu-id="e5c57-3526">medical attention</span><span class="sxs-lookup"><span data-stu-id="e5c57-3526">medical attention</span></span> 
- <span data-ttu-id="e5c57-3527">social security</span><span class="sxs-lookup"><span data-stu-id="e5c57-3527">social security</span></span> 
- <span data-ttu-id="e5c57-3528">great britain</span><span class="sxs-lookup"><span data-stu-id="e5c57-3528">great britain</span></span> 
- <span data-ttu-id="e5c57-3529">Versicherungs</span><span class="sxs-lookup"><span data-stu-id="e5c57-3529">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="e5c57-p146">US-amerikanische/britische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-p146">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3532">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3532">Format</span></span>

<span data-ttu-id="e5c57-3533">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3533">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3534">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3534">Pattern</span></span>

<span data-ttu-id="e5c57-3535">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3535">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3536">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3536">Checksum</span></span>

<span data-ttu-id="e5c57-3537">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3537">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3538">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3538">Definition</span></span>

<span data-ttu-id="e5c57-3539">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3540">Die Funktion Func_usa_uk_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3540">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3541">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3541">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-3542">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3542">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="e5c57-3543">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="e5c57-3543">Keyword_passport</span></span>

- <span data-ttu-id="e5c57-3544">Passport Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3544">Passport Number</span></span> 
- <span data-ttu-id="e5c57-3545">Passport No</span><span class="sxs-lookup"><span data-stu-id="e5c57-3545">Passport No</span></span> 
- <span data-ttu-id="e5c57-3546">Passport#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3546">Passport #</span></span> 
- <span data-ttu-id="e5c57-3547">Pass #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3547">Passport#</span></span> 
- <span data-ttu-id="e5c57-3548">Passport-Nr</span><span class="sxs-lookup"><span data-stu-id="e5c57-3548">PassportID</span></span> 
- <span data-ttu-id="e5c57-3549">Passportno</span><span class="sxs-lookup"><span data-stu-id="e5c57-3549">Passportno</span></span> 
- <span data-ttu-id="e5c57-3550">passportnumber</span><span class="sxs-lookup"><span data-stu-id="e5c57-3550">passportnumber</span></span> 
- <span data-ttu-id="e5c57-3551">パスポート</span><span class="sxs-lookup"><span data-stu-id="e5c57-3551">パスポート</span></span> 
- <span data-ttu-id="e5c57-3552">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="e5c57-3552">パスポート番号</span></span> 
- <span data-ttu-id="e5c57-3553">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="e5c57-3553">パスポートのNum</span></span> 
- <span data-ttu-id="e5c57-3554">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="e5c57-3554">パスポート＃</span></span> 
- <span data-ttu-id="e5c57-3555">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="e5c57-3555">Numéro de passeport</span></span> 
- <span data-ttu-id="e5c57-3556">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="e5c57-3556">Passeport n °</span></span> 
- <span data-ttu-id="e5c57-3557">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="e5c57-3557">Passeport Non</span></span> 
- <span data-ttu-id="e5c57-3558">Passeport#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3558">Passeport #</span></span> 
- <span data-ttu-id="e5c57-3559">Passeport #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3559">Passeport#</span></span> 
- <span data-ttu-id="e5c57-3560">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="e5c57-3560">PasseportNon</span></span> 
- <span data-ttu-id="e5c57-3561">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="e5c57-3561">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="e5c57-3562">US-Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3562">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3563">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3563">Format</span></span>

<span data-ttu-id="e5c57-3564">8-17 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3564">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3565">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3565">Pattern</span></span>

<span data-ttu-id="e5c57-3566">8-17 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3566">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3567">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3567">Checksum</span></span>

<span data-ttu-id="e5c57-3568">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3568">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3569">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3569">Definition</span></span>

<span data-ttu-id="e5c57-3570">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3570">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3571">Der reguläre Ausdruck Regex_usa_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3571">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3572">Ein Schlüsselwort aus Keyword_usa_Bank_Account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3572">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e5c57-3573">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3573">Keywords</span></span>

#### <a name="keyword_usa_bank_account"></a><span data-ttu-id="e5c57-3574">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="e5c57-3574">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="e5c57-3575">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3575">Checking Account Number</span></span> 
- <span data-ttu-id="e5c57-3576">Checking Account</span><span class="sxs-lookup"><span data-stu-id="e5c57-3576">Checking Account</span></span> 
- <span data-ttu-id="e5c57-3577">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3577">Checking Account #</span></span> 
- <span data-ttu-id="e5c57-3578">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3578">Checking Acct Number</span></span> 
- <span data-ttu-id="e5c57-3579">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3579">Checking Acct #</span></span> 
- <span data-ttu-id="e5c57-3580">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3580">Checking Acct No.</span></span> 
- <span data-ttu-id="e5c57-3581">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3581">Checking Account No.</span></span> 
- <span data-ttu-id="e5c57-3582">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3582">Bank Account Number</span></span> 
- <span data-ttu-id="e5c57-3583">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3583">Bank Account #</span></span> 
- <span data-ttu-id="e5c57-3584">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3584">Bank Acct Number</span></span> 
- <span data-ttu-id="e5c57-3585">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3585">Bank Acct #</span></span> 
- <span data-ttu-id="e5c57-3586">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3586">Bank Acct No.</span></span> 
- <span data-ttu-id="e5c57-3587">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3587">Bank Account No.</span></span> 
- <span data-ttu-id="e5c57-3588">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3588">Savings Account Number</span></span> 
- <span data-ttu-id="e5c57-3589">Savings Account</span><span class="sxs-lookup"><span data-stu-id="e5c57-3589">Savings Account.</span></span> 
- <span data-ttu-id="e5c57-3590">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3590">Savings Account #</span></span> 
- <span data-ttu-id="e5c57-3591">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3591">Savings Acct Number</span></span> 
- <span data-ttu-id="e5c57-3592">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3592">Savings Acct #</span></span> 
- <span data-ttu-id="e5c57-3593">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3593">Savings Acct No.</span></span> 
- <span data-ttu-id="e5c57-3594">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3594">Savings Account No.</span></span> 
- <span data-ttu-id="e5c57-3595">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3595">Debit Account Number</span></span> 
- <span data-ttu-id="e5c57-3596">Debit Account</span><span class="sxs-lookup"><span data-stu-id="e5c57-3596">Debit Account</span></span> 
- <span data-ttu-id="e5c57-3597">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3597">Debit Account #</span></span> 
- <span data-ttu-id="e5c57-3598">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3598">Debit Acct Number</span></span> 
- <span data-ttu-id="e5c57-3599">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3599">Debit Acct #</span></span> 
- <span data-ttu-id="e5c57-3600">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3600">Debit Acct No.</span></span> 
- <span data-ttu-id="e5c57-3601">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3601">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="e5c57-3602">US-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3602">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3603">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3603">Format</span></span>

<span data-ttu-id="e5c57-3604">Abhängig vom Bundesstaat</span><span class="sxs-lookup"><span data-stu-id="e5c57-3604">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3605">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3605">Pattern</span></span>

<span data-ttu-id="e5c57-3606">Abhängig vom Bundesstaat – am Beispiel für New York:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3606">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="e5c57-3607">Neun Ziffern, die wie DDD DDD DDD formatiert sind, stimmen überein.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3607">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="e5c57-3608">Neun Ziffern wie ddddddddd werden nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3608">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3609">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3609">Checksum</span></span>

<span data-ttu-id="e5c57-3610">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3610">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3611">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3611">Definition</span></span>

<span data-ttu-id="e5c57-3612">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3612">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3613">Die Funktion Func_new_york_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3613">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3614">Ein Schlüsselwort aus Keyword_[state_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3614">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="e5c57-3615">Ein Schlüsselwort aus Keyword_us_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3615">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="e5c57-3616">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3616">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3617">Die Funktion Func_new_york_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3617">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3618">Ein Schlüsselwort aus Keyword_[state_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3618">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="e5c57-3619">Ein Schlüsselwort aus Keyword_us_drivers_license_abbreviations wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3619">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="e5c57-3620">Es wurde kein Schlüsselwort aus Keyword_us_drivers_license gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3620">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3621">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3621">Keywords</span></span>

#### <a name="keyword_us_drivers_license_abbreviations"></a><span data-ttu-id="e5c57-3622">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="e5c57-3622">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="e5c57-3623">DL</span><span class="sxs-lookup"><span data-stu-id="e5c57-3623">DL</span></span> 
- <span data-ttu-id="e5c57-3624">DLS</span><span class="sxs-lookup"><span data-stu-id="e5c57-3624">DLS</span></span> 
- <span data-ttu-id="e5c57-3625">CDL</span><span class="sxs-lookup"><span data-stu-id="e5c57-3625">CDL</span></span> 
- <span data-ttu-id="e5c57-3626">CDLS</span><span class="sxs-lookup"><span data-stu-id="e5c57-3626">CDLS</span></span> 
- <span data-ttu-id="e5c57-3627">ID</span><span class="sxs-lookup"><span data-stu-id="e5c57-3627">ID</span></span> 
- <span data-ttu-id="e5c57-3628">IDs</span><span class="sxs-lookup"><span data-stu-id="e5c57-3628">IDs</span></span> 
- <span data-ttu-id="e5c57-3629">DL #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3629">DL#</span></span> 
- <span data-ttu-id="e5c57-3630">DLS #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3630">DLS#</span></span> 
- <span data-ttu-id="e5c57-3631">CDL #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3631">CDL#</span></span> 
- <span data-ttu-id="e5c57-3632">CDLS #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3632">CDLS#</span></span> 
- <span data-ttu-id="e5c57-3633">ID #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3633">ID#</span></span>
- <span data-ttu-id="e5c57-3634">IDs #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3634">IDs#</span></span> 
- <span data-ttu-id="e5c57-3635">ID number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3635">ID number</span></span> 
- <span data-ttu-id="e5c57-3636">ID numbers</span><span class="sxs-lookup"><span data-stu-id="e5c57-3636">ID numbers</span></span> 
- <span data-ttu-id="e5c57-3637">LIC</span><span class="sxs-lookup"><span data-stu-id="e5c57-3637">LIC</span></span> 
- <span data-ttu-id="e5c57-3638">LIC #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3638">LIC#</span></span> 

#### <a name="keyword_us_drivers_license"></a><span data-ttu-id="e5c57-3639">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="e5c57-3639">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="e5c57-3640">DriverLic</span><span class="sxs-lookup"><span data-stu-id="e5c57-3640">DriverLic</span></span> 
- <span data-ttu-id="e5c57-3641">DriverLics</span><span class="sxs-lookup"><span data-stu-id="e5c57-3641">DriverLics</span></span> 
- <span data-ttu-id="e5c57-3642">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="e5c57-3642">DriverLicense</span></span> 
- <span data-ttu-id="e5c57-3643">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-3643">DriverLicenses</span></span> 
- <span data-ttu-id="e5c57-3644">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-3644">Driver Lic</span></span> 
- <span data-ttu-id="e5c57-3645">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-3645">Driver Lics</span></span> 
- <span data-ttu-id="e5c57-3646">Driver License</span><span class="sxs-lookup"><span data-stu-id="e5c57-3646">Driver License</span></span> 
- <span data-ttu-id="e5c57-3647">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-3647">Driver Licenses</span></span> 
- <span data-ttu-id="e5c57-3648">DriversLic</span><span class="sxs-lookup"><span data-stu-id="e5c57-3648">DriversLic</span></span> 
- <span data-ttu-id="e5c57-3649">DriversLics</span><span class="sxs-lookup"><span data-stu-id="e5c57-3649">DriversLics</span></span> 
- <span data-ttu-id="e5c57-3650">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="e5c57-3650">DriversLicense</span></span> 
- <span data-ttu-id="e5c57-3651">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-3651">DriversLicenses</span></span> 
- <span data-ttu-id="e5c57-3652">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-3652">Drivers Lic</span></span> 
- <span data-ttu-id="e5c57-3653">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-3653">Drivers Lics</span></span> 
- <span data-ttu-id="e5c57-3654">Drivers License</span><span class="sxs-lookup"><span data-stu-id="e5c57-3654">Drivers License</span></span> 
- <span data-ttu-id="e5c57-3655">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-3655">Drivers Licenses</span></span> 
- <span data-ttu-id="e5c57-3656">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-3656">Driver'Lic</span></span> 
- <span data-ttu-id="e5c57-3657">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-3657">Driver'Lics</span></span> 
- <span data-ttu-id="e5c57-3658">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="e5c57-3658">Driver'License</span></span> 
- <span data-ttu-id="e5c57-3659">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-3659">Driver'Licenses</span></span> 
- <span data-ttu-id="e5c57-3660">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-3660">Driver' Lic</span></span> 
- <span data-ttu-id="e5c57-3661">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-3661">Driver' Lics</span></span> 
- <span data-ttu-id="e5c57-3662">Driver' License</span><span class="sxs-lookup"><span data-stu-id="e5c57-3662">Driver' License</span></span> 
- <span data-ttu-id="e5c57-3663">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-3663">Driver' Licenses</span></span>
- <span data-ttu-id="e5c57-3664">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="e5c57-3664">Driver'sLic</span></span> 
- <span data-ttu-id="e5c57-3665">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="e5c57-3665">Driver'sLics</span></span> 
- <span data-ttu-id="e5c57-3666">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="e5c57-3666">Driver'sLicense</span></span> 
- <span data-ttu-id="e5c57-3667">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-3667">Driver'sLicenses</span></span> 
- <span data-ttu-id="e5c57-3668">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="e5c57-3668">Driver's Lic</span></span> 
- <span data-ttu-id="e5c57-3669">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="e5c57-3669">Driver's Lics</span></span> 
- <span data-ttu-id="e5c57-3670">Driver's License</span><span class="sxs-lookup"><span data-stu-id="e5c57-3670">Driver's License</span></span> 
- <span data-ttu-id="e5c57-3671">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="e5c57-3671">Driver's Licenses</span></span> 
- <span data-ttu-id="e5c57-3672">identification number</span><span class="sxs-lookup"><span data-stu-id="e5c57-3672">identification number</span></span> 
- <span data-ttu-id="e5c57-3673">identification numbers</span><span class="sxs-lookup"><span data-stu-id="e5c57-3673">identification numbers</span></span> 
- <span data-ttu-id="e5c57-3674">identification#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3674">identification #</span></span> 
- <span data-ttu-id="e5c57-3675">id card</span><span class="sxs-lookup"><span data-stu-id="e5c57-3675">id card</span></span> 
- <span data-ttu-id="e5c57-3676">id cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-3676">id cards</span></span> 
- <span data-ttu-id="e5c57-3677">identification card</span><span class="sxs-lookup"><span data-stu-id="e5c57-3677">identification card</span></span> 
- <span data-ttu-id="e5c57-3678">identification cards</span><span class="sxs-lookup"><span data-stu-id="e5c57-3678">identification cards</span></span> 
- <span data-ttu-id="e5c57-3679">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3679">DriverLic#</span></span> 
- <span data-ttu-id="e5c57-3680">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3680">DriverLics#</span></span> 
- <span data-ttu-id="e5c57-3681">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3681">DriverLicense#</span></span> 
- <span data-ttu-id="e5c57-3682">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3682">DriverLicenses#</span></span> 
- <span data-ttu-id="e5c57-3683">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3683">Driver Lic#</span></span> 
- <span data-ttu-id="e5c57-3684">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3684">Driver Lics#</span></span> 
- <span data-ttu-id="e5c57-3685">Driver License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3685">Driver License#</span></span> 
- <span data-ttu-id="e5c57-3686">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3686">Driver Licenses#</span></span> 
- <span data-ttu-id="e5c57-3687">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3687">DriversLic#</span></span> 
- <span data-ttu-id="e5c57-3688">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3688">DriversLics#</span></span> 
- <span data-ttu-id="e5c57-3689">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3689">DriversLicense#</span></span> 
- <span data-ttu-id="e5c57-3690">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3690">DriversLicenses#</span></span> 
- <span data-ttu-id="e5c57-3691">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3691">Drivers Lic#</span></span> 
- <span data-ttu-id="e5c57-3692">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3692">Drivers Lics#</span></span> 
- <span data-ttu-id="e5c57-3693">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3693">Drivers License#</span></span> 
- <span data-ttu-id="e5c57-3694">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3694">Drivers Licenses#</span></span> 
- <span data-ttu-id="e5c57-3695">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3695">Driver'Lic#</span></span> 
- <span data-ttu-id="e5c57-3696">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3696">Driver'Lics#</span></span> 
- <span data-ttu-id="e5c57-3697">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3697">Driver'License#</span></span> 
- <span data-ttu-id="e5c57-3698">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3698">Driver'Licenses#</span></span> 
- <span data-ttu-id="e5c57-3699">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3699">Driver' Lic#</span></span> 
- <span data-ttu-id="e5c57-3700">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3700">Driver' Lics#</span></span> 
- <span data-ttu-id="e5c57-3701">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3701">Driver' License#</span></span> 
- <span data-ttu-id="e5c57-3702">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3702">Driver' Licenses#</span></span> 
- <span data-ttu-id="e5c57-3703">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3703">Driver'sLic#</span></span> 
- <span data-ttu-id="e5c57-3704">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3704">Driver'sLics#</span></span> 
- <span data-ttu-id="e5c57-3705">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3705">Driver'sLicense#</span></span> 
- <span data-ttu-id="e5c57-3706">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3706">Driver'sLicenses#</span></span> 
- <span data-ttu-id="e5c57-3707">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3707">Driver's Lic#</span></span> 
- <span data-ttu-id="e5c57-3708">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3708">Driver's Lics#</span></span> 
- <span data-ttu-id="e5c57-3709">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3709">Driver's License#</span></span> 
- <span data-ttu-id="e5c57-3710">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3710">Driver's Licenses#</span></span> 
- <span data-ttu-id="e5c57-3711">id card#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3711">id card#</span></span> 
- <span data-ttu-id="e5c57-3712">id cards#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3712">id cards#</span></span> 
- <span data-ttu-id="e5c57-3713">identification card#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3713">identification card#</span></span> 
- <span data-ttu-id="e5c57-3714">identification cards#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3714">identification cards#</span></span> 


#### <a name="keyword_state_name_drivers_license_name"></a><span data-ttu-id="e5c57-3715">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="e5c57-3715">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="e5c57-3716">Abkürzung für Bundesstaat (z. B. „NY“)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3716">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="e5c57-3717">Name des Bundesstaats (z. B. „New York“)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3717">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="e5c57-3718">US-Steueridentifikationsnummer (ITIN)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3718">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3719">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3719">Format</span></span>

<span data-ttu-id="e5c57-3720">Neun Ziffern, die mit "9" beginnen und "7" oder "8" als vierte Ziffer enthalten, optional mit Leerzeichen oder Bindestrichen formatiert</span><span class="sxs-lookup"><span data-stu-id="e5c57-3720">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3721">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3721">Pattern</span></span>

<span data-ttu-id="e5c57-3722">Formatiert</span><span class="sxs-lookup"><span data-stu-id="e5c57-3722">Formatted:</span></span>
- <span data-ttu-id="e5c57-3723">Die Ziffer 9</span><span class="sxs-lookup"><span data-stu-id="e5c57-3723">The digit "9"</span></span> 
- <span data-ttu-id="e5c57-3724">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3724">Two digits</span></span> 
- <span data-ttu-id="e5c57-3725">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-3725">A space or dash</span></span> 
- <span data-ttu-id="e5c57-3726">Eine 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="e5c57-3726">A "7" or "8"</span></span> 
- <span data-ttu-id="e5c57-3727">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3727">A digit</span></span> 
- <span data-ttu-id="e5c57-3728">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="e5c57-3728">A space, or dash</span></span> 
- <span data-ttu-id="e5c57-3729">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3729">Four digits</span></span>

<span data-ttu-id="e5c57-3730">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="e5c57-3730">Unformatted:</span></span>
- <span data-ttu-id="e5c57-3731">Die Ziffer 9</span><span class="sxs-lookup"><span data-stu-id="e5c57-3731">The digit "9"</span></span> 
- <span data-ttu-id="e5c57-3732">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3732">Two digits</span></span> 
- <span data-ttu-id="e5c57-3733">Eine 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="e5c57-3733">A "7" or "8"</span></span> 
- <span data-ttu-id="e5c57-3734">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3734">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3735">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3735">Checksum</span></span>

<span data-ttu-id="e5c57-3736">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3736">No</span></span>

### <a name="definition"></a><span data-ttu-id="e5c57-3737">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3737">Definition</span></span>

<span data-ttu-id="e5c57-3738">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3738">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3739">Die Funktion Func_formatted_itin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3739">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3740">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3740">At least one of the following is true:</span></span>
    - <span data-ttu-id="e5c57-3741">Ein Schlüsselwort aus Keyword_itin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3741">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="e5c57-3742">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3742">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="e5c57-3743">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3743">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="e5c57-3744">Ein Schlüsselwort aus Keyword_itin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3744">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="e5c57-3745">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3745">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3746">Die Funktion Func_unformatted_itin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3746">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3747">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3747">At least one of the following is true:</span></span>
    - <span data-ttu-id="e5c57-3748">Ein Schlüsselwort aus Keyword_itin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3748">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="e5c57-3749">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3749">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="e5c57-3750">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3750">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3751">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3751">Keywords</span></span>

#### <a name="keyword_itin"></a><span data-ttu-id="e5c57-3752">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="e5c57-3752">Keyword_itin</span></span>

- <span data-ttu-id="e5c57-3753">Steuer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3753">taxpayer</span></span> 
- <span data-ttu-id="e5c57-3754">tax id</span><span class="sxs-lookup"><span data-stu-id="e5c57-3754">tax id</span></span> 
- <span data-ttu-id="e5c57-3755">tax identification</span><span class="sxs-lookup"><span data-stu-id="e5c57-3755">tax identification</span></span> 
- <span data-ttu-id="e5c57-3756">Itin</span><span class="sxs-lookup"><span data-stu-id="e5c57-3756">itin</span></span> 
- <span data-ttu-id="e5c57-3757">SSN</span><span class="sxs-lookup"><span data-stu-id="e5c57-3757">ssn</span></span> 
- <span data-ttu-id="e5c57-3758">Zinn</span><span class="sxs-lookup"><span data-stu-id="e5c57-3758">tin</span></span> 
- <span data-ttu-id="e5c57-3759">social security</span><span class="sxs-lookup"><span data-stu-id="e5c57-3759">social security</span></span> 
- <span data-ttu-id="e5c57-3760">tax payer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3760">tax payer</span></span> 
- <span data-ttu-id="e5c57-3761">itins</span><span class="sxs-lookup"><span data-stu-id="e5c57-3761">itins</span></span> 
- <span data-ttu-id="e5c57-3762">per Taxi</span><span class="sxs-lookup"><span data-stu-id="e5c57-3762">taxid</span></span> 
- <span data-ttu-id="e5c57-3763">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3763">individual taxpayer</span></span> 

#### <a name="keyword_itin_collaborative"></a><span data-ttu-id="e5c57-3764">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="e5c57-3764">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="e5c57-3765">Lizenz</span><span class="sxs-lookup"><span data-stu-id="e5c57-3765">License</span></span> 
- <span data-ttu-id="e5c57-3766">DL</span><span class="sxs-lookup"><span data-stu-id="e5c57-3766">DL</span></span> 
- <span data-ttu-id="e5c57-3767">DOB</span><span class="sxs-lookup"><span data-stu-id="e5c57-3767">DOB</span></span> 
- <span data-ttu-id="e5c57-3768">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="e5c57-3768">Birthdate</span></span> 
- <span data-ttu-id="e5c57-3769">Geburtstag</span><span class="sxs-lookup"><span data-stu-id="e5c57-3769">Birthday</span></span> 
- <span data-ttu-id="e5c57-3770">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="e5c57-3770">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="e5c57-3771">US-Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e5c57-3771">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="e5c57-3772">Format</span><span class="sxs-lookup"><span data-stu-id="e5c57-3772">Format</span></span>

<span data-ttu-id="e5c57-3773">9 Ziffern in formatiertem oder unformatiertem Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3773">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="e5c57-3774">Wenn ein SSN vor Mitte 2011 ausgegeben wird, weist es eine starke Formatierung auf, bei der bestimmte Teile der Zahl in bestimmte Bereiche fallen müssen, um gültig zu sein (aber keine Prüfsumme).</span><span class="sxs-lookup"><span data-stu-id="e5c57-3774">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="e5c57-3775">Muster</span><span class="sxs-lookup"><span data-stu-id="e5c57-3775">Pattern</span></span>

<span data-ttu-id="e5c57-3776">Vier Funktionen suchen nach Sozialversicherungsnummern in vier verschiedenen Mustern:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3776">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="e5c57-3777">Func_ssn findet Sozialversicherungsnummern mit starker Formatierung vor 2011, die mit Bindestrichen oder Leerzeichen formatiert sind (DDD-DD-dddd oder DDD DD dddd)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3777">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="e5c57-3778">Func_unformatted_ssn findet Sozialversicherungsnummern mit starker Formatierung vor 2011, die als neun aufeinanderfolgende Ziffern (ddddddddd) unformatiert sind.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3778">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="e5c57-3779">Func_randomized_formatted_ssn findet Post-2011-Sozialversicherungsnummern, die mit Bindestrichen oder Leerzeichen formatiert sind (DDD-DD-dddd oder DDD DD dddd)</span><span class="sxs-lookup"><span data-stu-id="e5c57-3779">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="e5c57-3780">Func_randomized_unformatted_ssn findet Post-2011-Sozialversicherungsnummern, die als neun aufeinanderfolgende Ziffern (ddddddddd) unformatiert sind.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3780">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="e5c57-3781">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e5c57-3781">Checksum</span></span>

<span data-ttu-id="e5c57-3782">Nein</span><span class="sxs-lookup"><span data-stu-id="e5c57-3782">No</span></span>


### <a name="definition"></a><span data-ttu-id="e5c57-3783">Definition</span><span class="sxs-lookup"><span data-stu-id="e5c57-3783">Definition</span></span>

<span data-ttu-id="e5c57-3784">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3785">Die Funktion Func_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3785">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3786">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3786">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="e5c57-3787">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3787">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3788">Die Funktion Func_unformatted_ssn findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3788">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3789">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3789">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="e5c57-3790">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3790">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3791">Die Funktion Func_randomized_formatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3791">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3792">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3792">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="e5c57-3793">Die Funktion Func_ssn findet keine Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3793">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="e5c57-3794">Eine DLP-Richtlinie ist zu 55 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5c57-3794">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="e5c57-3795">Die Funktion Func_randomized_unformatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3795">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="e5c57-3796">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3796">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="e5c57-3797">Die Funktion Func_unformatted_ssn findet keine Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5c57-3797">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="e5c57-3798">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e5c57-3798">Keywords</span></span>

#### <a name="keyword_ssn"></a><span data-ttu-id="e5c57-3799">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="e5c57-3799">Keyword_ssn</span></span>

- <span data-ttu-id="e5c57-3800">Social Security</span><span class="sxs-lookup"><span data-stu-id="e5c57-3800">Social Security</span></span> 
- <span data-ttu-id="e5c57-3801">Social Security#</span><span class="sxs-lookup"><span data-stu-id="e5c57-3801">Social Security#</span></span> 
- <span data-ttu-id="e5c57-3802">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="e5c57-3802">Soc Sec</span></span> 
- <span data-ttu-id="e5c57-3803">SSN</span><span class="sxs-lookup"><span data-stu-id="e5c57-3803">SSN</span></span> 
- <span data-ttu-id="e5c57-3804">Sozialversicherungsnummern</span><span class="sxs-lookup"><span data-stu-id="e5c57-3804">SSNS</span></span> 
- <span data-ttu-id="e5c57-3805">SSN #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3805">SSN#</span></span> 
- <span data-ttu-id="e5c57-3806">SS #</span><span class="sxs-lookup"><span data-stu-id="e5c57-3806">SS#</span></span> 
- <span data-ttu-id="e5c57-3807">SSID</span><span class="sxs-lookup"><span data-stu-id="e5c57-3807">SSID</span></span> 
   

