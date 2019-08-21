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
ms.openlocfilehash: d486510c35aaf147e6d63e28d1df36ef689e3975
ms.sourcegitcommit: a5a7e43822336ed18d8f5879167766686cf6b2a3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2019
ms.locfileid: "36478254"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="57f50-104">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="57f50-104">What the sensitive information types look for</span></span>

<span data-ttu-id="57f50-105">Die Verhinderung von Datenverlust (Data Loss &amp; Prevention, DLP) im Office 365 Security Compliance Center umfasst viele Arten von vertraulichen Informationen, die Sie in ihren DLP-Richtlinien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="57f50-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="57f50-106">Dieses Thema enthält eine Liste aller dieser vertraulichen Informationstypen und zeigt, was eine DLP-Richtlinie sucht, wenn sie den jeweiligen Typen erkennt.</span><span class="sxs-lookup"><span data-stu-id="57f50-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="57f50-107">Ein vertraulicher Informationstyp wird durch ein Muster definiert, das durch einen regulären Ausdruck oder eine Funktion identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="57f50-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="57f50-108">Darüber hinaus können auch belegende Hinweise wie Schlüsselwörter oder Prüfsummen zum Identifizieren eines Typs vertraulicher Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57f50-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="57f50-109">Beim Auswertungsprozess können auch die Zuverlässigkeitsstufe und die Näherung herangezogen werden.</span><span class="sxs-lookup"><span data-stu-id="57f50-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="57f50-110">ABA Routing Number (US-Bankleitzahl)</span><span class="sxs-lookup"><span data-stu-id="57f50-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-111">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-111">Format</span></span>

<span data-ttu-id="57f50-112">9 Ziffern in formatiertem oder unformatiertem Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-113">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-113">Pattern</span></span>

<span data-ttu-id="57f50-114">Formatiert</span><span class="sxs-lookup"><span data-stu-id="57f50-114">Formatted:</span></span>
- <span data-ttu-id="57f50-115">Vier Ziffern, beginnend mit 0, 1, 2, 3, 6, 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="57f50-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="57f50-116">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-116">A hyphen</span></span>
- <span data-ttu-id="57f50-117">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-117">Four digits</span></span>
- <span data-ttu-id="57f50-118">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-118">A hyphen</span></span>
- <span data-ttu-id="57f50-119">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-119">A digit</span></span>

<span data-ttu-id="57f50-120">Unformatiert: 9 aufeinanderfolgende Ziffern, beginnend mit 0, 1, 2, 3, 6, 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="57f50-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="57f50-121">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-121">Checksum</span></span>

<span data-ttu-id="57f50-122">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-123">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-123">Definition</span></span>

<span data-ttu-id="57f50-124">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-125">Die Funktion Func_aba_routing findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-126">Ein Schlüsselwort aus Keyword_ABA_Routing wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```xml
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="57f50-127">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-127">Keywords</span></span>

#### <a name="keyword_aba_routing"></a><span data-ttu-id="57f50-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="57f50-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="57f50-129">ABA</span><span class="sxs-lookup"><span data-stu-id="57f50-129">aba</span></span>
- <span data-ttu-id="57f50-130">aba #</span><span class="sxs-lookup"><span data-stu-id="57f50-130">aba #</span></span>
- <span data-ttu-id="57f50-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="57f50-131">aba routing #</span></span>
- <span data-ttu-id="57f50-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="57f50-132">aba routing number</span></span>
- <span data-ttu-id="57f50-133">ABA #</span><span class="sxs-lookup"><span data-stu-id="57f50-133">aba#</span></span>
- <span data-ttu-id="57f50-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="57f50-134">abarouting#</span></span>
- <span data-ttu-id="57f50-135">aba number</span><span class="sxs-lookup"><span data-stu-id="57f50-135">aba number</span></span>
- <span data-ttu-id="57f50-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="57f50-136">abaroutingnumber</span></span>
- <span data-ttu-id="57f50-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="57f50-137">american bank association routing #</span></span>
- <span data-ttu-id="57f50-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="57f50-138">american bank association routing number</span></span>
- <span data-ttu-id="57f50-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="57f50-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="57f50-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="57f50-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="57f50-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="57f50-141">bank routing number</span></span>
- <span data-ttu-id="57f50-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="57f50-142">bankrouting#</span></span>
- <span data-ttu-id="57f50-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="57f50-143">bankroutingnumber</span></span>
- <span data-ttu-id="57f50-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="57f50-144">routing transit number</span></span>
- <span data-ttu-id="57f50-145">RTN</span><span class="sxs-lookup"><span data-stu-id="57f50-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="57f50-146">Argentina National Identity (DNI) Number</span><span class="sxs-lookup"><span data-stu-id="57f50-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-147">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-147">Format</span></span>

<span data-ttu-id="57f50-148">Acht Ziffern, durch Punkte getrennt</span><span class="sxs-lookup"><span data-stu-id="57f50-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-149">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-149">Pattern</span></span>

<span data-ttu-id="57f50-150">Acht Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-150">Eight digits:</span></span>
- <span data-ttu-id="57f50-151">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-151">Two digits</span></span>
- <span data-ttu-id="57f50-152">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="57f50-152">A period</span></span>
- <span data-ttu-id="57f50-153">Drei Ziffern </span><span class="sxs-lookup"><span data-stu-id="57f50-153">Three digits</span></span>
- <span data-ttu-id="57f50-154">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="57f50-154">A period</span></span>
- <span data-ttu-id="57f50-155">Drei Ziffern </span><span class="sxs-lookup"><span data-stu-id="57f50-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-156">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-156">Checksum</span></span>

<span data-ttu-id="57f50-157">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-158">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-158">Definition</span></span>

<span data-ttu-id="57f50-159">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-160">Der reguläre Ausdruck Regex_argentina_national_id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-161">Ein Schlüsselwort aus Keyword_argentina_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```xml
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-162">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-162">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="57f50-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="57f50-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="57f50-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="57f50-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="57f50-165">Identität</span><span class="sxs-lookup"><span data-stu-id="57f50-165">Identity</span></span> 
- <span data-ttu-id="57f50-166">Identification National Identity Card</span><span class="sxs-lookup"><span data-stu-id="57f50-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="57f50-167">DNI</span><span class="sxs-lookup"><span data-stu-id="57f50-167">DNI</span></span> 
- <span data-ttu-id="57f50-168">Nic-nationales Personenregister</span><span class="sxs-lookup"><span data-stu-id="57f50-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="57f50-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="57f50-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="57f50-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="57f50-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="57f50-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="57f50-171">Identidad</span></span> 
- <span data-ttu-id="57f50-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="57f50-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="57f50-173">Australische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="57f50-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-174">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-174">Format</span></span>

<span data-ttu-id="57f50-175">6-10 Stellen mit oder ohne Bankfilialnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-176">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-176">Pattern</span></span>

<span data-ttu-id="57f50-177">Kontonummer hat 6-10 Stellen.</span><span class="sxs-lookup"><span data-stu-id="57f50-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="57f50-178">Australische Bankleitzahl:</span><span class="sxs-lookup"><span data-stu-id="57f50-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="57f50-179">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-179">Three digits</span></span> 
- <span data-ttu-id="57f50-180">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-180">A hyphen</span></span> 
- <span data-ttu-id="57f50-181">Drei Stellen</span><span class="sxs-lookup"><span data-stu-id="57f50-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-182">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-182">Checksum</span></span>

<span data-ttu-id="57f50-183">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-184">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-184">Definition</span></span>

<span data-ttu-id="57f50-185">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-186">Der reguläre Ausdruck Regex_australia_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="57f50-187">Ein Schlüsselwort aus Keyword_australia_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="57f50-188">Der reguläre Ausdruck Regex_australia_bank_account_number_bsb findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="57f50-189">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-190">Der reguläre Ausdruck Regex_australia_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="57f50-191">Ein Schlüsselwort aus Keyword_australia_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-192">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-192">Keywords</span></span>

#### <a name="keyword_australia_bank_account_number"></a><span data-ttu-id="57f50-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="57f50-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="57f50-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="57f50-194">swift bank code</span></span>
- <span data-ttu-id="57f50-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="57f50-195">correspondent bank</span></span>
- <span data-ttu-id="57f50-196">base currency</span><span class="sxs-lookup"><span data-stu-id="57f50-196">base currency</span></span>
- <span data-ttu-id="57f50-197">usa account</span><span class="sxs-lookup"><span data-stu-id="57f50-197">usa account</span></span>
- <span data-ttu-id="57f50-198">holder address</span><span class="sxs-lookup"><span data-stu-id="57f50-198">holder address</span></span>
- <span data-ttu-id="57f50-199">bank address</span><span class="sxs-lookup"><span data-stu-id="57f50-199">bank address</span></span>
- <span data-ttu-id="57f50-200">information account</span><span class="sxs-lookup"><span data-stu-id="57f50-200">information account</span></span>
- <span data-ttu-id="57f50-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="57f50-201">fund transfers</span></span>
- <span data-ttu-id="57f50-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="57f50-202">bank charges</span></span>
- <span data-ttu-id="57f50-203">bank details</span><span class="sxs-lookup"><span data-stu-id="57f50-203">bank details</span></span>
- <span data-ttu-id="57f50-204">banking information</span><span class="sxs-lookup"><span data-stu-id="57f50-204">banking information</span></span>
- <span data-ttu-id="57f50-205">full names</span><span class="sxs-lookup"><span data-stu-id="57f50-205">full names</span></span>
- <span data-ttu-id="57f50-206">IAEO</span><span class="sxs-lookup"><span data-stu-id="57f50-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="57f50-207">Australische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-208">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-208">Format</span></span>

<span data-ttu-id="57f50-209">Neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-210">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-210">Pattern</span></span>

<span data-ttu-id="57f50-211">Neun Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="57f50-212">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="57f50-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="57f50-213">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-213">Two digits</span></span> 
- <span data-ttu-id="57f50-214">Fünf Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="57f50-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="57f50-215">ODER</span><span class="sxs-lookup"><span data-stu-id="57f50-215">OR</span></span>

- <span data-ttu-id="57f50-216">1-2 optionale Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="57f50-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="57f50-217">4 bis 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-217">4-9 digits</span></span>

<span data-ttu-id="57f50-218">ODER</span><span class="sxs-lookup"><span data-stu-id="57f50-218">OR</span></span>

- <span data-ttu-id="57f50-219">Neun Ziffern oder Buchstaben (Groß-/Kleinschreibung irrelevant)</span><span class="sxs-lookup"><span data-stu-id="57f50-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-220">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-220">Checksum</span></span>

<span data-ttu-id="57f50-221">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-222">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-222">Definition</span></span>

<span data-ttu-id="57f50-223">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-224">Der reguläre Ausdruck Regex_australia_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-225">Ein Schlüsselwort aus Keyword_australia_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="57f50-226">Es wurde kein Schlüsselwort aus Keyword_australia_drivers_license_number_exclusions gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-227">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-227">Keywords</span></span>

#### <a name="keyword_australia_drivers_license_number"></a><span data-ttu-id="57f50-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="57f50-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="57f50-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="57f50-229">international driving permits</span></span>
- <span data-ttu-id="57f50-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="57f50-230">australian automobile association</span></span>
- <span data-ttu-id="57f50-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="57f50-231">international driving permit</span></span>
- <span data-ttu-id="57f50-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="57f50-232">DriverLicence</span></span>
- <span data-ttu-id="57f50-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="57f50-233">DriverLicences</span></span>
- <span data-ttu-id="57f50-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-234">Driver Lic</span></span>
- <span data-ttu-id="57f50-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-235">Driver Licence</span></span>
- <span data-ttu-id="57f50-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-236">Driver Licences</span></span>
- <span data-ttu-id="57f50-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="57f50-237">DriversLic</span></span>
- <span data-ttu-id="57f50-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="57f50-238">DriversLicence</span></span>
- <span data-ttu-id="57f50-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="57f50-239">DriversLicences</span></span>
- <span data-ttu-id="57f50-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-240">Drivers Lic</span></span>
- <span data-ttu-id="57f50-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-241">Drivers Lics</span></span>
- <span data-ttu-id="57f50-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-242">Drivers Licence</span></span>
- <span data-ttu-id="57f50-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-243">Drivers Licences</span></span>
- <span data-ttu-id="57f50-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-244">Driver'Lic</span></span>
- <span data-ttu-id="57f50-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-245">Driver'Lics</span></span>
- <span data-ttu-id="57f50-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-246">Driver'Licence</span></span>
- <span data-ttu-id="57f50-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-247">Driver'Licences</span></span>
- <span data-ttu-id="57f50-248">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-248">Driver' Lic</span></span>
- <span data-ttu-id="57f50-249">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-249">Driver' Lics</span></span>
- <span data-ttu-id="57f50-250">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-250">Driver' Licence</span></span>
- <span data-ttu-id="57f50-251">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-251">Driver' Licences</span></span>
- <span data-ttu-id="57f50-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="57f50-252">Driver'sLic</span></span>
- <span data-ttu-id="57f50-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="57f50-253">Driver'sLics</span></span>
- <span data-ttu-id="57f50-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="57f50-254">Driver'sLicence</span></span>
- <span data-ttu-id="57f50-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="57f50-255">Driver'sLicences</span></span>
- <span data-ttu-id="57f50-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-256">Driver's Lic</span></span>
- <span data-ttu-id="57f50-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-257">Driver's Lics</span></span>
- <span data-ttu-id="57f50-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-258">Driver's Licence</span></span>
- <span data-ttu-id="57f50-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-259">Driver's Licences</span></span>
- <span data-ttu-id="57f50-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="57f50-260">DriverLic#</span></span>
- <span data-ttu-id="57f50-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="57f50-261">DriverLics#</span></span>
- <span data-ttu-id="57f50-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="57f50-262">DriverLicence#</span></span>
- <span data-ttu-id="57f50-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="57f50-263">DriverLicences#</span></span>
- <span data-ttu-id="57f50-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-264">Driver Lic#</span></span>
- <span data-ttu-id="57f50-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-265">Driver Lics#</span></span>
- <span data-ttu-id="57f50-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="57f50-266">Driver Licence#</span></span>
- <span data-ttu-id="57f50-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="57f50-267">Driver Licences#</span></span>
- <span data-ttu-id="57f50-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="57f50-268">DriversLic#</span></span>
- <span data-ttu-id="57f50-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="57f50-269">DriversLics#</span></span>
- <span data-ttu-id="57f50-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="57f50-270">DriversLicence#</span></span>
- <span data-ttu-id="57f50-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="57f50-271">DriversLicences#</span></span>
- <span data-ttu-id="57f50-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-272">Drivers Lic#</span></span>
- <span data-ttu-id="57f50-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-273">Drivers Lics#</span></span>
- <span data-ttu-id="57f50-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="57f50-274">Drivers Licence#</span></span>
- <span data-ttu-id="57f50-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="57f50-275">Drivers Licences#</span></span>
- <span data-ttu-id="57f50-276">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="57f50-276">Driver'Lic#</span></span>
- <span data-ttu-id="57f50-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="57f50-277">Driver'Lics#</span></span>
- <span data-ttu-id="57f50-278">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="57f50-278">Driver'Licence#</span></span>
- <span data-ttu-id="57f50-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="57f50-279">Driver'Licences#</span></span>
- <span data-ttu-id="57f50-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-280">Driver' Lic#</span></span>
- <span data-ttu-id="57f50-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-281">Driver' Lics#</span></span>
- <span data-ttu-id="57f50-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="57f50-282">Driver' Licence#</span></span>
- <span data-ttu-id="57f50-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="57f50-283">Driver' Licences#</span></span>
- <span data-ttu-id="57f50-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="57f50-284">Driver'sLic#</span></span>
- <span data-ttu-id="57f50-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="57f50-285">Driver'sLics#</span></span>
- <span data-ttu-id="57f50-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="57f50-286">Driver'sLicence#</span></span>
- <span data-ttu-id="57f50-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="57f50-287">Driver'sLicences#</span></span>
- <span data-ttu-id="57f50-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-288">Driver's Lic#</span></span>
- <span data-ttu-id="57f50-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-289">Driver's Lics#</span></span>
- <span data-ttu-id="57f50-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="57f50-290">Driver's Licence#</span></span>
- <span data-ttu-id="57f50-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="57f50-291">Driver's Licences#</span></span> 

#### <a name="keyword_australia_drivers_license_number_exclusions"></a><span data-ttu-id="57f50-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="57f50-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="57f50-293">aaa</span><span class="sxs-lookup"><span data-stu-id="57f50-293">aaa</span></span>
- <span data-ttu-id="57f50-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="57f50-294">DriverLicense</span></span>
- <span data-ttu-id="57f50-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="57f50-295">DriverLicenses</span></span>
- <span data-ttu-id="57f50-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="57f50-296">Driver License</span></span>
- <span data-ttu-id="57f50-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-297">Driver Licenses</span></span>
- <span data-ttu-id="57f50-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="57f50-298">DriversLicense</span></span>
- <span data-ttu-id="57f50-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="57f50-299">DriversLicenses</span></span>
- <span data-ttu-id="57f50-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="57f50-300">Drivers License</span></span>
- <span data-ttu-id="57f50-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-301">Drivers Licenses</span></span>
- <span data-ttu-id="57f50-302">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="57f50-302">Driver'License</span></span>
- <span data-ttu-id="57f50-303">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-303">Driver'Licenses</span></span>
- <span data-ttu-id="57f50-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="57f50-304">Driver' License</span></span>
- <span data-ttu-id="57f50-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-305">Driver' Licenses</span></span>
- <span data-ttu-id="57f50-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="57f50-306">Driver'sLicense</span></span>
- <span data-ttu-id="57f50-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="57f50-307">Driver'sLicenses</span></span>
- <span data-ttu-id="57f50-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="57f50-308">Driver's License</span></span>
- <span data-ttu-id="57f50-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-309">Driver's Licenses</span></span>
- <span data-ttu-id="57f50-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="57f50-310">DriverLicense#</span></span>
- <span data-ttu-id="57f50-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-311">DriverLicenses#</span></span>
- <span data-ttu-id="57f50-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="57f50-312">Driver License#</span></span>
- <span data-ttu-id="57f50-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-313">Driver Licenses#</span></span>
- <span data-ttu-id="57f50-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="57f50-314">DriversLicense#</span></span>
- <span data-ttu-id="57f50-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-315">DriversLicenses#</span></span>
- <span data-ttu-id="57f50-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="57f50-316">Drivers License#</span></span>
- <span data-ttu-id="57f50-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-317">Drivers Licenses#</span></span>
- <span data-ttu-id="57f50-318">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="57f50-318">Driver'License#</span></span>
- <span data-ttu-id="57f50-319">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-319">Driver'Licenses#</span></span>
- <span data-ttu-id="57f50-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="57f50-320">Driver' License#</span></span>
- <span data-ttu-id="57f50-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-321">Driver' Licenses#</span></span>
- <span data-ttu-id="57f50-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="57f50-322">Driver'sLicense#</span></span>
- <span data-ttu-id="57f50-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="57f50-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="57f50-324">Driver's License#</span></span>
- <span data-ttu-id="57f50-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="57f50-326">Australische Medical Account-Nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-327">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-327">Format</span></span>

<span data-ttu-id="57f50-328">10-11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-329">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-329">Pattern</span></span>

<span data-ttu-id="57f50-330">10-11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-330">10-11 digits:</span></span>
- <span data-ttu-id="57f50-331">Erste Ziffer im Bereich von 2-6</span><span class="sxs-lookup"><span data-stu-id="57f50-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="57f50-332">Neunte Ziffer ist eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="57f50-333">Zehnte Ziffer ist die Ausgabeziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="57f50-334">Elfte Ziffer (optional) ist die Einzelziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-335">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-335">Checksum</span></span>

<span data-ttu-id="57f50-336">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-337">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-337">Definition</span></span>

<span data-ttu-id="57f50-338">Eine DLP-Richtlinie ist zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-339">Die Funktion Func_australian_medical_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-340">Ein Schlüsselwort aus Keyword_Australia_Medical_Account_Number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="57f50-341">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-341">The checksum passes.</span></span>

<span data-ttu-id="57f50-342">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-343">Die Funktion Func_australian_medical_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-344">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-344">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-345">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-345">Keywords</span></span>

#### <a name="keyword_australia_medical_account_number"></a><span data-ttu-id="57f50-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="57f50-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="57f50-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="57f50-347">bank account details</span></span>
- <span data-ttu-id="57f50-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="57f50-348">medicare payments</span></span>
- <span data-ttu-id="57f50-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="57f50-349">mortgage account</span></span>
- <span data-ttu-id="57f50-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="57f50-350">bank payments</span></span>
- <span data-ttu-id="57f50-351">information branch</span><span class="sxs-lookup"><span data-stu-id="57f50-351">information branch</span></span>
- <span data-ttu-id="57f50-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="57f50-352">credit card loan</span></span>
- <span data-ttu-id="57f50-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="57f50-353">department of human services</span></span>
- <span data-ttu-id="57f50-354">local service</span><span class="sxs-lookup"><span data-stu-id="57f50-354">local service</span></span>
- <span data-ttu-id="57f50-355">Medicare</span><span class="sxs-lookup"><span data-stu-id="57f50-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="57f50-356">Australische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-357">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-357">Format</span></span>

<span data-ttu-id="57f50-358">Ein Buchstabe gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-359">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-359">Pattern</span></span>

<span data-ttu-id="57f50-360">Ein Buchstabe (Groß-/Kleinschreibung irrelevant) gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-361">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-361">Checksum</span></span>

<span data-ttu-id="57f50-362">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-363">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-363">Definition</span></span>

<span data-ttu-id="57f50-364">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-365">Der reguläre Ausdruck Regex_australia_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-366">Ein Schlüsselwort aus Keyword_passport oder Keyword_australia_passport_number wird gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-367">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-367">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="57f50-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="57f50-368">Keyword_passport</span></span>

- <span data-ttu-id="57f50-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="57f50-369">Passport Number</span></span>
- <span data-ttu-id="57f50-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="57f50-370">Passport No</span></span>
- <span data-ttu-id="57f50-371">Passport#</span><span class="sxs-lookup"><span data-stu-id="57f50-371">Passport #</span></span>
- <span data-ttu-id="57f50-372">Pass #</span><span class="sxs-lookup"><span data-stu-id="57f50-372">Passport#</span></span>
- <span data-ttu-id="57f50-373">Passport-Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-373">PassportID</span></span>
- <span data-ttu-id="57f50-374">Passportno</span><span class="sxs-lookup"><span data-stu-id="57f50-374">Passportno</span></span>
- <span data-ttu-id="57f50-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="57f50-375">passportnumber</span></span>
- <span data-ttu-id="57f50-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="57f50-376">パスポート</span></span>
- <span data-ttu-id="57f50-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="57f50-377">パスポート番号</span></span>
- <span data-ttu-id="57f50-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="57f50-378">パスポートのNum</span></span>
- <span data-ttu-id="57f50-379">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="57f50-379">パスポート ＃</span></span> 
- <span data-ttu-id="57f50-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="57f50-380">Numéro de passeport</span></span>
- <span data-ttu-id="57f50-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="57f50-381">Passeport n °</span></span>
- <span data-ttu-id="57f50-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="57f50-382">Passeport Non</span></span>
- <span data-ttu-id="57f50-383">Passeport#</span><span class="sxs-lookup"><span data-stu-id="57f50-383">Passeport #</span></span>
- <span data-ttu-id="57f50-384">Passeport #</span><span class="sxs-lookup"><span data-stu-id="57f50-384">Passeport#</span></span>
- <span data-ttu-id="57f50-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="57f50-385">PasseportNon</span></span>
- <span data-ttu-id="57f50-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="57f50-386">Passeportn °</span></span>

#### <a name="keyword_australia_passport_number"></a><span data-ttu-id="57f50-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="57f50-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="57f50-388">Pass</span><span class="sxs-lookup"><span data-stu-id="57f50-388">passport</span></span>
- <span data-ttu-id="57f50-389">passport details</span><span class="sxs-lookup"><span data-stu-id="57f50-389">passport details</span></span>
- <span data-ttu-id="57f50-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="57f50-390">immigration and citizenship</span></span>
- <span data-ttu-id="57f50-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="57f50-391">commonwealth of australia</span></span>
- <span data-ttu-id="57f50-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="57f50-392">department of immigration</span></span>
- <span data-ttu-id="57f50-393">residential address</span><span class="sxs-lookup"><span data-stu-id="57f50-393">residential address</span></span>
- <span data-ttu-id="57f50-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="57f50-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="57f50-395">Visa</span><span class="sxs-lookup"><span data-stu-id="57f50-395">visa</span></span>
- <span data-ttu-id="57f50-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="57f50-396">national identity card</span></span>
- <span data-ttu-id="57f50-397">passport number</span><span class="sxs-lookup"><span data-stu-id="57f50-397">passport number</span></span>
- <span data-ttu-id="57f50-398">travel document</span><span class="sxs-lookup"><span data-stu-id="57f50-398">travel document</span></span>
- <span data-ttu-id="57f50-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="57f50-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="57f50-400">Australische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="57f50-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-401">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-401">Format</span></span>

<span data-ttu-id="57f50-402">8-9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-403">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-403">Pattern</span></span>

<span data-ttu-id="57f50-404">8 bis 9 Ziffern, die in der Regel wie folgt mit Leerzeichen dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="57f50-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="57f50-405">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-405">Three digits</span></span> 
- <span data-ttu-id="57f50-406">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-406">An optional space</span></span> 
- <span data-ttu-id="57f50-407">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-407">Three digits</span></span> 
- <span data-ttu-id="57f50-408">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-408">An optional space</span></span> 
- <span data-ttu-id="57f50-409">2 bis 3 Ziffern, wobei die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="57f50-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-410">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-410">Checksum</span></span>

<span data-ttu-id="57f50-411">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-412">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-412">Definition</span></span>

<span data-ttu-id="57f50-413">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-414">Die Funktion Func_australian_tax_file_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-415">Es wurde kein Schlüsselwort aus Keyword_Australia_Tax_File_Number oder Keyword_number_exclusions gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="57f50-416">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-416">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-417">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-417">Keywords</span></span>

#### <a name="keyword_australia_tax_file_number"></a><span data-ttu-id="57f50-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="57f50-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="57f50-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="57f50-419">australian business number</span></span>
- <span data-ttu-id="57f50-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="57f50-420">marginal tax rate</span></span>
- <span data-ttu-id="57f50-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="57f50-421">medicare levy</span></span>
- <span data-ttu-id="57f50-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="57f50-422">portfolio number</span></span>
- <span data-ttu-id="57f50-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="57f50-423">service veterans</span></span>
- <span data-ttu-id="57f50-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="57f50-424">withholding tax</span></span>
- <span data-ttu-id="57f50-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="57f50-425">individual tax return</span></span>
- <span data-ttu-id="57f50-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="57f50-426">tax file number</span></span>

#### <a name="keyword_number_exclusions"></a><span data-ttu-id="57f50-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="57f50-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="57f50-428">00000000</span><span class="sxs-lookup"><span data-stu-id="57f50-428">00000000</span></span>
- <span data-ttu-id="57f50-429">11111111</span><span class="sxs-lookup"><span data-stu-id="57f50-429">11111111</span></span>
- <span data-ttu-id="57f50-430">22222222</span><span class="sxs-lookup"><span data-stu-id="57f50-430">22222222</span></span>
- <span data-ttu-id="57f50-431">33333333</span><span class="sxs-lookup"><span data-stu-id="57f50-431">33333333</span></span>
- <span data-ttu-id="57f50-432">44444444</span><span class="sxs-lookup"><span data-stu-id="57f50-432">44444444</span></span>
- <span data-ttu-id="57f50-433">55555555</span><span class="sxs-lookup"><span data-stu-id="57f50-433">55555555</span></span>
- <span data-ttu-id="57f50-434">66666666</span><span class="sxs-lookup"><span data-stu-id="57f50-434">66666666</span></span>
- <span data-ttu-id="57f50-435">77777777</span><span class="sxs-lookup"><span data-stu-id="57f50-435">77777777</span></span>
- <span data-ttu-id="57f50-436">88888888</span><span class="sxs-lookup"><span data-stu-id="57f50-436">88888888</span></span>
- <span data-ttu-id="57f50-437">99999999</span><span class="sxs-lookup"><span data-stu-id="57f50-437">99999999</span></span>
- <span data-ttu-id="57f50-438">000000000</span><span class="sxs-lookup"><span data-stu-id="57f50-438">000000000</span></span>
- <span data-ttu-id="57f50-439">111111111</span><span class="sxs-lookup"><span data-stu-id="57f50-439">111111111</span></span>
- <span data-ttu-id="57f50-440">222222222</span><span class="sxs-lookup"><span data-stu-id="57f50-440">222222222</span></span>
- <span data-ttu-id="57f50-441">333333333</span><span class="sxs-lookup"><span data-stu-id="57f50-441">333333333</span></span>
- <span data-ttu-id="57f50-442">444444444</span><span class="sxs-lookup"><span data-stu-id="57f50-442">444444444</span></span>
- <span data-ttu-id="57f50-443">555555555</span><span class="sxs-lookup"><span data-stu-id="57f50-443">555555555</span></span>
- <span data-ttu-id="57f50-444">666666666</span><span class="sxs-lookup"><span data-stu-id="57f50-444">666666666</span></span>
- <span data-ttu-id="57f50-445">777777777</span><span class="sxs-lookup"><span data-stu-id="57f50-445">777777777</span></span>
- <span data-ttu-id="57f50-446">888888888</span><span class="sxs-lookup"><span data-stu-id="57f50-446">888888888</span></span>
- <span data-ttu-id="57f50-447">999999999</span><span class="sxs-lookup"><span data-stu-id="57f50-447">999999999</span></span>
- <span data-ttu-id="57f50-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="57f50-448">0000000000</span></span>
- <span data-ttu-id="57f50-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="57f50-449">1111111111</span></span>
- <span data-ttu-id="57f50-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="57f50-450">2222222222</span></span>
- <span data-ttu-id="57f50-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="57f50-451">3333333333</span></span>
- <span data-ttu-id="57f50-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="57f50-452">4444444444</span></span>
- <span data-ttu-id="57f50-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="57f50-453">5555555555</span></span>
- <span data-ttu-id="57f50-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="57f50-454">6666666666</span></span>
- <span data-ttu-id="57f50-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="57f50-455">7777777777</span></span>
- <span data-ttu-id="57f50-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="57f50-456">8888888888</span></span>
- <span data-ttu-id="57f50-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="57f50-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="57f50-458">Azure DocumentDB-Authentifizierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="57f50-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="57f50-459">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-459">Format</span></span>

<span data-ttu-id="57f50-460">Die Zeichenfolge "DocumentDb" gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="57f50-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-461">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-461">Pattern</span></span>

- <span data-ttu-id="57f50-462">Die Zeichenfolge "DocumentDb"</span><span class="sxs-lookup"><span data-stu-id="57f50-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="57f50-463">Eine beliebige Kombination von zwischen 3-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="57f50-464">Ein größer als-Symbol (#a0), ein Gleichheitszeichen (=), ein Anführungszeichen (") oder ein Apostroph (')</span><span class="sxs-lookup"><span data-stu-id="57f50-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="57f50-465">Eine beliebige Kombination von 86 unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="57f50-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="57f50-466">Zwei Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-467">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-467">Checksum</span></span>

<span data-ttu-id="57f50-468">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-469">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-469">Definition</span></span>

<span data-ttu-id="57f50-470">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-471">Der reguläre Ausdruck CEP_Regex_AzureDocumentDBAuthKey sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-472">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-473">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-473">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="57f50-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="57f50-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="57f50-475">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="57f50-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="57f50-476">contoso</span><span class="sxs-lookup"><span data-stu-id="57f50-476">contoso</span></span>
- <span data-ttu-id="57f50-477">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="57f50-477">fabrikam</span></span>
- <span data-ttu-id="57f50-478">Northwind</span><span class="sxs-lookup"><span data-stu-id="57f50-478">northwind</span></span>
- <span data-ttu-id="57f50-479">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="57f50-479">sandbox</span></span>
- <span data-ttu-id="57f50-480">OneBox</span><span class="sxs-lookup"><span data-stu-id="57f50-480">onebox</span></span>
- <span data-ttu-id="57f50-481">localhost</span><span class="sxs-lookup"><span data-stu-id="57f50-481">localhost</span></span>
- <span data-ttu-id="57f50-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="57f50-482">127.0.0.1</span></span>
- <span data-ttu-id="57f50-483">testacs.</span><span class="sxs-lookup"><span data-stu-id="57f50-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-484">com</span><span class="sxs-lookup"><span data-stu-id="57f50-484">com</span></span>
- <span data-ttu-id="57f50-485">s-int.</span><span class="sxs-lookup"><span data-stu-id="57f50-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-486">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="57f50-487">Azure IaaS-Datenbankverbindungszeichenfolge und Azure SQL-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57f50-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="57f50-488">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-488">Format</span></span>

<span data-ttu-id="57f50-489">Die Zeichenfolge "Server", "Server" oder "Datenquelle", gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten, einschließlich der Zeichenfolge "cloudapp. Azure" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="57f50-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-490">com "oder" cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="57f50-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-491">NET "oder" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="57f50-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-492">NET "und die Zeichenfolge" Password "oder" Password "oder" pwd ".</span><span class="sxs-lookup"><span data-stu-id="57f50-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-493">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-493">Pattern</span></span>

- <span data-ttu-id="57f50-494">Die Zeichenfolge "Server", "Server" oder "Datenquelle"</span><span class="sxs-lookup"><span data-stu-id="57f50-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="57f50-495">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-496">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-496">An equal sign (=)</span></span>
- <span data-ttu-id="57f50-497">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-498">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="57f50-499">Die Zeichenfolge "cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="57f50-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-500">com "," cloudapp. Azure.</span><span class="sxs-lookup"><span data-stu-id="57f50-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-501">NET "oder" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="57f50-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-502">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-502">net"</span></span>
- <span data-ttu-id="57f50-503">Eine beliebige Kombination von zwischen 1-300 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="57f50-504">Die Zeichenfolge "Password", "Password" oder "pwd"</span><span class="sxs-lookup"><span data-stu-id="57f50-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="57f50-505">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-506">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-506">An equal sign (=)</span></span>
- <span data-ttu-id="57f50-507">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-508">Ein oder mehrere Zeichen, bei denen es sich nicht um ein Semikolon handelt (;), Anführungszeichen (") oder Apostroph (')</span><span class="sxs-lookup"><span data-stu-id="57f50-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="57f50-509">Ein Semikolon (;), Anführungszeichen (") oder Apostroph (')</span><span class="sxs-lookup"><span data-stu-id="57f50-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-510">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-510">Checksum</span></span>

<span data-ttu-id="57f50-511">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-512">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-512">Definition</span></span>

<span data-ttu-id="57f50-513">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-514">Der reguläre Ausdruck CEP_Regex_AzureConnectionString sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-515">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-516">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-516">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="57f50-517">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="57f50-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="57f50-518">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="57f50-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="57f50-519">contoso</span><span class="sxs-lookup"><span data-stu-id="57f50-519">contoso</span></span>
- <span data-ttu-id="57f50-520">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="57f50-520">fabrikam</span></span>
- <span data-ttu-id="57f50-521">Northwind</span><span class="sxs-lookup"><span data-stu-id="57f50-521">northwind</span></span>
- <span data-ttu-id="57f50-522">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="57f50-522">sandbox</span></span>
- <span data-ttu-id="57f50-523">OneBox</span><span class="sxs-lookup"><span data-stu-id="57f50-523">onebox</span></span>
- <span data-ttu-id="57f50-524">localhost</span><span class="sxs-lookup"><span data-stu-id="57f50-524">localhost</span></span>
- <span data-ttu-id="57f50-525">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="57f50-525">127.0.0.1</span></span>
- <span data-ttu-id="57f50-526">testacs.</span><span class="sxs-lookup"><span data-stu-id="57f50-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-527">com</span><span class="sxs-lookup"><span data-stu-id="57f50-527">com</span></span>
- <span data-ttu-id="57f50-528">s-int.</span><span class="sxs-lookup"><span data-stu-id="57f50-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-529">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="57f50-530">Azurey-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57f50-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="57f50-531">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-531">Format</span></span>

<span data-ttu-id="57f50-532">Die Zeichenfolge "Hostname" gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten beschrieben sind, einschließlich der Zeichenfolgen "Azure-Devices".</span><span class="sxs-lookup"><span data-stu-id="57f50-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-533">NET "und" SharedAccessKey ".</span><span class="sxs-lookup"><span data-stu-id="57f50-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-534">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-534">Pattern</span></span>

- <span data-ttu-id="57f50-535">Die Zeichenfolge "Hostname"</span><span class="sxs-lookup"><span data-stu-id="57f50-535">The string "HostName"</span></span>
- <span data-ttu-id="57f50-536">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-537">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-537">An equal sign (=)</span></span>
- <span data-ttu-id="57f50-538">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-539">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="57f50-540">Die Zeichenfolge "Azure-Devices.</span><span class="sxs-lookup"><span data-stu-id="57f50-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-541">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-541">net"</span></span>
- <span data-ttu-id="57f50-542">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="57f50-543">Die Zeichenfolge "SharedAccessKey"</span><span class="sxs-lookup"><span data-stu-id="57f50-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="57f50-544">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-545">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-545">An equal sign (=)</span></span>
- <span data-ttu-id="57f50-546">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-547">Eine beliebige Kombination von 43 unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="57f50-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="57f50-548">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-549">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-549">Checksum</span></span>

<span data-ttu-id="57f50-550">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-551">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-551">Definition</span></span>

<span data-ttu-id="57f50-552">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-553">Der reguläre Ausdruck CEP_Regex_AzureIoTConnectionString sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-554">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-555">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-555">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="57f50-556">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="57f50-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="57f50-557">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="57f50-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="57f50-558">contoso</span><span class="sxs-lookup"><span data-stu-id="57f50-558">contoso</span></span>
- <span data-ttu-id="57f50-559">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="57f50-559">fabrikam</span></span>
- <span data-ttu-id="57f50-560">Northwind</span><span class="sxs-lookup"><span data-stu-id="57f50-560">northwind</span></span>
- <span data-ttu-id="57f50-561">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="57f50-561">sandbox</span></span>
- <span data-ttu-id="57f50-562">OneBox</span><span class="sxs-lookup"><span data-stu-id="57f50-562">onebox</span></span>
- <span data-ttu-id="57f50-563">localhost</span><span class="sxs-lookup"><span data-stu-id="57f50-563">localhost</span></span>
- <span data-ttu-id="57f50-564">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="57f50-564">127.0.0.1</span></span>
- <span data-ttu-id="57f50-565">testacs.</span><span class="sxs-lookup"><span data-stu-id="57f50-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-566">com</span><span class="sxs-lookup"><span data-stu-id="57f50-566">com</span></span>
- <span data-ttu-id="57f50-567">s-int.</span><span class="sxs-lookup"><span data-stu-id="57f50-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-568">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="57f50-569">Kennwort für Azure-Veröffentlichungseinstellung</span><span class="sxs-lookup"><span data-stu-id="57f50-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="57f50-570">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-570">Format</span></span>

<span data-ttu-id="57f50-571">Die Zeichenfolge "benutzerkwt =" gefolgt von einer alphanumerischen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="57f50-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-572">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-572">Pattern</span></span>

- <span data-ttu-id="57f50-573">Die Zeichenfolge "benutzerkwt ="</span><span class="sxs-lookup"><span data-stu-id="57f50-573">The string "userpwd="</span></span>
- <span data-ttu-id="57f50-574">Eine beliebige Kombination von 60 Kleinbuchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="57f50-575">Ein Anführungszeichen (")</span><span class="sxs-lookup"><span data-stu-id="57f50-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-576">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-576">Checksum</span></span>

<span data-ttu-id="57f50-577">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-578">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-578">Definition</span></span>

<span data-ttu-id="57f50-579">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-580">Der reguläre Ausdruck CEP_Regex_AzurePublishSettingPasswords sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-581">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-582">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-582">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="57f50-583">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="57f50-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="57f50-584">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="57f50-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="57f50-585">contoso</span><span class="sxs-lookup"><span data-stu-id="57f50-585">contoso</span></span>
- <span data-ttu-id="57f50-586">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="57f50-586">fabrikam</span></span>
- <span data-ttu-id="57f50-587">Northwind</span><span class="sxs-lookup"><span data-stu-id="57f50-587">northwind</span></span>
- <span data-ttu-id="57f50-588">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="57f50-588">sandbox</span></span>
- <span data-ttu-id="57f50-589">OneBox</span><span class="sxs-lookup"><span data-stu-id="57f50-589">onebox</span></span>
- <span data-ttu-id="57f50-590">localhost</span><span class="sxs-lookup"><span data-stu-id="57f50-590">localhost</span></span>
- <span data-ttu-id="57f50-591">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="57f50-591">127.0.0.1</span></span>
- <span data-ttu-id="57f50-592">testacs.</span><span class="sxs-lookup"><span data-stu-id="57f50-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-593">com</span><span class="sxs-lookup"><span data-stu-id="57f50-593">com</span></span>
- <span data-ttu-id="57f50-594">s-int.</span><span class="sxs-lookup"><span data-stu-id="57f50-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-595">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="57f50-596">Azure-Zeichenfolgen-Cache-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57f50-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="57f50-597">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-597">Format</span></span>

<span data-ttu-id="57f50-598">Die Zeichenfolge "" Codestring. Cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="57f50-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-599">NET ", gefolgt von den Zeichen und Zeichenfolgen, die im folgenden Muster dargestellt werden, einschließlich der Zeichenfolge" Password "oder" pwd ".</span><span class="sxs-lookup"><span data-stu-id="57f50-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-600">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-600">Pattern</span></span>

- <span data-ttu-id="57f50-601">Die Zeichenfolge "" Codestring. Cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="57f50-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-602">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-602">net"</span></span>
- <span data-ttu-id="57f50-603">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="57f50-604">Die Zeichenfolge "Password" oder "pwd"</span><span class="sxs-lookup"><span data-stu-id="57f50-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="57f50-605">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-606">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-606">An equal sign (=)</span></span>
- <span data-ttu-id="57f50-607">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-608">Eine beliebige Kombination von 43 Zeichen mit unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="57f50-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="57f50-609">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-610">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-610">Checksum</span></span>

<span data-ttu-id="57f50-611">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-612">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-612">Definition</span></span>

<span data-ttu-id="57f50-613">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-614">Der reguläre Ausdruck CEP_Regex_AzureRedisCacheConnectionString sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="57f50-615">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-616">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-616">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="57f50-617">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="57f50-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="57f50-618">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="57f50-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="57f50-619">contoso</span><span class="sxs-lookup"><span data-stu-id="57f50-619">contoso</span></span>
- <span data-ttu-id="57f50-620">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="57f50-620">fabrikam</span></span>
- <span data-ttu-id="57f50-621">Northwind</span><span class="sxs-lookup"><span data-stu-id="57f50-621">northwind</span></span>
- <span data-ttu-id="57f50-622">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="57f50-622">sandbox</span></span>
- <span data-ttu-id="57f50-623">OneBox</span><span class="sxs-lookup"><span data-stu-id="57f50-623">onebox</span></span>
- <span data-ttu-id="57f50-624">localhost</span><span class="sxs-lookup"><span data-stu-id="57f50-624">localhost</span></span>
- <span data-ttu-id="57f50-625">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="57f50-625">127.0.0.1</span></span>
- <span data-ttu-id="57f50-626">testacs.</span><span class="sxs-lookup"><span data-stu-id="57f50-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-627">com</span><span class="sxs-lookup"><span data-stu-id="57f50-627">com</span></span>
- <span data-ttu-id="57f50-628">s-int.</span><span class="sxs-lookup"><span data-stu-id="57f50-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-629">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="57f50-630">Azure-SAS</span><span class="sxs-lookup"><span data-stu-id="57f50-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="57f50-631">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-631">Format</span></span>

<span data-ttu-id="57f50-632">Die Zeichenfolge "SIG" gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="57f50-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-633">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-633">Pattern</span></span>

- <span data-ttu-id="57f50-634">Die Zeichenfolge "SIG"</span><span class="sxs-lookup"><span data-stu-id="57f50-634">The string "sig"</span></span>
- <span data-ttu-id="57f50-635">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-636">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-636">An equal sign (=)</span></span>
- <span data-ttu-id="57f50-637">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-638">Eine beliebige Kombination von zwischen 43-53 Zeichen, die klein-oder Großbuchstaben, Ziffern oder das Prozentzeichen (%)</span><span class="sxs-lookup"><span data-stu-id="57f50-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="57f50-639">Die Zeichenfolge "% 3D"</span><span class="sxs-lookup"><span data-stu-id="57f50-639">The string "%3d"</span></span>
- <span data-ttu-id="57f50-640">Ein beliebiges Zeichen, das kein niedriger oder groß geschriebener Buchstabe, eine Ziffer oder ein Prozentzeichen ist (%)</span><span class="sxs-lookup"><span data-stu-id="57f50-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-641">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-641">Checksum</span></span>

<span data-ttu-id="57f50-642">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-643">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-643">Definition</span></span>

<span data-ttu-id="57f50-644">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-645">Der reguläre Ausdruck CEP_Regex_AzureSAS sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```xml
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="57f50-646">Azure Service Bus-Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57f50-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="57f50-647">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-647">Format</span></span>

<span data-ttu-id="57f50-648">Die Zeichenfolge "Endpoint" gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten, einschließlich der Zeichenfolgen "ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="57f50-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-649">NET "und" SharedAccesKey ".</span><span class="sxs-lookup"><span data-stu-id="57f50-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-650">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-650">Pattern</span></span>

- <span data-ttu-id="57f50-651">Die Zeichenfolge "Endpoint"</span><span class="sxs-lookup"><span data-stu-id="57f50-651">The string "EndPoint"</span></span>
- <span data-ttu-id="57f50-652">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-653">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-653">An equal sign (=)</span></span>
- <span data-ttu-id="57f50-654">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-655">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="57f50-656">Die Zeichenfolge "ServiceBus. Windows.</span><span class="sxs-lookup"><span data-stu-id="57f50-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-657">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-657">net"</span></span>
- <span data-ttu-id="57f50-658">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="57f50-659">Die Zeichenfolge "SharedAccessKey"</span><span class="sxs-lookup"><span data-stu-id="57f50-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="57f50-660">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-661">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-661">An equal sign (=)</span></span>
- <span data-ttu-id="57f50-662">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-663">Eine beliebige Kombination von 43 Zeichen mit unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="57f50-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="57f50-664">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-665">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-665">Checksum</span></span>

<span data-ttu-id="57f50-666">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-667">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-667">Definition</span></span>

<span data-ttu-id="57f50-668">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-669">Der reguläre Ausdruck CEP_Regex_AzureServiceBusConnectionString sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="57f50-670">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-671">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-671">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="57f50-672">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="57f50-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="57f50-673">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="57f50-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="57f50-674">contoso</span><span class="sxs-lookup"><span data-stu-id="57f50-674">contoso</span></span>
- <span data-ttu-id="57f50-675">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="57f50-675">fabrikam</span></span>
- <span data-ttu-id="57f50-676">Northwind</span><span class="sxs-lookup"><span data-stu-id="57f50-676">northwind</span></span>
- <span data-ttu-id="57f50-677">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="57f50-677">sandbox</span></span>
- <span data-ttu-id="57f50-678">OneBox</span><span class="sxs-lookup"><span data-stu-id="57f50-678">onebox</span></span>
- <span data-ttu-id="57f50-679">localhost</span><span class="sxs-lookup"><span data-stu-id="57f50-679">localhost</span></span>
- <span data-ttu-id="57f50-680">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="57f50-680">127.0.0.1</span></span>
- <span data-ttu-id="57f50-681">testacs.</span><span class="sxs-lookup"><span data-stu-id="57f50-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-682">com</span><span class="sxs-lookup"><span data-stu-id="57f50-682">com</span></span>
- <span data-ttu-id="57f50-683">s-int.</span><span class="sxs-lookup"><span data-stu-id="57f50-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-684">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="57f50-685">Azure Storage-Kontoschlüssel</span><span class="sxs-lookup"><span data-stu-id="57f50-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="57f50-686">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-686">Format</span></span>

<span data-ttu-id="57f50-687">Die Zeichenfolge "DefaultEndpointsProtocol", gefolgt von den Zeichen und Zeichenfolgen, die in dem Muster unten, einschließlich der Zeichenfolge "AccountKey", dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="57f50-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-688">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-688">Pattern</span></span>

- <span data-ttu-id="57f50-689">Die Zeichenfolge "DefaultEndpointsProtocol"</span><span class="sxs-lookup"><span data-stu-id="57f50-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="57f50-690">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-691">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-691">An equal sign (=)</span></span>
- <span data-ttu-id="57f50-692">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-693">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="57f50-694">Die Zeichenfolge "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="57f50-694">The string "AccountKey"</span></span>
- <span data-ttu-id="57f50-695">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-696">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-696">An equal sign (=)</span></span>
- <span data-ttu-id="57f50-697">0-2 Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="57f50-698">Eine beliebige Kombination von 86 Zeichen mit unter-oder Großbuchstaben, Ziffern, Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="57f50-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="57f50-699">Zwei Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-700">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-700">Checksum</span></span>

<span data-ttu-id="57f50-701">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-702">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-702">Definition</span></span>

<span data-ttu-id="57f50-703">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-704">Der reguläre Ausdruck CEP_Regex_AzureStorageAccountKey sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-705">Der reguläre Ausdruck CEP_AzureEmulatorStorageAccountFilter findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-706">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-707">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-707">Keywords</span></span>

#### <a name="cep_azureemulatorstorageaccountfilter"></a><span data-ttu-id="57f50-708">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="57f50-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="57f50-709">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="57f50-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="57f50-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw = =</span><span class="sxs-lookup"><span data-stu-id="57f50-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="57f50-711">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="57f50-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="57f50-712">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="57f50-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="57f50-713">contoso</span><span class="sxs-lookup"><span data-stu-id="57f50-713">contoso</span></span>
- <span data-ttu-id="57f50-714">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="57f50-714">fabrikam</span></span>
- <span data-ttu-id="57f50-715">Northwind</span><span class="sxs-lookup"><span data-stu-id="57f50-715">northwind</span></span>
- <span data-ttu-id="57f50-716">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="57f50-716">sandbox</span></span>
- <span data-ttu-id="57f50-717">OneBox</span><span class="sxs-lookup"><span data-stu-id="57f50-717">onebox</span></span>
- <span data-ttu-id="57f50-718">localhost</span><span class="sxs-lookup"><span data-stu-id="57f50-718">localhost</span></span>
- <span data-ttu-id="57f50-719">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="57f50-719">127.0.0.1</span></span>
- <span data-ttu-id="57f50-720">testacs.</span><span class="sxs-lookup"><span data-stu-id="57f50-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-721">com</span><span class="sxs-lookup"><span data-stu-id="57f50-721">com</span></span>
- <span data-ttu-id="57f50-722">s-int.</span><span class="sxs-lookup"><span data-stu-id="57f50-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-723">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="57f50-724">Azure Storage-Kontoschlüssel (generisch)</span><span class="sxs-lookup"><span data-stu-id="57f50-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-725">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-725">Format</span></span>

<span data-ttu-id="57f50-726">Eine beliebige Kombination von 86 unter-oder Großbuchstaben, Ziffern, den Schrägstrich (/) oder Pluszeichen (+), vorangestellt oder gefolgt von den im Muster unten beschriebenen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="57f50-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-727">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-727">Pattern</span></span>

- <span data-ttu-id="57f50-728">0-1 des größer als-Symbols (#a0), Apostroph ('), Gleichheitszeichen (=), Anführungszeichen (") oder Nummernzeichen (#)</span><span class="sxs-lookup"><span data-stu-id="57f50-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="57f50-729">Eine beliebige Kombination von 86 Zeichen mit unter-oder Großbuchstaben, Ziffern, dem Schrägstrich (/) oder Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="57f50-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="57f50-730">Zwei Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="57f50-731">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-731">Checksum</span></span>

<span data-ttu-id="57f50-732">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-733">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-733">Definition</span></span>

<span data-ttu-id="57f50-734">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-735">Der reguläre Ausdruck CEP_Regex_AzureStorageAccountKeyGeneric sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```xml
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="57f50-736">Belgien – Nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-737">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-737">Format</span></span>

<span data-ttu-id="57f50-738">11 Ziffern plus Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-739">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-739">Pattern</span></span>

<span data-ttu-id="57f50-740">11 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="57f50-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="57f50-741">Sechs Ziffern und zwei Punkte im Format JJ.MM.TT für das Geburtsdatum </span><span class="sxs-lookup"><span data-stu-id="57f50-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="57f50-742">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-742">A hyphen</span></span> 
- <span data-ttu-id="57f50-743">Drei aufeinander folgende Ziffern (ungerade für Männer, gerade für Frauen) </span><span class="sxs-lookup"><span data-stu-id="57f50-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="57f50-744">Ein Punkt</span><span class="sxs-lookup"><span data-stu-id="57f50-744">A period</span></span> 
- <span data-ttu-id="57f50-745">Zwei Ziffern als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-746">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-746">Checksum</span></span>

<span data-ttu-id="57f50-747">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-748">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-748">Definition</span></span>

<span data-ttu-id="57f50-749">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-750">Die Funktion Func_belgium_national_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-751">Ein Schlüsselwort aus Keyword_belgium_national_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="57f50-752">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-752">The checksum passes.</span></span>

```xml
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-753">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-753">Keywords</span></span>

#### <a name="keyword_belgium_national_number"></a><span data-ttu-id="57f50-754">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="57f50-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="57f50-755">Identität</span><span class="sxs-lookup"><span data-stu-id="57f50-755">Identity</span></span>
- <span data-ttu-id="57f50-756">Registrierung</span><span class="sxs-lookup"><span data-stu-id="57f50-756">Registration</span></span>
- <span data-ttu-id="57f50-757">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="57f50-757">Identification</span></span> 
- <span data-ttu-id="57f50-758">ID</span><span class="sxs-lookup"><span data-stu-id="57f50-758">ID</span></span> 
- <span data-ttu-id="57f50-759">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="57f50-759">Identiteitskaart</span></span>
- <span data-ttu-id="57f50-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-760">Registratie nummer</span></span> 
- <span data-ttu-id="57f50-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-761">Identificatie nummer</span></span> 
- <span data-ttu-id="57f50-762">Identiteit</span><span class="sxs-lookup"><span data-stu-id="57f50-762">Identiteit</span></span>
- <span data-ttu-id="57f50-763">Registratie</span><span class="sxs-lookup"><span data-stu-id="57f50-763">Registratie</span></span>
- <span data-ttu-id="57f50-764">Identificatie</span><span class="sxs-lookup"><span data-stu-id="57f50-764">Identificatie</span></span> 
- <span data-ttu-id="57f50-765">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="57f50-765">Carte d’identité</span></span> 
- <span data-ttu-id="57f50-766">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="57f50-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="57f50-767">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="57f50-767">numéro d'identification</span></span>
- <span data-ttu-id="57f50-768">identité</span><span class="sxs-lookup"><span data-stu-id="57f50-768">identité</span></span> 
- <span data-ttu-id="57f50-769">Inschrift</span><span class="sxs-lookup"><span data-stu-id="57f50-769">inscription</span></span> 
- <span data-ttu-id="57f50-770">Identifikation</span><span class="sxs-lookup"><span data-stu-id="57f50-770">Identifikation</span></span>
- <span data-ttu-id="57f50-771">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="57f50-771">Identifizierung</span></span>
- <span data-ttu-id="57f50-772">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-772">Identifikationsnummer</span></span>
- <span data-ttu-id="57f50-773">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-773">Personalausweis</span></span>
- <span data-ttu-id="57f50-774">Registrierung</span><span class="sxs-lookup"><span data-stu-id="57f50-774">Registrierung</span></span>
- <span data-ttu-id="57f50-775">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="57f50-776">Brazil CPF Number</span><span class="sxs-lookup"><span data-stu-id="57f50-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-777">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-777">Format</span></span>

<span data-ttu-id="57f50-778">11 Ziffern, die eine Prüfziffer umfassen und die formatiert oder unformatiert sein können</span><span class="sxs-lookup"><span data-stu-id="57f50-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-779">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-779">Pattern</span></span>

<span data-ttu-id="57f50-780">Formatiert</span><span class="sxs-lookup"><span data-stu-id="57f50-780">Formatted:</span></span>
- <span data-ttu-id="57f50-781">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-781">Three digits</span></span> 
- <span data-ttu-id="57f50-782">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="57f50-782">A period</span></span> 
- <span data-ttu-id="57f50-783">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-783">Three digits</span></span> 
- <span data-ttu-id="57f50-784">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="57f50-784">A period</span></span> 
- <span data-ttu-id="57f50-785">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-785">Three digits</span></span> 
- <span data-ttu-id="57f50-786">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-786">A hyphen</span></span> 
- <span data-ttu-id="57f50-787">Zwei Ziffern, die Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="57f50-787">Two digits which are check digits</span></span>

<span data-ttu-id="57f50-788">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="57f50-788">Unformatted:</span></span>
- <span data-ttu-id="57f50-789">11 Ziffern, wobei die letzten beiden Ziffern Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="57f50-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-790">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-790">Checksum</span></span>

<span data-ttu-id="57f50-791">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-792">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-792">Definition</span></span>

<span data-ttu-id="57f50-793">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-794">Die Funktion Func_brazil_cpf findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-795">Ein Schlüsselwort aus Keyword_brazil_cpf wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="57f50-796">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-796">The checksum passes.</span></span>

<span data-ttu-id="57f50-797">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-798">Die Funktion Func_brazil_cpf findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-799">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-799">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-800">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-800">Keywords</span></span>

#### <a name="keyword_brazil_cpf"></a><span data-ttu-id="57f50-801">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="57f50-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="57f50-802">CPF</span><span class="sxs-lookup"><span data-stu-id="57f50-802">CPF</span></span>
- <span data-ttu-id="57f50-803">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="57f50-803">Identification</span></span>
- <span data-ttu-id="57f50-804">Registrierung</span><span class="sxs-lookup"><span data-stu-id="57f50-804">Registration</span></span>
- <span data-ttu-id="57f50-805">Umsatz</span><span class="sxs-lookup"><span data-stu-id="57f50-805">Revenue</span></span>
- <span data-ttu-id="57f50-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="57f50-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="57f50-807">Imposto</span><span class="sxs-lookup"><span data-stu-id="57f50-807">Imposto</span></span> 
- <span data-ttu-id="57f50-808">Identificação</span><span class="sxs-lookup"><span data-stu-id="57f50-808">Identificação</span></span> 
- <span data-ttu-id="57f50-809">Inscrição</span><span class="sxs-lookup"><span data-stu-id="57f50-809">Inscrição</span></span> 
- <span data-ttu-id="57f50-810">Receita</span><span class="sxs-lookup"><span data-stu-id="57f50-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="57f50-811">Brasilien – Juristische Personennummer (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="57f50-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-812">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-812">Format</span></span>

<span data-ttu-id="57f50-813">14 Ziffern, die eine Registrierungsnummer, eine Zweignummer und Prüfnziffern sowie Trennzeichen umfassen</span><span class="sxs-lookup"><span data-stu-id="57f50-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-814">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-814">Pattern</span></span>
<span data-ttu-id="57f50-815">14 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="57f50-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="57f50-816">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-816">Two digits</span></span> 
- <span data-ttu-id="57f50-817">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="57f50-817">A period</span></span> 
- <span data-ttu-id="57f50-818">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-818">Three digits</span></span> 
- <span data-ttu-id="57f50-819">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="57f50-819">A period</span></span> 
- <span data-ttu-id="57f50-820">Drei Ziffern (diese ersten acht Ziffern sind die Registrierungsnummer) </span><span class="sxs-lookup"><span data-stu-id="57f50-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="57f50-821">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="57f50-821">A forward slash</span></span> 
- <span data-ttu-id="57f50-822">Vierstellige Zweignummer </span><span class="sxs-lookup"><span data-stu-id="57f50-822">Four-digit branch number</span></span> 
- <span data-ttu-id="57f50-823">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-823">A hyphen</span></span> 
- <span data-ttu-id="57f50-824">Zwei Ziffern, die Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="57f50-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-825">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-825">Checksum</span></span>

<span data-ttu-id="57f50-826">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-827">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-827">Definition</span></span>

<span data-ttu-id="57f50-828">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-829">Die Funktion Func_brazil_cnpj findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-830">Ein Schlüsselwort aus Keyword_brazil_cnpj wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="57f50-831">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-831">The checksum passes.</span></span>

<span data-ttu-id="57f50-832">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-833">Die Funktion Func_brazil_cnpj findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-834">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-834">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-835">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-835">Keywords</span></span>

#### <a name="keyword_brazil_cnpj"></a><span data-ttu-id="57f50-836">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="57f50-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="57f50-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="57f50-837">CNPJ</span></span> 
- <span data-ttu-id="57f50-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="57f50-838">CNPJ/MF</span></span> 
- <span data-ttu-id="57f50-839">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="57f50-839">CNPJ-MF</span></span> 
- <span data-ttu-id="57f50-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="57f50-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="57f50-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="57f50-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="57f50-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="57f50-842">Legal entity</span></span> 
- <span data-ttu-id="57f50-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="57f50-843">Legal entities</span></span> 
- <span data-ttu-id="57f50-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="57f50-844">Registration Status</span></span> 
- <span data-ttu-id="57f50-845">Business</span><span class="sxs-lookup"><span data-stu-id="57f50-845">Business</span></span> 
- <span data-ttu-id="57f50-846">Company</span><span class="sxs-lookup"><span data-stu-id="57f50-846">Company</span></span>
- <span data-ttu-id="57f50-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="57f50-847">CNPJ</span></span> 
- <span data-ttu-id="57f50-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="57f50-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="57f50-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="57f50-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="57f50-850">CGC</span><span class="sxs-lookup"><span data-stu-id="57f50-850">CGC</span></span> 
- <span data-ttu-id="57f50-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="57f50-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="57f50-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="57f50-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="57f50-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="57f50-853">Situação cadastral</span></span> 
- <span data-ttu-id="57f50-854">Inscrição</span><span class="sxs-lookup"><span data-stu-id="57f50-854">Inscrição</span></span> 
- <span data-ttu-id="57f50-855">Empresa</span><span class="sxs-lookup"><span data-stu-id="57f50-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="57f50-856">	Brasilien – Personalausweis (RG)</span><span class="sxs-lookup"><span data-stu-id="57f50-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-857">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-857">Format</span></span>

<span data-ttu-id="57f50-858">Registro Geral (altes Format): neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="57f50-859">Registro de Identidade (RIC) (neues Format): 11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-860">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-860">Pattern</span></span>

<span data-ttu-id="57f50-861">Registro Geral (altes Format):</span><span class="sxs-lookup"><span data-stu-id="57f50-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="57f50-862">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-862">Two digits</span></span> 
- <span data-ttu-id="57f50-863">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="57f50-863">A period</span></span> 
- <span data-ttu-id="57f50-864">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-864">Three digits</span></span> 
- <span data-ttu-id="57f50-865">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="57f50-865">A period</span></span> 
- <span data-ttu-id="57f50-866">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-866">Three digits</span></span> 
- <span data-ttu-id="57f50-867">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-867">A hyphen</span></span> 
- <span data-ttu-id="57f50-868">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-868">One digit which is a check digit</span></span>

<span data-ttu-id="57f50-869">Registro de Identidade (RIC) (neues Format):</span><span class="sxs-lookup"><span data-stu-id="57f50-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="57f50-870">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-870">10 digits</span></span> 
- <span data-ttu-id="57f50-871">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-871">A hyphen</span></span> 
- <span data-ttu-id="57f50-872">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-873">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-873">Checksum</span></span>

<span data-ttu-id="57f50-874">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-875">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-875">Definition</span></span>

<span data-ttu-id="57f50-876">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-877">Die Funktion Func_brazil_rg findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-878">Ein Schlüsselwort aus Keyword_brazil_rg wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="57f50-879">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-879">The checksum passes.</span></span>

<span data-ttu-id="57f50-880">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-881">Die Funktion Func_brazil_rg findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-882">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-882">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-883">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-883">Keywords</span></span>

#### <a name="keyword_brazil_rg"></a><span data-ttu-id="57f50-884">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="57f50-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="57f50-885">Cédula de identidade Personalausweis National ID número de rregistro Registro de Iidentidade Registro Geral RG (bei diesem Schlüsselwort wird die Groß-/Kleinschreibung beachtet) RIC (bei diesem Schlüsselwort wird die Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="57f50-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="57f50-886">Kanadische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="57f50-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-887">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-887">Format</span></span>

<span data-ttu-id="57f50-888">Sieben oder zwölf Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-889">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-889">Pattern</span></span>

<span data-ttu-id="57f50-890">Eine kanadische Kontonummer umfasst sieben oder zwölf Ziffern.</span><span class="sxs-lookup"><span data-stu-id="57f50-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="57f50-891">Eine kanadische Bankkontonummer setzt sich wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="57f50-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="57f50-892">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-892">Five digits</span></span> 
- <span data-ttu-id="57f50-893">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-893">A hyphen</span></span> 
- <span data-ttu-id="57f50-894">Drei Ziffern oder</span><span class="sxs-lookup"><span data-stu-id="57f50-894">Three digits OR</span></span>
- <span data-ttu-id="57f50-895">Eine 0 (null) </span><span class="sxs-lookup"><span data-stu-id="57f50-895">A zero "0"</span></span> 
- <span data-ttu-id="57f50-896">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-897">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-897">Checksum</span></span>

<span data-ttu-id="57f50-898">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-899">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-899">Definition</span></span>

<span data-ttu-id="57f50-900">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-901">Der reguläre Ausdruck Regex_canada_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-902">Ein Schlüsselwort aus Keyword_canada_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="57f50-903">Der reguläre Ausdruck Regex_canada_bank_account_transit_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="57f50-904">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-905">Der reguläre Ausdruck Regex_canada_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-906">Ein Schlüsselwort aus Keyword_canada_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-907">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-907">Keywords</span></span>

#### <a name="keyword_canada_bank_account_number"></a><span data-ttu-id="57f50-908">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="57f50-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="57f50-909">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="57f50-909">canada savings bonds</span></span>
- <span data-ttu-id="57f50-910">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="57f50-910">canada revenue agency</span></span>
- <span data-ttu-id="57f50-911">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="57f50-911">canadian financial institution</span></span>
- <span data-ttu-id="57f50-912">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="57f50-912">direct deposit form</span></span>
- <span data-ttu-id="57f50-913">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="57f50-913">canadian citizen</span></span>
- <span data-ttu-id="57f50-914">legal representative</span><span class="sxs-lookup"><span data-stu-id="57f50-914">legal representative</span></span>
- <span data-ttu-id="57f50-915">notary public</span><span class="sxs-lookup"><span data-stu-id="57f50-915">notary public</span></span>
- <span data-ttu-id="57f50-916">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="57f50-916">commissioner for oaths</span></span>
- <span data-ttu-id="57f50-917">child care benefit</span><span class="sxs-lookup"><span data-stu-id="57f50-917">child care benefit</span></span>
- <span data-ttu-id="57f50-918">universal child care</span><span class="sxs-lookup"><span data-stu-id="57f50-918">universal child care</span></span>
- <span data-ttu-id="57f50-919">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="57f50-919">canada child tax benefit</span></span>
- <span data-ttu-id="57f50-920">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="57f50-920">income tax benefit</span></span>
- <span data-ttu-id="57f50-921">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="57f50-921">harmonized sales tax</span></span>
- <span data-ttu-id="57f50-922">social insurance number</span><span class="sxs-lookup"><span data-stu-id="57f50-922">social insurance number</span></span>
- <span data-ttu-id="57f50-923">income tax refund</span><span class="sxs-lookup"><span data-stu-id="57f50-923">income tax refund</span></span>
- <span data-ttu-id="57f50-924">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="57f50-924">child tax benefit</span></span>
- <span data-ttu-id="57f50-925">territorial payments</span><span class="sxs-lookup"><span data-stu-id="57f50-925">territorial payments</span></span>
- <span data-ttu-id="57f50-926">institution number</span><span class="sxs-lookup"><span data-stu-id="57f50-926">institution number</span></span>
- <span data-ttu-id="57f50-927">deposit request</span><span class="sxs-lookup"><span data-stu-id="57f50-927">deposit request</span></span>
- <span data-ttu-id="57f50-928">banking information</span><span class="sxs-lookup"><span data-stu-id="57f50-928">banking information</span></span>
- <span data-ttu-id="57f50-929">direct deposit</span><span class="sxs-lookup"><span data-stu-id="57f50-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="57f50-930">Kanadische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-931">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-931">Format</span></span>

<span data-ttu-id="57f50-932">Variiert je nach Provinz</span><span class="sxs-lookup"><span data-stu-id="57f50-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-933">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-933">Pattern</span></span>

<span data-ttu-id="57f50-934">Verschiedene Muster in Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec und Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="57f50-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-935">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-935">Checksum</span></span>

<span data-ttu-id="57f50-936">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-937">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-937">Definition</span></span>

<span data-ttu-id="57f50-938">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-939">Die Funktion Func_[province_name]_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-940">Ein Schlüsselwort aus Keyword_[province_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="57f50-941">Ein Schlüsselwort aus Keyword_canada_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-942">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-942">Keywords</span></span>

#### <a name="keyword_province_name_drivers_license_name"></a><span data-ttu-id="57f50-943">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="57f50-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="57f50-944">Die Abkürzung für die Provinz, z. B. AB</span><span class="sxs-lookup"><span data-stu-id="57f50-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="57f50-945">Der Name der Provinz, beispielsweise „Alberta“</span><span class="sxs-lookup"><span data-stu-id="57f50-945">The province name, for example Alberta</span></span>

#### <a name="keyword_canada_drivers_license"></a><span data-ttu-id="57f50-946">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="57f50-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="57f50-947">DL</span><span class="sxs-lookup"><span data-stu-id="57f50-947">DL</span></span>
- <span data-ttu-id="57f50-948">DLS</span><span class="sxs-lookup"><span data-stu-id="57f50-948">DLS</span></span>
- <span data-ttu-id="57f50-949">CDL</span><span class="sxs-lookup"><span data-stu-id="57f50-949">CDL</span></span>
- <span data-ttu-id="57f50-950">CDLS</span><span class="sxs-lookup"><span data-stu-id="57f50-950">CDLS</span></span>
- <span data-ttu-id="57f50-951">DriverLic</span><span class="sxs-lookup"><span data-stu-id="57f50-951">DriverLic</span></span>
- <span data-ttu-id="57f50-952">DriverLics</span><span class="sxs-lookup"><span data-stu-id="57f50-952">DriverLics</span></span>
- <span data-ttu-id="57f50-953">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="57f50-953">DriverLicense</span></span>
- <span data-ttu-id="57f50-954">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="57f50-954">DriverLicenses</span></span>
- <span data-ttu-id="57f50-955">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="57f50-955">DriverLicence</span></span>
- <span data-ttu-id="57f50-956">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="57f50-956">DriverLicences</span></span>
- <span data-ttu-id="57f50-957">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-957">Driver Lic</span></span>
- <span data-ttu-id="57f50-958">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-958">Driver Lics</span></span>
- <span data-ttu-id="57f50-959">Driver License</span><span class="sxs-lookup"><span data-stu-id="57f50-959">Driver License</span></span>
- <span data-ttu-id="57f50-960">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-960">Driver Licenses</span></span>
- <span data-ttu-id="57f50-961">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-961">Driver Licence</span></span>
- <span data-ttu-id="57f50-962">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-962">Driver Licences</span></span>
- <span data-ttu-id="57f50-963">DriversLic</span><span class="sxs-lookup"><span data-stu-id="57f50-963">DriversLic</span></span>
- <span data-ttu-id="57f50-964">DriversLics</span><span class="sxs-lookup"><span data-stu-id="57f50-964">DriversLics</span></span>
- <span data-ttu-id="57f50-965">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="57f50-965">DriversLicence</span></span>
- <span data-ttu-id="57f50-966">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="57f50-966">DriversLicences</span></span>
- <span data-ttu-id="57f50-967">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="57f50-967">DriversLicense</span></span>
- <span data-ttu-id="57f50-968">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="57f50-968">DriversLicenses</span></span>
- <span data-ttu-id="57f50-969">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-969">Drivers Lic</span></span>
- <span data-ttu-id="57f50-970">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-970">Drivers Lics</span></span>
- <span data-ttu-id="57f50-971">Drivers License</span><span class="sxs-lookup"><span data-stu-id="57f50-971">Drivers License</span></span>
- <span data-ttu-id="57f50-972">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-972">Drivers Licenses</span></span>
- <span data-ttu-id="57f50-973">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-973">Drivers Licence</span></span>
- <span data-ttu-id="57f50-974">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-974">Drivers Licences</span></span>
- <span data-ttu-id="57f50-975">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-975">Driver'Lic</span></span>
- <span data-ttu-id="57f50-976">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-976">Driver'Lics</span></span>
- <span data-ttu-id="57f50-977">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="57f50-977">Driver'License</span></span>
- <span data-ttu-id="57f50-978">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-978">Driver'Licenses</span></span>
- <span data-ttu-id="57f50-979">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-979">Driver'Licence</span></span>
- <span data-ttu-id="57f50-980">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-980">Driver'Licences</span></span>
- <span data-ttu-id="57f50-981">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-981">Driver' Lic</span></span>
- <span data-ttu-id="57f50-982">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-982">Driver' Lics</span></span>
- <span data-ttu-id="57f50-983">Driver' License</span><span class="sxs-lookup"><span data-stu-id="57f50-983">Driver' License</span></span>
- <span data-ttu-id="57f50-984">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-984">Driver' Licenses</span></span>
- <span data-ttu-id="57f50-985">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-985">Driver' Licence</span></span>
- <span data-ttu-id="57f50-986">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-986">Driver' Licences</span></span>
- <span data-ttu-id="57f50-987">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="57f50-987">Driver'sLic</span></span>
- <span data-ttu-id="57f50-988">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="57f50-988">Driver'sLics</span></span>
- <span data-ttu-id="57f50-989">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="57f50-989">Driver'sLicense</span></span>
- <span data-ttu-id="57f50-990">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="57f50-990">Driver'sLicenses</span></span>
- <span data-ttu-id="57f50-991">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="57f50-991">Driver'sLicence</span></span>
- <span data-ttu-id="57f50-992">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="57f50-992">Driver'sLicences</span></span>
- <span data-ttu-id="57f50-993">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-993">Driver's Lic</span></span>
- <span data-ttu-id="57f50-994">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-994">Driver's Lics</span></span>
- <span data-ttu-id="57f50-995">Driver's License</span><span class="sxs-lookup"><span data-stu-id="57f50-995">Driver's License</span></span>
- <span data-ttu-id="57f50-996">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-996">Driver's Licenses</span></span>
- <span data-ttu-id="57f50-997">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-997">Driver's Licence</span></span>
- <span data-ttu-id="57f50-998">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-998">Driver's Licences</span></span>
- <span data-ttu-id="57f50-999">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="57f50-999">Permis de Conduire</span></span>
- <span data-ttu-id="57f50-1000">id</span><span class="sxs-lookup"><span data-stu-id="57f50-1000">id</span></span>
- <span data-ttu-id="57f50-1001">ids</span><span class="sxs-lookup"><span data-stu-id="57f50-1001">ids</span></span>
- <span data-ttu-id="57f50-1002">idcard number</span><span class="sxs-lookup"><span data-stu-id="57f50-1002">idcard number</span></span>
- <span data-ttu-id="57f50-1003">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="57f50-1003">idcard numbers</span></span>
- <span data-ttu-id="57f50-1004">idcard #</span><span class="sxs-lookup"><span data-stu-id="57f50-1004">idcard #</span></span>
- <span data-ttu-id="57f50-1005">idcard #s</span><span class="sxs-lookup"><span data-stu-id="57f50-1005">idcard #s</span></span>
- <span data-ttu-id="57f50-1006">idcard card</span><span class="sxs-lookup"><span data-stu-id="57f50-1006">idcard card</span></span>
- <span data-ttu-id="57f50-1007">idcard cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1007">idcard cards</span></span>
- <span data-ttu-id="57f50-1008">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-1008">idcard</span></span>
- <span data-ttu-id="57f50-1009">identification number</span><span class="sxs-lookup"><span data-stu-id="57f50-1009">identification number</span></span>
- <span data-ttu-id="57f50-1010">identification numbers</span><span class="sxs-lookup"><span data-stu-id="57f50-1010">identification numbers</span></span>
- <span data-ttu-id="57f50-1011">identification #</span><span class="sxs-lookup"><span data-stu-id="57f50-1011">identification #</span></span>
- <span data-ttu-id="57f50-1012">identification #s</span><span class="sxs-lookup"><span data-stu-id="57f50-1012">identification #s</span></span>
- <span data-ttu-id="57f50-1013">identification card</span><span class="sxs-lookup"><span data-stu-id="57f50-1013">identification card</span></span>
- <span data-ttu-id="57f50-1014">identification cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1014">identification cards</span></span>
- <span data-ttu-id="57f50-1015">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="57f50-1015">identification</span></span> 
- <span data-ttu-id="57f50-1016">DL #</span><span class="sxs-lookup"><span data-stu-id="57f50-1016">DL#</span></span>
- <span data-ttu-id="57f50-1017">DLS #</span><span class="sxs-lookup"><span data-stu-id="57f50-1017">DLS#</span></span> 
- <span data-ttu-id="57f50-1018">CDL #</span><span class="sxs-lookup"><span data-stu-id="57f50-1018">CDL#</span></span> 
- <span data-ttu-id="57f50-1019">CDLS #</span><span class="sxs-lookup"><span data-stu-id="57f50-1019">CDLS#</span></span> 
- <span data-ttu-id="57f50-1020">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="57f50-1020">DriverLic#</span></span> 
- <span data-ttu-id="57f50-1021">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="57f50-1021">DriverLics#</span></span> 
- <span data-ttu-id="57f50-1022">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="57f50-1022">DriverLicense#</span></span> 
- <span data-ttu-id="57f50-1023">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="57f50-1024">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="57f50-1024">DriverLicence#</span></span> 
- <span data-ttu-id="57f50-1025">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="57f50-1025">DriverLicences#</span></span> 
- <span data-ttu-id="57f50-1026">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-1026">Driver Lic#</span></span>
- <span data-ttu-id="57f50-1027">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-1027">Driver Lics#</span></span> 
- <span data-ttu-id="57f50-1028">Driver License#</span><span class="sxs-lookup"><span data-stu-id="57f50-1028">Driver License#</span></span> 
- <span data-ttu-id="57f50-1029">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="57f50-1030">Driver License#</span><span class="sxs-lookup"><span data-stu-id="57f50-1030">Driver License#</span></span> 
- <span data-ttu-id="57f50-1031">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="57f50-1031">Driver Licences#</span></span> 
- <span data-ttu-id="57f50-1032">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="57f50-1032">DriversLic#</span></span> 
- <span data-ttu-id="57f50-1033">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="57f50-1033">DriversLics#</span></span> 
- <span data-ttu-id="57f50-1034">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="57f50-1034">DriversLicense#</span></span> 
- <span data-ttu-id="57f50-1035">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="57f50-1036">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="57f50-1036">DriversLicence#</span></span> 
- <span data-ttu-id="57f50-1037">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="57f50-1037">DriversLicences#</span></span> 
- <span data-ttu-id="57f50-1038">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="57f50-1039">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="57f50-1040">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="57f50-1040">Drivers License#</span></span> 
- <span data-ttu-id="57f50-1041">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="57f50-1042">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="57f50-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="57f50-1043">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="57f50-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="57f50-1044">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="57f50-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="57f50-1045">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="57f50-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="57f50-1046">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="57f50-1046">Driver'License#</span></span> 
- <span data-ttu-id="57f50-1047">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="57f50-1048">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="57f50-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="57f50-1049">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="57f50-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="57f50-1050">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="57f50-1051">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="57f50-1052">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="57f50-1052">Driver' License#</span></span> 
- <span data-ttu-id="57f50-1053">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="57f50-1054">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="57f50-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="57f50-1055">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="57f50-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="57f50-1056">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="57f50-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="57f50-1057">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="57f50-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="57f50-1058">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="57f50-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="57f50-1059">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="57f50-1060">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="57f50-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="57f50-1061">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="57f50-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="57f50-1062">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="57f50-1063">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="57f50-1064">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="57f50-1064">Driver's License#</span></span> 
- <span data-ttu-id="57f50-1065">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="57f50-1066">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="57f50-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="57f50-1067">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="57f50-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="57f50-1068">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="57f50-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="57f50-1069">ID #</span><span class="sxs-lookup"><span data-stu-id="57f50-1069">id#</span></span> 
- <span data-ttu-id="57f50-1070">IDs #</span><span class="sxs-lookup"><span data-stu-id="57f50-1070">ids#</span></span> 
- <span data-ttu-id="57f50-1071">idcard card#</span><span class="sxs-lookup"><span data-stu-id="57f50-1071">idcard card#</span></span> 
- <span data-ttu-id="57f50-1072">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="57f50-1072">idcard cards#</span></span> 
- <span data-ttu-id="57f50-1073">Personalausweis #</span><span class="sxs-lookup"><span data-stu-id="57f50-1073">idcard#</span></span> 
- <span data-ttu-id="57f50-1074">identification card#</span><span class="sxs-lookup"><span data-stu-id="57f50-1074">identification card#</span></span> 
- <span data-ttu-id="57f50-1075">identification cards#</span><span class="sxs-lookup"><span data-stu-id="57f50-1075">identification cards#</span></span> 
- <span data-ttu-id="57f50-1076">Identifizierung #</span><span class="sxs-lookup"><span data-stu-id="57f50-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="57f50-1077">Kanadische Health Service-Nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1078">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1078">Format</span></span>

<span data-ttu-id="57f50-1079">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1080">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1080">Pattern</span></span>

<span data-ttu-id="57f50-1081">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1082">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1082">Checksum</span></span>

<span data-ttu-id="57f50-1083">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1084">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1084">Definition</span></span>

<span data-ttu-id="57f50-1085">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1086">Der reguläre Ausdruck Regex_canada_health_service_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1087">Ein Schlüsselwort aus Keyword_canada_health_service_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-1088">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1088">Keywords</span></span>

#### <a name="keyword_canada_health_service_number"></a><span data-ttu-id="57f50-1089">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="57f50-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="57f50-1090">personal health number</span><span class="sxs-lookup"><span data-stu-id="57f50-1090">personal health number</span></span>
- <span data-ttu-id="57f50-1091">patient information</span><span class="sxs-lookup"><span data-stu-id="57f50-1091">patient information</span></span>
- <span data-ttu-id="57f50-1092">health services</span><span class="sxs-lookup"><span data-stu-id="57f50-1092">health services</span></span>
- <span data-ttu-id="57f50-1093">speciality services</span><span class="sxs-lookup"><span data-stu-id="57f50-1093">speciality services</span></span>
- <span data-ttu-id="57f50-1094">automobile accident</span><span class="sxs-lookup"><span data-stu-id="57f50-1094">automobile accident</span></span>
- <span data-ttu-id="57f50-1095">patient hospital</span><span class="sxs-lookup"><span data-stu-id="57f50-1095">patient hospital</span></span>
- <span data-ttu-id="57f50-1096">Psychiater</span><span class="sxs-lookup"><span data-stu-id="57f50-1096">psychiatrist</span></span>
- <span data-ttu-id="57f50-1097">workers compensation</span><span class="sxs-lookup"><span data-stu-id="57f50-1097">workers compensation</span></span>
- <span data-ttu-id="57f50-1098">Disability</span><span class="sxs-lookup"><span data-stu-id="57f50-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="57f50-1099">Kanadische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1100">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1100">Format</span></span>

<span data-ttu-id="57f50-1101">Zwei Großbuchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1102">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1102">Pattern</span></span>

<span data-ttu-id="57f50-1103">Zwei Großbuchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1104">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1104">Checksum</span></span>

<span data-ttu-id="57f50-1105">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1106">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1106">Definition</span></span>

<span data-ttu-id="57f50-1107">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1108">Der reguläre Ausdruck Regex_canada_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1109">Ein Schlüsselwort aus Keyword_canada_passport_number oder Keyword_passport wird gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

```xml 
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

### <a name="keywords"></a><span data-ttu-id="57f50-1110">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1110">Keywords</span></span>

#### <a name="keyword_canada_passport_number"></a><span data-ttu-id="57f50-1111">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="57f50-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="57f50-1112">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="57f50-1112">canadian citizenship</span></span>
- <span data-ttu-id="57f50-1113">canadian passport</span><span class="sxs-lookup"><span data-stu-id="57f50-1113">canadian passport</span></span>
- <span data-ttu-id="57f50-1114">passport application</span><span class="sxs-lookup"><span data-stu-id="57f50-1114">passport application</span></span>
- <span data-ttu-id="57f50-1115">passport photos</span><span class="sxs-lookup"><span data-stu-id="57f50-1115">passport photos</span></span>
- <span data-ttu-id="57f50-1116">certified translator</span><span class="sxs-lookup"><span data-stu-id="57f50-1116">certified translator</span></span>
- <span data-ttu-id="57f50-1117">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="57f50-1117">canadian citizens</span></span>
- <span data-ttu-id="57f50-1118">processing times</span><span class="sxs-lookup"><span data-stu-id="57f50-1118">processing times</span></span>
- <span data-ttu-id="57f50-1119">renewal application</span><span class="sxs-lookup"><span data-stu-id="57f50-1119">renewal application</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="57f50-1120">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="57f50-1120">Keyword_passport</span></span>

- <span data-ttu-id="57f50-1121">Passport Number</span><span class="sxs-lookup"><span data-stu-id="57f50-1121">Passport Number</span></span>
- <span data-ttu-id="57f50-1122">Passport No</span><span class="sxs-lookup"><span data-stu-id="57f50-1122">Passport No</span></span>
- <span data-ttu-id="57f50-1123">Passport#</span><span class="sxs-lookup"><span data-stu-id="57f50-1123">Passport #</span></span>
- <span data-ttu-id="57f50-1124">Pass #</span><span class="sxs-lookup"><span data-stu-id="57f50-1124">Passport#</span></span>
- <span data-ttu-id="57f50-1125">Passport-Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-1125">PassportID</span></span>
- <span data-ttu-id="57f50-1126">Passportno</span><span class="sxs-lookup"><span data-stu-id="57f50-1126">Passportno</span></span>
- <span data-ttu-id="57f50-1127">passportnumber</span><span class="sxs-lookup"><span data-stu-id="57f50-1127">passportnumber</span></span>
- <span data-ttu-id="57f50-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="57f50-1128">パスポート</span></span>
- <span data-ttu-id="57f50-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="57f50-1129">パスポート番号</span></span>
- <span data-ttu-id="57f50-1130">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="57f50-1130">パスポートのNum</span></span>
- <span data-ttu-id="57f50-1131">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="57f50-1131">パスポート＃</span></span>
- <span data-ttu-id="57f50-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="57f50-1132">Numéro de passeport</span></span>
- <span data-ttu-id="57f50-1133">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="57f50-1133">Passeport n °</span></span>
- <span data-ttu-id="57f50-1134">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="57f50-1134">Passeport Non</span></span>
- <span data-ttu-id="57f50-1135">Passeport#</span><span class="sxs-lookup"><span data-stu-id="57f50-1135">Passeport #</span></span>
- <span data-ttu-id="57f50-1136">Passeport #</span><span class="sxs-lookup"><span data-stu-id="57f50-1136">Passeport#</span></span>
- <span data-ttu-id="57f50-1137">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="57f50-1137">PasseportNon</span></span>
- <span data-ttu-id="57f50-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="57f50-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="57f50-1139">Kanadische Personal Health Identification-Nummer (PHIN)</span><span class="sxs-lookup"><span data-stu-id="57f50-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1140">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1140">Format</span></span>

<span data-ttu-id="57f50-1141">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1142">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1142">Pattern</span></span>

<span data-ttu-id="57f50-1143">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1144">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1144">Checksum</span></span>

<span data-ttu-id="57f50-1145">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1146">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1146">Definition</span></span>

<span data-ttu-id="57f50-1147">Eine DLP-Richtlinie ist 75% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: der reguläre Ausdruck Regex_canada_phin findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="57f50-1148">Mindestens zwei Schlüsselwörter aus Keyword_canada_phin oder Keyword_canada_provinces werden gefunden..</span><span class="sxs-lookup"><span data-stu-id="57f50-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-1149">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1149">Keywords</span></span>

#### <a name="keyword_canada_phin"></a><span data-ttu-id="57f50-1150">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="57f50-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="57f50-1151">social insurance number</span><span class="sxs-lookup"><span data-stu-id="57f50-1151">social insurance number</span></span>
- <span data-ttu-id="57f50-1152">health information act</span><span class="sxs-lookup"><span data-stu-id="57f50-1152">health information act</span></span>
- <span data-ttu-id="57f50-1153">income tax information</span><span class="sxs-lookup"><span data-stu-id="57f50-1153">income tax information</span></span>
- <span data-ttu-id="57f50-1154">manitoba health</span><span class="sxs-lookup"><span data-stu-id="57f50-1154">manitoba health</span></span>
- <span data-ttu-id="57f50-1155">health registration</span><span class="sxs-lookup"><span data-stu-id="57f50-1155">health registration</span></span>
- <span data-ttu-id="57f50-1156">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="57f50-1156">prescription purchases</span></span>
- <span data-ttu-id="57f50-1157">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="57f50-1157">benefit eligibility</span></span>
- <span data-ttu-id="57f50-1158">personal health</span><span class="sxs-lookup"><span data-stu-id="57f50-1158">personal health</span></span>
- <span data-ttu-id="57f50-1159">power of attorney</span><span class="sxs-lookup"><span data-stu-id="57f50-1159">power of attorney</span></span>
- <span data-ttu-id="57f50-1160">registration number</span><span class="sxs-lookup"><span data-stu-id="57f50-1160">registration number</span></span>
- <span data-ttu-id="57f50-1161">personal health number</span><span class="sxs-lookup"><span data-stu-id="57f50-1161">personal health number</span></span>
- <span data-ttu-id="57f50-1162">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="57f50-1162">practitioner referral</span></span>
- <span data-ttu-id="57f50-1163">wellness professional</span><span class="sxs-lookup"><span data-stu-id="57f50-1163">wellness professional</span></span>
- <span data-ttu-id="57f50-1164">patient referral</span><span class="sxs-lookup"><span data-stu-id="57f50-1164">patient referral</span></span>
- <span data-ttu-id="57f50-1165">health and wellness</span><span class="sxs-lookup"><span data-stu-id="57f50-1165">health and wellness</span></span>

#### <a name="keyword_canada_provinces"></a><span data-ttu-id="57f50-1166">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="57f50-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="57f50-1167">Nunavut</span><span class="sxs-lookup"><span data-stu-id="57f50-1167">Nunavut</span></span>
- <span data-ttu-id="57f50-1168">Quebec</span><span class="sxs-lookup"><span data-stu-id="57f50-1168">Quebec</span></span>
- <span data-ttu-id="57f50-1169">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="57f50-1169">Northwest Territories</span></span>
- <span data-ttu-id="57f50-1170">Ontario</span><span class="sxs-lookup"><span data-stu-id="57f50-1170">Ontario</span></span>
- <span data-ttu-id="57f50-1171">British Columbia</span><span class="sxs-lookup"><span data-stu-id="57f50-1171">British Columbia</span></span>
- <span data-ttu-id="57f50-1172">Alberta</span><span class="sxs-lookup"><span data-stu-id="57f50-1172">Alberta</span></span>
- <span data-ttu-id="57f50-1173">Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="57f50-1173">Saskatchewan</span></span>
- <span data-ttu-id="57f50-1174">Manitoba</span><span class="sxs-lookup"><span data-stu-id="57f50-1174">Manitoba</span></span>
- <span data-ttu-id="57f50-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="57f50-1175">Yukon</span></span>
- <span data-ttu-id="57f50-1176">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="57f50-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="57f50-1177">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="57f50-1177">New Brunswick</span></span>
- <span data-ttu-id="57f50-1178">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="57f50-1178">Nova Scotia</span></span>
- <span data-ttu-id="57f50-1179">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="57f50-1179">Prince Edward Island</span></span>
- <span data-ttu-id="57f50-1180">Kanada</span><span class="sxs-lookup"><span data-stu-id="57f50-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="57f50-1181">Kanadische Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1182">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1182">Format</span></span>

<span data-ttu-id="57f50-1183">Neun Ziffern mit optionalen Bindestrichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1184">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1184">Pattern</span></span>

<span data-ttu-id="57f50-1185">Formatiert</span><span class="sxs-lookup"><span data-stu-id="57f50-1185">Formatted:</span></span>
- <span data-ttu-id="57f50-1186">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1186">Three digits</span></span> 
- <span data-ttu-id="57f50-1187">Ein Bindestrich oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-1187">A hyphen or space</span></span> 
- <span data-ttu-id="57f50-1188">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1188">Three digits</span></span> 
- <span data-ttu-id="57f50-1189">Ein Bindestrich oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-1189">A hyphen or space</span></span> 
- <span data-ttu-id="57f50-1190">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1190">Three digits</span></span>

<span data-ttu-id="57f50-1191">Unformatiert: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1192">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1192">Checksum</span></span>

<span data-ttu-id="57f50-1193">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1194">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1194">Definition</span></span>

<span data-ttu-id="57f50-1195">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1196">Die Funktion Func_canadian_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1197">Mindestens zwei dieser eine beliebige Kombination der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="57f50-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="57f50-1198">Ein Schlüsselwort aus Keyword_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="57f50-1199">Ein Schlüsselwort aus Keyword_sin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="57f50-1200">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="57f50-1201">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1201">The checksum passes.</span></span>

<span data-ttu-id="57f50-1202">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1203">Die Funktion Func_unformatted_canadian_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1204">Ein Schlüsselwort aus Keyword_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="57f50-1205">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1205">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-1206">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1206">Keywords</span></span>

#### <a name="keyword_sin"></a><span data-ttu-id="57f50-1207">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="57f50-1207">Keyword_sin</span></span>

- <span data-ttu-id="57f50-1208">sin</span><span class="sxs-lookup"><span data-stu-id="57f50-1208">sin</span></span> 
- <span data-ttu-id="57f50-1209">social insurance</span><span class="sxs-lookup"><span data-stu-id="57f50-1209">social insurance</span></span> 
- <span data-ttu-id="57f50-1210">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="57f50-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="57f50-1211">Todsünden</span><span class="sxs-lookup"><span data-stu-id="57f50-1211">sins</span></span> 
- <span data-ttu-id="57f50-1212">SSN</span><span class="sxs-lookup"><span data-stu-id="57f50-1212">ssn</span></span> 
- <span data-ttu-id="57f50-1213">Sozialversicherungsnummern</span><span class="sxs-lookup"><span data-stu-id="57f50-1213">ssns</span></span> 
- <span data-ttu-id="57f50-1214">social security</span><span class="sxs-lookup"><span data-stu-id="57f50-1214">social security</span></span> 
- <span data-ttu-id="57f50-1215">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="57f50-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="57f50-1216">national identification number</span><span class="sxs-lookup"><span data-stu-id="57f50-1216">national identification number</span></span> 
- <span data-ttu-id="57f50-1217">national id</span><span class="sxs-lookup"><span data-stu-id="57f50-1217">national id</span></span> 
- <span data-ttu-id="57f50-1218">Sin #</span><span class="sxs-lookup"><span data-stu-id="57f50-1218">sin#</span></span> 
- <span data-ttu-id="57f50-1219">soc ins</span><span class="sxs-lookup"><span data-stu-id="57f50-1219">soc ins</span></span> 
- <span data-ttu-id="57f50-1220">social ins</span><span class="sxs-lookup"><span data-stu-id="57f50-1220">social ins</span></span> 

#### <a name="keyword_sin_collaborative"></a><span data-ttu-id="57f50-1221">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="57f50-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="57f50-1222">driver's license</span><span class="sxs-lookup"><span data-stu-id="57f50-1222">driver's license</span></span> 
- <span data-ttu-id="57f50-1223">drivers license</span><span class="sxs-lookup"><span data-stu-id="57f50-1223">drivers license</span></span> 
- <span data-ttu-id="57f50-1224">driver's licence</span><span class="sxs-lookup"><span data-stu-id="57f50-1224">driver's licence</span></span> 
- <span data-ttu-id="57f50-1225">drivers licence</span><span class="sxs-lookup"><span data-stu-id="57f50-1225">drivers licence</span></span> 
- <span data-ttu-id="57f50-1226">DOB</span><span class="sxs-lookup"><span data-stu-id="57f50-1226">DOB</span></span> 
- <span data-ttu-id="57f50-1227">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="57f50-1227">Birthdate</span></span> 
- <span data-ttu-id="57f50-1228">Geburtstag</span><span class="sxs-lookup"><span data-stu-id="57f50-1228">Birthday</span></span> 
- <span data-ttu-id="57f50-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="57f50-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="57f50-1230">	Chile Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="57f50-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1231">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1231">Format</span></span>

<span data-ttu-id="57f50-1232">7-8 Ziffern Plus Trennzeichen für eine Prüfziffer oder einen Buchstaben</span><span class="sxs-lookup"><span data-stu-id="57f50-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1233">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1233">Pattern</span></span>

<span data-ttu-id="57f50-1234">7-8 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="57f50-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="57f50-1235">1-2 Ziffern </span><span class="sxs-lookup"><span data-stu-id="57f50-1235">1-2 digits</span></span> 
- <span data-ttu-id="57f50-1236">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="57f50-1236">A period</span></span> 
- <span data-ttu-id="57f50-1237">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1237">Three digits</span></span> 
- <span data-ttu-id="57f50-1238">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="57f50-1238">A period</span></span> 
- <span data-ttu-id="57f50-1239">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1239">Three digits</span></span> 
- <span data-ttu-id="57f50-1240">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-1240">A dash</span></span> 
- <span data-ttu-id="57f50-1241">Eine Ziffer oder ein Buchstabe (Groß-/Kleinschreibung nicht unterschieden), die bzw. der eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="57f50-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1242">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1242">Checksum</span></span>

<span data-ttu-id="57f50-1243">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1244">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1244">Definition</span></span>

<span data-ttu-id="57f50-1245">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1246">Die Funktion Func_chile_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1247">Ein Schlüsselwort aus Keyword_chile_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="57f50-1248">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1248">The checksum passes.</span></span>

<span data-ttu-id="57f50-1249">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1250">Die Funktion Func_chile_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1251">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1251">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-1252">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1252">Keywords</span></span>

#### <a name="keyword_chile_id_card"></a><span data-ttu-id="57f50-1253">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="57f50-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="57f50-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="57f50-1254">National Identification Number</span></span> 
- <span data-ttu-id="57f50-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="57f50-1255">Identity card</span></span> 
- <span data-ttu-id="57f50-1256">ID</span><span class="sxs-lookup"><span data-stu-id="57f50-1256">ID</span></span> 
- <span data-ttu-id="57f50-1257">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="57f50-1257">Identification</span></span> 
- <span data-ttu-id="57f50-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="57f50-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="57f50-1259">Ausführen</span><span class="sxs-lookup"><span data-stu-id="57f50-1259">RUN</span></span> 
- <span data-ttu-id="57f50-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="57f50-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="57f50-1261">Rut</span><span class="sxs-lookup"><span data-stu-id="57f50-1261">RUT</span></span> 
- <span data-ttu-id="57f50-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="57f50-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="57f50-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="57f50-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="57f50-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="57f50-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="57f50-1265">Identificación</span><span class="sxs-lookup"><span data-stu-id="57f50-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="57f50-1266">	China (PRC) – Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1267">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1267">Format</span></span>

<span data-ttu-id="57f50-1268">18 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1269">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1269">Pattern</span></span>

<span data-ttu-id="57f50-1270">18 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-1270">18 digits:</span></span>
- <span data-ttu-id="57f50-1271">Sechs Ziffern, die einen Adresscode angeben </span><span class="sxs-lookup"><span data-stu-id="57f50-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="57f50-1272">Acht Ziffern im Fomat JJJJMMTT, wobei es sich um das Geburtsdatum handelt </span><span class="sxs-lookup"><span data-stu-id="57f50-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="57f50-1273">Drei Ziffern, die ein Reihenfolgencode sind </span><span class="sxs-lookup"><span data-stu-id="57f50-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="57f50-1274">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1275">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1275">Checksum</span></span>

<span data-ttu-id="57f50-1276">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1277">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1277">Definition</span></span>

<span data-ttu-id="57f50-1278">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1279">Die Funktion Func_china_resident_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1280">Ein Schlüsselwort aus Keyword_china_resident_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="57f50-1281">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1281">The checksum passes.</span></span>

<span data-ttu-id="57f50-1282">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1283">Die Funktion Func_china_resident_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1284">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1284">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-1285">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1285">Keywords</span></span>

### <a name="keyword_china_resident_id"></a><span data-ttu-id="57f50-1286">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="57f50-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="57f50-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="57f50-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="57f50-1288">PRC</span><span class="sxs-lookup"><span data-stu-id="57f50-1288">PRC</span></span> 
- <span data-ttu-id="57f50-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="57f50-1289">National Identification Card</span></span> 
- <span data-ttu-id="57f50-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="57f50-1290">身份证</span></span> 
- <span data-ttu-id="57f50-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="57f50-1291">居民 身份证</span></span> 
- <span data-ttu-id="57f50-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="57f50-1292">居民身份证</span></span> 
- <span data-ttu-id="57f50-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="57f50-1293">鉴定</span></span> 
- <span data-ttu-id="57f50-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="57f50-1294">身分證</span></span> 
- <span data-ttu-id="57f50-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-1295">居民 身份證</span></span>
- <span data-ttu-id="57f50-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="57f50-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="57f50-1297">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1298">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1298">Format</span></span>

<span data-ttu-id="57f50-1299">16 Ziffern, die formatiert oder unformatiert (dddddddddddddddd) sein können und den Luhn-Test bestehen müssen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1299">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1300">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1300">Pattern</span></span>

<span data-ttu-id="57f50-1301">Sehr komplexe und robuste Muster, die Karten aller wichtigen Marken weltweit, einschließlich Visa, MasterCard, Discover-Karte, JCB, American Express, Geschenkgutscheine und Restaurantkarten erkennen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1302">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1302">Checksum</span></span>

<span data-ttu-id="57f50-1303">Ja, die Luhn-Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1304">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1304">Definition</span></span>

<span data-ttu-id="57f50-1305">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1306">Die Funktion Func_credit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1307">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="57f50-1307">One of the following is true:</span></span>
    - <span data-ttu-id="57f50-1308">Ein Schlüsselwort aus Keyword_cc_verification wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="57f50-1309">Ein Schlüsselwort aus Keyword_cc_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="57f50-1310">Die Funktion Func_expiration_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="57f50-1311">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1311">The checksum passes.</span></span>

<span data-ttu-id="57f50-1312">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1313">Die Funktion Func_credit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1314">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1314">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-1315">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1315">Keywords</span></span>

#### <a name="keyword_cc_verification"></a><span data-ttu-id="57f50-1316">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="57f50-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="57f50-1317">card verification</span><span class="sxs-lookup"><span data-stu-id="57f50-1317">card verification</span></span>
- <span data-ttu-id="57f50-1318">card identification number</span><span class="sxs-lookup"><span data-stu-id="57f50-1318">card identification number</span></span>
- <span data-ttu-id="57f50-1319">CVN</span><span class="sxs-lookup"><span data-stu-id="57f50-1319">cvn</span></span>
- <span data-ttu-id="57f50-1320">cid</span><span class="sxs-lookup"><span data-stu-id="57f50-1320">cid</span></span>
- <span data-ttu-id="57f50-1321">CVC2</span><span class="sxs-lookup"><span data-stu-id="57f50-1321">cvc2</span></span>
- <span data-ttu-id="57f50-1322">CVV2</span><span class="sxs-lookup"><span data-stu-id="57f50-1322">cvv2</span></span>
- <span data-ttu-id="57f50-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="57f50-1323">pin block</span></span>
- <span data-ttu-id="57f50-1324">security code</span><span class="sxs-lookup"><span data-stu-id="57f50-1324">security code</span></span>
- <span data-ttu-id="57f50-1325">security number</span><span class="sxs-lookup"><span data-stu-id="57f50-1325">security number</span></span>
- <span data-ttu-id="57f50-1326">security no</span><span class="sxs-lookup"><span data-stu-id="57f50-1326">security no</span></span>
- <span data-ttu-id="57f50-1327">issue number</span><span class="sxs-lookup"><span data-stu-id="57f50-1327">issue number</span></span>
- <span data-ttu-id="57f50-1328">issue no</span><span class="sxs-lookup"><span data-stu-id="57f50-1328">issue no</span></span>
- <span data-ttu-id="57f50-1329">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="57f50-1329">cryptogramme</span></span>
- <span data-ttu-id="57f50-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="57f50-1330">numéro de sécurité</span></span>
- <span data-ttu-id="57f50-1331">numero de securite</span><span class="sxs-lookup"><span data-stu-id="57f50-1331">numero de securite</span></span>
- <span data-ttu-id="57f50-1332">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="57f50-1333">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="57f50-1334">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-1334">prüfziffer</span></span>
- <span data-ttu-id="57f50-1335">prufziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-1335">prufziffer</span></span>
- <span data-ttu-id="57f50-1336">Sicherheitskode</span><span class="sxs-lookup"><span data-stu-id="57f50-1336">sicherheits Kode</span></span>
- <span data-ttu-id="57f50-1337">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="57f50-1337">sicherheitscode</span></span>
- <span data-ttu-id="57f50-1338">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="57f50-1339">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="57f50-1339">verfalldatum</span></span>
- <span data-ttu-id="57f50-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="57f50-1340">codice di verifica</span></span>
- <span data-ttu-id="57f50-1341">COD.</span><span class="sxs-lookup"><span data-stu-id="57f50-1341">cod.</span></span> <span data-ttu-id="57f50-1342">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="57f50-1342">sicurezza</span></span>
- <span data-ttu-id="57f50-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="57f50-1343">cod sicurezza</span></span>
- <span data-ttu-id="57f50-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="57f50-1344">n autorizzazione</span></span>
- <span data-ttu-id="57f50-1345">Código</span><span class="sxs-lookup"><span data-stu-id="57f50-1345">código</span></span>
- <span data-ttu-id="57f50-1346">codigo</span><span class="sxs-lookup"><span data-stu-id="57f50-1346">codigo</span></span>
- <span data-ttu-id="57f50-1347">COD.</span><span class="sxs-lookup"><span data-stu-id="57f50-1347">cod.</span></span> <span data-ttu-id="57f50-1348">SEG</span><span class="sxs-lookup"><span data-stu-id="57f50-1348">seg</span></span>
- <span data-ttu-id="57f50-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="57f50-1349">cod seg</span></span>
- <span data-ttu-id="57f50-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1350">código de segurança</span></span>
- <span data-ttu-id="57f50-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="57f50-1351">codigo de seguranca</span></span>
- <span data-ttu-id="57f50-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1352">codigo de segurança</span></span>
- <span data-ttu-id="57f50-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="57f50-1353">código de seguranca</span></span>
- <span data-ttu-id="57f50-1354">cód.</span><span class="sxs-lookup"><span data-stu-id="57f50-1354">cód.</span></span> <span data-ttu-id="57f50-1355">Segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1355">segurança</span></span>
- <span data-ttu-id="57f50-1356">COD.</span><span class="sxs-lookup"><span data-stu-id="57f50-1356">cod.</span></span> <span data-ttu-id="57f50-1357">Seguranca COD.</span><span class="sxs-lookup"><span data-stu-id="57f50-1357">seguranca cod.</span></span> <span data-ttu-id="57f50-1358">Segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1358">segurança</span></span>
- <span data-ttu-id="57f50-1359">cód.</span><span class="sxs-lookup"><span data-stu-id="57f50-1359">cód.</span></span> <span data-ttu-id="57f50-1360">seguranca</span><span class="sxs-lookup"><span data-stu-id="57f50-1360">seguranca</span></span>
- <span data-ttu-id="57f50-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1361">cód segurança</span></span>
- <span data-ttu-id="57f50-1362">COD Seguranca COD Segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="57f50-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="57f50-1363">cód seguranca</span></span>
- <span data-ttu-id="57f50-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="57f50-1364">número de verificação</span></span>
- <span data-ttu-id="57f50-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="57f50-1365">numero de verificacao</span></span>
- <span data-ttu-id="57f50-1366">Ablauf</span><span class="sxs-lookup"><span data-stu-id="57f50-1366">ablauf</span></span>
- <span data-ttu-id="57f50-1367">Gültig bis</span><span class="sxs-lookup"><span data-stu-id="57f50-1367">gültig bis</span></span>
- <span data-ttu-id="57f50-1368">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="57f50-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="57f50-1369">Gultig bis</span><span class="sxs-lookup"><span data-stu-id="57f50-1369">gultig bis</span></span>
- <span data-ttu-id="57f50-1370">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="57f50-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="57f50-1371">scadenza</span><span class="sxs-lookup"><span data-stu-id="57f50-1371">scadenza</span></span>
- <span data-ttu-id="57f50-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="57f50-1372">data scad</span></span>
- <span data-ttu-id="57f50-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="57f50-1373">fecha de expiracion</span></span>
- <span data-ttu-id="57f50-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="57f50-1374">fecha de venc</span></span>
- <span data-ttu-id="57f50-1375">vencimiento</span><span class="sxs-lookup"><span data-stu-id="57f50-1375">vencimiento</span></span>
- <span data-ttu-id="57f50-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="57f50-1376">válido hasta</span></span>
- <span data-ttu-id="57f50-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="57f50-1377">valido hasta</span></span>
- <span data-ttu-id="57f50-1378">VTO</span><span class="sxs-lookup"><span data-stu-id="57f50-1378">vto</span></span>
- <span data-ttu-id="57f50-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="57f50-1379">data de expiração</span></span>
- <span data-ttu-id="57f50-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="57f50-1380">data de expiracao</span></span>
- <span data-ttu-id="57f50-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="57f50-1381">data em que expira</span></span>
- <span data-ttu-id="57f50-1382">validade</span><span class="sxs-lookup"><span data-stu-id="57f50-1382">validade</span></span>
- <span data-ttu-id="57f50-1383">Valor</span><span class="sxs-lookup"><span data-stu-id="57f50-1383">valor</span></span>
- <span data-ttu-id="57f50-1384">vencimento</span><span class="sxs-lookup"><span data-stu-id="57f50-1384">vencimento</span></span>
- <span data-ttu-id="57f50-1385">Venc</span><span class="sxs-lookup"><span data-stu-id="57f50-1385">Venc</span></span> 

#### <a name="keyword_cc_name"></a><span data-ttu-id="57f50-1386">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="57f50-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="57f50-1387">Amex</span><span class="sxs-lookup"><span data-stu-id="57f50-1387">amex</span></span>
- <span data-ttu-id="57f50-1388">american express</span><span class="sxs-lookup"><span data-stu-id="57f50-1388">american express</span></span>
- <span data-ttu-id="57f50-1389">AmericanExpress</span><span class="sxs-lookup"><span data-stu-id="57f50-1389">americanexpress</span></span>
- <span data-ttu-id="57f50-1390">Visa</span><span class="sxs-lookup"><span data-stu-id="57f50-1390">Visa</span></span>
- <span data-ttu-id="57f50-1391">MasterCard</span><span class="sxs-lookup"><span data-stu-id="57f50-1391">mastercard</span></span>
- <span data-ttu-id="57f50-1392">master card</span><span class="sxs-lookup"><span data-stu-id="57f50-1392">master card</span></span>
- <span data-ttu-id="57f50-1393">Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="57f50-1393">mc</span></span> 
- <span data-ttu-id="57f50-1394">MasterCards gesichert</span><span class="sxs-lookup"><span data-stu-id="57f50-1394">mastercards</span></span>
- <span data-ttu-id="57f50-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1395">master cards</span></span>
- <span data-ttu-id="57f50-1396">diner's Club</span><span class="sxs-lookup"><span data-stu-id="57f50-1396">diner's Club</span></span>
- <span data-ttu-id="57f50-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="57f50-1397">diners club</span></span>
- <span data-ttu-id="57f50-1398">DinersClub</span><span class="sxs-lookup"><span data-stu-id="57f50-1398">dinersclub</span></span>
- <span data-ttu-id="57f50-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="57f50-1399">discover card</span></span>
- <span data-ttu-id="57f50-1400">discovercard</span><span class="sxs-lookup"><span data-stu-id="57f50-1400">discovercard</span></span>
- <span data-ttu-id="57f50-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1401">discover cards</span></span>
- <span data-ttu-id="57f50-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="57f50-1402">JCB</span></span>
- <span data-ttu-id="57f50-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="57f50-1403">japanese card bureau</span></span>
- <span data-ttu-id="57f50-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="57f50-1404">carte blanche</span></span>
- <span data-ttu-id="57f50-1405">CarteBlanche</span><span class="sxs-lookup"><span data-stu-id="57f50-1405">carteblanche</span></span>
- <span data-ttu-id="57f50-1406">credit card</span><span class="sxs-lookup"><span data-stu-id="57f50-1406">credit card</span></span>
- <span data-ttu-id="57f50-1407">CC #</span><span class="sxs-lookup"><span data-stu-id="57f50-1407">cc#</span></span>
- <span data-ttu-id="57f50-1408">cc #:</span><span class="sxs-lookup"><span data-stu-id="57f50-1408">cc#:</span></span>
- <span data-ttu-id="57f50-1409">expiration date</span><span class="sxs-lookup"><span data-stu-id="57f50-1409">expiration date</span></span>
- <span data-ttu-id="57f50-1410">exp date</span><span class="sxs-lookup"><span data-stu-id="57f50-1410">exp date</span></span>
- <span data-ttu-id="57f50-1411">expiry date</span><span class="sxs-lookup"><span data-stu-id="57f50-1411">expiry date</span></span>
- <span data-ttu-id="57f50-1412">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="57f50-1412">date d’expiration</span></span>
- <span data-ttu-id="57f50-1413">date d'exp</span><span class="sxs-lookup"><span data-stu-id="57f50-1413">date d'exp</span></span>
- <span data-ttu-id="57f50-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="57f50-1414">date expiration</span></span>
- <span data-ttu-id="57f50-1415">bank card</span><span class="sxs-lookup"><span data-stu-id="57f50-1415">bank card</span></span>
- <span data-ttu-id="57f50-1416">Bankcard</span><span class="sxs-lookup"><span data-stu-id="57f50-1416">bankcard</span></span>
- <span data-ttu-id="57f50-1417">card number</span><span class="sxs-lookup"><span data-stu-id="57f50-1417">card number</span></span>
- <span data-ttu-id="57f50-1418">card num</span><span class="sxs-lookup"><span data-stu-id="57f50-1418">card num</span></span>
- <span data-ttu-id="57f50-1419">cardNumber</span><span class="sxs-lookup"><span data-stu-id="57f50-1419">cardnumber</span></span>
- <span data-ttu-id="57f50-1420">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="57f50-1420">cardnumbers</span></span>
- <span data-ttu-id="57f50-1421">card numbers</span><span class="sxs-lookup"><span data-stu-id="57f50-1421">card numbers</span></span>
- <span data-ttu-id="57f50-1422">CreditCard</span><span class="sxs-lookup"><span data-stu-id="57f50-1422">creditcard</span></span>
- <span data-ttu-id="57f50-1423">credit cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1423">credit cards</span></span>
- <span data-ttu-id="57f50-1424">creditCards</span><span class="sxs-lookup"><span data-stu-id="57f50-1424">creditcards</span></span>
- <span data-ttu-id="57f50-1425">Angaben</span><span class="sxs-lookup"><span data-stu-id="57f50-1425">ccn</span></span>
- <span data-ttu-id="57f50-1426">card holder</span><span class="sxs-lookup"><span data-stu-id="57f50-1426">card holder</span></span>
- <span data-ttu-id="57f50-1427">Inhaber</span><span class="sxs-lookup"><span data-stu-id="57f50-1427">cardholder</span></span>
- <span data-ttu-id="57f50-1428">card holders</span><span class="sxs-lookup"><span data-stu-id="57f50-1428">card holders</span></span>
- <span data-ttu-id="57f50-1429">Inhaber</span><span class="sxs-lookup"><span data-stu-id="57f50-1429">cardholders</span></span>
- <span data-ttu-id="57f50-1430">check card</span><span class="sxs-lookup"><span data-stu-id="57f50-1430">check card</span></span>
- <span data-ttu-id="57f50-1431">checkcard</span><span class="sxs-lookup"><span data-stu-id="57f50-1431">checkcard</span></span>
- <span data-ttu-id="57f50-1432">check cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1432">check cards</span></span>
- <span data-ttu-id="57f50-1433">checkcards</span><span class="sxs-lookup"><span data-stu-id="57f50-1433">checkcards</span></span>
- <span data-ttu-id="57f50-1434">debit card</span><span class="sxs-lookup"><span data-stu-id="57f50-1434">debit card</span></span>
- <span data-ttu-id="57f50-1435">Debitkarte</span><span class="sxs-lookup"><span data-stu-id="57f50-1435">debitcard</span></span>
- <span data-ttu-id="57f50-1436">debit cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1436">debit cards</span></span>
- <span data-ttu-id="57f50-1437">debitcards</span><span class="sxs-lookup"><span data-stu-id="57f50-1437">debitcards</span></span>
- <span data-ttu-id="57f50-1438">atm card</span><span class="sxs-lookup"><span data-stu-id="57f50-1438">atm card</span></span>
- <span data-ttu-id="57f50-1439">atmcard</span><span class="sxs-lookup"><span data-stu-id="57f50-1439">atmcard</span></span>
- <span data-ttu-id="57f50-1440">atm cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1440">atm cards</span></span>
- <span data-ttu-id="57f50-1441">atmcards</span><span class="sxs-lookup"><span data-stu-id="57f50-1441">atmcards</span></span>
- <span data-ttu-id="57f50-1442">enroute</span><span class="sxs-lookup"><span data-stu-id="57f50-1442">enroute</span></span>
- <span data-ttu-id="57f50-1443">en route</span><span class="sxs-lookup"><span data-stu-id="57f50-1443">en route</span></span>
- <span data-ttu-id="57f50-1444">card type</span><span class="sxs-lookup"><span data-stu-id="57f50-1444">card type</span></span>
- <span data-ttu-id="57f50-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="57f50-1445">carte bancaire</span></span>
- <span data-ttu-id="57f50-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="57f50-1446">carte de crédit</span></span>
- <span data-ttu-id="57f50-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="57f50-1447">carte de credit</span></span>
- <span data-ttu-id="57f50-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="57f50-1448">numéro de carte</span></span>
- <span data-ttu-id="57f50-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="57f50-1449">numero de carte</span></span>
- <span data-ttu-id="57f50-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="57f50-1450">nº de la carte</span></span>
- <span data-ttu-id="57f50-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="57f50-1451">nº de carte</span></span>
- <span data-ttu-id="57f50-1452">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="57f50-1452">kreditkarte</span></span>
- <span data-ttu-id="57f50-1453">Karte</span><span class="sxs-lookup"><span data-stu-id="57f50-1453">karte</span></span>
- <span data-ttu-id="57f50-1454">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="57f50-1454">karteninhaber</span></span>
- <span data-ttu-id="57f50-1455">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="57f50-1455">karteninhabers</span></span>
- <span data-ttu-id="57f50-1456">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="57f50-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="57f50-1457">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="57f50-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="57f50-1458">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="57f50-1458">kreditkartentyp</span></span>
- <span data-ttu-id="57f50-1459">eigentümername</span><span class="sxs-lookup"><span data-stu-id="57f50-1459">eigentümername</span></span>
- <span data-ttu-id="57f50-1460">kartennr</span><span class="sxs-lookup"><span data-stu-id="57f50-1460">kartennr</span></span> 
- <span data-ttu-id="57f50-1461">kartennummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1461">kartennummer</span></span>
- <span data-ttu-id="57f50-1462">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1462">kreditkartennummer</span></span>
- <span data-ttu-id="57f50-1463">Kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="57f50-1464">carta di credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1464">carta di credito</span></span>
- <span data-ttu-id="57f50-1465">carta credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1465">carta credito</span></span>
- <span data-ttu-id="57f50-1466">Carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1466">carta</span></span>
- <span data-ttu-id="57f50-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1467">n carta</span></span>
- <span data-ttu-id="57f50-1468">Nr.</span><span class="sxs-lookup"><span data-stu-id="57f50-1468">nr.</span></span> <span data-ttu-id="57f50-1469">Carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1469">carta</span></span>
- <span data-ttu-id="57f50-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1470">nr carta</span></span>
- <span data-ttu-id="57f50-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1471">numero carta</span></span>
- <span data-ttu-id="57f50-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1472">numero della carta</span></span>
- <span data-ttu-id="57f50-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1473">numero di carta</span></span>
- <span data-ttu-id="57f50-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1474">tarjeta credito</span></span>
- <span data-ttu-id="57f50-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1475">tarjeta de credito</span></span>
- <span data-ttu-id="57f50-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="57f50-1476">tarjeta crédito</span></span>
- <span data-ttu-id="57f50-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="57f50-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="57f50-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="57f50-1478">tarjeta de atm</span></span>
- <span data-ttu-id="57f50-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="57f50-1479">tarjeta atm</span></span>
- <span data-ttu-id="57f50-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="57f50-1480">tarjeta debito</span></span>
- <span data-ttu-id="57f50-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="57f50-1481">tarjeta de debito</span></span>
- <span data-ttu-id="57f50-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="57f50-1482">tarjeta débito</span></span>
- <span data-ttu-id="57f50-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="57f50-1483">tarjeta de débito</span></span>
- <span data-ttu-id="57f50-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="57f50-1484">nº de tarjeta</span></span>
- <span data-ttu-id="57f50-1485">Nein.</span><span class="sxs-lookup"><span data-stu-id="57f50-1485">no.</span></span> <span data-ttu-id="57f50-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="57f50-1486">de tarjeta</span></span>
- <span data-ttu-id="57f50-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="57f50-1487">no de tarjeta</span></span>
- <span data-ttu-id="57f50-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="57f50-1488">numero de tarjeta</span></span>
- <span data-ttu-id="57f50-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="57f50-1489">número de tarjeta</span></span>
- <span data-ttu-id="57f50-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="57f50-1490">tarjeta no</span></span>
- <span data-ttu-id="57f50-1491">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="57f50-1491">tarjetahabiente</span></span>
- <span data-ttu-id="57f50-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="57f50-1492">cartão de crédito</span></span>
- <span data-ttu-id="57f50-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1493">cartão de credito</span></span>
- <span data-ttu-id="57f50-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="57f50-1494">cartao de crédito</span></span>
- <span data-ttu-id="57f50-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1495">cartao de credito</span></span>
- <span data-ttu-id="57f50-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="57f50-1496">cartão de débito</span></span>
- <span data-ttu-id="57f50-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="57f50-1497">cartao de débito</span></span>
- <span data-ttu-id="57f50-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="57f50-1498">cartão de debito</span></span>
- <span data-ttu-id="57f50-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="57f50-1499">cartao de debito</span></span>
- <span data-ttu-id="57f50-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="57f50-1500">débito automático</span></span>
- <span data-ttu-id="57f50-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="57f50-1501">debito automatico</span></span>
- <span data-ttu-id="57f50-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1502">número do cartão</span></span>
- <span data-ttu-id="57f50-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1503">numero do cartão</span></span> 
- <span data-ttu-id="57f50-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1504">número do cartao</span></span>
- <span data-ttu-id="57f50-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1505">numero do cartao</span></span>
- <span data-ttu-id="57f50-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1506">número de cartão</span></span>
- <span data-ttu-id="57f50-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1507">numero de cartão</span></span>
- <span data-ttu-id="57f50-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1508">número de cartao</span></span>
- <span data-ttu-id="57f50-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1509">numero de cartao</span></span>
- <span data-ttu-id="57f50-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1510">nº do cartão</span></span>
- <span data-ttu-id="57f50-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1511">nº do cartao</span></span>
- <span data-ttu-id="57f50-1512">nº.</span><span class="sxs-lookup"><span data-stu-id="57f50-1512">nº.</span></span> <span data-ttu-id="57f50-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1513">do cartão</span></span>
- <span data-ttu-id="57f50-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1514">no do cartão</span></span>
- <span data-ttu-id="57f50-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1515">no do cartao</span></span>
- <span data-ttu-id="57f50-1516">Nein.</span><span class="sxs-lookup"><span data-stu-id="57f50-1516">no.</span></span> <span data-ttu-id="57f50-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1517">do cartão</span></span>
- <span data-ttu-id="57f50-1518">Nein.</span><span class="sxs-lookup"><span data-stu-id="57f50-1518">no.</span></span> <span data-ttu-id="57f50-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="57f50-1520">	Kroatien – Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1521">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1521">Format</span></span>

<span data-ttu-id="57f50-1522">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1523">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1523">Pattern</span></span>

<span data-ttu-id="57f50-1524">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1525">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1525">Checksum</span></span>

<span data-ttu-id="57f50-1526">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1527">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1527">Definition</span></span>

<span data-ttu-id="57f50-1528">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1529">Die Funktion Func_croatia_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1530">Ein Schlüsselwort aus Keyword_croatia_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```xml
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-1531">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1531">Keywords</span></span>

#### <a name="keyword_croatia_id_card"></a><span data-ttu-id="57f50-1532">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="57f50-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="57f50-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="57f50-1533">Croatian identity card</span></span>
- <span data-ttu-id="57f50-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="57f50-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="57f50-1535">	Croatia Personal Identification (OIB) Number</span><span class="sxs-lookup"><span data-stu-id="57f50-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1536">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1536">Format</span></span>

<span data-ttu-id="57f50-1537">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1538">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1538">Pattern</span></span>

<span data-ttu-id="57f50-1539">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-1539">11 digits:</span></span>
- <span data-ttu-id="57f50-1540">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1540">10 digits</span></span> 
- <span data-ttu-id="57f50-1541">Letzte Ziffer ist eine Prüfziffer für den Zweck des internationalen Datenaustauschs, die Buchstaben HR werden vor den elf Ziffern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1542">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1542">Checksum</span></span>

<span data-ttu-id="57f50-1543">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1544">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1544">Definition</span></span>

<span data-ttu-id="57f50-1545">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1546">Die Funktion Func_croatia_oib_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1547">Ein Schlüsselwort aus Keyword_croatia_oib_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="57f50-1548">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1548">The checksum passes.</span></span>

<span data-ttu-id="57f50-1549">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1550">Die Funktion Func_croatia_oib_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1551">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1551">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-1552">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1552">Keywords</span></span>

#### <a name="keyword_croatia_oib_number"></a><span data-ttu-id="57f50-1553">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="57f50-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="57f50-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="57f50-1554">Personal Identification Number</span></span>
- <span data-ttu-id="57f50-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="57f50-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="57f50-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="57f50-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="57f50-1557">Tschechische Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1558">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1558">Format</span></span>

<span data-ttu-id="57f50-1559">Neun Ziffern mit optionalem Schrägstrich (altes Format) 10 Ziffern mit optionalem Schrägstrich (neues Format)</span><span class="sxs-lookup"><span data-stu-id="57f50-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1560">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1560">Pattern</span></span>

<span data-ttu-id="57f50-1561">Neun Ziffern (altes Format):</span><span class="sxs-lookup"><span data-stu-id="57f50-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="57f50-1562">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1562">Nine digits</span></span>

<span data-ttu-id="57f50-1563">ODER</span><span class="sxs-lookup"><span data-stu-id="57f50-1563">OR</span></span>

- <span data-ttu-id="57f50-1564">Sechs Ziffern, die das Geburtsdatum darstellen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="57f50-1565">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="57f50-1565">A forward slash</span></span>
- <span data-ttu-id="57f50-1566">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1566">Three digits</span></span>

<span data-ttu-id="57f50-1567">10 Ziffern (neues Format):</span><span class="sxs-lookup"><span data-stu-id="57f50-1567">10 digits (new format):</span></span>
- <span data-ttu-id="57f50-1568">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1568">10 digits</span></span>

<span data-ttu-id="57f50-1569">ODER</span><span class="sxs-lookup"><span data-stu-id="57f50-1569">OR</span></span>

- <span data-ttu-id="57f50-1570">Sechs Ziffern, die das Geburtsdatum darstellen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="57f50-1571">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="57f50-1571">A forward slash</span></span> 
- <span data-ttu-id="57f50-1572">Vier Ziffern, wobei die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="57f50-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1573">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1573">Checksum</span></span>

<span data-ttu-id="57f50-1574">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1575">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1575">Definition</span></span>

<span data-ttu-id="57f50-1576">Eine DLP-Richtlinie ist 85% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: die Funktion Func_czech_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="57f50-1577">Ein Schlüsselwort aus Keyword_czech_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="57f50-1578">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1578">The checksum passes.</span></span>

```xml
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="57f50-1579">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1579">Keywords</span></span>

- <span data-ttu-id="57f50-1580">Tschechische Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1580">czech personal identity number</span></span>
- <span data-ttu-id="57f50-1581">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="57f50-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="57f50-1582">	Dänemark – Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1583">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1583">Format</span></span>

<span data-ttu-id="57f50-1584">10 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="57f50-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1585">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1585">Pattern</span></span>

<span data-ttu-id="57f50-1586">10 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-1586">10 digits:</span></span>
- <span data-ttu-id="57f50-1587">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="57f50-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="57f50-1588">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-1588">A hyphen</span></span> 
- <span data-ttu-id="57f50-1589">Vier Ziffern, bei denen die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="57f50-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1590">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1590">Checksum</span></span>

<span data-ttu-id="57f50-1591">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1592">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1592">Definition</span></span>

<span data-ttu-id="57f50-1593">Eine DLP-Richtlinie ist 75% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: der reguläre Ausdruck Regex_denmark_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="57f50-1594">Ein Schlüsselwort aus Keyword_denmark_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="57f50-1595">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1595">The checksum passes.</span></span>

```xml
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-1596">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1596">Keywords</span></span>

#### <a name="keyword_denmark_id"></a><span data-ttu-id="57f50-1597">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="57f50-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="57f50-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="57f50-1598">Personal Identification Number</span></span>
- <span data-ttu-id="57f50-1599">CPR</span><span class="sxs-lookup"><span data-stu-id="57f50-1599">CPR</span></span>
- <span data-ttu-id="57f50-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="57f50-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="57f50-1601">Personnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="57f50-1602">Drug Enforcement Agency (DEA)-Nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1603">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1603">Format</span></span>

<span data-ttu-id="57f50-1604">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1605">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1605">Pattern</span></span>

<span data-ttu-id="57f50-1606">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="57f50-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="57f50-1607">Einen Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) aus der folgenden Gruppe möglicher Buchstaben: abcdefghjklmnprstux, was einem Registrantencode entspricht</span><span class="sxs-lookup"><span data-stu-id="57f50-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="57f50-1608">Ein Buchstabe (bei dem die Groß-und Kleinschreibung nicht beachtet wird), der dem ersten Buchstaben des Nachnamens des Registrants entspricht</span><span class="sxs-lookup"><span data-stu-id="57f50-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="57f50-1609">Sieben Ziffern, von denen die letzte die Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="57f50-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1610">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1610">Checksum</span></span>

<span data-ttu-id="57f50-1611">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1612">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1612">Definition</span></span>

<span data-ttu-id="57f50-1613">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1614">Die Funktion Func_dea_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1615">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1615">The checksum passes.</span></span>

```xml
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-1616">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1616">Keywords</span></span>

<span data-ttu-id="57f50-1617">Keine</span><span class="sxs-lookup"><span data-stu-id="57f50-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="57f50-1618">EU Debit Card-Nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1619">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1619">Format</span></span>

<span data-ttu-id="57f50-1620">16 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1621">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1621">Pattern</span></span>

<span data-ttu-id="57f50-1622">Sehr komplexes und robustes Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1623">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1623">Checksum</span></span>

<span data-ttu-id="57f50-1624">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1625">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1625">Definition</span></span>

<span data-ttu-id="57f50-1626">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1627">Die Funktion Func_eu_debit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1628">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="57f50-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="57f50-1629">Ein Schlüsselwort aus Keyword_eu_debit_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="57f50-1630">Ein Schlüsselwort aus Keyword_card_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="57f50-1631">Ein Schlüsselwort aus Keyword_card_security_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="57f50-1632">Ein Schlüsselwort aus Keyword_card_expiration_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="57f50-1633">Die Funktion Func_expiration_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="57f50-1634">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1634">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-1635">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1635">Keywords</span></span>

#### <a name="keyword_eu_debit_card"></a><span data-ttu-id="57f50-1636">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="57f50-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="57f50-1637">account number</span><span class="sxs-lookup"><span data-stu-id="57f50-1637">account number</span></span> 
- <span data-ttu-id="57f50-1638">card number</span><span class="sxs-lookup"><span data-stu-id="57f50-1638">card number</span></span> 
- <span data-ttu-id="57f50-1639">card no.</span><span class="sxs-lookup"><span data-stu-id="57f50-1639">card no.</span></span> 
- <span data-ttu-id="57f50-1640">security number</span><span class="sxs-lookup"><span data-stu-id="57f50-1640">security number</span></span> 
- <span data-ttu-id="57f50-1641">CC #</span><span class="sxs-lookup"><span data-stu-id="57f50-1641">cc#</span></span> 

#### <a name="keyword_card_terms_dict"></a><span data-ttu-id="57f50-1642">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="57f50-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="57f50-1643">acct nbr</span><span class="sxs-lookup"><span data-stu-id="57f50-1643">acct nbr</span></span> 
- <span data-ttu-id="57f50-1644">acct num</span><span class="sxs-lookup"><span data-stu-id="57f50-1644">acct num</span></span> 
- <span data-ttu-id="57f50-1645">acct no</span><span class="sxs-lookup"><span data-stu-id="57f50-1645">acct no</span></span> 
- <span data-ttu-id="57f50-1646">american express</span><span class="sxs-lookup"><span data-stu-id="57f50-1646">american express</span></span> 
- <span data-ttu-id="57f50-1647">AmericanExpress</span><span class="sxs-lookup"><span data-stu-id="57f50-1647">americanexpress</span></span> 
- <span data-ttu-id="57f50-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="57f50-1648">americano espresso</span></span> 
- <span data-ttu-id="57f50-1649">Amex</span><span class="sxs-lookup"><span data-stu-id="57f50-1649">amex</span></span> 
- <span data-ttu-id="57f50-1650">atm card</span><span class="sxs-lookup"><span data-stu-id="57f50-1650">atm card</span></span> 
- <span data-ttu-id="57f50-1651">atm cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1651">atm cards</span></span> 
- <span data-ttu-id="57f50-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="57f50-1652">atm kaart</span></span> 
- <span data-ttu-id="57f50-1653">atmcard</span><span class="sxs-lookup"><span data-stu-id="57f50-1653">atmcard</span></span> 
- <span data-ttu-id="57f50-1654">atmcards</span><span class="sxs-lookup"><span data-stu-id="57f50-1654">atmcards</span></span> 
- <span data-ttu-id="57f50-1655">atmkaart</span><span class="sxs-lookup"><span data-stu-id="57f50-1655">atmkaart</span></span> 
- <span data-ttu-id="57f50-1656">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="57f50-1656">atmkaarten</span></span> 
- <span data-ttu-id="57f50-1657">Bancontact</span><span class="sxs-lookup"><span data-stu-id="57f50-1657">bancontact</span></span> 
- <span data-ttu-id="57f50-1658">bank card</span><span class="sxs-lookup"><span data-stu-id="57f50-1658">bank card</span></span> 
- <span data-ttu-id="57f50-1659">bankkaart</span><span class="sxs-lookup"><span data-stu-id="57f50-1659">bankkaart</span></span> 
- <span data-ttu-id="57f50-1660">card holder</span><span class="sxs-lookup"><span data-stu-id="57f50-1660">card holder</span></span> 
- <span data-ttu-id="57f50-1661">card holders</span><span class="sxs-lookup"><span data-stu-id="57f50-1661">card holders</span></span> 
- <span data-ttu-id="57f50-1662">card num</span><span class="sxs-lookup"><span data-stu-id="57f50-1662">card num</span></span> 
- <span data-ttu-id="57f50-1663">card number</span><span class="sxs-lookup"><span data-stu-id="57f50-1663">card number</span></span> 
- <span data-ttu-id="57f50-1664">card numbers</span><span class="sxs-lookup"><span data-stu-id="57f50-1664">card numbers</span></span> 
- <span data-ttu-id="57f50-1665">card type</span><span class="sxs-lookup"><span data-stu-id="57f50-1665">card type</span></span> 
- <span data-ttu-id="57f50-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="57f50-1666">cardano numerico</span></span> 
- <span data-ttu-id="57f50-1667">Inhaber</span><span class="sxs-lookup"><span data-stu-id="57f50-1667">cardholder</span></span> 
- <span data-ttu-id="57f50-1668">Inhaber</span><span class="sxs-lookup"><span data-stu-id="57f50-1668">cardholders</span></span> 
- <span data-ttu-id="57f50-1669">cardNumber</span><span class="sxs-lookup"><span data-stu-id="57f50-1669">cardnumber</span></span> 
- <span data-ttu-id="57f50-1670">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="57f50-1670">cardnumbers</span></span> 
- <span data-ttu-id="57f50-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="57f50-1671">carta bianca</span></span> 
- <span data-ttu-id="57f50-1672">carta credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1672">carta credito</span></span> 
- <span data-ttu-id="57f50-1673">carta di credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1673">carta di credito</span></span> 
- <span data-ttu-id="57f50-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1674">cartao de credito</span></span> 
- <span data-ttu-id="57f50-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="57f50-1675">cartao de crédito</span></span> 
- <span data-ttu-id="57f50-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="57f50-1676">cartao de debito</span></span> 
- <span data-ttu-id="57f50-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="57f50-1677">cartao de débito</span></span> 
- <span data-ttu-id="57f50-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="57f50-1678">carte bancaire</span></span> 
- <span data-ttu-id="57f50-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="57f50-1679">carte blanche</span></span> 
- <span data-ttu-id="57f50-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="57f50-1680">carte bleue</span></span> 
- <span data-ttu-id="57f50-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="57f50-1681">carte de credit</span></span> 
- <span data-ttu-id="57f50-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="57f50-1682">carte de crédit</span></span> 
- <span data-ttu-id="57f50-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1683">carte di credito</span></span> 
- <span data-ttu-id="57f50-1684">CarteBlanche</span><span class="sxs-lookup"><span data-stu-id="57f50-1684">carteblanche</span></span> 
- <span data-ttu-id="57f50-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1685">cartão de credito</span></span> 
- <span data-ttu-id="57f50-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="57f50-1686">cartão de crédito</span></span> 
- <span data-ttu-id="57f50-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="57f50-1687">cartão de debito</span></span> 
- <span data-ttu-id="57f50-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="57f50-1688">cartão de débito</span></span> 
- <span data-ttu-id="57f50-1689">cb</span><span class="sxs-lookup"><span data-stu-id="57f50-1689">cb</span></span> 
- <span data-ttu-id="57f50-1690">Angaben</span><span class="sxs-lookup"><span data-stu-id="57f50-1690">ccn</span></span> 
- <span data-ttu-id="57f50-1691">check card</span><span class="sxs-lookup"><span data-stu-id="57f50-1691">check card</span></span> 
- <span data-ttu-id="57f50-1692">check cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1692">check cards</span></span> 
- <span data-ttu-id="57f50-1693">checkcard</span><span class="sxs-lookup"><span data-stu-id="57f50-1693">checkcard</span></span>
- <span data-ttu-id="57f50-1694">checkcards</span><span class="sxs-lookup"><span data-stu-id="57f50-1694">checkcards</span></span> 
- <span data-ttu-id="57f50-1695">chequekaart</span><span class="sxs-lookup"><span data-stu-id="57f50-1695">chequekaart</span></span> 
- <span data-ttu-id="57f50-1696">Cirrus</span><span class="sxs-lookup"><span data-stu-id="57f50-1696">cirrus</span></span> 
- <span data-ttu-id="57f50-1697">Cirrus-EDC-Maestro</span><span class="sxs-lookup"><span data-stu-id="57f50-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="57f50-1698">controlekaart</span><span class="sxs-lookup"><span data-stu-id="57f50-1698">controlekaart</span></span> 
- <span data-ttu-id="57f50-1699">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="57f50-1699">controlekaarten</span></span> 
- <span data-ttu-id="57f50-1700">credit card</span><span class="sxs-lookup"><span data-stu-id="57f50-1700">credit card</span></span> 
- <span data-ttu-id="57f50-1701">credit cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1701">credit cards</span></span> 
- <span data-ttu-id="57f50-1702">CreditCard</span><span class="sxs-lookup"><span data-stu-id="57f50-1702">creditcard</span></span> 
- <span data-ttu-id="57f50-1703">creditCards</span><span class="sxs-lookup"><span data-stu-id="57f50-1703">creditcards</span></span> 
- <span data-ttu-id="57f50-1704">debetkaart</span><span class="sxs-lookup"><span data-stu-id="57f50-1704">debetkaart</span></span> 
- <span data-ttu-id="57f50-1705">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="57f50-1705">debetkaarten</span></span> 
- <span data-ttu-id="57f50-1706">debit card</span><span class="sxs-lookup"><span data-stu-id="57f50-1706">debit card</span></span> 
- <span data-ttu-id="57f50-1707">debit cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1707">debit cards</span></span> 
- <span data-ttu-id="57f50-1708">Debitkarte</span><span class="sxs-lookup"><span data-stu-id="57f50-1708">debitcard</span></span> 
- <span data-ttu-id="57f50-1709">debitcards</span><span class="sxs-lookup"><span data-stu-id="57f50-1709">debitcards</span></span> 
- <span data-ttu-id="57f50-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="57f50-1710">debito automatico</span></span> 
- <span data-ttu-id="57f50-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="57f50-1711">diners club</span></span> 
- <span data-ttu-id="57f50-1712">DinersClub</span><span class="sxs-lookup"><span data-stu-id="57f50-1712">dinersclub</span></span> 
- <span data-ttu-id="57f50-1713">ermitteln</span><span class="sxs-lookup"><span data-stu-id="57f50-1713">discover</span></span> 
- <span data-ttu-id="57f50-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="57f50-1714">discover card</span></span> 
- <span data-ttu-id="57f50-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1715">discover cards</span></span> 
- <span data-ttu-id="57f50-1716">discovercard</span><span class="sxs-lookup"><span data-stu-id="57f50-1716">discovercard</span></span> 
- <span data-ttu-id="57f50-1717">discovercards</span><span class="sxs-lookup"><span data-stu-id="57f50-1717">discovercards</span></span> 
- <span data-ttu-id="57f50-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="57f50-1718">débito automático</span></span>
- <span data-ttu-id="57f50-1719">EDC</span><span class="sxs-lookup"><span data-stu-id="57f50-1719">edc</span></span> 
- <span data-ttu-id="57f50-1720">eigentümername</span><span class="sxs-lookup"><span data-stu-id="57f50-1720">eigentümername</span></span> 
- <span data-ttu-id="57f50-1721">european debit card</span><span class="sxs-lookup"><span data-stu-id="57f50-1721">european debit card</span></span> 
- <span data-ttu-id="57f50-1722">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="57f50-1722">hoofdkaart</span></span> 
- <span data-ttu-id="57f50-1723">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="57f50-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="57f50-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="57f50-1724">in viaggio</span></span> 
- <span data-ttu-id="57f50-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="57f50-1725">japanese card bureau</span></span> 
- <span data-ttu-id="57f50-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="57f50-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="57f50-1727">JCB</span><span class="sxs-lookup"><span data-stu-id="57f50-1727">jcb</span></span> 
- <span data-ttu-id="57f50-1728">Kaart</span><span class="sxs-lookup"><span data-stu-id="57f50-1728">kaart</span></span> 
- <span data-ttu-id="57f50-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="57f50-1729">kaart num</span></span> 
- <span data-ttu-id="57f50-1730">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="57f50-1730">kaartaantal</span></span> 
- <span data-ttu-id="57f50-1731">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="57f50-1731">kaartaantallen</span></span> 
- <span data-ttu-id="57f50-1732">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="57f50-1732">kaarthouder</span></span> 
- <span data-ttu-id="57f50-1733">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="57f50-1733">kaarthouders</span></span> 
- <span data-ttu-id="57f50-1734">Karte</span><span class="sxs-lookup"><span data-stu-id="57f50-1734">karte</span></span>  
- <span data-ttu-id="57f50-1735">karteninhaber</span><span class="sxs-lookup"><span data-stu-id="57f50-1735">karteninhaber</span></span> 
- <span data-ttu-id="57f50-1736">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="57f50-1736">karteninhabers</span></span>
- <span data-ttu-id="57f50-1737">kartennr</span><span class="sxs-lookup"><span data-stu-id="57f50-1737">kartennr</span></span> 
- <span data-ttu-id="57f50-1738">kartennummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1738">kartennummer</span></span> 
- <span data-ttu-id="57f50-1739">kreditkarte</span><span class="sxs-lookup"><span data-stu-id="57f50-1739">kreditkarte</span></span> 
- <span data-ttu-id="57f50-1740">Kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="57f50-1741">kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="57f50-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="57f50-1742">kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="57f50-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="57f50-1743">kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="57f50-1744">kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="57f50-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="57f50-1745">Maestro</span><span class="sxs-lookup"><span data-stu-id="57f50-1745">maestro</span></span> 
- <span data-ttu-id="57f50-1746">master card</span><span class="sxs-lookup"><span data-stu-id="57f50-1746">master card</span></span> 
- <span data-ttu-id="57f50-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="57f50-1747">master cards</span></span> 
- <span data-ttu-id="57f50-1748">MasterCard</span><span class="sxs-lookup"><span data-stu-id="57f50-1748">mastercard</span></span> 
- <span data-ttu-id="57f50-1749">MasterCards gesichert</span><span class="sxs-lookup"><span data-stu-id="57f50-1749">mastercards</span></span> 
- <span data-ttu-id="57f50-1750">Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="57f50-1750">mc</span></span> 
- <span data-ttu-id="57f50-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="57f50-1751">mister cash</span></span> 
- <span data-ttu-id="57f50-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1752">n carta</span></span> 
- <span data-ttu-id="57f50-1753">Carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1753">carta</span></span> 
- <span data-ttu-id="57f50-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="57f50-1754">no de tarjeta</span></span> 
- <span data-ttu-id="57f50-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1755">no do cartao</span></span> 
- <span data-ttu-id="57f50-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1756">no do cartão</span></span> 
- <span data-ttu-id="57f50-1757">Nein.</span><span class="sxs-lookup"><span data-stu-id="57f50-1757">no.</span></span> <span data-ttu-id="57f50-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="57f50-1758">de tarjeta</span></span> 
- <span data-ttu-id="57f50-1759">Nein.</span><span class="sxs-lookup"><span data-stu-id="57f50-1759">no.</span></span> <span data-ttu-id="57f50-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1760">do cartao</span></span> 
- <span data-ttu-id="57f50-1761">Nein.</span><span class="sxs-lookup"><span data-stu-id="57f50-1761">no.</span></span> <span data-ttu-id="57f50-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1762">do cartão</span></span> 
- <span data-ttu-id="57f50-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1763">nr carta</span></span> 
- <span data-ttu-id="57f50-1764">Nr.</span><span class="sxs-lookup"><span data-stu-id="57f50-1764">nr.</span></span> <span data-ttu-id="57f50-1765">Carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1765">carta</span></span> 
- <span data-ttu-id="57f50-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="57f50-1766">numeri di scheda</span></span> 
- <span data-ttu-id="57f50-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1767">numero carta</span></span> 
- <span data-ttu-id="57f50-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1768">numero de cartao</span></span> 
- <span data-ttu-id="57f50-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="57f50-1769">numero de carte</span></span> 
- <span data-ttu-id="57f50-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1770">numero de cartão</span></span> 
- <span data-ttu-id="57f50-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="57f50-1771">numero de tarjeta</span></span>
- <span data-ttu-id="57f50-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1772">numero della carta</span></span> 
- <span data-ttu-id="57f50-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1773">numero di carta</span></span> 
- <span data-ttu-id="57f50-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="57f50-1774">numero di scheda</span></span> 
- <span data-ttu-id="57f50-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1775">numero do cartao</span></span> 
- <span data-ttu-id="57f50-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1776">numero do cartão</span></span> 
- <span data-ttu-id="57f50-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="57f50-1777">numéro de carte</span></span> 
- <span data-ttu-id="57f50-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="57f50-1778">nº carta</span></span> 
- <span data-ttu-id="57f50-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="57f50-1779">nº de carte</span></span> 
- <span data-ttu-id="57f50-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="57f50-1780">nº de la carte</span></span> 
- <span data-ttu-id="57f50-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="57f50-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="57f50-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1782">nº do cartao</span></span> 
- <span data-ttu-id="57f50-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1783">nº do cartão</span></span> 
- <span data-ttu-id="57f50-1784">nº.</span><span class="sxs-lookup"><span data-stu-id="57f50-1784">nº.</span></span> <span data-ttu-id="57f50-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1785">do cartão</span></span> 
- <span data-ttu-id="57f50-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1786">número de cartao</span></span> 
- <span data-ttu-id="57f50-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="57f50-1787">número de cartão</span></span> 
- <span data-ttu-id="57f50-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="57f50-1788">número de tarjeta</span></span> 
- <span data-ttu-id="57f50-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="57f50-1789">número do cartao</span></span> 
- <span data-ttu-id="57f50-1790">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="57f50-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="57f50-1791">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="57f50-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="57f50-1792">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="57f50-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="57f50-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="57f50-1793">scheda della banca</span></span> 
- <span data-ttu-id="57f50-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="57f50-1794">scheda di controllo</span></span> 
- <span data-ttu-id="57f50-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="57f50-1795">scheda di debito</span></span> 
- <span data-ttu-id="57f50-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="57f50-1796">scheda matrice</span></span> 
- <span data-ttu-id="57f50-1797">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="57f50-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="57f50-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="57f50-1798">schede di controllo</span></span> 
- <span data-ttu-id="57f50-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="57f50-1799">schede di debito</span></span> 
- <span data-ttu-id="57f50-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="57f50-1800">schede matrici</span></span> 
- <span data-ttu-id="57f50-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="57f50-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="57f50-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="57f50-1802">scoprono le schede</span></span> 
- <span data-ttu-id="57f50-1803">Solo</span><span class="sxs-lookup"><span data-stu-id="57f50-1803">solo</span></span> 
- <span data-ttu-id="57f50-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="57f50-1804">supporti di scheda</span></span> 
- <span data-ttu-id="57f50-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="57f50-1805">supporto di scheda</span></span> 
- <span data-ttu-id="57f50-1806">Schalter</span><span class="sxs-lookup"><span data-stu-id="57f50-1806">switch</span></span> 
- <span data-ttu-id="57f50-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="57f50-1807">tarjeta atm</span></span> 
- <span data-ttu-id="57f50-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1808">tarjeta credito</span></span> 
- <span data-ttu-id="57f50-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="57f50-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="57f50-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="57f50-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="57f50-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="57f50-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="57f50-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="57f50-1812">tarjeta debito</span></span> 
- <span data-ttu-id="57f50-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="57f50-1813">tarjeta no</span></span>
- <span data-ttu-id="57f50-1814">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="57f50-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="57f50-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="57f50-1815">tipo della scheda</span></span> 
- <span data-ttu-id="57f50-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="57f50-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="57f50-1817">Scheda</span><span class="sxs-lookup"><span data-stu-id="57f50-1817">scheda</span></span> 
- <span data-ttu-id="57f50-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="57f50-1818">v pay</span></span> 
- <span data-ttu-id="57f50-1819">v-Pay</span><span class="sxs-lookup"><span data-stu-id="57f50-1819">v-pay</span></span> 
- <span data-ttu-id="57f50-1820">Visa</span><span class="sxs-lookup"><span data-stu-id="57f50-1820">visa</span></span> 
- <span data-ttu-id="57f50-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="57f50-1821">visa plus</span></span> 
- <span data-ttu-id="57f50-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="57f50-1822">visa electron</span></span> 
- <span data-ttu-id="57f50-1823">Visto</span><span class="sxs-lookup"><span data-stu-id="57f50-1823">visto</span></span> 
- <span data-ttu-id="57f50-1824">Visum</span><span class="sxs-lookup"><span data-stu-id="57f50-1824">visum</span></span> 
- <span data-ttu-id="57f50-1825">vpay</span><span class="sxs-lookup"><span data-stu-id="57f50-1825">vpay</span></span>   

#### <a name="keyword_card_security_terms_dict"></a><span data-ttu-id="57f50-1826">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="57f50-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="57f50-1827">card identification number</span><span class="sxs-lookup"><span data-stu-id="57f50-1827">card identification number</span></span>
- <span data-ttu-id="57f50-1828">card verification</span><span class="sxs-lookup"><span data-stu-id="57f50-1828">card verification</span></span> 
- <span data-ttu-id="57f50-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="57f50-1829">cardi la verifica</span></span> 
- <span data-ttu-id="57f50-1830">cid</span><span class="sxs-lookup"><span data-stu-id="57f50-1830">cid</span></span> 
- <span data-ttu-id="57f50-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="57f50-1831">cod seg</span></span> 
- <span data-ttu-id="57f50-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="57f50-1832">cod seguranca</span></span> 
- <span data-ttu-id="57f50-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1833">cod segurança</span></span> 
- <span data-ttu-id="57f50-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="57f50-1834">cod sicurezza</span></span> 
- <span data-ttu-id="57f50-1835">COD.</span><span class="sxs-lookup"><span data-stu-id="57f50-1835">cod.</span></span> <span data-ttu-id="57f50-1836">SEG</span><span class="sxs-lookup"><span data-stu-id="57f50-1836">seg</span></span> 
- <span data-ttu-id="57f50-1837">COD.</span><span class="sxs-lookup"><span data-stu-id="57f50-1837">cod.</span></span> <span data-ttu-id="57f50-1838">seguranca</span><span class="sxs-lookup"><span data-stu-id="57f50-1838">seguranca</span></span> 
- <span data-ttu-id="57f50-1839">COD.</span><span class="sxs-lookup"><span data-stu-id="57f50-1839">cod.</span></span> <span data-ttu-id="57f50-1840">Segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1840">segurança</span></span> 
- <span data-ttu-id="57f50-1841">COD.</span><span class="sxs-lookup"><span data-stu-id="57f50-1841">cod.</span></span> <span data-ttu-id="57f50-1842">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="57f50-1842">sicurezza</span></span> 
- <span data-ttu-id="57f50-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="57f50-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="57f50-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="57f50-1844">codice di verifica</span></span> 
- <span data-ttu-id="57f50-1845">codigo</span><span class="sxs-lookup"><span data-stu-id="57f50-1845">codigo</span></span> 
- <span data-ttu-id="57f50-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="57f50-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="57f50-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1847">codigo de segurança</span></span> 
- <span data-ttu-id="57f50-1848">crittogramma</span><span class="sxs-lookup"><span data-stu-id="57f50-1848">crittogramma</span></span> 
- <span data-ttu-id="57f50-1849">Kryptogramm</span><span class="sxs-lookup"><span data-stu-id="57f50-1849">cryptogram</span></span> 
- <span data-ttu-id="57f50-1850">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="57f50-1850">cryptogramme</span></span> 
- <span data-ttu-id="57f50-1851">CV2</span><span class="sxs-lookup"><span data-stu-id="57f50-1851">cv2</span></span> 
- <span data-ttu-id="57f50-1852">CVC</span><span class="sxs-lookup"><span data-stu-id="57f50-1852">cvc</span></span> 
- <span data-ttu-id="57f50-1853">CVC2</span><span class="sxs-lookup"><span data-stu-id="57f50-1853">cvc2</span></span> 
- <span data-ttu-id="57f50-1854">CVN</span><span class="sxs-lookup"><span data-stu-id="57f50-1854">cvn</span></span> 
- <span data-ttu-id="57f50-1855">CVV</span><span class="sxs-lookup"><span data-stu-id="57f50-1855">cvv</span></span> 
- <span data-ttu-id="57f50-1856">CVV2</span><span class="sxs-lookup"><span data-stu-id="57f50-1856">cvv2</span></span> 
- <span data-ttu-id="57f50-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="57f50-1857">cód seguranca</span></span> 
- <span data-ttu-id="57f50-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1858">cód segurança</span></span> 
- <span data-ttu-id="57f50-1859">cód.</span><span class="sxs-lookup"><span data-stu-id="57f50-1859">cód.</span></span> <span data-ttu-id="57f50-1860">seguranca</span><span class="sxs-lookup"><span data-stu-id="57f50-1860">seguranca</span></span> 
- <span data-ttu-id="57f50-1861">cód.</span><span class="sxs-lookup"><span data-stu-id="57f50-1861">cód.</span></span> <span data-ttu-id="57f50-1862">Segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1862">segurança</span></span> 
- <span data-ttu-id="57f50-1863">Código</span><span class="sxs-lookup"><span data-stu-id="57f50-1863">código</span></span> 
- <span data-ttu-id="57f50-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="57f50-1864">código de seguranca</span></span> 
- <span data-ttu-id="57f50-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="57f50-1865">código de segurança</span></span> 
- <span data-ttu-id="57f50-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="57f50-1866">de kaart controle</span></span> 
- <span data-ttu-id="57f50-1867">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="57f50-1867">geeft nr uit</span></span> 
- <span data-ttu-id="57f50-1868">issue no</span><span class="sxs-lookup"><span data-stu-id="57f50-1868">issue no</span></span> 
- <span data-ttu-id="57f50-1869">issue number</span><span class="sxs-lookup"><span data-stu-id="57f50-1869">issue number</span></span> 
- <span data-ttu-id="57f50-1870">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="57f50-1871">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="57f50-1872">kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="57f50-1873">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="57f50-1873">kwestieaantal</span></span> 
- <span data-ttu-id="57f50-1874">Nein.</span><span class="sxs-lookup"><span data-stu-id="57f50-1874">no.</span></span> <span data-ttu-id="57f50-1875">Dell ' edizione</span><span class="sxs-lookup"><span data-stu-id="57f50-1875">dell'edizione</span></span> 
- <span data-ttu-id="57f50-1876">Nein.</span><span class="sxs-lookup"><span data-stu-id="57f50-1876">no.</span></span> <span data-ttu-id="57f50-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="57f50-1877">di sicurezza</span></span> 
- <span data-ttu-id="57f50-1878">numero de securite</span><span class="sxs-lookup"><span data-stu-id="57f50-1878">numero de securite</span></span> 
- <span data-ttu-id="57f50-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="57f50-1879">numero de verificacao</span></span> 
- <span data-ttu-id="57f50-1880">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="57f50-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="57f50-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="57f50-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="57f50-1882">Scheda</span><span class="sxs-lookup"><span data-stu-id="57f50-1882">scheda</span></span> 
- <span data-ttu-id="57f50-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="57f50-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="57f50-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="57f50-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="57f50-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="57f50-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="57f50-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="57f50-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="57f50-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="57f50-1887">número de verificação</span></span> 
- <span data-ttu-id="57f50-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="57f50-1888">perno il blocco</span></span> 
- <span data-ttu-id="57f50-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="57f50-1889">pin block</span></span> 
- <span data-ttu-id="57f50-1890">prufziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-1890">prufziffer</span></span> 
- <span data-ttu-id="57f50-1891">prüfziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-1891">prüfziffer</span></span> 
- <span data-ttu-id="57f50-1892">security code</span><span class="sxs-lookup"><span data-stu-id="57f50-1892">security code</span></span> 
- <span data-ttu-id="57f50-1893">security no</span><span class="sxs-lookup"><span data-stu-id="57f50-1893">security no</span></span> 
- <span data-ttu-id="57f50-1894">security number</span><span class="sxs-lookup"><span data-stu-id="57f50-1894">security number</span></span> 
- <span data-ttu-id="57f50-1895">Sicherheitskode</span><span class="sxs-lookup"><span data-stu-id="57f50-1895">sicherheits kode</span></span> 
- <span data-ttu-id="57f50-1896">sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="57f50-1896">sicherheitscode</span></span> 
- <span data-ttu-id="57f50-1897">sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="57f50-1898">speldblok</span><span class="sxs-lookup"><span data-stu-id="57f50-1898">speldblok</span></span> 
- <span data-ttu-id="57f50-1899">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="57f50-1899">veiligheid nr</span></span> 
- <span data-ttu-id="57f50-1900">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="57f50-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="57f50-1901">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="57f50-1901">veiligheidscode</span></span> 
- <span data-ttu-id="57f50-1902">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="57f50-1903">verfalldatum</span><span class="sxs-lookup"><span data-stu-id="57f50-1903">verfalldatum</span></span> 

#### <a name="keyword_card_expiration_terms_dict"></a><span data-ttu-id="57f50-1904">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="57f50-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="57f50-1905">Ablauf</span><span class="sxs-lookup"><span data-stu-id="57f50-1905">ablauf</span></span> 
- <span data-ttu-id="57f50-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="57f50-1906">data de expiracao</span></span> 
- <span data-ttu-id="57f50-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="57f50-1907">data de expiração</span></span> 
- <span data-ttu-id="57f50-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="57f50-1908">data del exp</span></span> 
- <span data-ttu-id="57f50-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="57f50-1909">data di exp</span></span> 
- <span data-ttu-id="57f50-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="57f50-1910">data di scadenza</span></span> 
- <span data-ttu-id="57f50-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="57f50-1911">data em que expira</span></span> 
- <span data-ttu-id="57f50-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="57f50-1912">data scad</span></span> 
- <span data-ttu-id="57f50-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="57f50-1913">data scadenza</span></span> 
- <span data-ttu-id="57f50-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="57f50-1914">date de validité</span></span> 
- <span data-ttu-id="57f50-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="57f50-1915">datum afloop</span></span> 
- <span data-ttu-id="57f50-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="57f50-1916">datum van exp</span></span> 
- <span data-ttu-id="57f50-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="57f50-1917">de afloop</span></span> 
- <span data-ttu-id="57f50-1918">Espira</span><span class="sxs-lookup"><span data-stu-id="57f50-1918">espira</span></span> 
- <span data-ttu-id="57f50-1919">Espira</span><span class="sxs-lookup"><span data-stu-id="57f50-1919">espira</span></span> 
- <span data-ttu-id="57f50-1920">exp date</span><span class="sxs-lookup"><span data-stu-id="57f50-1920">exp date</span></span> 
- <span data-ttu-id="57f50-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="57f50-1921">exp datum</span></span> 
- <span data-ttu-id="57f50-1922">Ablauf</span><span class="sxs-lookup"><span data-stu-id="57f50-1922">expiration</span></span> 
- <span data-ttu-id="57f50-1923">ablaufen</span><span class="sxs-lookup"><span data-stu-id="57f50-1923">expire</span></span> 
- <span data-ttu-id="57f50-1924">abläuft</span><span class="sxs-lookup"><span data-stu-id="57f50-1924">expires</span></span> 
- <span data-ttu-id="57f50-1925">Ablauf</span><span class="sxs-lookup"><span data-stu-id="57f50-1925">expiry</span></span> 
- <span data-ttu-id="57f50-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="57f50-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="57f50-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="57f50-1927">fecha de venc</span></span> 
- <span data-ttu-id="57f50-1928">Gultig bis</span><span class="sxs-lookup"><span data-stu-id="57f50-1928">gultig bis</span></span> 
- <span data-ttu-id="57f50-1929">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="57f50-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="57f50-1930">Gültig bis</span><span class="sxs-lookup"><span data-stu-id="57f50-1930">gültig bis</span></span> 
- <span data-ttu-id="57f50-1931">gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="57f50-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="57f50-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="57f50-1932">la scadenza</span></span> 
- <span data-ttu-id="57f50-1933">scadenza</span><span class="sxs-lookup"><span data-stu-id="57f50-1933">scadenza</span></span> 
- <span data-ttu-id="57f50-1934">valable</span><span class="sxs-lookup"><span data-stu-id="57f50-1934">valable</span></span> 
- <span data-ttu-id="57f50-1935">validade</span><span class="sxs-lookup"><span data-stu-id="57f50-1935">validade</span></span> 
- <span data-ttu-id="57f50-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="57f50-1936">valido hasta</span></span> 
- <span data-ttu-id="57f50-1937">Valor</span><span class="sxs-lookup"><span data-stu-id="57f50-1937">valor</span></span> 
- <span data-ttu-id="57f50-1938">venc</span><span class="sxs-lookup"><span data-stu-id="57f50-1938">venc</span></span> 
- <span data-ttu-id="57f50-1939">vencimento</span><span class="sxs-lookup"><span data-stu-id="57f50-1939">vencimento</span></span> 
- <span data-ttu-id="57f50-1940">vencimiento</span><span class="sxs-lookup"><span data-stu-id="57f50-1940">vencimiento</span></span> 
- <span data-ttu-id="57f50-1941">verloopt</span><span class="sxs-lookup"><span data-stu-id="57f50-1941">verloopt</span></span> 
- <span data-ttu-id="57f50-1942">vervaldag</span><span class="sxs-lookup"><span data-stu-id="57f50-1942">vervaldag</span></span> 
- <span data-ttu-id="57f50-1943">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="57f50-1943">vervaldatum</span></span> 
- <span data-ttu-id="57f50-1944">VTO</span><span class="sxs-lookup"><span data-stu-id="57f50-1944">vto</span></span> 
- <span data-ttu-id="57f50-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="57f50-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="57f50-1946">EU-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1946">EU Driver's License Number</span></span>

<span data-ttu-id="57f50-1947">Weitere Informationen finden Sie unter [EU-Führerscheinnummer vertraulicher Informationstyp](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="57f50-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="57f50-1948">EU-nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1948">EU National Identification Number</span></span>

<span data-ttu-id="57f50-1949">Weitere Informationen finden Sie unter [sensible Informationstypen für die nationale Identifikationsnummer der EU](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="57f50-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="57f50-1950">EU-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1950">EU Passport Number</span></span>

<span data-ttu-id="57f50-1951">Weitere Informationen finden Sie unter [sensible Informationstypen für EU-Passport-Nummern](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="57f50-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="57f50-1952">EU-Sozialversicherungsnummer oder gleichwertige ID</span><span class="sxs-lookup"><span data-stu-id="57f50-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="57f50-1953">Weitere Informationen finden Sie unter [EU-Sozialversicherungsnummer oder gleichwertiger ID-Typ für vertrauliche Informationen](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="57f50-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="57f50-1954">EU-Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="57f50-1955">Weitere Informationen finden Sie unter [vertraulicher Informationstyp der EU-Steueridentifikationsnummer](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="57f50-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="57f50-1956">Finland National ID (Finnischer Personalausweis)</span><span class="sxs-lookup"><span data-stu-id="57f50-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1957">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1957">Format</span></span>

<span data-ttu-id="57f50-1958">Sechs Ziffern plus ein Zeichen, das ein Jahrhundert angibt, plus drei Ziffern plus einer Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1959">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1959">Pattern</span></span>

<span data-ttu-id="57f50-1960">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="57f50-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="57f50-1961">Sechs Ziffern im Format TTMMJJ, die ein Geburtsdatum darstellen</span><span class="sxs-lookup"><span data-stu-id="57f50-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="57f50-1962">Jahrhundertkennzeichnung (entweder „-“, „+“ oder „a“)</span><span class="sxs-lookup"><span data-stu-id="57f50-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="57f50-1963">Dreistellige persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="57f50-1964">Eine Ziffer oder ein Buchstabe (Groß-/Kleinschreibung irrelevant), die bzw. der eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="57f50-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1965">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1965">Checksum</span></span>

<span data-ttu-id="57f50-1966">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1967">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1967">Definition</span></span>

<span data-ttu-id="57f50-1968">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1969">Die Funktion Func_finnish_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1970">Ein Schlüsselwort aus Keyword_finnish_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="57f50-1971">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-1971">The checksum passes.</span></span>

```xml
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-1972">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1972">Keywords</span></span>

- <span data-ttu-id="57f50-1973">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="57f50-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="57f50-1974">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="57f50-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="57f50-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="57f50-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="57f50-1976">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="57f50-1976">Personbeteckning</span></span>
- <span data-ttu-id="57f50-1977">Personnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="57f50-1978">Finnland – Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1978">Finland Passport Number</span></span>

<span data-ttu-id="57f50-1979">Format Kombination von neun Buchstaben und Ziffern Muster Kombination aus neun Buchstaben und Ziffern: zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet) siebenstellige Prüfsumme keine Definition eine DLP-Richtlinie ist 75% zuversichtlich, dass diese Art von vertraulichen Informationen erkannt wurde, wenn innerhalb eines Proximity of 300 Characters: der reguläre Ausdruck Regex_finland_passport_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1979">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="57f50-1980">Ein Schlüsselwort aus Keyword_finland_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1980">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
<span data-ttu-id="57f50-1981"><Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="57f50-1981"></span></span>
<span data-ttu-id="57f50-1982">Schlüsselwörter Keyword_finland_passport_number Passport Passi</span><span class="sxs-lookup"><span data-stu-id="57f50-1982">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="57f50-1983">Französische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-1983">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-1984">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-1984">Format</span></span>

<span data-ttu-id="57f50-1985">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-1985">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-1986">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-1986">Pattern</span></span>

<span data-ttu-id="57f50-1987">12 Ziffern mit Validierung, um ähnliche Muster ( z. B. französische Telefonnummern) auszuschließen</span><span class="sxs-lookup"><span data-stu-id="57f50-1987">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-1988">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-1988">Checksum</span></span>

<span data-ttu-id="57f50-1989">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-1989">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-1990">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-1990">Definition</span></span>

<span data-ttu-id="57f50-1991">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-1991">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-1992">Die Funktion Func_french_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-1992">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-1993">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="57f50-1993">At least one of the following is true:</span></span>
- <span data-ttu-id="57f50-1994">Ein Schlüsselwort aus Keyword_french_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-1994">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="57f50-1995">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-1995">The function Func_eu_date finds a date in the right date format.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-1996">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-1996">Keywords</span></span>

#### <a name="keyword_french_drivers_license"></a><span data-ttu-id="57f50-1997">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="57f50-1997">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="57f50-1998">drivers licence</span><span class="sxs-lookup"><span data-stu-id="57f50-1998">drivers licence</span></span>
- <span data-ttu-id="57f50-1999">drivers license</span><span class="sxs-lookup"><span data-stu-id="57f50-1999">drivers license</span></span>
- <span data-ttu-id="57f50-2000">Führerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2000">driving licence</span></span>
- <span data-ttu-id="57f50-2001">driving license</span><span class="sxs-lookup"><span data-stu-id="57f50-2001">driving license</span></span>
- <span data-ttu-id="57f50-2002">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="57f50-2002">permis de conduire</span></span>
- <span data-ttu-id="57f50-2003">licence number</span><span class="sxs-lookup"><span data-stu-id="57f50-2003">licence number</span></span>
- <span data-ttu-id="57f50-2004">license number</span><span class="sxs-lookup"><span data-stu-id="57f50-2004">license number</span></span>
- <span data-ttu-id="57f50-2005">licence numbers</span><span class="sxs-lookup"><span data-stu-id="57f50-2005">licence numbers</span></span>
- <span data-ttu-id="57f50-2006">license numbers</span><span class="sxs-lookup"><span data-stu-id="57f50-2006">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="57f50-2007">Französische Carte nationale d'identité (CNI)</span><span class="sxs-lookup"><span data-stu-id="57f50-2007">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2008">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2008">Format</span></span>

<span data-ttu-id="57f50-2009">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2009">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2010">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2010">Pattern</span></span>

<span data-ttu-id="57f50-2011">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2011">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2012">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2012">Checksum</span></span>

<span data-ttu-id="57f50-2013">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2013">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2014">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2014">Definition</span></span>

<span data-ttu-id="57f50-2015">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2015">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2016">Der reguläre Ausdruck Regex_france_cni findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2016">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```xml
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2017">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2017">Keywords</span></span>

<span data-ttu-id="57f50-2018">Keine</span><span class="sxs-lookup"><span data-stu-id="57f50-2018">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="57f50-2019">Französische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2019">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2020">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2020">Format</span></span>

<span data-ttu-id="57f50-2021">Neun Ziffern und Buchstaben</span><span class="sxs-lookup"><span data-stu-id="57f50-2021">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2022">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2022">Pattern</span></span>

<span data-ttu-id="57f50-2023">Neun Ziffern und Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="57f50-2023">Nine digits and letters:</span></span>
- <span data-ttu-id="57f50-2024">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2024">Two digits</span></span> 
- <span data-ttu-id="57f50-2025">Zwei Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="57f50-2025">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="57f50-2026">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2026">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2027">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2027">Checksum</span></span>

<span data-ttu-id="57f50-2028">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2028">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2029">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2029">Definition</span></span>

<span data-ttu-id="57f50-2030">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2030">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2031">Die Funktion Func_fr_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2031">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2032">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2032">A keyword from Keyword_passport is found.</span></span>

```xml
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2033">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2033">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="57f50-2034">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="57f50-2034">Keyword_passport</span></span>

- <span data-ttu-id="57f50-2035">Passport Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2035">Passport Number</span></span>
- <span data-ttu-id="57f50-2036">Passport No</span><span class="sxs-lookup"><span data-stu-id="57f50-2036">Passport No</span></span>
- <span data-ttu-id="57f50-2037">Passport#</span><span class="sxs-lookup"><span data-stu-id="57f50-2037">Passport #</span></span>
- <span data-ttu-id="57f50-2038">Pass #</span><span class="sxs-lookup"><span data-stu-id="57f50-2038">Passport#</span></span>
- <span data-ttu-id="57f50-2039">Passport-Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-2039">PassportID</span></span>
- <span data-ttu-id="57f50-2040">Passportno</span><span class="sxs-lookup"><span data-stu-id="57f50-2040">Passportno</span></span>
- <span data-ttu-id="57f50-2041">passportnumber</span><span class="sxs-lookup"><span data-stu-id="57f50-2041">passportnumber</span></span>
- <span data-ttu-id="57f50-2042">パスポート</span><span class="sxs-lookup"><span data-stu-id="57f50-2042">パスポート</span></span>
- <span data-ttu-id="57f50-2043">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2043">パスポート番号</span></span>
- <span data-ttu-id="57f50-2044">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="57f50-2044">パスポートのNum</span></span>
- <span data-ttu-id="57f50-2045">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="57f50-2045">パスポート ＃</span></span> 
- <span data-ttu-id="57f50-2046">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="57f50-2046">Numéro de passeport</span></span>
- <span data-ttu-id="57f50-2047">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="57f50-2047">Passeport n °</span></span>
- <span data-ttu-id="57f50-2048">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="57f50-2048">Passeport Non</span></span>
- <span data-ttu-id="57f50-2049">Passeport#</span><span class="sxs-lookup"><span data-stu-id="57f50-2049">Passeport #</span></span>
- <span data-ttu-id="57f50-2050">Passeport #</span><span class="sxs-lookup"><span data-stu-id="57f50-2050">Passeport#</span></span>
- <span data-ttu-id="57f50-2051">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="57f50-2051">PasseportNon</span></span>
- <span data-ttu-id="57f50-2052">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="57f50-2052">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="57f50-2053">Französische Sozialversicherungsnummer (INSEE)</span><span class="sxs-lookup"><span data-stu-id="57f50-2053">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2054">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2054">Format</span></span>

<span data-ttu-id="57f50-2055">15 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2055">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2056">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2056">Pattern</span></span>

<span data-ttu-id="57f50-2057">Muss einem von zwei Mustern entsprechen:</span><span class="sxs-lookup"><span data-stu-id="57f50-2057">Must match one of two patterns:</span></span>
- <span data-ttu-id="57f50-2058">13 Ziffern, gefolgt von einem Leerzeichen, gefolgt von zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2058">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="57f50-2059">oder</span><span class="sxs-lookup"><span data-stu-id="57f50-2059">or</span></span>
- <span data-ttu-id="57f50-2060">15 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2060">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2061">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2061">Checksum</span></span>

<span data-ttu-id="57f50-2062">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2062">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2063">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2063">Definition</span></span>

<span data-ttu-id="57f50-2064">Eine DLP-Richtlinie ist zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2064">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2065">Die Funktion Func_french_insee oder Func_fr_insee sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2065">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2066">Ein Schlüsselwort aus Keyword_fr_insee wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2066">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="57f50-2067">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2067">The checksum passes.</span></span>

<span data-ttu-id="57f50-2068">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2068">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2069">Die Funktion Func_french_insee oder Func_fr_insee sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2069">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2070">Es wurde kein Schlüsselwort aus Keyword_fr_insee gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2070">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="57f50-2071">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2071">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2072">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2072">Keywords</span></span>

#### <a name="keyword_fr_insee"></a><span data-ttu-id="57f50-2073">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="57f50-2073">Keyword_fr_insee</span></span>

- <span data-ttu-id="57f50-2074">INSEE</span><span class="sxs-lookup"><span data-stu-id="57f50-2074">insee</span></span>
- <span data-ttu-id="57f50-2075">securité sociale</span><span class="sxs-lookup"><span data-stu-id="57f50-2075">securité sociale</span></span>
- <span data-ttu-id="57f50-2076">securite sociale</span><span class="sxs-lookup"><span data-stu-id="57f50-2076">securite sociale</span></span>
- <span data-ttu-id="57f50-2077">national id</span><span class="sxs-lookup"><span data-stu-id="57f50-2077">national id</span></span>
- <span data-ttu-id="57f50-2078">national identification</span><span class="sxs-lookup"><span data-stu-id="57f50-2078">national identification</span></span>
- <span data-ttu-id="57f50-2079">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="57f50-2079">numéro d'identité</span></span>
- <span data-ttu-id="57f50-2080">no d'identité</span><span class="sxs-lookup"><span data-stu-id="57f50-2080">no d'identité</span></span>
- <span data-ttu-id="57f50-2081">Nein.</span><span class="sxs-lookup"><span data-stu-id="57f50-2081">no.</span></span> <span data-ttu-id="57f50-2082">d ' identité</span><span class="sxs-lookup"><span data-stu-id="57f50-2082">d'identité</span></span>
- <span data-ttu-id="57f50-2083">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="57f50-2083">numero d'identite</span></span>
- <span data-ttu-id="57f50-2084">no d'identite</span><span class="sxs-lookup"><span data-stu-id="57f50-2084">no d'identite</span></span>
- <span data-ttu-id="57f50-2085">Nein.</span><span class="sxs-lookup"><span data-stu-id="57f50-2085">no.</span></span> <span data-ttu-id="57f50-2086">d'identite</span><span class="sxs-lookup"><span data-stu-id="57f50-2086">d'identite</span></span>
- <span data-ttu-id="57f50-2087">social security number</span><span class="sxs-lookup"><span data-stu-id="57f50-2087">social security number</span></span>
- <span data-ttu-id="57f50-2088">social security code</span><span class="sxs-lookup"><span data-stu-id="57f50-2088">social security code</span></span>
- <span data-ttu-id="57f50-2089">social insurance number</span><span class="sxs-lookup"><span data-stu-id="57f50-2089">social insurance number</span></span>
- <span data-ttu-id="57f50-2090">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="57f50-2090">le numéro d'identification nationale</span></span>
- <span data-ttu-id="57f50-2091">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="57f50-2091">d'identité nationale</span></span>
- <span data-ttu-id="57f50-2092">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="57f50-2092">numéro de sécurité sociale</span></span>
- <span data-ttu-id="57f50-2093">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="57f50-2093">le code de la sécurité sociale</span></span>
- <span data-ttu-id="57f50-2094">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="57f50-2094">numéro d'assurance sociale</span></span>
- <span data-ttu-id="57f50-2095">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="57f50-2095">numéro de sécu</span></span>
- <span data-ttu-id="57f50-2096">code sécu</span><span class="sxs-lookup"><span data-stu-id="57f50-2096">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="57f50-2097">Deutsche Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2097">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2098">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2098">Format</span></span>

<span data-ttu-id="57f50-2099">Kombination von 11 Ziffern und Buchstaben</span><span class="sxs-lookup"><span data-stu-id="57f50-2099">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2100">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2100">Pattern</span></span>

<span data-ttu-id="57f50-2101">11 Zahlen und Buchstaben (ohne Beachtung der Groß-/Kleinschreibung):</span><span class="sxs-lookup"><span data-stu-id="57f50-2101">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="57f50-2102">Eine Ziffer oder ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="57f50-2102">A digit or letter</span></span> 
- <span data-ttu-id="57f50-2103">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2103">Two digits</span></span> 
- <span data-ttu-id="57f50-2104">Sechs Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="57f50-2104">Six digits or letters</span></span> 
- <span data-ttu-id="57f50-2105">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-2105">A digit</span></span> 
- <span data-ttu-id="57f50-2106">Eine Ziffer oder ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="57f50-2106">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2107">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2107">Checksum</span></span>

<span data-ttu-id="57f50-2108">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2108">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2109">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2109">Definition</span></span>

<span data-ttu-id="57f50-2110">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2110">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2111">Die Funktion Func_german_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2111">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2112">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="57f50-2112">At least one of the following is true:</span></span>
    - <span data-ttu-id="57f50-2113">Ein Schlüsselwort aus Keyword_german_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2113">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="57f50-2114">Ein Schlüsselwort aus Keyword_german_drivers_license_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2114">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="57f50-2115">Ein Schlüsselwort aus Keyword_german_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2115">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="57f50-2116">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2116">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2117">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2117">Keywords</span></span>

#### <a name="keyword_german_drivers_license_number"></a><span data-ttu-id="57f50-2118">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2118">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="57f50-2119">Führerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2119">Führerschein</span></span>
- <span data-ttu-id="57f50-2120">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2120">Fuhrerschein</span></span>
- <span data-ttu-id="57f50-2121">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2121">Fuehrerschein</span></span>
- <span data-ttu-id="57f50-2122">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2122">Führerscheinnummer</span></span>
- <span data-ttu-id="57f50-2123">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2123">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="57f50-2124">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2124">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="57f50-2125">Führerschein-</span><span class="sxs-lookup"><span data-stu-id="57f50-2125">Führerschein-</span></span> 
- <span data-ttu-id="57f50-2126">Fuhrerschein-</span><span class="sxs-lookup"><span data-stu-id="57f50-2126">Fuhrerschein-</span></span> 
- <span data-ttu-id="57f50-2127">Fuehrerschein-</span><span class="sxs-lookup"><span data-stu-id="57f50-2127">Fuehrerschein-</span></span> 
- <span data-ttu-id="57f50-2128">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="57f50-2128">FührerscheinnummerNr</span></span>
- <span data-ttu-id="57f50-2129">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="57f50-2129">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="57f50-2130">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="57f50-2130">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="57f50-2131">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2131">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="57f50-2132">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2132">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="57f50-2133">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2133">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="57f50-2134">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-2134">Führerschein- Nr</span></span>
- <span data-ttu-id="57f50-2135">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-2135">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="57f50-2136">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-2136">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="57f50-2137">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2137">Führerschein- Klasse</span></span> 
- <span data-ttu-id="57f50-2138">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2138">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="57f50-2139">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2139">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="57f50-2140">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="57f50-2140">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="57f50-2141">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="57f50-2141">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="57f50-2142">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="57f50-2142">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="57f50-2143">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2143">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="57f50-2144">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2144">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="57f50-2145">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2145">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="57f50-2146">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-2146">Führerschein- Nr</span></span> 
- <span data-ttu-id="57f50-2147">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-2147">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="57f50-2148">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-2148">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="57f50-2149">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2149">Führerschein- Klasse</span></span> 
- <span data-ttu-id="57f50-2150">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2150">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="57f50-2151">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2151">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="57f50-2152">DL</span><span class="sxs-lookup"><span data-stu-id="57f50-2152">DL</span></span> 
- <span data-ttu-id="57f50-2153">DLS</span><span class="sxs-lookup"><span data-stu-id="57f50-2153">DLS</span></span>
- <span data-ttu-id="57f50-2154">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-2154">Driv Lic</span></span> 
- <span data-ttu-id="57f50-2155">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="57f50-2155">Driv Licen</span></span> 
- <span data-ttu-id="57f50-2156">Driv License</span><span class="sxs-lookup"><span data-stu-id="57f50-2156">Driv License</span></span>
- <span data-ttu-id="57f50-2157">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-2157">Driv Licenses</span></span> 
- <span data-ttu-id="57f50-2158">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-2158">Driv Licence</span></span> 
- <span data-ttu-id="57f50-2159">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-2159">Driv Licences</span></span> 
- <span data-ttu-id="57f50-2160">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-2160">Driv Lic</span></span> 
- <span data-ttu-id="57f50-2161">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="57f50-2161">Driver Licen</span></span> 
- <span data-ttu-id="57f50-2162">Driver License</span><span class="sxs-lookup"><span data-stu-id="57f50-2162">Driver License</span></span> 
- <span data-ttu-id="57f50-2163">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-2163">Driver Licenses</span></span> 
- <span data-ttu-id="57f50-2164">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-2164">Driver Licence</span></span> 
- <span data-ttu-id="57f50-2165">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-2165">Driver Licences</span></span> 
- <span data-ttu-id="57f50-2166">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-2166">Drivers Lic</span></span> 
- <span data-ttu-id="57f50-2167">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="57f50-2167">Drivers Licen</span></span> 
- <span data-ttu-id="57f50-2168">Drivers License</span><span class="sxs-lookup"><span data-stu-id="57f50-2168">Drivers License</span></span> 
- <span data-ttu-id="57f50-2169">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-2169">Drivers Licenses</span></span> 
- <span data-ttu-id="57f50-2170">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-2170">Drivers Licence</span></span> 
- <span data-ttu-id="57f50-2171">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-2171">Drivers Licences</span></span> 
- <span data-ttu-id="57f50-2172">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-2172">Driver's Lic</span></span> 
- <span data-ttu-id="57f50-2173">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="57f50-2173">Driver's Licen</span></span> 
- <span data-ttu-id="57f50-2174">Driver's License</span><span class="sxs-lookup"><span data-stu-id="57f50-2174">Driver's License</span></span> 
- <span data-ttu-id="57f50-2175">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-2175">Driver's Licenses</span></span> 
- <span data-ttu-id="57f50-2176">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-2176">Driver's Licence</span></span> 
- <span data-ttu-id="57f50-2177">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-2177">Driver's Licences</span></span> 
- <span data-ttu-id="57f50-2178">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-2178">Driving Lic</span></span> 
- <span data-ttu-id="57f50-2179">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="57f50-2179">Driving Licen</span></span> 
- <span data-ttu-id="57f50-2180">Driving License</span><span class="sxs-lookup"><span data-stu-id="57f50-2180">Driving License</span></span> 
- <span data-ttu-id="57f50-2181">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-2181">Driving Licenses</span></span> 
- <span data-ttu-id="57f50-2182">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="57f50-2182">Driving Licence</span></span> 
- <span data-ttu-id="57f50-2183">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="57f50-2183">Driving Licences</span></span>

#### <a name="keyword_german_drivers_license_collaborative"></a><span data-ttu-id="57f50-2184">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="57f50-2184">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="57f50-2185">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2185">Nr-Führerschein</span></span> 
- <span data-ttu-id="57f50-2186">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2186">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="57f50-2187">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2187">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="57f50-2188">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2188">No-Führerschein</span></span> 
- <span data-ttu-id="57f50-2189">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2189">No-Fuhrerschein</span></span> 
- <span data-ttu-id="57f50-2190">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2190">No-Fuehrerschein</span></span> 
- <span data-ttu-id="57f50-2191">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2191">N-Führerschein</span></span> 
- <span data-ttu-id="57f50-2192">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2192">N-Fuhrerschein</span></span> 
- <span data-ttu-id="57f50-2193">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2193">N-Fuehrerschein</span></span>
- <span data-ttu-id="57f50-2194">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2194">Nr-Führerschein</span></span> 
- <span data-ttu-id="57f50-2195">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2195">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="57f50-2196">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2196">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="57f50-2197">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2197">No-Führerschein</span></span> 
- <span data-ttu-id="57f50-2198">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2198">No-Fuhrerschein</span></span> 
- <span data-ttu-id="57f50-2199">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2199">No-Fuehrerschein</span></span> 
- <span data-ttu-id="57f50-2200">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2200">N-Führerschein</span></span> 
- <span data-ttu-id="57f50-2201">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2201">N-Fuhrerschein</span></span> 
- <span data-ttu-id="57f50-2202">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="57f50-2202">N-Fuehrerschein</span></span> 

#### <a name="keyword_german_drivers_license"></a><span data-ttu-id="57f50-2203">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="57f50-2203">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="57f50-2204">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="57f50-2204">ausstellungsdatum</span></span>
- <span data-ttu-id="57f50-2205">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="57f50-2205">ausstellungsort</span></span>
- <span data-ttu-id="57f50-2206">Ausstellende Behöde</span><span class="sxs-lookup"><span data-stu-id="57f50-2206">ausstellende behöde</span></span>
- <span data-ttu-id="57f50-2207">Ausstellende Behorde</span><span class="sxs-lookup"><span data-stu-id="57f50-2207">ausstellende behorde</span></span>
- <span data-ttu-id="57f50-2208">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="57f50-2208">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="57f50-2209">Deutsche Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2209">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2210">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2210">Format</span></span>

<span data-ttu-id="57f50-2211">10 Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="57f50-2211">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2212">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2212">Pattern</span></span>

<span data-ttu-id="57f50-2213">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="57f50-2213">Pattern must include all of the following:</span></span>
- <span data-ttu-id="57f50-2214">Das erste Zeichen ist eine Ziffer oder ein Buchstabe aus dieser Gruppe (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="57f50-2214">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="57f50-2215">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2215">Three digits</span></span> 
- <span data-ttu-id="57f50-2216">Fünf Ziffern oder Buchstaben aus dieser Gruppe (C -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="57f50-2216">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="57f50-2217">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-2217">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2218">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2218">Checksum</span></span>

<span data-ttu-id="57f50-2219">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2219">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2220">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2220">Definition</span></span>

<span data-ttu-id="57f50-2221">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2221">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2222">Die Funktion Func_german_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2222">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2223">Ein Schlüsselwort aus einer der fünf Schlüsselwortlisten wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2223">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="57f50-2224">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2224">The checksum passes.</span></span>

<span data-ttu-id="57f50-2225">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2226">Die Funktion Func_german_passport_data findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2226">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2227">Ein Schlüsselwort aus einer der fünf Schlüsselwortlisten wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2227">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="57f50-2228">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2228">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2229">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2229">Keywords</span></span>

#### <a name="keyword_german_passport"></a><span data-ttu-id="57f50-2230">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="57f50-2230">Keyword_german_passport</span></span>

- <span data-ttu-id="57f50-2231">Reisepass</span><span class="sxs-lookup"><span data-stu-id="57f50-2231">reisepass</span></span>
- <span data-ttu-id="57f50-2232">reisepasse</span><span class="sxs-lookup"><span data-stu-id="57f50-2232">reisepasse</span></span>
- <span data-ttu-id="57f50-2233">reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2233">reisepassnummer</span></span>
- <span data-ttu-id="57f50-2234">Pass</span><span class="sxs-lookup"><span data-stu-id="57f50-2234">passport</span></span>
- <span data-ttu-id="57f50-2235">Pässe</span><span class="sxs-lookup"><span data-stu-id="57f50-2235">passports</span></span>

#### <a name="keyword_german_passport_collaborative"></a><span data-ttu-id="57f50-2236">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="57f50-2236">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="57f50-2237">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="57f50-2237">geburtsdatum</span></span>
- <span data-ttu-id="57f50-2238">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="57f50-2238">ausstellungsdatum</span></span>
- <span data-ttu-id="57f50-2239">ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="57f50-2239">ausstellungsort</span></span>

#### <a name="keyword_german_passport_number"></a><span data-ttu-id="57f50-2240">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2240">Keyword_german_passport_number</span></span>

<span data-ttu-id="57f50-2241">No-Reisepass Nr-Reisepass</span><span class="sxs-lookup"><span data-stu-id="57f50-2241">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keyword_german_passport1"></a><span data-ttu-id="57f50-2242">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="57f50-2242">Keyword_german_passport1</span></span>

<span data-ttu-id="57f50-2243">Reisepass-Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-2243">Reisepass-Nr</span></span>

#### <a name="keyword_german_passport2"></a><span data-ttu-id="57f50-2244">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="57f50-2244">Keyword_german_passport2</span></span>

<span data-ttu-id="57f50-2245">bnationalit. t</span><span class="sxs-lookup"><span data-stu-id="57f50-2245">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="57f50-2246">Deutsche Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2246">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2247">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2247">Format</span></span>

<span data-ttu-id="57f50-2248">Seit dem 1. November 2010: neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2248">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="57f50-2249">Vom 1. April 1987 bis 31. Oktober 2010:10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2249">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2250">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2250">Pattern</span></span>

<span data-ttu-id="57f50-2251">Seit 1. November 2010:</span><span class="sxs-lookup"><span data-stu-id="57f50-2251">Since 1 November 2010:</span></span>
- <span data-ttu-id="57f50-2252">Ein Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="57f50-2252">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="57f50-2253">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2253">Eight digits</span></span>

<span data-ttu-id="57f50-2254">Vom 1. April 1987 bis 31. Oktober 2010:</span><span class="sxs-lookup"><span data-stu-id="57f50-2254">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="57f50-2255">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2255">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2256">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2256">Checksum</span></span>

<span data-ttu-id="57f50-2257">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2257">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2258">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2258">Definition</span></span>

<span data-ttu-id="57f50-2259">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2259">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2260">Der reguläre Ausdruck Regex_germany_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2260">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2261">Ein Schlüsselwort aus Keyword_germany_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2261">A keyword from Keyword_germany_id_card is found.</span></span>

```xml
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2262">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2262">Keywords</span></span>

#### <a name="keyword_germany_id_card"></a><span data-ttu-id="57f50-2263">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="57f50-2263">Keyword_germany_id_card</span></span>

- <span data-ttu-id="57f50-2264">Identity Card</span><span class="sxs-lookup"><span data-stu-id="57f50-2264">Identity Card</span></span>
- <span data-ttu-id="57f50-2265">ID</span><span class="sxs-lookup"><span data-stu-id="57f50-2265">ID</span></span>
- <span data-ttu-id="57f50-2266">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="57f50-2266">Identification</span></span>
- <span data-ttu-id="57f50-2267">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-2267">Personalausweis</span></span>
- <span data-ttu-id="57f50-2268">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2268">Identifizierungsnummer</span></span>
- <span data-ttu-id="57f50-2269">Ausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-2269">Ausweis</span></span>
- <span data-ttu-id="57f50-2270">Identifikation</span><span class="sxs-lookup"><span data-stu-id="57f50-2270">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="57f50-2271">Griechenland – Personalausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-2271">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2272">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2272">Format</span></span>

<span data-ttu-id="57f50-2273">Kombination von 7-8 Buchstaben und Zahlen plus einem Gedankenstrich</span><span class="sxs-lookup"><span data-stu-id="57f50-2273">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2274">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2274">Pattern</span></span>

<span data-ttu-id="57f50-2275">Sieben Buchstaben und Zahlen (altes Format):</span><span class="sxs-lookup"><span data-stu-id="57f50-2275">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="57f50-2276">Ein Buchstabe (jeder Buchstabe des griechischen Alphabets) </span><span class="sxs-lookup"><span data-stu-id="57f50-2276">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="57f50-2277">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-2277">A dash</span></span> 
- <span data-ttu-id="57f50-2278">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2278">Six digits</span></span>

<span data-ttu-id="57f50-2279">Acht Buchstaben und Zahlen (neues Format):</span><span class="sxs-lookup"><span data-stu-id="57f50-2279">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="57f50-2280">Zwei Buchstaben, deren Großbuchstabe sowohl im griechischen als auch lateinischen Alphabet (ABEZHIKMNOPTYX) vorkommt </span><span class="sxs-lookup"><span data-stu-id="57f50-2280">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="57f50-2281">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-2281">A dash</span></span> 
- <span data-ttu-id="57f50-2282">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2282">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2283">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2283">Checksum</span></span>

<span data-ttu-id="57f50-2284">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2284">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2285">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2285">Definition</span></span>

<span data-ttu-id="57f50-2286">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2286">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2287">Der reguläre Ausdruck Regex_greece_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2287">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2288">Ein Schlüsselwort aus Keyword_greece_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2288">A keyword from Keyword_greece_id_card is found.</span></span>

```xml
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2289">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2289">Keywords</span></span>

#### <a name="keyword_greece_id_card"></a><span data-ttu-id="57f50-2290">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="57f50-2290">Keyword_greece_id_card</span></span>

- <span data-ttu-id="57f50-2291">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="57f50-2291">Greek identity Card</span></span>
- <span data-ttu-id="57f50-2292">Tautotita</span><span class="sxs-lookup"><span data-stu-id="57f50-2292">Tautotita</span></span>
- <span data-ttu-id="57f50-2293">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="57f50-2293">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="57f50-2294">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="57f50-2294">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="57f50-2295">Hongkong (HKID) - Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2295">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2296">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2296">Format</span></span>

<span data-ttu-id="57f50-2297">Kombination aus 8-9Buchstaben und Zahlen sowie optionale Klammern um das letzte Zeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-2297">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2298">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2298">Pattern</span></span>

<span data-ttu-id="57f50-2299">Kombination aus Buchstaben 8-9 Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="57f50-2299">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="57f50-2300">1-2 Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="57f50-2300">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="57f50-2301">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2301">Six digits</span></span> 
- <span data-ttu-id="57f50-2302">Das letzte Zeichen (eine Ziffer oder der Buchstabe A), bei dem es sich um die Prüfziffer handelt, die optional in Klammern eingeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="57f50-2302">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2303">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2303">Checksum</span></span>

<span data-ttu-id="57f50-2304">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2304">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2305">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2305">Definition</span></span>

<span data-ttu-id="57f50-2306">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2306">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2307">Die Funktion Func_hong_kong_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2307">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2308">Ein Schlüsselwort aus Keyword_hong_kong_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2308">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="57f50-2309">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2309">The checksum passes.</span></span>

<span data-ttu-id="57f50-2310">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2310">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2311">Die Funktion Func_hong_kong_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2311">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2312">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2312">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2313">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2313">Keywords</span></span>

#### <a name="keyword_hong_kong_id_card"></a><span data-ttu-id="57f50-2314">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="57f50-2314">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="57f50-2315">Hong Kong Identity Card</span><span class="sxs-lookup"><span data-stu-id="57f50-2315">hong kong identity card</span></span>
- <span data-ttu-id="57f50-2316">HKIDC</span><span class="sxs-lookup"><span data-stu-id="57f50-2316">HKIDC</span></span>
- <span data-ttu-id="57f50-2317">id card</span><span class="sxs-lookup"><span data-stu-id="57f50-2317">id card</span></span>
- <span data-ttu-id="57f50-2318">identity card</span><span class="sxs-lookup"><span data-stu-id="57f50-2318">identity card</span></span>
- <span data-ttu-id="57f50-2319">HK-Personalausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-2319">hk identity card</span></span>
- <span data-ttu-id="57f50-2320">Hong Kong-ID</span><span class="sxs-lookup"><span data-stu-id="57f50-2320">hong kong id</span></span>
- <span data-ttu-id="57f50-2321">香港身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-2321">香港身份證</span></span>
- <span data-ttu-id="57f50-2322">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-2322">香港永久性居民身份證</span></span>
- <span data-ttu-id="57f50-2323">身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-2323">身份證</span></span>
- <span data-ttu-id="57f50-2324">身份証</span><span class="sxs-lookup"><span data-stu-id="57f50-2324">身份証</span></span>
- <span data-ttu-id="57f50-2325">身分證</span><span class="sxs-lookup"><span data-stu-id="57f50-2325">身分證</span></span>
- <span data-ttu-id="57f50-2326">身分証</span><span class="sxs-lookup"><span data-stu-id="57f50-2326">身分証</span></span>
- <span data-ttu-id="57f50-2327">香港身份証</span><span class="sxs-lookup"><span data-stu-id="57f50-2327">香港身份証</span></span>
- <span data-ttu-id="57f50-2328">香港身分證</span><span class="sxs-lookup"><span data-stu-id="57f50-2328">香港身分證</span></span>
- <span data-ttu-id="57f50-2329">香港身分証</span><span class="sxs-lookup"><span data-stu-id="57f50-2329">香港身分証</span></span>
- <span data-ttu-id="57f50-2330">香港身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-2330">香港身份證</span></span>
- <span data-ttu-id="57f50-2331">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-2331">香港居民身份證</span></span>
- <span data-ttu-id="57f50-2332">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="57f50-2332">香港居民身份証</span></span>
- <span data-ttu-id="57f50-2333">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="57f50-2333">香港居民身分證</span></span>
- <span data-ttu-id="57f50-2334">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="57f50-2334">香港居民身分証</span></span>
- <span data-ttu-id="57f50-2335">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="57f50-2335">香港永久性居民身份証</span></span>
- <span data-ttu-id="57f50-2336">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="57f50-2336">香港永久性居民身分證</span></span>
- <span data-ttu-id="57f50-2337">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="57f50-2337">香港永久性居民身分証</span></span>
- <span data-ttu-id="57f50-2338">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-2338">香港永久性居民身份證</span></span>
- <span data-ttu-id="57f50-2339">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-2339">香港非永久性居民身份證</span></span>
- <span data-ttu-id="57f50-2340">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="57f50-2340">香港非永久性居民身份証</span></span>
- <span data-ttu-id="57f50-2341">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="57f50-2341">香港非永久性居民身分證</span></span>
- <span data-ttu-id="57f50-2342">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="57f50-2342">香港非永久性居民身分証</span></span>
- <span data-ttu-id="57f50-2343">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-2343">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="57f50-2344">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="57f50-2344">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="57f50-2345">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="57f50-2345">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="57f50-2346">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="57f50-2346">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="57f50-2347">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-2347">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="57f50-2348">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="57f50-2348">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="57f50-2349">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="57f50-2349">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="57f50-2350">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="57f50-2350">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="57f50-2351">Indien – Permanente Kontonummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2351">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2352">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2352">Format</span></span>

<span data-ttu-id="57f50-2353">10 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2353">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2354">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2354">Pattern</span></span>

<span data-ttu-id="57f50-2355">10 Buchstaben oder Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-2355">10 letters or digits:</span></span>
- <span data-ttu-id="57f50-2356">Fünf Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="57f50-2356">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="57f50-2357">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2357">Four digits</span></span> 
- <span data-ttu-id="57f50-2358">Ein Buchstabe, der eine alphabetische Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="57f50-2358">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2359">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2359">Checksum</span></span>

<span data-ttu-id="57f50-2360">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2360">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2361">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2361">Definition</span></span>

<span data-ttu-id="57f50-2362">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2362">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2363">Der reguläre Ausdruck Regex_india_permanent_account_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2363">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2364">Ein Schlüsselwort aus Keyword_india_permanent_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2364">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="57f50-2365">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2365">The checksum passes.</span></span>

```xml
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2366">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2366">Keywords</span></span>

#### <a name="keyword_india_permanent_account_number"></a><span data-ttu-id="57f50-2367">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2367">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="57f50-2368">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2368">Permanent Account Number</span></span> 
- <span data-ttu-id="57f50-2369">Schwenken</span><span class="sxs-lookup"><span data-stu-id="57f50-2369">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="57f50-2370">Indien - Eindeutige Identifikationsnummer (Aadhaar)</span><span class="sxs-lookup"><span data-stu-id="57f50-2370">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2371">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2371">Format</span></span>

<span data-ttu-id="57f50-2372">12 Ziffern mit optionalen Leerzeichen oder Bindestrichen</span><span class="sxs-lookup"><span data-stu-id="57f50-2372">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2373">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2373">Pattern</span></span>

<span data-ttu-id="57f50-2374">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-2374">12 digits:</span></span>
- <span data-ttu-id="57f50-2375">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2375">Four digits</span></span> 
- <span data-ttu-id="57f50-2376">Eine optionales Leerzeichen oder ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-2376">An optional space or dash</span></span> 
- <span data-ttu-id="57f50-2377">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2377">Four digits</span></span> 
- <span data-ttu-id="57f50-2378">Eine optionales Leerzeichen oder ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-2378">An optional space or dash</span></span> 
- <span data-ttu-id="57f50-2379">Die letzte Ziffer, die eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="57f50-2379">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2380">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2380">Checksum</span></span>

<span data-ttu-id="57f50-2381">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2382">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2382">Definition</span></span>

<span data-ttu-id="57f50-2383">Eine DLP-Richtlinie ist 85% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: die Funktion Func_india_aadhaar findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2383">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="57f50-2384">Ein Schlüsselwort aus Keyword_india_aadhar wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2384">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="57f50-2385">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2385">The checksum passes.</span></span>
<span data-ttu-id="57f50-2386">Eine DLP-Richtlinie ist 75% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: die Funktion Func_india_aadhaar findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2386">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="57f50-2387">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2387">The checksum passes.</span></span>
```xml
<!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_india_aadhaar"/>
     <Match idRef="Keyword_india_aadhar"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_india_aadhaar"/>
  </Pattern>
</Entity>

### Keywords
   
#### Keyword_india_aadhar
- Aadhar
- Aadhaar
- UID
- आधार
   
## Indonesia Identity Card (KTP) Number

### Format

16 digits containing optional periods

### Pattern

16 digits:
- Two-digit province code 
- A period (optional) 
- Two-digit regency or city code 
- Two-digit subdistrict code 
- A period (optional) 
- Six digits in the format DDMMYY which are the date of birth 
- A period (optional) 
- Four digits

### Checksum

No

### Definition

A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The regular expression Regex_indonesia_id_card finds content that matches the pattern.
- A keyword from Keyword_indonesia_id_card is found.

A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The regular expression Regex_indonesia_id_card finds content that matches the pattern.

```
<!-- Indonesia Identity Card (KTP) Number -->
<span data-ttu-id="57f50-2388"><Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Regex_indonesia_id_card"/> <Match idRef="Keyword_indonesia_id_card"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_indonesia_id_card"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="57f50-2388"></span></span>
```

### Keywords
   
#### Keyword_indonesia_id_card

- KTP
- Kartu Tanda Penduduk 
- Nomor Induk Kependudukan 
   
## International Banking Account Number (IBAN)

### Format

Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)

### Pattern

Pattern must include all of the following:

- Two-letter country code
- Two check digits (followed by an optional space) 
- 1-7 groups of four letters or digits (can be separated by spaces)
- 1-3 letters or digits

The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:

ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg

### Checksum

Yes

### Definition

A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The function Func_iban finds content that matches the pattern.
- The checksum passes.

```xml
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2389">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2389">Keywords</span></span>

<span data-ttu-id="57f50-2390">Keine</span><span class="sxs-lookup"><span data-stu-id="57f50-2390">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="57f50-2391">IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="57f50-2391">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2392">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2392">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="57f50-2393">IPv4</span><span class="sxs-lookup"><span data-stu-id="57f50-2393">IPv4:</span></span>
<span data-ttu-id="57f50-2394">Komplexes Muster, das formatierte (Punkte) und unformatierte (keine Punkte) Versionen der IPv4-Adressen angibt</span><span class="sxs-lookup"><span data-stu-id="57f50-2394">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="57f50-2395">IPv6</span><span class="sxs-lookup"><span data-stu-id="57f50-2395">IPv6:</span></span>
<span data-ttu-id="57f50-2396"> Komplexes Muster, das formatierte IPv6-Nummern angibt (schließt Doppelpunkte ein)</span><span class="sxs-lookup"><span data-stu-id="57f50-2396">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2397">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2397">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2398">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2398">Checksum</span></span>

<span data-ttu-id="57f50-2399">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2399">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2400">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2400">Definition</span></span>

<span data-ttu-id="57f50-2401">Für IPv6 ist eine DLP-Richtlinie zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2401">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2402">Der reguläre Ausdruck Regex_ipv6_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2402">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2403">Es wurde kein Schlüsselwort aus Keyword_ipaddress gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2403">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="57f50-2404">Für IPv4 ist eine DLP-Richtlinie zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2404">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2405">Der reguläre Ausdruck Regex_ipv4_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2405">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2406">Ein Schlüsselwort aus Keyword_ipaddress wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2406">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="57f50-2407">Für IPv6 ist eine DLP-Richtlinie zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2407">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2408">Der reguläre Ausdruck Regex_ipv6_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2408">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2409">Es wurde kein Schlüsselwort aus Keyword_ipaddress gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2409">No keyword from Keyword_ipaddress is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2410">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2410">Keywords</span></span>

#### <a name="keyword_ipaddress"></a><span data-ttu-id="57f50-2411">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="57f50-2411">Keyword_ipaddress</span></span>

- <span data-ttu-id="57f50-2412">IP (bei diesem Schlüsselwort wird die Groß-/Kleinschreibung unterschieden)</span><span class="sxs-lookup"><span data-stu-id="57f50-2412">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="57f50-2413">ip address</span><span class="sxs-lookup"><span data-stu-id="57f50-2413">ip address</span></span> 
- <span data-ttu-id="57f50-2414">IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="57f50-2414">ip addresses</span></span>
- <span data-ttu-id="57f50-2415">internet protocol</span><span class="sxs-lookup"><span data-stu-id="57f50-2415">internet protocol</span></span>
- <span data-ttu-id="57f50-2416">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="57f50-2416">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="57f50-2417">Internationale Klassifikation von Krankheiten (ICD-10-cm)</span><span class="sxs-lookup"><span data-stu-id="57f50-2417">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2418">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2418">Format</span></span>

<span data-ttu-id="57f50-2419">Dictionary</span><span class="sxs-lookup"><span data-stu-id="57f50-2419">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2420">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2420">Pattern</span></span>

<span data-ttu-id="57f50-2421">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="57f50-2421">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2422">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2422">Checksum</span></span>

<span data-ttu-id="57f50-2423">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2423">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2424">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2424">Definition</span></span>

<span data-ttu-id="57f50-2425">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2425">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2426">Ein Schlüsselwort aus Dictionary_icd_10_cm wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2426">A keyword from Dictionary_icd_10_cm is found.</span></span>

```xml
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="57f50-2427">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2427">Keywords</span></span>

<span data-ttu-id="57f50-2428">Ein beliebiger Ausdruck aus dem Dictionary_icd_10_cm-Stichwort Wörterbuch, das auf der [internationalen Klassifikation von Krankheiten basiert, zehnte Überarbeitung, klinische Änderung (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="57f50-2428">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="57f50-2429">Dieser Typ sucht nur nach dem Begriff, nicht nach den Versicherungs Codes.</span><span class="sxs-lookup"><span data-stu-id="57f50-2429">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="57f50-2430">Internationale Klassifikation von Krankheiten (ICD-9-cm)</span><span class="sxs-lookup"><span data-stu-id="57f50-2430">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2431">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2431">Format</span></span>

<span data-ttu-id="57f50-2432">Dictionary</span><span class="sxs-lookup"><span data-stu-id="57f50-2432">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2433">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2433">Pattern</span></span>

<span data-ttu-id="57f50-2434">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="57f50-2434">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2435">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2435">Checksum</span></span>

<span data-ttu-id="57f50-2436">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2436">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2437">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2437">Definition</span></span>

<span data-ttu-id="57f50-2438">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2438">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2439">Ein Schlüsselwort aus Dictionary_icd_9_cm wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2439">A keyword from Dictionary_icd_9_cm is found.</span></span>

```xml
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2440">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2440">Keywords</span></span>

<span data-ttu-id="57f50-2441">Ein beliebiger Ausdruck aus dem Dictionary_icd_9_cm-Stichwort Wörterbuch, das auf der [internationalen Klassifikation von Krankheiten basiert, neunte Revision, klinische Änderung (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="57f50-2441">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="57f50-2442">Dieser Typ sucht nur nach dem Begriff, nicht nach den Versicherungs Codes.</span><span class="sxs-lookup"><span data-stu-id="57f50-2442">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="57f50-2443">Irland – Personal Public Service-Nummer (PPS)</span><span class="sxs-lookup"><span data-stu-id="57f50-2443">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2444">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2444">Format</span></span>

<span data-ttu-id="57f50-2445">Altes Format (bis 31. Dez. 2012):</span><span class="sxs-lookup"><span data-stu-id="57f50-2445">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="57f50-2446">Sieben Ziffern, gefolgt von 1-2 Buchstaben </span><span class="sxs-lookup"><span data-stu-id="57f50-2446">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="57f50-2447">Neues Format (1 Jan 2013 und danach):</span><span class="sxs-lookup"><span data-stu-id="57f50-2447">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="57f50-2448">Sieben Ziffern, gefolgt von zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="57f50-2448">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2449">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2449">Pattern</span></span>

<span data-ttu-id="57f50-2450">Altes Format (bis 31. Dez. 2012):</span><span class="sxs-lookup"><span data-stu-id="57f50-2450">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="57f50-2451">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="57f50-2451">Seven digits</span></span> 
- <span data-ttu-id="57f50-2452">1-2 Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="57f50-2452">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="57f50-2453">Neues Format (1 Jan 2013 und danach):</span><span class="sxs-lookup"><span data-stu-id="57f50-2453">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="57f50-2454">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="57f50-2454">Seven digits</span></span> 
- <span data-ttu-id="57f50-2455">Ein Buchstabe (Groß-/Kleinschreibung irrelevant), wobei es sich um eine alphabetische Prüfziffer handelt </span><span class="sxs-lookup"><span data-stu-id="57f50-2455">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="57f50-2456">Die Buchstaben "A" oder "H" (Groß-/Kleinschreibung irrelevant)</span><span class="sxs-lookup"><span data-stu-id="57f50-2456">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2457">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2457">Checksum</span></span>

<span data-ttu-id="57f50-2458">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2458">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2459">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2459">Definition</span></span>

<span data-ttu-id="57f50-2460">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2461">Die Funktion Func_ireland_pps findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2461">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2462">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="57f50-2462">One of the following is true:</span></span>
    - <span data-ttu-id="57f50-2463">Ein Schlüsselwort aus Keyword_ireland_pps wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2463">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="57f50-2464">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-2464">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="57f50-2465">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2465">The checksum passes.</span></span>

<span data-ttu-id="57f50-2466">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2466">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2467">Die Funktion Func_ireland_pps findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2467">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2468">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2468">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2469">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2469">Keywords</span></span>

#### <a name="keyword_ireland_pps"></a><span data-ttu-id="57f50-2470">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="57f50-2470">Keyword_ireland_pps</span></span>

- <span data-ttu-id="57f50-2471">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2471">Personal Public Service Number</span></span> 
- <span data-ttu-id="57f50-2472">PPS Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2472">PPS Number</span></span> 
- <span data-ttu-id="57f50-2473">PPS Num</span><span class="sxs-lookup"><span data-stu-id="57f50-2473">PPS Num</span></span> 
- <span data-ttu-id="57f50-2474">PPS No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2474">PPS No.</span></span> 
- <span data-ttu-id="57f50-2475">PPS #</span><span class="sxs-lookup"><span data-stu-id="57f50-2475">PPS #</span></span> 
- <span data-ttu-id="57f50-2476">PPS #</span><span class="sxs-lookup"><span data-stu-id="57f50-2476">PPS#</span></span> 
- <span data-ttu-id="57f50-2477">PPSN</span><span class="sxs-lookup"><span data-stu-id="57f50-2477">PPSN</span></span> 
- <span data-ttu-id="57f50-2478">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="57f50-2478">Public Services Card</span></span> 
- <span data-ttu-id="57f50-2479">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="57f50-2479">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="57f50-2480">Uimh.</span><span class="sxs-lookup"><span data-stu-id="57f50-2480">Uimh.</span></span> <span data-ttu-id="57f50-2481">PSP</span><span class="sxs-lookup"><span data-stu-id="57f50-2481">PSP</span></span> 
- <span data-ttu-id="57f50-2482">PSP</span><span class="sxs-lookup"><span data-stu-id="57f50-2482">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="57f50-2483">Israelische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2483">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2484">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2484">Format</span></span>

<span data-ttu-id="57f50-2485">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2485">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2486">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2486">Pattern</span></span>

<span data-ttu-id="57f50-2487">Formatiert</span><span class="sxs-lookup"><span data-stu-id="57f50-2487">Formatted:</span></span>
- <span data-ttu-id="57f50-2488">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2488">Two digits</span></span> 
- <span data-ttu-id="57f50-2489">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-2489">A dash</span></span> 
- <span data-ttu-id="57f50-2490">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2490">Three digits</span></span> 
- <span data-ttu-id="57f50-2491">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-2491">A dash</span></span> 
- <span data-ttu-id="57f50-2492">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2492">Eight digits</span></span>

<span data-ttu-id="57f50-2493">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="57f50-2493">Unformatted:</span></span>
- <span data-ttu-id="57f50-2494">	13 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2494">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2495">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2495">Checksum</span></span>

<span data-ttu-id="57f50-2496">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2496">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2497">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2497">Definition</span></span>

<span data-ttu-id="57f50-2498">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2499">Der reguläre Ausdruck Regex_israel_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2499">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2500">Ein Schlüsselwort aus Keyword_israel_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2500">A keyword from Keyword_israel_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2501">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2501">Keywords</span></span>

#### <a name="keyword_israel_bank_account_number"></a><span data-ttu-id="57f50-2502">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2502">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="57f50-2503">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2503">Bank Account Number</span></span> 
- <span data-ttu-id="57f50-2504">Bank Account</span><span class="sxs-lookup"><span data-stu-id="57f50-2504">Bank Account</span></span> 
- <span data-ttu-id="57f50-2505">Account Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2505">Account Number</span></span> 
- <span data-ttu-id="57f50-2506">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="57f50-2506">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="57f50-2507">Israelische Ausweis-ID</span><span class="sxs-lookup"><span data-stu-id="57f50-2507">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2508">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2508">Format</span></span>

<span data-ttu-id="57f50-2509">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2509">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2510">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2510">Pattern</span></span>

<span data-ttu-id="57f50-2511">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2511">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2512">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2512">Checksum</span></span>

<span data-ttu-id="57f50-2513">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2513">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2514">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2514">Definition</span></span>

<span data-ttu-id="57f50-2515">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2515">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2516">Die Funktion Func_israeli_national_id_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2516">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2517">Ein Schlüsselwort aus Keyword_Israel_National_ID wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2517">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="57f50-2518">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2518">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2519">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2519">Keywords</span></span>

#### <a name="keyword_israel_national_id"></a><span data-ttu-id="57f50-2520">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="57f50-2520">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="57f50-2521">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="57f50-2521">מספר זהות</span></span> 
- <span data-ttu-id="57f50-2522">National ID Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2522">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="57f50-2523">Italienische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2523">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2524">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2524">Format</span></span>

<span data-ttu-id="57f50-2525">Eine Kombination von 10 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2525">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2526">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2526">Pattern</span></span>

- <span data-ttu-id="57f50-2527">Eine Kombination aus 10 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-2527">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="57f50-2528">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="57f50-2528">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="57f50-2529">Der Buchstabe „A“ oder „W“ (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="57f50-2529">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="57f50-2530">Sieben Buchstaben (ohne Beachtung der Groß-/Kleinschreibung), Ziffern oder der Unterstrich</span><span class="sxs-lookup"><span data-stu-id="57f50-2530">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="57f50-2531">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="57f50-2531">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2532">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2532">Checksum</span></span>

<span data-ttu-id="57f50-2533">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2533">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2534">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2534">Definition</span></span>

<span data-ttu-id="57f50-2535">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2536">Der reguläre Ausdruck Regex_italy_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2536">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2537">Ein Schlüsselwort aus Keyword_italy_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2537">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2538">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2538">Keywords</span></span>

#### <a name="keyword_italy_drivers_license_number"></a><span data-ttu-id="57f50-2539">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2539">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="57f50-2540">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="57f50-2540">numero di patente di guida</span></span> 
- <span data-ttu-id="57f50-2541">patente di guida</span><span class="sxs-lookup"><span data-stu-id="57f50-2541">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="57f50-2542">Japanische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2542">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2543">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2543">Format</span></span>

<span data-ttu-id="57f50-2544">Sieben oder acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2544">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2545">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2545">Pattern</span></span>

<span data-ttu-id="57f50-2546">Bankkontonummer:</span><span class="sxs-lookup"><span data-stu-id="57f50-2546">Bank account number:</span></span>
- <span data-ttu-id="57f50-2547">Sieben oder acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2547">Seven or eight digits</span></span>
- <span data-ttu-id="57f50-2548">Niederlassungscode der Bank:</span><span class="sxs-lookup"><span data-stu-id="57f50-2548">Bank account branch code:</span></span>
- <span data-ttu-id="57f50-2549">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2549">Four digits</span></span> 
- <span data-ttu-id="57f50-2550">Ein Leerzeichen oder ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="57f50-2550">A space or dash (optional)</span></span> 
- <span data-ttu-id="57f50-2551">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2551">Three digits</span></span>

<span data-ttu-id="57f50-2552">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2552">Checksum</span></span>

<span data-ttu-id="57f50-2553">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2553">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2554">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2554">Definition</span></span>

<span data-ttu-id="57f50-2555">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2555">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2556">Die Funktion Func_jp_bank_account findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2556">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2557">Ein Schlüsselwort aus Keyword_jp_bank_account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2557">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="57f50-2558">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="57f50-2558">One of the following is true:</span></span>
- <span data-ttu-id="57f50-2559">Die Funktion Func_jp_bank_account_branch_code findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2559">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2560">Ein Schlüsselwort aus Keyword_jp_bank_branch_code wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2560">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="57f50-2561">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2561">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2562">Die Funktion Func_jp_bank_account findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2562">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2563">Ein Schlüsselwort aus Keyword_jp_bank_account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2563">A keyword from Keyword_jp_bank_account is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2564">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2564">Keywords</span></span>

#### <a name="keyword_jp_bank_account"></a><span data-ttu-id="57f50-2565">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="57f50-2565">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="57f50-2566">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2566">Checking Account Number</span></span> 
- <span data-ttu-id="57f50-2567">Checking Account</span><span class="sxs-lookup"><span data-stu-id="57f50-2567">Checking Account</span></span> 
- <span data-ttu-id="57f50-2568">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="57f50-2568">Checking Account #</span></span> 
- <span data-ttu-id="57f50-2569">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2569">Checking Acct Number</span></span> 
- <span data-ttu-id="57f50-2570">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="57f50-2570">Checking Acct #</span></span> 
- <span data-ttu-id="57f50-2571">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2571">Checking Acct No.</span></span> 
- <span data-ttu-id="57f50-2572">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2572">Checking Account No.</span></span> 
- <span data-ttu-id="57f50-2573">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2573">Bank Account Number</span></span> 
- <span data-ttu-id="57f50-2574">Bank Account</span><span class="sxs-lookup"><span data-stu-id="57f50-2574">Bank Account</span></span> 
- <span data-ttu-id="57f50-2575">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="57f50-2575">Bank Account #</span></span> 
- <span data-ttu-id="57f50-2576">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2576">Bank Acct Number</span></span> 
- <span data-ttu-id="57f50-2577">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="57f50-2577">Bank Acct #</span></span> 
- <span data-ttu-id="57f50-2578">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2578">Bank Acct No.</span></span> 
- <span data-ttu-id="57f50-2579">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2579">Bank Account No.</span></span> 
- <span data-ttu-id="57f50-2580">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2580">Savings Account Number</span></span> 
- <span data-ttu-id="57f50-2581">Savings Account</span><span class="sxs-lookup"><span data-stu-id="57f50-2581">Savings Account</span></span> 
- <span data-ttu-id="57f50-2582">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="57f50-2582">Savings Account #</span></span> 
- <span data-ttu-id="57f50-2583">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2583">Savings Acct Number</span></span> 
- <span data-ttu-id="57f50-2584">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="57f50-2584">Savings Acct #</span></span> 
- <span data-ttu-id="57f50-2585">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2585">Savings Acct No.</span></span> 
- <span data-ttu-id="57f50-2586">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2586">Savings Account No.</span></span> 
- <span data-ttu-id="57f50-2587">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2587">Debit Account Number</span></span> 
- <span data-ttu-id="57f50-2588">Debit Account</span><span class="sxs-lookup"><span data-stu-id="57f50-2588">Debit Account</span></span> 
- <span data-ttu-id="57f50-2589">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="57f50-2589">Debit Account #</span></span> 
- <span data-ttu-id="57f50-2590">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2590">Debit Acct Number</span></span> 
- <span data-ttu-id="57f50-2591">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="57f50-2591">Debit Acct #</span></span> 
- <span data-ttu-id="57f50-2592">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2592">Debit Acct No.</span></span> 
- <span data-ttu-id="57f50-2593">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2593">Debit Account No.</span></span> 
- <span data-ttu-id="57f50-2594">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="57f50-2594">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="57f50-2595">#アカウントの確認, 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="57f50-2595">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="57f50-2596">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="57f50-2596">＃勘定の確認</span></span> 
- <span data-ttu-id="57f50-2597">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="57f50-2597">勘定番号の確認</span></span> 
- <span data-ttu-id="57f50-2598">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="57f50-2598">口座番号の確認</span></span> 
- <span data-ttu-id="57f50-2599">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2599">銀行口座番号</span></span> 
- <span data-ttu-id="57f50-2600">銀行口座</span><span class="sxs-lookup"><span data-stu-id="57f50-2600">銀行口座</span></span> 
- <span data-ttu-id="57f50-2601">銀行口座＃</span><span class="sxs-lookup"><span data-stu-id="57f50-2601">銀行口座＃</span></span> 
- <span data-ttu-id="57f50-2602">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2602">銀行の勘定番号</span></span> 
- <span data-ttu-id="57f50-2603">銀行のacct＃</span><span class="sxs-lookup"><span data-stu-id="57f50-2603">銀行のacct＃</span></span> 
- <span data-ttu-id="57f50-2604">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="57f50-2604">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="57f50-2605">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2605">銀行口座番号</span></span>
- <span data-ttu-id="57f50-2606">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2606">普通預金口座番号</span></span> 
- <span data-ttu-id="57f50-2607">預金口座</span><span class="sxs-lookup"><span data-stu-id="57f50-2607">預金口座</span></span> 
- <span data-ttu-id="57f50-2608">貯蓄口座＃</span><span class="sxs-lookup"><span data-stu-id="57f50-2608">貯蓄口座＃</span></span> 
- <span data-ttu-id="57f50-2609">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="57f50-2609">貯蓄勘定の数</span></span> 
- <span data-ttu-id="57f50-2610">貯蓄勘定＃</span><span class="sxs-lookup"><span data-stu-id="57f50-2610">貯蓄勘定＃</span></span> 
- <span data-ttu-id="57f50-2611">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2611">貯蓄勘定番号</span></span> 
- <span data-ttu-id="57f50-2612">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2612">普通預金口座番号</span></span> 
- <span data-ttu-id="57f50-2613">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2613">引き落とし口座番号</span></span> 
- <span data-ttu-id="57f50-2614">口座番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2614">口座番号</span></span> 
- <span data-ttu-id="57f50-2615">口座番号＃</span><span class="sxs-lookup"><span data-stu-id="57f50-2615">口座番号＃</span></span> 
- <span data-ttu-id="57f50-2616">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2616">デビットのacct番号</span></span> 
- <span data-ttu-id="57f50-2617">デビット勘定＃</span><span class="sxs-lookup"><span data-stu-id="57f50-2617">デビット勘定＃</span></span> 
- <span data-ttu-id="57f50-2618">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2618">デビットACCTの番号</span></span> 
- <span data-ttu-id="57f50-2619">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2619">デビット口座番号</span></span> 

#### <a name="keyword_jp_bank_branch_code"></a><span data-ttu-id="57f50-2620">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="57f50-2620">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="57f50-2621">Otemachi</span><span class="sxs-lookup"><span data-stu-id="57f50-2621">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="57f50-2622">Japanische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2622">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2623">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2623">Format</span></span>

<span data-ttu-id="57f50-2624">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2624">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2625">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2625">Pattern</span></span>

<span data-ttu-id="57f50-2626">12 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2626">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2627">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2627">Checksum</span></span>

<span data-ttu-id="57f50-2628">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2628">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2629">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2629">Definition</span></span>

<span data-ttu-id="57f50-2630">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2630">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2631">Die Funktion Func_jp_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2631">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2632">Ein Schlüsselwort aus Keyword_jp_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2632">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```xml
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2633">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2633">Keywords</span></span>

#### <a name="keyword_jp_drivers_license_number"></a><span data-ttu-id="57f50-2634">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2634">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="57f50-2635">DL #</span><span class="sxs-lookup"><span data-stu-id="57f50-2635">dl#</span></span> 
- <span data-ttu-id="57f50-2636">DL</span><span class="sxs-lookup"><span data-stu-id="57f50-2636">DL＃</span></span> 
- <span data-ttu-id="57f50-2637">DLS #</span><span class="sxs-lookup"><span data-stu-id="57f50-2637">dls#</span></span> 
- <span data-ttu-id="57f50-2638">DLS</span><span class="sxs-lookup"><span data-stu-id="57f50-2638">DLS＃</span></span> 
- <span data-ttu-id="57f50-2639">driver license</span><span class="sxs-lookup"><span data-stu-id="57f50-2639">driver license</span></span> 
- <span data-ttu-id="57f50-2640">driver licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-2640">driver licenses</span></span> 
- <span data-ttu-id="57f50-2641">drivers license</span><span class="sxs-lookup"><span data-stu-id="57f50-2641">drivers license</span></span> 
- <span data-ttu-id="57f50-2642">driver's license</span><span class="sxs-lookup"><span data-stu-id="57f50-2642">driver's license</span></span> 
- <span data-ttu-id="57f50-2643">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-2643">drivers licenses</span></span> 
- <span data-ttu-id="57f50-2644">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-2644">driver's licenses</span></span> 
- <span data-ttu-id="57f50-2645">driving licence</span><span class="sxs-lookup"><span data-stu-id="57f50-2645">driving licence</span></span> 
- <span data-ttu-id="57f50-2646">lic #</span><span class="sxs-lookup"><span data-stu-id="57f50-2646">lic#</span></span> 
- <span data-ttu-id="57f50-2647">LIC</span><span class="sxs-lookup"><span data-stu-id="57f50-2647">LIC＃</span></span> 
- <span data-ttu-id="57f50-2648">LiCS #</span><span class="sxs-lookup"><span data-stu-id="57f50-2648">lics#</span></span> 
- <span data-ttu-id="57f50-2649">state id</span><span class="sxs-lookup"><span data-stu-id="57f50-2649">state id</span></span> 
- <span data-ttu-id="57f50-2650">state identification</span><span class="sxs-lookup"><span data-stu-id="57f50-2650">state identification</span></span> 
- <span data-ttu-id="57f50-2651">state identification number</span><span class="sxs-lookup"><span data-stu-id="57f50-2651">state identification number</span></span> 
- <span data-ttu-id="57f50-2652">低所得国＃</span><span class="sxs-lookup"><span data-stu-id="57f50-2652">低所得国＃</span></span> 
- <span data-ttu-id="57f50-2653">免許証</span><span class="sxs-lookup"><span data-stu-id="57f50-2653">免許証</span></span> 
- <span data-ttu-id="57f50-2654">状態ID</span><span class="sxs-lookup"><span data-stu-id="57f50-2654">状態ID</span></span>
- <span data-ttu-id="57f50-2655">状態の識別</span><span class="sxs-lookup"><span data-stu-id="57f50-2655">状態の識別</span></span> 
- <span data-ttu-id="57f50-2656">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2656">状態の識別番号</span></span> 
- <span data-ttu-id="57f50-2657">運転免許</span><span class="sxs-lookup"><span data-stu-id="57f50-2657">運転免許</span></span> 
- <span data-ttu-id="57f50-2658">運転免許証</span><span class="sxs-lookup"><span data-stu-id="57f50-2658">運転免許証</span></span> 
- <span data-ttu-id="57f50-2659">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2659">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="57f50-2660">Japanische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2660">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2661">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2661">Format</span></span>

<span data-ttu-id="57f50-2662">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2662">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2663">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2663">Pattern</span></span>

<span data-ttu-id="57f50-2664">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2664">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2665">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2665">Checksum</span></span>

<span data-ttu-id="57f50-2666">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2666">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2667">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2667">Definition</span></span>

<span data-ttu-id="57f50-2668">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2668">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2669">Die Funktion Func_jp_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2669">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2670">Ein Schlüsselwort aus Keyword_jp_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2670">A keyword from Keyword_jp_passport is found.</span></span>

```xml
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2671">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2671">Keywords</span></span>

#### <a name="keyword_jp_passport"></a><span data-ttu-id="57f50-2672">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="57f50-2672">Keyword_jp_passport</span></span>

- <span data-ttu-id="57f50-2673">パスポート</span><span class="sxs-lookup"><span data-stu-id="57f50-2673">パスポート</span></span> 
- <span data-ttu-id="57f50-2674">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2674">パスポート番号</span></span> 
- <span data-ttu-id="57f50-2675">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="57f50-2675">パスポートのNum</span></span> 
- <span data-ttu-id="57f50-2676">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="57f50-2676">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="57f50-2677">Japanische Einwohnerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2677">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2678">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2678">Format</span></span>

<span data-ttu-id="57f50-2679">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2679">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2680">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2680">Pattern</span></span>

<span data-ttu-id="57f50-2681">11 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2681">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2682">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2682">Checksum</span></span>

<span data-ttu-id="57f50-2683">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2683">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2684">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2684">Definition</span></span>

<span data-ttu-id="57f50-2685">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2685">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2686">Die Funktion Func_jp_resident_registration_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2686">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2687">Ein Schlüsselwort aus Keyword_jp_resident_registration_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2687">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```xml
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2688">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2688">Keywords</span></span>

#### <a name="keyword_jp_resident_registration_number"></a><span data-ttu-id="57f50-2689">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2689">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="57f50-2690">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2690">Resident Registration Number</span></span>
- <span data-ttu-id="57f50-2691">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2691">Resident Register Number</span></span> 
- <span data-ttu-id="57f50-2692">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2692">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="57f50-2693">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2693">Resident Registration No.</span></span> 
- <span data-ttu-id="57f50-2694">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2694">Resident Register No.</span></span> 
- <span data-ttu-id="57f50-2695">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2695">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="57f50-2696">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2696">Basic Resident Register No.</span></span> 
- <span data-ttu-id="57f50-2697">住民登録番号、登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="57f50-2697">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="57f50-2698">住民基本登録番号、登録番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2698">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="57f50-2699">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="57f50-2699">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="57f50-2700">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2700">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="57f50-2701">Japanische Sozialversicherungsnummer (SIN)</span><span class="sxs-lookup"><span data-stu-id="57f50-2701">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2702">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2702">Format</span></span>

<span data-ttu-id="57f50-2703">7-12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2703">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2704">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2704">Pattern</span></span>

<span data-ttu-id="57f50-2705">7 bis 12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-2705">7-12 digits:</span></span>
- <span data-ttu-id="57f50-2706">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2706">Four digits</span></span> 
- <span data-ttu-id="57f50-2707">Ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="57f50-2707">A hyphen (optional)</span></span> 
- <span data-ttu-id="57f50-2708">Sechs Ziffern oder</span><span class="sxs-lookup"><span data-stu-id="57f50-2708">Six digits OR</span></span>
- <span data-ttu-id="57f50-2709">7-12 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2709">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2710">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2710">Checksum</span></span>

<span data-ttu-id="57f50-2711">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2711">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2712">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2712">Definition</span></span>

<span data-ttu-id="57f50-2713">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2713">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2714">Die Funktion Func_jp_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2714">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2715">Ein Schlüsselwort aus Keyword_jp_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2715">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="57f50-2716">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2716">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2717">Die Funktion Func_jp_sin_pre_1997 findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2717">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2718">Ein Schlüsselwort aus Keyword_jp_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2718">A keyword from Keyword_jp_sin is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2719">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2719">Keywords</span></span>

#### <a name="keyword_jp_sin"></a><span data-ttu-id="57f50-2720">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="57f50-2720">Keyword_jp_sin</span></span>

- <span data-ttu-id="57f50-2721">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="57f50-2721">Social Insurance No.</span></span> 
- <span data-ttu-id="57f50-2722">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="57f50-2722">Social Insurance Num</span></span> 
- <span data-ttu-id="57f50-2723">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2723">Social Insurance Number</span></span> 
- <span data-ttu-id="57f50-2724">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="57f50-2724">社会保険のテンキー</span></span> 
- <span data-ttu-id="57f50-2725">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2725">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="57f50-2726">Japanische Residenz Kartennummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2726">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2727">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2727">Format</span></span>

<span data-ttu-id="57f50-2728">12 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2728">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2729">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2729">Pattern</span></span>

<span data-ttu-id="57f50-2730">12 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-2730">12 letters and digits:</span></span>
- <span data-ttu-id="57f50-2731">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="57f50-2731">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="57f50-2732">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2732">Eight digits</span></span> 
- <span data-ttu-id="57f50-2733">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="57f50-2733">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2734">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2734">Checksum</span></span>

<span data-ttu-id="57f50-2735">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2735">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2736">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2736">Definition</span></span>

<span data-ttu-id="57f50-2737">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2737">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2738">Der reguläre Ausdruck Regex_jp_residence_card_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2738">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2739">Ein Schlüsselwort aus Keyword_jp_residence_card_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2739">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```xml
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2740">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2740">Keywords</span></span>

#### <a name="keyword_jp_residence_card_number"></a><span data-ttu-id="57f50-2741">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2741">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="57f50-2742">Wohnsitz Kartennummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2742">Residence card number</span></span>
- <span data-ttu-id="57f50-2743">Residenzkarte Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2743">Residence card no</span></span>
- <span data-ttu-id="57f50-2744">Aufenthaltskarte #</span><span class="sxs-lookup"><span data-stu-id="57f50-2744">Residence card #</span></span>
- <span data-ttu-id="57f50-2745">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="57f50-2745">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="57f50-2746">Malaysia -ID-Kartennummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2746">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2747">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2747">Format</span></span>

<span data-ttu-id="57f50-2748">12 Ziffern mit optionalen Bindestrichen</span><span class="sxs-lookup"><span data-stu-id="57f50-2748">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2749">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2749">Pattern</span></span>

<span data-ttu-id="57f50-2750">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-2750">12 digits:</span></span>
- <span data-ttu-id="57f50-2751">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="57f50-2751">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="57f50-2752">Ein Bindestrich (optional) </span><span class="sxs-lookup"><span data-stu-id="57f50-2752">A dash (optional)</span></span> 
- <span data-ttu-id="57f50-2753">Zwei Buchstaben als Code für den Geburtsort </span><span class="sxs-lookup"><span data-stu-id="57f50-2753">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="57f50-2754">Ein Bindestrich (optional) </span><span class="sxs-lookup"><span data-stu-id="57f50-2754">A dash (optional)</span></span> 
- <span data-ttu-id="57f50-2755">Drei beliebige Ziffern </span><span class="sxs-lookup"><span data-stu-id="57f50-2755">Three random digits</span></span> 
- <span data-ttu-id="57f50-2756">Einstelliger Code für das Geschlecht</span><span class="sxs-lookup"><span data-stu-id="57f50-2756">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2757">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2757">Checksum</span></span>

<span data-ttu-id="57f50-2758">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2758">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2759">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2759">Definition</span></span>

<span data-ttu-id="57f50-2760">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2760">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2761">Der reguläre Ausdruck Regex_malaysia_id_card_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2761">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2762">Ein Schlüsselwort aus Keyword_malaysia_id_card_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2762">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

```xml
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2763">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2763">Keywords</span></span>
   
#### <a name="keyword_malaysia_id_card_number"></a><span data-ttu-id="57f50-2764">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2764">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="57f50-2765">digitale Anwendungs Karte</span><span class="sxs-lookup"><span data-stu-id="57f50-2765">digital application card</span></span>
- <span data-ttu-id="57f50-2766">i/c</span><span class="sxs-lookup"><span data-stu-id="57f50-2766">i/c</span></span>
- <span data-ttu-id="57f50-2767">i/c Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2767">i/c no</span></span>
- <span data-ttu-id="57f50-2768">IK</span><span class="sxs-lookup"><span data-stu-id="57f50-2768">ic</span></span>
- <span data-ttu-id="57f50-2769">IC Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2769">ic no</span></span>
- <span data-ttu-id="57f50-2770">id card</span><span class="sxs-lookup"><span data-stu-id="57f50-2770">id card</span></span>
- <span data-ttu-id="57f50-2771">Ausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-2771">identification Card</span></span>
- <span data-ttu-id="57f50-2772">identity card</span><span class="sxs-lookup"><span data-stu-id="57f50-2772">identity card</span></span>
- <span data-ttu-id="57f50-2773">k/p</span><span class="sxs-lookup"><span data-stu-id="57f50-2773">k/p</span></span>
- <span data-ttu-id="57f50-2774">k/p Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2774">k/p no</span></span>
- <span data-ttu-id="57f50-2775">Kad akuan Diri</span><span class="sxs-lookup"><span data-stu-id="57f50-2775">kad akuan diri</span></span>
- <span data-ttu-id="57f50-2776">Kad aplikasi Digital</span><span class="sxs-lookup"><span data-stu-id="57f50-2776">kad aplikasi digital</span></span>
- <span data-ttu-id="57f50-2777">Kad Einführung in Malaysia</span><span class="sxs-lookup"><span data-stu-id="57f50-2777">kad pengenalan malaysia</span></span>
- <span data-ttu-id="57f50-2778">KP</span><span class="sxs-lookup"><span data-stu-id="57f50-2778">kp</span></span>
- <span data-ttu-id="57f50-2779">KP Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2779">kp no</span></span>
- <span data-ttu-id="57f50-2780">MyKAD</span><span class="sxs-lookup"><span data-stu-id="57f50-2780">mykad</span></span>
- <span data-ttu-id="57f50-2781">mykas</span><span class="sxs-lookup"><span data-stu-id="57f50-2781">mykas</span></span>
- <span data-ttu-id="57f50-2782">mykid</span><span class="sxs-lookup"><span data-stu-id="57f50-2782">mykid</span></span>
- <span data-ttu-id="57f50-2783">mypr</span><span class="sxs-lookup"><span data-stu-id="57f50-2783">mypr</span></span>
- <span data-ttu-id="57f50-2784">mytentera</span><span class="sxs-lookup"><span data-stu-id="57f50-2784">mytentera</span></span>
- <span data-ttu-id="57f50-2785">Malaysia-Personalausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-2785">malaysia identity card</span></span>
- <span data-ttu-id="57f50-2786">malaysischer Personalausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-2786">malaysian identity card</span></span>
- <span data-ttu-id="57f50-2787">NRIC</span><span class="sxs-lookup"><span data-stu-id="57f50-2787">nric</span></span>
- <span data-ttu-id="57f50-2788">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-2788">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="57f50-2789">Niederlande – Bürgerdienstnummer (BSN)</span><span class="sxs-lookup"><span data-stu-id="57f50-2789">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2790">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2790">Format</span></span>

<span data-ttu-id="57f50-2791">8-9 Ziffern mit optionalen Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-2791">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2792">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2792">Pattern</span></span>

<span data-ttu-id="57f50-2793">8-9 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-2793">8-9 digits:</span></span>
- <span data-ttu-id="57f50-2794">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2794">Three digits</span></span> 
- <span data-ttu-id="57f50-2795">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="57f50-2795">A space (optional)</span></span> 
- <span data-ttu-id="57f50-2796">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2796">Three digits</span></span> 
- <span data-ttu-id="57f50-2797">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="57f50-2797">A space (optional)</span></span> 
- <span data-ttu-id="57f50-2798">2-3 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2798">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2799">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2799">Checksum</span></span>

<span data-ttu-id="57f50-2800">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2800">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2801">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2801">Definition</span></span>

<span data-ttu-id="57f50-2802">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2802">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2803">Die Funktion Func_netherlands_bsn findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2803">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2804">Ein Schlüsselwort aus Keyword_netherlands_bsn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2804">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="57f50-2805">Die Funktion Func_eu_date2 sucht ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-2805">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="57f50-2806">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2806">The checksum passes.</span></span>

```xml
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2807">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2807">Keywords</span></span>

#### <a name="keyword_netherlands_bsn"></a><span data-ttu-id="57f50-2808">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="57f50-2808">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="57f50-2809">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="57f50-2809">Citizen service number</span></span> 
- <span data-ttu-id="57f50-2810">BSN</span><span class="sxs-lookup"><span data-stu-id="57f50-2810">BSN</span></span> 
- <span data-ttu-id="57f50-2811">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2811">Burgerservicenummer</span></span> 
- <span data-ttu-id="57f50-2812">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2812">Sofinummer</span></span> 
- <span data-ttu-id="57f50-2813">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2813">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="57f50-2814">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2814">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="57f50-2815">Neuseeländische Gesundheitsministeriumsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2815">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2816">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2816">Format</span></span>

<span data-ttu-id="57f50-2817">Drei Buchstaben, ein Leerzeichen (optional) und vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2817">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2818">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2818">Pattern</span></span>

<span data-ttu-id="57f50-2819">Drei Buchstaben (Groß-/Kleinschreibung nicht beachtet) ein Leerzeichen (optional) vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2819">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2820">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2820">Checksum</span></span>

<span data-ttu-id="57f50-2821">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2821">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2822">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2822">Definition</span></span>

<span data-ttu-id="57f50-2823">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2823">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2824">Die Funktion Func_new_zealand_ministry_of_health_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2824">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2825">Ein Schlüsselwort aus Keyword_nz_terms wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2825">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="57f50-2826">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2826">The checksum passes.</span></span>

```xml
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

<span data-ttu-id="57f50-2827">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2827">Keywords</span></span>

<span data-ttu-id="57f50-2828">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="57f50-2828">Keyword_nz_terms</span></span>

- <span data-ttu-id="57f50-2829">Nhi</span><span class="sxs-lookup"><span data-stu-id="57f50-2829">NHI</span></span> 
- <span data-ttu-id="57f50-2830">New Zealand</span><span class="sxs-lookup"><span data-stu-id="57f50-2830">New Zealand</span></span> 
- <span data-ttu-id="57f50-2831">Health</span><span class="sxs-lookup"><span data-stu-id="57f50-2831">Health</span></span> 
- <span data-ttu-id="57f50-2832">Behandlung</span><span class="sxs-lookup"><span data-stu-id="57f50-2832">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="57f50-2833">Norwegen – Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2833">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2834">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2834">Format</span></span>

<span data-ttu-id="57f50-2835">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2835">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2836">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2836">Pattern</span></span>

<span data-ttu-id="57f50-2837">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-2837">11 digits:</span></span>
- <span data-ttu-id="57f50-2838">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="57f50-2838">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="57f50-2839">Dreistellige individuelle Zahl </span><span class="sxs-lookup"><span data-stu-id="57f50-2839">Three-digit individual number</span></span> 
- <span data-ttu-id="57f50-2840">Zwei Prüfziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2840">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2841">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2841">Checksum</span></span>

<span data-ttu-id="57f50-2842">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2842">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2843">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2843">Definition</span></span>

<span data-ttu-id="57f50-2844">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2844">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2845">Die Funktion Func_norway_id_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2845">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2846">Ein Schlüsselwort aus Keyword_norway_id_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2846">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="57f50-2847">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2847">The checksum passes.</span></span>
- <span data-ttu-id="57f50-2848">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2848">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2849">Die Funktion Func_norway_id_numbe findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2849">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2850">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2850">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2851">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2851">Keywords</span></span>

#### <a name="keyword_norway_id_number"></a><span data-ttu-id="57f50-2852">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2852">Keyword_norway_id_number</span></span>

- <span data-ttu-id="57f50-2853">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="57f50-2853">Personal identification number</span></span>
- <span data-ttu-id="57f50-2854">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2854">Norwegian ID Number</span></span>
- <span data-ttu-id="57f50-2855">ID Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2855">ID Number</span></span>
- <span data-ttu-id="57f50-2856">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="57f50-2856">Identification</span></span>
- <span data-ttu-id="57f50-2857">Personnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2857">Personnummer</span></span>
- <span data-ttu-id="57f50-2858">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2858">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="57f50-2859">Philippinen – Vereinheitlichte Mehrzweck-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2859">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2860">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2860">Format</span></span>

<span data-ttu-id="57f50-2861">12 Ziffern, durch Bindestriche getrennt</span><span class="sxs-lookup"><span data-stu-id="57f50-2861">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2862">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2862">Pattern</span></span>

<span data-ttu-id="57f50-2863">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-2863">12 digits:</span></span>
- <span data-ttu-id="57f50-2864">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2864">Four digits</span></span> 
- <span data-ttu-id="57f50-2865">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-2865">A hyphen</span></span> 
- <span data-ttu-id="57f50-2866">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="57f50-2866">Seven digits</span></span> 
- <span data-ttu-id="57f50-2867">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-2867">A hyphen</span></span> 
- <span data-ttu-id="57f50-2868">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-2868">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2869">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2869">Checksum</span></span>

<span data-ttu-id="57f50-2870">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2870">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2871">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2871">Definition</span></span>

<span data-ttu-id="57f50-2872">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2872">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2873">Der reguläre Ausdruck Regex_philippines_unified_id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2873">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2874">Ein Schlüsselwort aus Keyword_philippines_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2874">A keyword from Keyword_philippines_id is found.</span></span>

```xml
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2875">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2875">Keywords</span></span>
   
#### <a name="keyword_philippines_id"></a><span data-ttu-id="57f50-2876">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="57f50-2876">Keyword_philippines_id</span></span>

- <span data-ttu-id="57f50-2877">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="57f50-2877">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="57f50-2878">Umid</span><span class="sxs-lookup"><span data-stu-id="57f50-2878">UMID</span></span> 
- <span data-ttu-id="57f50-2879">Identity Card</span><span class="sxs-lookup"><span data-stu-id="57f50-2879">Identity Card</span></span> 
- <span data-ttu-id="57f50-2880">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="57f50-2880">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="57f50-2881">Polen Personalausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-2881">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2882">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2882">Format</span></span>

<span data-ttu-id="57f50-2883">Drei Buchstaben und sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2883">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2884">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2884">Pattern</span></span>

<span data-ttu-id="57f50-2885">Drei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2885">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2886">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2886">Checksum</span></span>

<span data-ttu-id="57f50-2887">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2887">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2888">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2888">Definition</span></span>

<span data-ttu-id="57f50-2889">Eine DLP-Richtlinie ist 75% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn in einer Nähe von 300 Zeichen: die Funktion Func_polish_national_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2889">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="57f50-2890">Ein Schlüsselwort aus Keyword_polish_national_id_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2890">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="57f50-2891">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2891">The checksum passes.</span></span>

```xml
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2892">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2892">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="57f50-2893">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2893">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="57f50-2894">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="57f50-2894">Dowód osobisty</span></span>
- <span data-ttu-id="57f50-2895">Numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="57f50-2895">Numer dowodu osobistego</span></span>
- <span data-ttu-id="57f50-2896">Nazwa i Numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="57f50-2896">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="57f50-2897">Nazwa i Nr dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="57f50-2897">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="57f50-2898">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="57f50-2898">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="57f50-2899">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="57f50-2899">Dowód Tożsamości</span></span>
- <span data-ttu-id="57f50-2900">Dow.</span><span class="sxs-lookup"><span data-stu-id="57f50-2900">dow.</span></span> <span data-ttu-id="57f50-2901">OS.</span><span class="sxs-lookup"><span data-stu-id="57f50-2901">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="57f50-2902">Polnische ID-Karte (PESEL)</span><span class="sxs-lookup"><span data-stu-id="57f50-2902">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2903">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2903">Format</span></span>

<span data-ttu-id="57f50-2904">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2904">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2905">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2905">Pattern</span></span>

<span data-ttu-id="57f50-2906">11 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2906">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2907">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2907">Checksum</span></span>

<span data-ttu-id="57f50-2908">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2908">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2909">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2909">Definition</span></span>

<span data-ttu-id="57f50-2910">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2910">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2911">Die Funktion Func_pesel_identification_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2911">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2912">Ein Schlüsselwort aus Keyword_pesel_identification_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2912">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="57f50-2913">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2913">The checksum passes.</span></span>

```xml
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2914">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2914">Keywords</span></span>

#### <a name="keyword_pesel_identification_number"></a><span data-ttu-id="57f50-2915">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2915">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="57f50-2916">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="57f50-2916">Nr PESEL</span></span>
- <span data-ttu-id="57f50-2917">PESEL</span><span class="sxs-lookup"><span data-stu-id="57f50-2917">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="57f50-2918">Polen Reisepass</span><span class="sxs-lookup"><span data-stu-id="57f50-2918">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2919">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2919">Format</span></span>

<span data-ttu-id="57f50-2920">Zwei Buchstaben und sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2920">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2921">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2921">Pattern</span></span>

<span data-ttu-id="57f50-2922">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2922">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2923">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2923">Checksum</span></span>

<span data-ttu-id="57f50-2924">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2924">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2925">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2925">Definition</span></span>

<span data-ttu-id="57f50-2926">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2926">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2927">Die Funktion Func_polish_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2927">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2928">Ein Schlüsselwort aus Keyword_polish_national_id_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2928">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="57f50-2929">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2929">The checksum passes.</span></span>

```xml
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2930">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2930">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="57f50-2931">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="57f50-2931">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="57f50-2932">Numer paszportu</span><span class="sxs-lookup"><span data-stu-id="57f50-2932">Numer paszportu</span></span>
- <span data-ttu-id="57f50-2933">Nr.</span><span class="sxs-lookup"><span data-stu-id="57f50-2933">Nr.</span></span> <span data-ttu-id="57f50-2934">Paszportu</span><span class="sxs-lookup"><span data-stu-id="57f50-2934">Paszportu</span></span>
- <span data-ttu-id="57f50-2935">Paszport</span><span class="sxs-lookup"><span data-stu-id="57f50-2935">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="57f50-2936">Portugal – Bürgerkartennummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2936">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2937">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2937">Format</span></span>

<span data-ttu-id="57f50-2938">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2938">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2939">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2939">Pattern</span></span>

<span data-ttu-id="57f50-2940">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2940">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2941">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2941">Checksum</span></span>

<span data-ttu-id="57f50-2942">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2942">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2943">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2943">Definition</span></span>

<span data-ttu-id="57f50-2944">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2944">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2945">Der reguläre Ausdruck Regex_portugal_citizen_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2945">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2946">Ein Schlüsselwort aus Keyword_portugal_citizen_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2946">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```xml
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-2947">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2947">Keywords</span></span>

#### <a name="keyword_portugal_citizen_card"></a><span data-ttu-id="57f50-2948">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="57f50-2948">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="57f50-2949">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="57f50-2949">Citizen Card</span></span>
- <span data-ttu-id="57f50-2950">National ID Card</span><span class="sxs-lookup"><span data-stu-id="57f50-2950">National ID Card</span></span>
- <span data-ttu-id="57f50-2951">CC</span><span class="sxs-lookup"><span data-stu-id="57f50-2951">CC</span></span>
- <span data-ttu-id="57f50-2952">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="57f50-2952">Cartão de Cidadão</span></span>
- <span data-ttu-id="57f50-2953">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="57f50-2953">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="57f50-2954">Saudi-Arabische Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2954">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2955">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2955">Format</span></span>

<span data-ttu-id="57f50-2956">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2956">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2957">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2957">Pattern</span></span>

<span data-ttu-id="57f50-2958">10 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2958">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2959">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2959">Checksum</span></span>

<span data-ttu-id="57f50-2960">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-2960">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2961">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2961">Definition</span></span>

<span data-ttu-id="57f50-2962">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2962">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2963">Der reguläre Ausdruck Regex_saudi_arabia_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2963">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2964">Ein Schlüsselwort aus Keyword_saudi_arabia_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2964">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2965">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2965">Keywords</span></span>

#### <a name="keyword_saudi_arabia_national_id"></a><span data-ttu-id="57f50-2966">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="57f50-2966">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="57f50-2967">Identification Card</span><span class="sxs-lookup"><span data-stu-id="57f50-2967">Identification Card</span></span> 
- <span data-ttu-id="57f50-2968">I card number</span><span class="sxs-lookup"><span data-stu-id="57f50-2968">I card number</span></span> 
- <span data-ttu-id="57f50-2969">ID number</span><span class="sxs-lookup"><span data-stu-id="57f50-2969">ID number</span></span> 
- <span data-ttu-id="57f50-2970">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="57f50-2970">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="57f50-2971">Singapur – National Registration Identity Card-Nummer (NRIC)</span><span class="sxs-lookup"><span data-stu-id="57f50-2971">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-2972">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-2972">Format</span></span>

<span data-ttu-id="57f50-2973">Neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-2973">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-2974">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-2974">Pattern</span></span>

- <span data-ttu-id="57f50-2975">Neun Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-2975">Nine letters and digits:</span></span>
- <span data-ttu-id="57f50-2976">Die Buchstaben "F", "G", "S" oder "T" (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="57f50-2976">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="57f50-2977">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="57f50-2977">Seven digits</span></span> 
- <span data-ttu-id="57f50-2978">Eine alphabetische Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-2978">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-2979">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-2979">Checksum</span></span>

<span data-ttu-id="57f50-2980">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-2980">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-2981">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-2981">Definition</span></span>

<span data-ttu-id="57f50-2982">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2982">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2983">Der reguläre Ausdruck Regex_singapore_nric sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2983">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2984">Ein Schlüsselwort aus Keyword_singapore_nric wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-2984">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="57f50-2985">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2985">The checksum passes.</span></span>

<span data-ttu-id="57f50-2986">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-2986">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-2987">Der reguläre Ausdruck Regex_singapore_nric sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-2987">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-2988">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-2988">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-2989">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-2989">Keywords</span></span>
   
#### <a name="keyword_singapore_nric"></a><span data-ttu-id="57f50-2990">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="57f50-2990">Keyword_singapore_nric</span></span>

- <span data-ttu-id="57f50-2991">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="57f50-2991">National Registration Identity Card</span></span> 
- <span data-ttu-id="57f50-2992">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2992">Identity Card Number</span></span> 
- <span data-ttu-id="57f50-2993">NRIC</span><span class="sxs-lookup"><span data-stu-id="57f50-2993">NRIC</span></span> 
- <span data-ttu-id="57f50-2994">IK</span><span class="sxs-lookup"><span data-stu-id="57f50-2994">IC</span></span> 
- <span data-ttu-id="57f50-2995">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="57f50-2995">Foreign Identification Number</span></span> 
- <span data-ttu-id="57f50-2996">FIN</span><span class="sxs-lookup"><span data-stu-id="57f50-2996">FIN</span></span> 
- <span data-ttu-id="57f50-2997">身份证</span><span class="sxs-lookup"><span data-stu-id="57f50-2997">身份证</span></span> 
- <span data-ttu-id="57f50-2998">身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-2998">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="57f50-2999">Südafrika – Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-2999">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3000">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3000">Format</span></span>

<span data-ttu-id="57f50-3001">13 Ziffern, die Leerzeichen enthalten können</span><span class="sxs-lookup"><span data-stu-id="57f50-3001">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3002">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3002">Pattern</span></span>

<span data-ttu-id="57f50-3003">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-3003">13 digits:</span></span>
- <span data-ttu-id="57f50-3004">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="57f50-3004">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="57f50-3005">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3005">Four digits</span></span> 
- <span data-ttu-id="57f50-3006">Ein einstelliger Citizenship-Indikator </span><span class="sxs-lookup"><span data-stu-id="57f50-3006">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="57f50-3007">Die Ziffer "8" oder "9" </span><span class="sxs-lookup"><span data-stu-id="57f50-3007">The digit "8" or "9"</span></span> 
- <span data-ttu-id="57f50-3008">Eine Ziffer als Prüfsummenziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-3008">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3009">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3009">Checksum</span></span>

<span data-ttu-id="57f50-3010">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-3010">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3011">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3011">Definition</span></span>

<span data-ttu-id="57f50-3012">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3012">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3013">Die Funktion Func_south_africa_identification_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3013">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3014">Ein Schlüsselwort aus Keyword_south_africa_identification_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3014">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="57f50-3015">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-3015">The checksum passes.</span></span>

```xml
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-3016">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3016">Keywords</span></span>
   
#### <a name="keyword_south_africa_identification_number"></a><span data-ttu-id="57f50-3017">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="57f50-3017">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="57f50-3018">Identity card</span><span class="sxs-lookup"><span data-stu-id="57f50-3018">Identity card</span></span>
- <span data-ttu-id="57f50-3019">ID</span><span class="sxs-lookup"><span data-stu-id="57f50-3019">ID</span></span>
- <span data-ttu-id="57f50-3020">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="57f50-3020">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="57f50-3021">Südkorea – Einwohnerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-3021">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3022">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3022">Format</span></span>

<span data-ttu-id="57f50-3023">13 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="57f50-3023">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3024">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3024">Pattern</span></span>

<span data-ttu-id="57f50-3025">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-3025">13 digits:</span></span>
- <span data-ttu-id="57f50-3026">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="57f50-3026">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="57f50-3027">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="57f50-3027">A hyphen</span></span> 
- <span data-ttu-id="57f50-3028">Eine Ziffer, die durch das Jahrhundert und das Geschlecht bestimmt wird </span><span class="sxs-lookup"><span data-stu-id="57f50-3028">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="57f50-3029">Vierstelliger Code für die Geburtsregion </span><span class="sxs-lookup"><span data-stu-id="57f50-3029">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="57f50-3030">Eine Ziffer, um Personen zu unterscheiden, für die die vorhergehenden Zahlen identisch sind </span><span class="sxs-lookup"><span data-stu-id="57f50-3030">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="57f50-3031">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-3031">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3032">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3032">Checksum</span></span>

<span data-ttu-id="57f50-3033">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-3033">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3034">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3034">Definition</span></span>

<span data-ttu-id="57f50-3035">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3035">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3036">Die Funktion Func_south_korea_resident_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3036">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3037">Ein Schlüsselwort aus Keyword_south_korea_resident_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3037">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="57f50-3038">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-3038">The checksum passes.</span></span>

<span data-ttu-id="57f50-3039">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3039">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3040">Die Funktion Func_south_korea_resident_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3040">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3041">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-3041">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-3042">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3042">Keywords</span></span>
   
#### <a name="keyword_south_korea_resident_number"></a><span data-ttu-id="57f50-3043">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="57f50-3043">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="57f50-3044">National ID card</span><span class="sxs-lookup"><span data-stu-id="57f50-3044">National ID card</span></span> 
- <span data-ttu-id="57f50-3045">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3045">Citizen's Registration Number</span></span> 
- <span data-ttu-id="57f50-3046">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="57f50-3046">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="57f50-3047">RRN</span><span class="sxs-lookup"><span data-stu-id="57f50-3047">RRN</span></span> 
- <span data-ttu-id="57f50-3048">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="57f50-3048">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="57f50-3049">Spanische Sozialversicherungsnummer (SSN)</span><span class="sxs-lookup"><span data-stu-id="57f50-3049">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3050">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3050">Format</span></span>

<span data-ttu-id="57f50-3051">11-12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3051">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3052">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3052">Pattern</span></span>

<span data-ttu-id="57f50-3053">11-12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-3053">11-12 digits:</span></span>
- <span data-ttu-id="57f50-3054">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3054">Two digits</span></span> 
- <span data-ttu-id="57f50-3055">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="57f50-3055">A forward slash (optional)</span></span> 
- <span data-ttu-id="57f50-3056">7 bis 8 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3056">7-8 digits</span></span> 
- <span data-ttu-id="57f50-3057">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="57f50-3057">A forward slash (optional)</span></span> 
- <span data-ttu-id="57f50-3058">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3058">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3059">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3059">Checksum</span></span>

<span data-ttu-id="57f50-3060">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3061">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3061">Definition</span></span>

<span data-ttu-id="57f50-3062">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3063">Die Funktion Func_spanish_social_security_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3063">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3064">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-3064">The checksum passes.</span></span>

```xml
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-3065">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3065">Keywords</span></span>

<span data-ttu-id="57f50-3066">Keine</span><span class="sxs-lookup"><span data-stu-id="57f50-3066">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="57f50-3067">SQL Server Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57f50-3067">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3068">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3068">Format</span></span>

<span data-ttu-id="57f50-3069">Die Zeichenfolge "Benutzer-ID", "Benutzer-ID", "UID" oder "UserID", gefolgt von den Zeichen und Zeichenfolgen, die im Muster unten dargestellt sind.</span><span class="sxs-lookup"><span data-stu-id="57f50-3069">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3070">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3070">Pattern</span></span>

- <span data-ttu-id="57f50-3071">Die Zeichenfolge "Benutzer-ID", "Benutzer-ID", "UID" oder "UserID"</span><span class="sxs-lookup"><span data-stu-id="57f50-3071">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="57f50-3072">Eine beliebige Kombination von zwischen 1-200 unter-oder Großbuchstaben, Ziffern, Symbolen, Sonderzeichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-3072">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="57f50-3073">Die Zeichenfolge "Password" oder "pwd", wobei "pwd" kein Kleinbuchstabe vorangestellt ist</span><span class="sxs-lookup"><span data-stu-id="57f50-3073">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="57f50-3074">Ein Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-3074">An equal sign (=)</span></span>
- <span data-ttu-id="57f50-3075">Ein beliebiges Zeichen, das kein Dollarzeichen ($), Prozentzeichen (%), größer als das Symbol (#a0), Symbol (@), Anführungszeichen ("), Semikolon (;), linke geschweifte Klammer ([) oder linke Klammer ({) ist.</span><span class="sxs-lookup"><span data-stu-id="57f50-3075">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="57f50-3076">Eine beliebige Kombination von 7-128 Zeichen, die kein Semikolon sind (;), Schrägstrich (/) oder Anführungszeichen (")</span><span class="sxs-lookup"><span data-stu-id="57f50-3076">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="57f50-3077">Ein Semikolon (;) oder Anführungszeichen (")</span><span class="sxs-lookup"><span data-stu-id="57f50-3077">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3078">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3078">Checksum</span></span>

<span data-ttu-id="57f50-3079">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3079">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3080">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3080">Definition</span></span>

<span data-ttu-id="57f50-3081">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3081">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3082">Der reguläre Ausdruck CEP_Regex_SQLServerConnectionString sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3082">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3083">Ein Schlüsselwort aus CEP_GlobalFilter wurde **nicht** gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3083">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="57f50-3084">Der reguläre Ausdruck CEP_PasswordPlaceHolder findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3084">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3085">Der reguläre Ausdruck CEP_CommonExampleKeywords findet **keine** Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3085">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```sql
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

### <a name="keywords"></a><span data-ttu-id="57f50-3086">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3086">Keywords</span></span>

#### <a name="cep_globalfilter"></a><span data-ttu-id="57f50-3087">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="57f50-3087">CEP_GlobalFilter</span></span>

- <span data-ttu-id="57f50-3088">Einige-Kennwort</span><span class="sxs-lookup"><span data-stu-id="57f50-3088">some-password</span></span>
- <span data-ttu-id="57f50-3089">somepassword</span><span class="sxs-lookup"><span data-stu-id="57f50-3089">somepassword</span></span>
- <span data-ttu-id="57f50-3090">secretPassword</span><span class="sxs-lookup"><span data-stu-id="57f50-3090">secretPassword</span></span>
- <span data-ttu-id="57f50-3091">Beispiel</span><span class="sxs-lookup"><span data-stu-id="57f50-3091">sample</span></span>

#### <a name="cep_passwordplaceholder"></a><span data-ttu-id="57f50-3092">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="57f50-3092">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="57f50-3093">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="57f50-3093">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="57f50-3094">Password oder PWD gefolgt von 0-2 Leerzeichen, ein Gleichheitszeichen (=), 0-2 Leerzeichen und ein Sternchen (\*)--oder--</span><span class="sxs-lookup"><span data-stu-id="57f50-3094">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="57f50-3095">Password oder PWD gefolgt von:</span><span class="sxs-lookup"><span data-stu-id="57f50-3095">Password or pwd followed by:</span></span>
    - <span data-ttu-id="57f50-3096">Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="57f50-3096">Equal sign (=)</span></span>
    - <span data-ttu-id="57f50-3097">Kleiner als-Symbol (#a0)</span><span class="sxs-lookup"><span data-stu-id="57f50-3097">Less than symbol (<)</span></span>
    - <span data-ttu-id="57f50-3098">Eine beliebige Kombination von 1-200 Zeichen mit groß-oder Kleinbuchstaben, Ziffern, einem Sternchen (\*), einem Bindestrich (-), einem Unterstrich (_) oder einem Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-3098">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="57f50-3099">Größer als-Symbol (#a0)</span><span class="sxs-lookup"><span data-stu-id="57f50-3099">Greater than symbol (>)</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="57f50-3100">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="57f50-3100">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="57f50-3101">(Beachten Sie, dass dieser vertrauliche Informationstyp technisch diese Schlüsselwörter mit einem regulären Ausdruck und nicht mit einer Stichwortliste identifiziert.)</span><span class="sxs-lookup"><span data-stu-id="57f50-3101">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="57f50-3102">contoso</span><span class="sxs-lookup"><span data-stu-id="57f50-3102">contoso</span></span>
- <span data-ttu-id="57f50-3103">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="57f50-3103">fabrikam</span></span>
- <span data-ttu-id="57f50-3104">Northwind</span><span class="sxs-lookup"><span data-stu-id="57f50-3104">northwind</span></span>
- <span data-ttu-id="57f50-3105">Sandkasten</span><span class="sxs-lookup"><span data-stu-id="57f50-3105">sandbox</span></span>
- <span data-ttu-id="57f50-3106">OneBox</span><span class="sxs-lookup"><span data-stu-id="57f50-3106">onebox</span></span>
- <span data-ttu-id="57f50-3107">localhost</span><span class="sxs-lookup"><span data-stu-id="57f50-3107">localhost</span></span>
- <span data-ttu-id="57f50-3108">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="57f50-3108">127.0.0.1</span></span>
- <span data-ttu-id="57f50-3109">testacs.</span><span class="sxs-lookup"><span data-stu-id="57f50-3109">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-3110">com</span><span class="sxs-lookup"><span data-stu-id="57f50-3110">com</span></span>
- <span data-ttu-id="57f50-3111">s-int.</span><span class="sxs-lookup"><span data-stu-id="57f50-3111">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="57f50-3112">NET</span><span class="sxs-lookup"><span data-stu-id="57f50-3112">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="57f50-3113">Schwedische Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-3113">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3114">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3114">Format</span></span>

<span data-ttu-id="57f50-3115">10 oder 12 Ziffern und ein optionales Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-3115">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3116">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3116">Pattern</span></span>

<span data-ttu-id="57f50-3117">10 oder 12 Ziffern und ein optionals Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="57f50-3117">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="57f50-3118">2 bis 4 Ziffern (optional)</span><span class="sxs-lookup"><span data-stu-id="57f50-3118">2-4 digits (optional)</span></span> 
- <span data-ttu-id="57f50-3119">Sechs Ziffern im Datumsformat JJMMTT</span><span class="sxs-lookup"><span data-stu-id="57f50-3119">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="57f50-3120">Trennzeichen „-“ oder „+“ (optional) und</span><span class="sxs-lookup"><span data-stu-id="57f50-3120">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="57f50-3121">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3121">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3122">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3122">Checksum</span></span>

<span data-ttu-id="57f50-3123">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-3123">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3124">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3124">Definition</span></span>

<span data-ttu-id="57f50-3125">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3125">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3126">Die Funktion Func_swedish_national_identifier findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3126">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3127">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-3127">The checksum passes.</span></span>

```xml
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-3128">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3128">Keywords</span></span>

<span data-ttu-id="57f50-3129">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3129">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="57f50-3130">Schwedische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-3130">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3131">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3131">Format</span></span>

<span data-ttu-id="57f50-3132">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3132">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3133">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3133">Pattern</span></span>

<span data-ttu-id="57f50-3134">Acht aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3134">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3135">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3135">Checksum</span></span>

<span data-ttu-id="57f50-3136">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3136">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3137">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3137">Definition</span></span>

<span data-ttu-id="57f50-3138">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3139">Der reguläre Ausdruck Regex_sweden_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3139">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3140">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="57f50-3140">One of the following is true:</span></span>
    - <span data-ttu-id="57f50-3141">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3141">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="57f50-3142">Ein Schlüsselwort aus Keyword_sweden_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3142">A keyword from Keyword_sweden_passport is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-3143">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3143">Keywords</span></span>
   
#### <a name="keyword_sweden_passport"></a><span data-ttu-id="57f50-3144">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="57f50-3144">Keyword_sweden_passport</span></span>

- <span data-ttu-id="57f50-3145">visa requirements</span><span class="sxs-lookup"><span data-stu-id="57f50-3145">visa requirements</span></span> 
- <span data-ttu-id="57f50-3146">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="57f50-3146">Alien Registration Card</span></span> 
- <span data-ttu-id="57f50-3147">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="57f50-3147">Schengen visas</span></span> 
- <span data-ttu-id="57f50-3148">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="57f50-3148">Schengen visa</span></span> 
- <span data-ttu-id="57f50-3149">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="57f50-3149">Visa Processing</span></span> 
- <span data-ttu-id="57f50-3150">Visa Type</span><span class="sxs-lookup"><span data-stu-id="57f50-3150">Visa Type</span></span> 
- <span data-ttu-id="57f50-3151">Single Entry</span><span class="sxs-lookup"><span data-stu-id="57f50-3151">Single Entry</span></span> 
- <span data-ttu-id="57f50-3152">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="57f50-3152">Multiple Entry</span></span> 
- <span data-ttu-id="57f50-3153">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="57f50-3153">G3 Processing Fees</span></span> 

#### <a name="keyword_passport"></a><span data-ttu-id="57f50-3154">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="57f50-3154">Keyword_passport</span></span>

- <span data-ttu-id="57f50-3155">Passport Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3155">Passport Number</span></span> 
- <span data-ttu-id="57f50-3156">Passport No</span><span class="sxs-lookup"><span data-stu-id="57f50-3156">Passport No</span></span> 
- <span data-ttu-id="57f50-3157">Passport#</span><span class="sxs-lookup"><span data-stu-id="57f50-3157">Passport #</span></span> 
- <span data-ttu-id="57f50-3158">Pass #</span><span class="sxs-lookup"><span data-stu-id="57f50-3158">Passport#</span></span> 
- <span data-ttu-id="57f50-3159">Passport-Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-3159">PassportID</span></span> 
- <span data-ttu-id="57f50-3160">Passportno</span><span class="sxs-lookup"><span data-stu-id="57f50-3160">Passportno</span></span> 
- <span data-ttu-id="57f50-3161">passportnumber</span><span class="sxs-lookup"><span data-stu-id="57f50-3161">passportnumber</span></span> 
- <span data-ttu-id="57f50-3162">パスポート</span><span class="sxs-lookup"><span data-stu-id="57f50-3162">パスポート</span></span> 
- <span data-ttu-id="57f50-3163">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="57f50-3163">パスポート番号</span></span> 
- <span data-ttu-id="57f50-3164">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="57f50-3164">パスポートのNum</span></span> 
- <span data-ttu-id="57f50-3165">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="57f50-3165">パスポート＃</span></span> 
- <span data-ttu-id="57f50-3166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="57f50-3166">Numéro de passeport</span></span> 
- <span data-ttu-id="57f50-3167">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="57f50-3167">Passeport n °</span></span> 
- <span data-ttu-id="57f50-3168">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="57f50-3168">Passeport Non</span></span> 
- <span data-ttu-id="57f50-3169">Passeport#</span><span class="sxs-lookup"><span data-stu-id="57f50-3169">Passeport #</span></span> 
- <span data-ttu-id="57f50-3170">Passeport #</span><span class="sxs-lookup"><span data-stu-id="57f50-3170">Passeport#</span></span> 
- <span data-ttu-id="57f50-3171">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="57f50-3171">PasseportNon</span></span> 
- <span data-ttu-id="57f50-3172">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="57f50-3172">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="57f50-3173">SWIFT-Code</span><span class="sxs-lookup"><span data-stu-id="57f50-3173">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3174">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3174">Format</span></span>

<span data-ttu-id="57f50-3175">Vier Buchstaben, gefolgt von 5-31 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3175">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3176">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3176">Pattern</span></span>

<span data-ttu-id="57f50-3177">Vier Buchstaben, gefolgt von 5 bis 31 Buchstaben oder Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-3177">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="57f50-3178">Vier Buchstaben für den Bankcode (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="57f50-3178">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="57f50-3179">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-3179">An optional space</span></span> 
- <span data-ttu-id="57f50-3180">4 bis 28 Buchstaben oder Ziffern (BBAN, Basic Bank Account Number)</span><span class="sxs-lookup"><span data-stu-id="57f50-3180">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="57f50-3181">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-3181">An optional space</span></span> 
- <span data-ttu-id="57f50-3182">1 bis 3 Buchstaben oder Ziffern (Rest des BBAN)</span><span class="sxs-lookup"><span data-stu-id="57f50-3182">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3183">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3183">Checksum</span></span>

<span data-ttu-id="57f50-3184">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3184">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3185">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3185">Definition</span></span>

<span data-ttu-id="57f50-3186">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3186">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3187">Der reguläre Ausdruck Regex_swift findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3187">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3188">Ein Schlüsselwort aus Keyword_swift wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3188">A keyword from Keyword_swift is found.</span></span>

```xml
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-3189">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3189">Keywords</span></span>
   
#### <a name="keyword_swift"></a><span data-ttu-id="57f50-3190">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="57f50-3190">Keyword_swift</span></span>

- <span data-ttu-id="57f50-3191">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="57f50-3191">international organization for standardization 9362</span></span> 
- <span data-ttu-id="57f50-3192">iso 9362</span><span class="sxs-lookup"><span data-stu-id="57f50-3192">iso 9362</span></span> 
- <span data-ttu-id="57f50-3193">iso9362</span><span class="sxs-lookup"><span data-stu-id="57f50-3193">iso9362</span></span> 
- <span data-ttu-id="57f50-3194">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="57f50-3194">swift\#</span></span> 
- <span data-ttu-id="57f50-3195">Swiftcode</span><span class="sxs-lookup"><span data-stu-id="57f50-3195">swiftcode</span></span> 
- <span data-ttu-id="57f50-3196">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="57f50-3196">swiftnumber</span></span> 
- <span data-ttu-id="57f50-3197">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="57f50-3197">swiftroutingnumber</span></span> 
- <span data-ttu-id="57f50-3198">swift code</span><span class="sxs-lookup"><span data-stu-id="57f50-3198">swift code</span></span> 
- <span data-ttu-id="57f50-3199">swift number #</span><span class="sxs-lookup"><span data-stu-id="57f50-3199">swift number #</span></span> 
- <span data-ttu-id="57f50-3200">swift routing number</span><span class="sxs-lookup"><span data-stu-id="57f50-3200">swift routing number</span></span> 
- <span data-ttu-id="57f50-3201">bic number</span><span class="sxs-lookup"><span data-stu-id="57f50-3201">bic number</span></span> 
- <span data-ttu-id="57f50-3202">bic code</span><span class="sxs-lookup"><span data-stu-id="57f50-3202">bic code</span></span> 
- <span data-ttu-id="57f50-3203">BIC\#</span><span class="sxs-lookup"><span data-stu-id="57f50-3203">bic \#</span></span> 
- <span data-ttu-id="57f50-3204">BIC\#</span><span class="sxs-lookup"><span data-stu-id="57f50-3204">bic\#</span></span> 
- <span data-ttu-id="57f50-3205">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="57f50-3205">bank identifier code</span></span> 
- <span data-ttu-id="57f50-3206">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="57f50-3206">標準化9362</span></span> 
- <span data-ttu-id="57f50-3207">迅速＃</span><span class="sxs-lookup"><span data-stu-id="57f50-3207">迅速＃</span></span> 
- <span data-ttu-id="57f50-3208">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="57f50-3208">SWIFTコード</span></span> 
- <span data-ttu-id="57f50-3209">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="57f50-3209">SWIFT番号</span></span> 
- <span data-ttu-id="57f50-3210">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="57f50-3210">迅速なルーティング番号</span></span> 
- <span data-ttu-id="57f50-3211">BIC番号</span><span class="sxs-lookup"><span data-stu-id="57f50-3211">BIC番号</span></span> 
- <span data-ttu-id="57f50-3212">BICコード</span><span class="sxs-lookup"><span data-stu-id="57f50-3212">BICコード</span></span> 
- <span data-ttu-id="57f50-3213">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="57f50-3213">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="57f50-3214">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="57f50-3214">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="57f50-3215">rapide\#</span><span class="sxs-lookup"><span data-stu-id="57f50-3215">rapide \#</span></span> 
- <span data-ttu-id="57f50-3216">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="57f50-3216">code SWIFT</span></span> 
- <span data-ttu-id="57f50-3217">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="57f50-3217">le numéro de swift</span></span> 
- <span data-ttu-id="57f50-3218">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="57f50-3218">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="57f50-3219">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="57f50-3219">le numéro BIC</span></span> 
- <span data-ttu-id="57f50-3220">\#BIC</span><span class="sxs-lookup"><span data-stu-id="57f50-3220">\# BIC</span></span> 
- <span data-ttu-id="57f50-3221">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="57f50-3221">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="57f50-3222">Taiwanesicher Personalausweis</span><span class="sxs-lookup"><span data-stu-id="57f50-3222">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3223">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3223">Format</span></span>

<span data-ttu-id="57f50-3224">Ein Buchstabe (auf Englisch) gefolgt von neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3224">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3225">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3225">Pattern</span></span>

<span data-ttu-id="57f50-3226">Ein Buchstabe (Englisch), gefolgt von neun Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-3226">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="57f50-3227">Ein Buchstabe (Englisch, Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="57f50-3227">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="57f50-3228">Die Ziffer 1 oder 2</span><span class="sxs-lookup"><span data-stu-id="57f50-3228">The digit "1" or "2"</span></span> 
- <span data-ttu-id="57f50-3229">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3229">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3230">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3230">Checksum</span></span>

<span data-ttu-id="57f50-3231">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-3231">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3232">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3232">Definition</span></span>

<span data-ttu-id="57f50-3233">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3233">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3234">Die Funktion Func_taiwanese_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3234">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3235">Ein Schlüsselwort aus Keyword_taiwanese_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3235">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="57f50-3236">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-3236">The checksum passes.</span></span>

```xml
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-3237">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3237">Keywords</span></span>

#### <a name="keyword_taiwanese_national_id"></a><span data-ttu-id="57f50-3238">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="57f50-3238">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="57f50-3239">身份證字號</span><span class="sxs-lookup"><span data-stu-id="57f50-3239">身份證字號</span></span> 
- <span data-ttu-id="57f50-3240">身份證</span><span class="sxs-lookup"><span data-stu-id="57f50-3240">身份證</span></span> 
- <span data-ttu-id="57f50-3241">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="57f50-3241">身份證號碼</span></span> 
- <span data-ttu-id="57f50-3242">身份證號</span><span class="sxs-lookup"><span data-stu-id="57f50-3242">身份證號</span></span> 
- <span data-ttu-id="57f50-3243">身分證字號</span><span class="sxs-lookup"><span data-stu-id="57f50-3243">身分證字號</span></span> 
- <span data-ttu-id="57f50-3244">身分證</span><span class="sxs-lookup"><span data-stu-id="57f50-3244">身分證</span></span> 
- <span data-ttu-id="57f50-3245">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="57f50-3245">身分證號碼</span></span> 
- <span data-ttu-id="57f50-3246">身份證號</span><span class="sxs-lookup"><span data-stu-id="57f50-3246">身份證號</span></span> 
- <span data-ttu-id="57f50-3247">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="57f50-3247">身分證統一編號</span></span> 
- <span data-ttu-id="57f50-3248">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="57f50-3248">國民身分證統一編號</span></span> 
- <span data-ttu-id="57f50-3249">簽名</span><span class="sxs-lookup"><span data-stu-id="57f50-3249">簽名</span></span> 
- <span data-ttu-id="57f50-3250">蓋章</span><span class="sxs-lookup"><span data-stu-id="57f50-3250">蓋章</span></span> 
- <span data-ttu-id="57f50-3251">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="57f50-3251">簽名或蓋章</span></span> 
- <span data-ttu-id="57f50-3252">簽章</span><span class="sxs-lookup"><span data-stu-id="57f50-3252">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="57f50-3253">	Taiwan – Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-3253">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3254">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3254">Format</span></span>

- <span data-ttu-id="57f50-3255">Biometrische Passport-Nummer: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3255">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="57f50-3256">Nicht biometrische Passport-Nummer: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3256">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3257">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3257">Pattern</span></span>
<span data-ttu-id="57f50-3258">Biometrische Passnummer:</span><span class="sxs-lookup"><span data-stu-id="57f50-3258">Biometric passport number:</span></span>
- <span data-ttu-id="57f50-3259">Die Ziffer "3" </span><span class="sxs-lookup"><span data-stu-id="57f50-3259">The digit "3"</span></span> 
- <span data-ttu-id="57f50-3260">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3260">Eight digits</span></span>

<span data-ttu-id="57f50-3261">Nicht biometrische Passnummer:</span><span class="sxs-lookup"><span data-stu-id="57f50-3261">Non-biometric passport number:</span></span>
- <span data-ttu-id="57f50-3262">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3262">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3263">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3263">Checksum</span></span>

<span data-ttu-id="57f50-3264">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3264">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3265">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3265">Definition</span></span>

<span data-ttu-id="57f50-3266">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3266">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3267">Der reguläre Ausdruck Regex_taiwan_passport sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3267">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3268">Ein Schlüsselwort aus Keyword_taiwan_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3268">A keyword from Keyword_taiwan_passport is found.</span></span>

```xml
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-3269">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3269">Keywords</span></span>

#### <a name="keyword_taiwan_passport"></a><span data-ttu-id="57f50-3270">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="57f50-3270">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="57f50-3271">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="57f50-3271">ROC passport number</span></span> 
- <span data-ttu-id="57f50-3272">Passport number</span><span class="sxs-lookup"><span data-stu-id="57f50-3272">Passport number</span></span> 
- <span data-ttu-id="57f50-3273">Passport no</span><span class="sxs-lookup"><span data-stu-id="57f50-3273">Passport no</span></span> 
- <span data-ttu-id="57f50-3274">Passport Num</span><span class="sxs-lookup"><span data-stu-id="57f50-3274">Passport Num</span></span> 
- <span data-ttu-id="57f50-3275">Passport #</span><span class="sxs-lookup"><span data-stu-id="57f50-3275">Passport #</span></span> 
- <span data-ttu-id="57f50-3276">护照</span><span class="sxs-lookup"><span data-stu-id="57f50-3276">护照</span></span> 
- <span data-ttu-id="57f50-3277">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="57f50-3277">中華民國護照</span></span> 
- <span data-ttu-id="57f50-3278">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="57f50-3278">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="57f50-3279">Taiwan – Einwohnerzertifikatsnummer (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="57f50-3279">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3280">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3280">Format</span></span>

<span data-ttu-id="57f50-3281">10 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3281">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3282">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3282">Pattern</span></span>

<span data-ttu-id="57f50-3283">10 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-3283">10 letters and digits:</span></span>
- <span data-ttu-id="57f50-3284">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="57f50-3284">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="57f50-3285">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3285">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3286">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3286">Checksum</span></span>

<span data-ttu-id="57f50-3287">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3287">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3288">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3288">Definition</span></span>

<span data-ttu-id="57f50-3289">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3289">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3290">Der reguläre Ausdruck Regex_taiwan_resident_certificate sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3290">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3291">Ein Schlüsselwort aus Keyword_taiwan_resident_certificate wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3291">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```xml
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-3292">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3292">Keywords</span></span>

#### <a name="keyword_taiwan_resident_certificate"></a><span data-ttu-id="57f50-3293">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="57f50-3293">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="57f50-3294">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="57f50-3294">Resident Certificate</span></span> 
- <span data-ttu-id="57f50-3295">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="57f50-3295">Resident Cert</span></span> 
- <span data-ttu-id="57f50-3296">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="57f50-3296">Resident Cert.</span></span> 
- <span data-ttu-id="57f50-3297">Identification card</span><span class="sxs-lookup"><span data-stu-id="57f50-3297">Identification card</span></span> 
- <span data-ttu-id="57f50-3298">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="57f50-3298">Alien Resident Certificate</span></span> 
- <span data-ttu-id="57f50-3299">Bogens</span><span class="sxs-lookup"><span data-stu-id="57f50-3299">ARC</span></span> 
- <span data-ttu-id="57f50-3300">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="57f50-3300">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="57f50-3301">TARC</span><span class="sxs-lookup"><span data-stu-id="57f50-3301">TARC</span></span> 
- <span data-ttu-id="57f50-3302">居留證</span><span class="sxs-lookup"><span data-stu-id="57f50-3302">居留證</span></span> 
- <span data-ttu-id="57f50-3303">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="57f50-3303">外僑居留證</span></span> 
- <span data-ttu-id="57f50-3304">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="57f50-3304">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="57f50-3305">Thai-Populations Kennzeichnungs Code</span><span class="sxs-lookup"><span data-stu-id="57f50-3305">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3306">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3306">Format</span></span>

<span data-ttu-id="57f50-3307">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3307">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3308">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3308">Pattern</span></span>

<span data-ttu-id="57f50-3309">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-3309">13 digits:</span></span>
- <span data-ttu-id="57f50-3310">Die erste Ziffer ist nicht 0 oder 9.</span><span class="sxs-lookup"><span data-stu-id="57f50-3310">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="57f50-3311">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3311">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3312">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3312">Checksum</span></span>

<span data-ttu-id="57f50-3313">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-3313">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3314">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3314">Definition</span></span>

<span data-ttu-id="57f50-3315">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3315">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3316">Die Funktion Func_Thai_Citizen_Id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3316">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3317">Ein Schlüsselwort aus Keyword_Thai_Citizen_Id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3317">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="57f50-3318">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3318">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3319">Die Funktion Func_Thai_Citizen_Id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3319">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-3320">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3320">Keywords</span></span>

#### <a name="keyword_thai_citizen_id"></a><span data-ttu-id="57f50-3321">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="57f50-3321">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="57f50-3322">ID Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3322">ID Number</span></span>
- <span data-ttu-id="57f50-3323">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-3323">Identification Number</span></span>
- <span data-ttu-id="57f50-3324">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="57f50-3324">บัตรประชาชน</span></span>
- <span data-ttu-id="57f50-3325">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="57f50-3325">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="57f50-3326">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="57f50-3326">บัตรประชาชน</span></span>
- <span data-ttu-id="57f50-3327">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="57f50-3327">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="57f50-3328">Türkische nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-3328">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3329">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3329">Format</span></span>

<span data-ttu-id="57f50-3330">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3330">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3331">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3331">Pattern</span></span>

<span data-ttu-id="57f50-3332">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3332">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3333">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3333">Checksum</span></span>

<span data-ttu-id="57f50-3334">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-3334">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3335">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3335">Definition</span></span>

<span data-ttu-id="57f50-3336">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3336">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3337">Die Funktion Func_Turkish_National_Id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3337">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3338">Ein Schlüsselwort aus Keyword_Turkish_National_Id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3338">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="57f50-3339">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3339">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3340">Die Funktion Func_Turkish_National_Id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3340">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-3341">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3341">Keywords</span></span>

#### <a name="keyword_turkish_national_id"></a><span data-ttu-id="57f50-3342">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="57f50-3342">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="57f50-3343">TC KİMLİK Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3343">TC Kimlik No</span></span>
- <span data-ttu-id="57f50-3344">TC KİMLİK numarası</span><span class="sxs-lookup"><span data-stu-id="57f50-3344">TC Kimlik numarası</span></span>
- <span data-ttu-id="57f50-3345">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="57f50-3345">Vatandaşlık numarası</span></span>
- <span data-ttu-id="57f50-3346">Vatandaşlık Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3346">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="57f50-p141">Britische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3349">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3349">Format</span></span>

<span data-ttu-id="57f50-3350">Kombination aus 18 Buchstaben und Ziffern im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3350">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3351">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3351">Pattern</span></span>

<span data-ttu-id="57f50-3352">18 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="57f50-3352">18 letters and digits:</span></span>
- <span data-ttu-id="57f50-3353">Fünf Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) oder die Ziffer 9 anstelle eines Buchstabens</span><span class="sxs-lookup"><span data-stu-id="57f50-3353">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="57f50-3354">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-3354">One digit</span></span> 
- <span data-ttu-id="57f50-3355">Fünf Ziffern im Datumsformat TTMMJ für das Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="57f50-3355">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="57f50-3356">Zwei Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) oder die Ziffer 9 anstelle eines Buchstabens</span><span class="sxs-lookup"><span data-stu-id="57f50-3356">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="57f50-3357">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3357">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3358">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3358">Checksum</span></span>

<span data-ttu-id="57f50-3359">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-3359">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3360">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3360">Definition</span></span>

<span data-ttu-id="57f50-3361">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3361">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3362">Die Funktion Func_uk_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3362">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3363">Ein Schlüsselwort aus Keyword_uk_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3363">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="57f50-3364">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-3364">The checksum passes.</span></span>

```xml
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-3365">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3365">Keywords</span></span>

#### <a name="keyword_uk_drivers_license"></a><span data-ttu-id="57f50-3366">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="57f50-3366">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="57f50-3367">DVLA</span><span class="sxs-lookup"><span data-stu-id="57f50-3367">DVLA</span></span> 
- <span data-ttu-id="57f50-3368">light vans</span><span class="sxs-lookup"><span data-stu-id="57f50-3368">light vans</span></span> 
- <span data-ttu-id="57f50-3369">Quads entwickelt</span><span class="sxs-lookup"><span data-stu-id="57f50-3369">quadbikes</span></span> 
- <span data-ttu-id="57f50-3370">motor cars</span><span class="sxs-lookup"><span data-stu-id="57f50-3370">motor cars</span></span> 
- <span data-ttu-id="57f50-3371">125cc</span><span class="sxs-lookup"><span data-stu-id="57f50-3371">125cc</span></span> 
- <span data-ttu-id="57f50-3372">Beiwagen</span><span class="sxs-lookup"><span data-stu-id="57f50-3372">sidecar</span></span> 
- <span data-ttu-id="57f50-3373">Dreiräder</span><span class="sxs-lookup"><span data-stu-id="57f50-3373">tricycles</span></span> 
- <span data-ttu-id="57f50-3374">Motorrad</span><span class="sxs-lookup"><span data-stu-id="57f50-3374">motorcycles</span></span> 
- <span data-ttu-id="57f50-3375">photocard licence</span><span class="sxs-lookup"><span data-stu-id="57f50-3375">photocard licence</span></span> 
- <span data-ttu-id="57f50-3376">learner drivers</span><span class="sxs-lookup"><span data-stu-id="57f50-3376">learner drivers</span></span> 
- <span data-ttu-id="57f50-3377">licence holder</span><span class="sxs-lookup"><span data-stu-id="57f50-3377">licence holder</span></span> 
- <span data-ttu-id="57f50-3378">licence holders</span><span class="sxs-lookup"><span data-stu-id="57f50-3378">licence holders</span></span> 
- <span data-ttu-id="57f50-3379">driving licences</span><span class="sxs-lookup"><span data-stu-id="57f50-3379">driving licences</span></span> 
- <span data-ttu-id="57f50-3380">driving licence</span><span class="sxs-lookup"><span data-stu-id="57f50-3380">driving licence</span></span> 
- <span data-ttu-id="57f50-3381">dual control car</span><span class="sxs-lookup"><span data-stu-id="57f50-3381">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="57f50-p142">Britische Wählerverzeichnisnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3384">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3384">Format</span></span>

<span data-ttu-id="57f50-3385">Zwei Buchstaben gefolgt von 1-4 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3385">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3386">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3386">Pattern</span></span>

<span data-ttu-id="57f50-3387">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von 1-4 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3387">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3388">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3388">Checksum</span></span>

<span data-ttu-id="57f50-3389">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3389">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3390">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3390">Definition</span></span>

<span data-ttu-id="57f50-3391">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3391">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3392">Der reguläre Ausdruck Regex_uk_electoral findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3392">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3393">Ein Schlüsselwort aus Keyword_uk_electoral wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3393">A keyword from Keyword_uk_electoral is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-3394">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3394">Keywords</span></span>

#### <a name="keyword_uk_electoral"></a><span data-ttu-id="57f50-3395">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="57f50-3395">Keyword_uk_electoral</span></span>

- <span data-ttu-id="57f50-3396">council nomination</span><span class="sxs-lookup"><span data-stu-id="57f50-3396">council nomination</span></span> 
- <span data-ttu-id="57f50-3397">nomination form</span><span class="sxs-lookup"><span data-stu-id="57f50-3397">nomination form</span></span> 
- <span data-ttu-id="57f50-3398">electoral register</span><span class="sxs-lookup"><span data-stu-id="57f50-3398">electoral register</span></span> 
- <span data-ttu-id="57f50-3399">electoral roll</span><span class="sxs-lookup"><span data-stu-id="57f50-3399">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="57f50-p143">Britische National Health Service-Nummer</span><span class="sxs-lookup"><span data-stu-id="57f50-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3402">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3402">Format</span></span>

<span data-ttu-id="57f50-3403">10-17 Ziffern, durch Leerzeichen getrennt</span><span class="sxs-lookup"><span data-stu-id="57f50-3403">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3404">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3404">Pattern</span></span>

<span data-ttu-id="57f50-3405">10 bis 17 Stellen:</span><span class="sxs-lookup"><span data-stu-id="57f50-3405">10-17 digits:</span></span>
- <span data-ttu-id="57f50-3406">3 oder 10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3406">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="57f50-3407">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-3407">A space</span></span> 
- <span data-ttu-id="57f50-3408">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3408">Three digits</span></span> 
- <span data-ttu-id="57f50-3409">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="57f50-3409">A space</span></span> 
- <span data-ttu-id="57f50-3410">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3410">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3411">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3411">Checksum</span></span>

<span data-ttu-id="57f50-3412">Ja</span><span class="sxs-lookup"><span data-stu-id="57f50-3412">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3413">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3413">Definition</span></span>

<span data-ttu-id="57f50-3414">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3415">Die Funktion Func_uk_nhs_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3415">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3416">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="57f50-3416">One of the following is true:</span></span>
    - <span data-ttu-id="57f50-3417">Ein Schlüsselwort aus Keyword_uk_nhs_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3417">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="57f50-3418">Ein Schlüsselwort aus Keyword_uk_nhs_number1 wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3418">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="57f50-3419">Ein Schlüsselwort aus Keyword_uk_nhs_number_dob wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3419">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="57f50-3420">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="57f50-3420">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-3421">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3421">Keywords</span></span>
   
#### <a name="keyword_uk_nhs_number"></a><span data-ttu-id="57f50-3422">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="57f50-3422">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="57f50-3423">national health service</span><span class="sxs-lookup"><span data-stu-id="57f50-3423">national health service</span></span> 
- <span data-ttu-id="57f50-3424">NHS</span><span class="sxs-lookup"><span data-stu-id="57f50-3424">nhs</span></span> 
- <span data-ttu-id="57f50-3425">health services authority</span><span class="sxs-lookup"><span data-stu-id="57f50-3425">health services authority</span></span> 
- <span data-ttu-id="57f50-3426">health authority</span><span class="sxs-lookup"><span data-stu-id="57f50-3426">health authority</span></span>

#### <a name="keyword_uk_nhs_number1"></a><span data-ttu-id="57f50-3427">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="57f50-3427">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="57f50-3428">patient id</span><span class="sxs-lookup"><span data-stu-id="57f50-3428">patient id</span></span> 
- <span data-ttu-id="57f50-3429">patient identification</span><span class="sxs-lookup"><span data-stu-id="57f50-3429">patient identification</span></span> 
- <span data-ttu-id="57f50-3430">patient no</span><span class="sxs-lookup"><span data-stu-id="57f50-3430">patient no</span></span> 
- <span data-ttu-id="57f50-3431">patient number</span><span class="sxs-lookup"><span data-stu-id="57f50-3431">patient number</span></span>

#### <a name="keyword_uk_nhs_number_dob"></a><span data-ttu-id="57f50-3432">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="57f50-3432">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="57f50-3433">GP</span><span class="sxs-lookup"><span data-stu-id="57f50-3433">GP</span></span> 
- <span data-ttu-id="57f50-3434">DOB</span><span class="sxs-lookup"><span data-stu-id="57f50-3434">DOB</span></span> 
- <span data-ttu-id="57f50-3435">D. O. B</span><span class="sxs-lookup"><span data-stu-id="57f50-3435">D.O.B</span></span> 
- <span data-ttu-id="57f50-3436">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="57f50-3436">Date of Birth</span></span> 
- <span data-ttu-id="57f50-3437">Birth Date</span><span class="sxs-lookup"><span data-stu-id="57f50-3437">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="57f50-p144">Britische nationale Versicherungsnummer (NINO)</span><span class="sxs-lookup"><span data-stu-id="57f50-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3440">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3440">Format</span></span>

<span data-ttu-id="57f50-3441">7 Zeichen oder 9 Zeichen, getrennt durch Leerzeichen oder Bindestriche</span><span class="sxs-lookup"><span data-stu-id="57f50-3441">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3442">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3442">Pattern</span></span>

<span data-ttu-id="57f50-3443">Zwei mögliche Muster:</span><span class="sxs-lookup"><span data-stu-id="57f50-3443">Two possible patterns:</span></span>

- <span data-ttu-id="57f50-3444">Zwei Buchstaben (gültige Ninos verwenden nur bestimmte Zeichen in diesem Präfix, die von diesem Muster überprüft werden; Groß-/Kleinschreibung wird nicht berücksichtigt)</span><span class="sxs-lookup"><span data-stu-id="57f50-3444">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="57f50-3445">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3445">Six digits</span></span>
- <span data-ttu-id="57f50-3446">Entweder "A", "B", "C" oder "'d" (wie das Präfix sind nur bestimmte Zeichen im Suffix zulässig; Groß-/Kleinschreibung wird nicht berücksichtigt)</span><span class="sxs-lookup"><span data-stu-id="57f50-3446">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="57f50-3447">ODER</span><span class="sxs-lookup"><span data-stu-id="57f50-3447">OR</span></span>

- <span data-ttu-id="57f50-3448">Zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="57f50-3448">Two letters</span></span>
- <span data-ttu-id="57f50-3449">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-3449">A space or dash</span></span>
- <span data-ttu-id="57f50-3450">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3450">Two digits</span></span>
- <span data-ttu-id="57f50-3451">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-3451">A space or dash</span></span>
- <span data-ttu-id="57f50-3452">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3452">Two digits</span></span>
- <span data-ttu-id="57f50-3453">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-3453">A space or dash</span></span>
- <span data-ttu-id="57f50-3454">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3454">Two digits</span></span>
- <span data-ttu-id="57f50-3455">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-3455">A space or dash</span></span>
- <span data-ttu-id="57f50-3456">Entweder "A", "B", "C" oder "'d"</span><span class="sxs-lookup"><span data-stu-id="57f50-3456">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3457">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3457">Checksum</span></span>

<span data-ttu-id="57f50-3458">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3458">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3459">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3459">Definition</span></span>

<span data-ttu-id="57f50-3460">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3461">Die Funktion Func_uk_nino findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3461">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3462">Ein Schlüsselwort aus Keyword_uk_nino wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3462">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="57f50-3463">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3463">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3464">Die Funktion Func_uk_nino findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3464">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3465">Es wurde kein Schlüsselwort aus Keyword_uk_nino gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3465">No keyword from Keyword_uk_nino is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-3466">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3466">Keywords</span></span>

#### <a name="keyword_uk_nino"></a><span data-ttu-id="57f50-3467">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="57f50-3467">Keyword_uk_nino</span></span>

- <span data-ttu-id="57f50-3468">national insurance number</span><span class="sxs-lookup"><span data-stu-id="57f50-3468">national insurance number</span></span> 
- <span data-ttu-id="57f50-3469">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="57f50-3469">national insurance contributions</span></span> 
- <span data-ttu-id="57f50-3470">protection act</span><span class="sxs-lookup"><span data-stu-id="57f50-3470">protection act</span></span> 
- <span data-ttu-id="57f50-3471">Versicherungs</span><span class="sxs-lookup"><span data-stu-id="57f50-3471">insurance</span></span> 
- <span data-ttu-id="57f50-3472">social security number</span><span class="sxs-lookup"><span data-stu-id="57f50-3472">social security number</span></span> 
- <span data-ttu-id="57f50-3473">insurance application</span><span class="sxs-lookup"><span data-stu-id="57f50-3473">insurance application</span></span> 
- <span data-ttu-id="57f50-3474">medical application</span><span class="sxs-lookup"><span data-stu-id="57f50-3474">medical application</span></span> 
- <span data-ttu-id="57f50-3475">social insurance</span><span class="sxs-lookup"><span data-stu-id="57f50-3475">social insurance</span></span> 
- <span data-ttu-id="57f50-3476">medical attention</span><span class="sxs-lookup"><span data-stu-id="57f50-3476">medical attention</span></span> 
- <span data-ttu-id="57f50-3477">social security</span><span class="sxs-lookup"><span data-stu-id="57f50-3477">social security</span></span> 
- <span data-ttu-id="57f50-3478">great britain</span><span class="sxs-lookup"><span data-stu-id="57f50-3478">great britain</span></span> 
- <span data-ttu-id="57f50-3479">Versicherungs</span><span class="sxs-lookup"><span data-stu-id="57f50-3479">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="57f50-p145">US-amerikanische/britische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3482">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3482">Format</span></span>

<span data-ttu-id="57f50-3483">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3483">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3484">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3484">Pattern</span></span>

<span data-ttu-id="57f50-3485">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3485">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3486">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3486">Checksum</span></span>

<span data-ttu-id="57f50-3487">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3487">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3488">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3488">Definition</span></span>

<span data-ttu-id="57f50-3489">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3489">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3490">Die Funktion Func_usa_uk_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3490">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3491">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3491">A keyword from Keyword_passport is found.</span></span>

```xml
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-3492">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3492">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="57f50-3493">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="57f50-3493">Keyword_passport</span></span>

- <span data-ttu-id="57f50-3494">Passport Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3494">Passport Number</span></span> 
- <span data-ttu-id="57f50-3495">Passport No</span><span class="sxs-lookup"><span data-stu-id="57f50-3495">Passport No</span></span> 
- <span data-ttu-id="57f50-3496">Passport#</span><span class="sxs-lookup"><span data-stu-id="57f50-3496">Passport #</span></span> 
- <span data-ttu-id="57f50-3497">Pass #</span><span class="sxs-lookup"><span data-stu-id="57f50-3497">Passport#</span></span> 
- <span data-ttu-id="57f50-3498">Passport-Nr</span><span class="sxs-lookup"><span data-stu-id="57f50-3498">PassportID</span></span> 
- <span data-ttu-id="57f50-3499">Passportno</span><span class="sxs-lookup"><span data-stu-id="57f50-3499">Passportno</span></span> 
- <span data-ttu-id="57f50-3500">passportnumber</span><span class="sxs-lookup"><span data-stu-id="57f50-3500">passportnumber</span></span> 
- <span data-ttu-id="57f50-3501">パスポート</span><span class="sxs-lookup"><span data-stu-id="57f50-3501">パスポート</span></span> 
- <span data-ttu-id="57f50-3502">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="57f50-3502">パスポート番号</span></span> 
- <span data-ttu-id="57f50-3503">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="57f50-3503">パスポートのNum</span></span> 
- <span data-ttu-id="57f50-3504">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="57f50-3504">パスポート＃</span></span> 
- <span data-ttu-id="57f50-3505">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="57f50-3505">Numéro de passeport</span></span> 
- <span data-ttu-id="57f50-3506">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="57f50-3506">Passeport n °</span></span> 
- <span data-ttu-id="57f50-3507">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="57f50-3507">Passeport Non</span></span> 
- <span data-ttu-id="57f50-3508">Passeport#</span><span class="sxs-lookup"><span data-stu-id="57f50-3508">Passeport #</span></span> 
- <span data-ttu-id="57f50-3509">Passeport #</span><span class="sxs-lookup"><span data-stu-id="57f50-3509">Passeport#</span></span> 
- <span data-ttu-id="57f50-3510">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="57f50-3510">PasseportNon</span></span> 
- <span data-ttu-id="57f50-3511">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="57f50-3511">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="57f50-3512">US-Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="57f50-3512">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3513">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3513">Format</span></span>

<span data-ttu-id="57f50-3514">8-17 Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3514">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3515">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3515">Pattern</span></span>

<span data-ttu-id="57f50-3516">8-17 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3516">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3517">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3517">Checksum</span></span>

<span data-ttu-id="57f50-3518">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3518">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3519">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3519">Definition</span></span>

<span data-ttu-id="57f50-3520">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3520">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3521">Der reguläre Ausdruck Regex_usa_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3521">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3522">Ein Schlüsselwort aus Keyword_usa_Bank_Account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3522">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```xml
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-3523">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3523">Keywords</span></span>

#### <a name="keyword_usa_bank_account"></a><span data-ttu-id="57f50-3524">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="57f50-3524">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="57f50-3525">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3525">Checking Account Number</span></span> 
- <span data-ttu-id="57f50-3526">Checking Account</span><span class="sxs-lookup"><span data-stu-id="57f50-3526">Checking Account</span></span> 
- <span data-ttu-id="57f50-3527">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="57f50-3527">Checking Account #</span></span> 
- <span data-ttu-id="57f50-3528">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3528">Checking Acct Number</span></span> 
- <span data-ttu-id="57f50-3529">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="57f50-3529">Checking Acct #</span></span> 
- <span data-ttu-id="57f50-3530">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="57f50-3530">Checking Acct No.</span></span> 
- <span data-ttu-id="57f50-3531">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="57f50-3531">Checking Account No.</span></span> 
- <span data-ttu-id="57f50-3532">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3532">Bank Account Number</span></span> 
- <span data-ttu-id="57f50-3533">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="57f50-3533">Bank Account #</span></span> 
- <span data-ttu-id="57f50-3534">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3534">Bank Acct Number</span></span> 
- <span data-ttu-id="57f50-3535">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="57f50-3535">Bank Acct #</span></span> 
- <span data-ttu-id="57f50-3536">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="57f50-3536">Bank Acct No.</span></span> 
- <span data-ttu-id="57f50-3537">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="57f50-3537">Bank Account No.</span></span> 
- <span data-ttu-id="57f50-3538">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3538">Savings Account Number</span></span> 
- <span data-ttu-id="57f50-3539">Savings Account</span><span class="sxs-lookup"><span data-stu-id="57f50-3539">Savings Account.</span></span> 
- <span data-ttu-id="57f50-3540">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="57f50-3540">Savings Account #</span></span> 
- <span data-ttu-id="57f50-3541">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3541">Savings Acct Number</span></span> 
- <span data-ttu-id="57f50-3542">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="57f50-3542">Savings Acct #</span></span> 
- <span data-ttu-id="57f50-3543">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="57f50-3543">Savings Acct No.</span></span> 
- <span data-ttu-id="57f50-3544">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="57f50-3544">Savings Account No.</span></span> 
- <span data-ttu-id="57f50-3545">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3545">Debit Account Number</span></span> 
- <span data-ttu-id="57f50-3546">Debit Account</span><span class="sxs-lookup"><span data-stu-id="57f50-3546">Debit Account</span></span> 
- <span data-ttu-id="57f50-3547">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="57f50-3547">Debit Account #</span></span> 
- <span data-ttu-id="57f50-3548">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="57f50-3548">Debit Acct Number</span></span> 
- <span data-ttu-id="57f50-3549">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="57f50-3549">Debit Acct #</span></span> 
- <span data-ttu-id="57f50-3550">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="57f50-3550">Debit Acct No.</span></span> 
- <span data-ttu-id="57f50-3551">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="57f50-3551">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="57f50-3552">US-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-3552">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3553">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3553">Format</span></span>

<span data-ttu-id="57f50-3554">Abhängig vom Bundesstaat</span><span class="sxs-lookup"><span data-stu-id="57f50-3554">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3555">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3555">Pattern</span></span>

<span data-ttu-id="57f50-3556">Abhängig vom Bundesstaat – am Beispiel für New York:</span><span class="sxs-lookup"><span data-stu-id="57f50-3556">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="57f50-3557">Neun Ziffern, die wie DDD DDD DDD formatiert sind, stimmen überein.</span><span class="sxs-lookup"><span data-stu-id="57f50-3557">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="57f50-3558">Neun Ziffern wie ddddddddd werden nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3558">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3559">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3559">Checksum</span></span>

<span data-ttu-id="57f50-3560">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3560">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3561">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3561">Definition</span></span>

<span data-ttu-id="57f50-3562">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3562">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3563">Die Funktion Func_new_york_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3563">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3564">Ein Schlüsselwort aus Keyword_[state_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3564">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="57f50-3565">Ein Schlüsselwort aus Keyword_us_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3565">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="57f50-3566">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3566">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3567">Die Funktion Func_new_york_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3567">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3568">Ein Schlüsselwort aus Keyword_[state_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3568">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="57f50-3569">Ein Schlüsselwort aus Keyword_us_drivers_license_abbreviations wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3569">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="57f50-3570">Es wurde kein Schlüsselwort aus Keyword_us_drivers_license gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3570">No keyword from Keyword_us_drivers_license is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-3571">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3571">Keywords</span></span>

#### <a name="keyword_us_drivers_license_abbreviations"></a><span data-ttu-id="57f50-3572">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="57f50-3572">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="57f50-3573">DL</span><span class="sxs-lookup"><span data-stu-id="57f50-3573">DL</span></span> 
- <span data-ttu-id="57f50-3574">DLS</span><span class="sxs-lookup"><span data-stu-id="57f50-3574">DLS</span></span> 
- <span data-ttu-id="57f50-3575">CDL</span><span class="sxs-lookup"><span data-stu-id="57f50-3575">CDL</span></span> 
- <span data-ttu-id="57f50-3576">CDLS</span><span class="sxs-lookup"><span data-stu-id="57f50-3576">CDLS</span></span> 
- <span data-ttu-id="57f50-3577">ID</span><span class="sxs-lookup"><span data-stu-id="57f50-3577">ID</span></span> 
- <span data-ttu-id="57f50-3578">IDs</span><span class="sxs-lookup"><span data-stu-id="57f50-3578">IDs</span></span> 
- <span data-ttu-id="57f50-3579">DL #</span><span class="sxs-lookup"><span data-stu-id="57f50-3579">DL#</span></span> 
- <span data-ttu-id="57f50-3580">DLS #</span><span class="sxs-lookup"><span data-stu-id="57f50-3580">DLS#</span></span> 
- <span data-ttu-id="57f50-3581">CDL #</span><span class="sxs-lookup"><span data-stu-id="57f50-3581">CDL#</span></span> 
- <span data-ttu-id="57f50-3582">CDLS #</span><span class="sxs-lookup"><span data-stu-id="57f50-3582">CDLS#</span></span> 
- <span data-ttu-id="57f50-3583">ID #</span><span class="sxs-lookup"><span data-stu-id="57f50-3583">ID#</span></span>
- <span data-ttu-id="57f50-3584">IDs #</span><span class="sxs-lookup"><span data-stu-id="57f50-3584">IDs#</span></span> 
- <span data-ttu-id="57f50-3585">ID number</span><span class="sxs-lookup"><span data-stu-id="57f50-3585">ID number</span></span> 
- <span data-ttu-id="57f50-3586">ID numbers</span><span class="sxs-lookup"><span data-stu-id="57f50-3586">ID numbers</span></span> 
- <span data-ttu-id="57f50-3587">LIC</span><span class="sxs-lookup"><span data-stu-id="57f50-3587">LIC</span></span> 
- <span data-ttu-id="57f50-3588">LIC #</span><span class="sxs-lookup"><span data-stu-id="57f50-3588">LIC#</span></span> 

#### <a name="keyword_us_drivers_license"></a><span data-ttu-id="57f50-3589">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="57f50-3589">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="57f50-3590">DriverLic</span><span class="sxs-lookup"><span data-stu-id="57f50-3590">DriverLic</span></span> 
- <span data-ttu-id="57f50-3591">DriverLics</span><span class="sxs-lookup"><span data-stu-id="57f50-3591">DriverLics</span></span> 
- <span data-ttu-id="57f50-3592">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="57f50-3592">DriverLicense</span></span> 
- <span data-ttu-id="57f50-3593">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="57f50-3593">DriverLicenses</span></span> 
- <span data-ttu-id="57f50-3594">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-3594">Driver Lic</span></span> 
- <span data-ttu-id="57f50-3595">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-3595">Driver Lics</span></span> 
- <span data-ttu-id="57f50-3596">Driver License</span><span class="sxs-lookup"><span data-stu-id="57f50-3596">Driver License</span></span> 
- <span data-ttu-id="57f50-3597">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-3597">Driver Licenses</span></span> 
- <span data-ttu-id="57f50-3598">DriversLic</span><span class="sxs-lookup"><span data-stu-id="57f50-3598">DriversLic</span></span> 
- <span data-ttu-id="57f50-3599">DriversLics</span><span class="sxs-lookup"><span data-stu-id="57f50-3599">DriversLics</span></span> 
- <span data-ttu-id="57f50-3600">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="57f50-3600">DriversLicense</span></span> 
- <span data-ttu-id="57f50-3601">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="57f50-3601">DriversLicenses</span></span> 
- <span data-ttu-id="57f50-3602">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-3602">Drivers Lic</span></span> 
- <span data-ttu-id="57f50-3603">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-3603">Drivers Lics</span></span> 
- <span data-ttu-id="57f50-3604">Drivers License</span><span class="sxs-lookup"><span data-stu-id="57f50-3604">Drivers License</span></span> 
- <span data-ttu-id="57f50-3605">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-3605">Drivers Licenses</span></span> 
- <span data-ttu-id="57f50-3606">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-3606">Driver'Lic</span></span> 
- <span data-ttu-id="57f50-3607">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-3607">Driver'Lics</span></span> 
- <span data-ttu-id="57f50-3608">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="57f50-3608">Driver'License</span></span> 
- <span data-ttu-id="57f50-3609">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-3609">Driver'Licenses</span></span> 
- <span data-ttu-id="57f50-3610">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-3610">Driver' Lic</span></span> 
- <span data-ttu-id="57f50-3611">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-3611">Driver' Lics</span></span> 
- <span data-ttu-id="57f50-3612">Driver' License</span><span class="sxs-lookup"><span data-stu-id="57f50-3612">Driver' License</span></span> 
- <span data-ttu-id="57f50-3613">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-3613">Driver' Licenses</span></span>
- <span data-ttu-id="57f50-3614">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="57f50-3614">Driver'sLic</span></span> 
- <span data-ttu-id="57f50-3615">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="57f50-3615">Driver'sLics</span></span> 
- <span data-ttu-id="57f50-3616">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="57f50-3616">Driver'sLicense</span></span> 
- <span data-ttu-id="57f50-3617">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="57f50-3617">Driver'sLicenses</span></span> 
- <span data-ttu-id="57f50-3618">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="57f50-3618">Driver's Lic</span></span> 
- <span data-ttu-id="57f50-3619">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="57f50-3619">Driver's Lics</span></span> 
- <span data-ttu-id="57f50-3620">Driver's License</span><span class="sxs-lookup"><span data-stu-id="57f50-3620">Driver's License</span></span> 
- <span data-ttu-id="57f50-3621">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="57f50-3621">Driver's Licenses</span></span> 
- <span data-ttu-id="57f50-3622">identification number</span><span class="sxs-lookup"><span data-stu-id="57f50-3622">identification number</span></span> 
- <span data-ttu-id="57f50-3623">identification numbers</span><span class="sxs-lookup"><span data-stu-id="57f50-3623">identification numbers</span></span> 
- <span data-ttu-id="57f50-3624">identification#</span><span class="sxs-lookup"><span data-stu-id="57f50-3624">identification #</span></span> 
- <span data-ttu-id="57f50-3625">id card</span><span class="sxs-lookup"><span data-stu-id="57f50-3625">id card</span></span> 
- <span data-ttu-id="57f50-3626">id cards</span><span class="sxs-lookup"><span data-stu-id="57f50-3626">id cards</span></span> 
- <span data-ttu-id="57f50-3627">identification card</span><span class="sxs-lookup"><span data-stu-id="57f50-3627">identification card</span></span> 
- <span data-ttu-id="57f50-3628">identification cards</span><span class="sxs-lookup"><span data-stu-id="57f50-3628">identification cards</span></span> 
- <span data-ttu-id="57f50-3629">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="57f50-3629">DriverLic#</span></span> 
- <span data-ttu-id="57f50-3630">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="57f50-3630">DriverLics#</span></span> 
- <span data-ttu-id="57f50-3631">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="57f50-3631">DriverLicense#</span></span> 
- <span data-ttu-id="57f50-3632">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-3632">DriverLicenses#</span></span> 
- <span data-ttu-id="57f50-3633">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-3633">Driver Lic#</span></span> 
- <span data-ttu-id="57f50-3634">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-3634">Driver Lics#</span></span> 
- <span data-ttu-id="57f50-3635">Driver License#</span><span class="sxs-lookup"><span data-stu-id="57f50-3635">Driver License#</span></span> 
- <span data-ttu-id="57f50-3636">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-3636">Driver Licenses#</span></span> 
- <span data-ttu-id="57f50-3637">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="57f50-3637">DriversLic#</span></span> 
- <span data-ttu-id="57f50-3638">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="57f50-3638">DriversLics#</span></span> 
- <span data-ttu-id="57f50-3639">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="57f50-3639">DriversLicense#</span></span> 
- <span data-ttu-id="57f50-3640">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-3640">DriversLicenses#</span></span> 
- <span data-ttu-id="57f50-3641">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-3641">Drivers Lic#</span></span> 
- <span data-ttu-id="57f50-3642">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-3642">Drivers Lics#</span></span> 
- <span data-ttu-id="57f50-3643">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="57f50-3643">Drivers License#</span></span> 
- <span data-ttu-id="57f50-3644">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-3644">Drivers Licenses#</span></span> 
- <span data-ttu-id="57f50-3645">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="57f50-3645">Driver'Lic#</span></span> 
- <span data-ttu-id="57f50-3646">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="57f50-3646">Driver'Lics#</span></span> 
- <span data-ttu-id="57f50-3647">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="57f50-3647">Driver'License#</span></span> 
- <span data-ttu-id="57f50-3648">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-3648">Driver'Licenses#</span></span> 
- <span data-ttu-id="57f50-3649">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-3649">Driver' Lic#</span></span> 
- <span data-ttu-id="57f50-3650">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-3650">Driver' Lics#</span></span> 
- <span data-ttu-id="57f50-3651">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="57f50-3651">Driver' License#</span></span> 
- <span data-ttu-id="57f50-3652">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-3652">Driver' Licenses#</span></span> 
- <span data-ttu-id="57f50-3653">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="57f50-3653">Driver'sLic#</span></span> 
- <span data-ttu-id="57f50-3654">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="57f50-3654">Driver'sLics#</span></span> 
- <span data-ttu-id="57f50-3655">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="57f50-3655">Driver'sLicense#</span></span> 
- <span data-ttu-id="57f50-3656">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="57f50-3656">Driver'sLicenses#</span></span> 
- <span data-ttu-id="57f50-3657">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="57f50-3657">Driver's Lic#</span></span> 
- <span data-ttu-id="57f50-3658">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="57f50-3658">Driver's Lics#</span></span> 
- <span data-ttu-id="57f50-3659">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="57f50-3659">Driver's License#</span></span> 
- <span data-ttu-id="57f50-3660">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="57f50-3660">Driver's Licenses#</span></span> 
- <span data-ttu-id="57f50-3661">id card#</span><span class="sxs-lookup"><span data-stu-id="57f50-3661">id card#</span></span> 
- <span data-ttu-id="57f50-3662">id cards#</span><span class="sxs-lookup"><span data-stu-id="57f50-3662">id cards#</span></span> 
- <span data-ttu-id="57f50-3663">identification card#</span><span class="sxs-lookup"><span data-stu-id="57f50-3663">identification card#</span></span> 
- <span data-ttu-id="57f50-3664">identification cards#</span><span class="sxs-lookup"><span data-stu-id="57f50-3664">identification cards#</span></span> 


#### <a name="keyword_state_name_drivers_license_name"></a><span data-ttu-id="57f50-3665">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="57f50-3665">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="57f50-3666">Abkürzung für Bundesstaat (z. B. „NY“)</span><span class="sxs-lookup"><span data-stu-id="57f50-3666">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="57f50-3667">Name des Bundesstaats (z. B. „New York“)</span><span class="sxs-lookup"><span data-stu-id="57f50-3667">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="57f50-3668">US-Steueridentifikationsnummer (ITIN)</span><span class="sxs-lookup"><span data-stu-id="57f50-3668">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3669">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3669">Format</span></span>

<span data-ttu-id="57f50-3670">Neun Ziffern, die mit "9" beginnen und "7" oder "8" als vierte Ziffer enthalten, optional mit Leerzeichen oder Bindestrichen formatiert</span><span class="sxs-lookup"><span data-stu-id="57f50-3670">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3671">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3671">Pattern</span></span>

<span data-ttu-id="57f50-3672">Formatiert</span><span class="sxs-lookup"><span data-stu-id="57f50-3672">Formatted:</span></span>
- <span data-ttu-id="57f50-3673">Die Ziffer 9</span><span class="sxs-lookup"><span data-stu-id="57f50-3673">The digit "9"</span></span> 
- <span data-ttu-id="57f50-3674">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3674">Two digits</span></span> 
- <span data-ttu-id="57f50-3675">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-3675">A space or dash</span></span> 
- <span data-ttu-id="57f50-3676">Eine 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="57f50-3676">A "7" or "8"</span></span> 
- <span data-ttu-id="57f50-3677">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="57f50-3677">A digit</span></span> 
- <span data-ttu-id="57f50-3678">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="57f50-3678">A space, or dash</span></span> 
- <span data-ttu-id="57f50-3679">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3679">Four digits</span></span>

<span data-ttu-id="57f50-3680">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="57f50-3680">Unformatted:</span></span>
- <span data-ttu-id="57f50-3681">Die Ziffer 9</span><span class="sxs-lookup"><span data-stu-id="57f50-3681">The digit "9"</span></span> 
- <span data-ttu-id="57f50-3682">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3682">Two digits</span></span> 
- <span data-ttu-id="57f50-3683">Eine 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="57f50-3683">A "7" or "8"</span></span> 
- <span data-ttu-id="57f50-3684">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="57f50-3684">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3685">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3685">Checksum</span></span>

<span data-ttu-id="57f50-3686">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3686">No</span></span>

### <a name="definition"></a><span data-ttu-id="57f50-3687">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3687">Definition</span></span>

<span data-ttu-id="57f50-3688">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3689">Die Funktion Func_formatted_itin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3689">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3690">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="57f50-3690">At least one of the following is true:</span></span>
    - <span data-ttu-id="57f50-3691">Ein Schlüsselwort aus Keyword_itin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3691">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="57f50-3692">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="57f50-3692">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="57f50-3693">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-3693">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="57f50-3694">Ein Schlüsselwort aus Keyword_itin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3694">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="57f50-3695">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3695">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3696">Die Funktion Func_unformatted_itin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3696">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3697">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="57f50-3697">At least one of the following is true:</span></span>
    - <span data-ttu-id="57f50-3698">Ein Schlüsselwort aus Keyword_itin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3698">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="57f50-3699">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="57f50-3699">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="57f50-3700">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-3700">The function Func_us_date finds a date in the right date format.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="57f50-3701">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3701">Keywords</span></span>

#### <a name="keyword_itin"></a><span data-ttu-id="57f50-3702">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="57f50-3702">Keyword_itin</span></span>

- <span data-ttu-id="57f50-3703">Steuer</span><span class="sxs-lookup"><span data-stu-id="57f50-3703">taxpayer</span></span> 
- <span data-ttu-id="57f50-3704">tax id</span><span class="sxs-lookup"><span data-stu-id="57f50-3704">tax id</span></span> 
- <span data-ttu-id="57f50-3705">tax identification</span><span class="sxs-lookup"><span data-stu-id="57f50-3705">tax identification</span></span> 
- <span data-ttu-id="57f50-3706">Itin</span><span class="sxs-lookup"><span data-stu-id="57f50-3706">itin</span></span> 
- <span data-ttu-id="57f50-3707">SSN</span><span class="sxs-lookup"><span data-stu-id="57f50-3707">ssn</span></span> 
- <span data-ttu-id="57f50-3708">Zinn</span><span class="sxs-lookup"><span data-stu-id="57f50-3708">tin</span></span> 
- <span data-ttu-id="57f50-3709">social security</span><span class="sxs-lookup"><span data-stu-id="57f50-3709">social security</span></span> 
- <span data-ttu-id="57f50-3710">tax payer</span><span class="sxs-lookup"><span data-stu-id="57f50-3710">tax payer</span></span> 
- <span data-ttu-id="57f50-3711">itins</span><span class="sxs-lookup"><span data-stu-id="57f50-3711">itins</span></span> 
- <span data-ttu-id="57f50-3712">per Taxi</span><span class="sxs-lookup"><span data-stu-id="57f50-3712">taxid</span></span> 
- <span data-ttu-id="57f50-3713">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="57f50-3713">individual taxpayer</span></span> 

#### <a name="keyword_itin_collaborative"></a><span data-ttu-id="57f50-3714">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="57f50-3714">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="57f50-3715">Lizenz</span><span class="sxs-lookup"><span data-stu-id="57f50-3715">License</span></span> 
- <span data-ttu-id="57f50-3716">DL</span><span class="sxs-lookup"><span data-stu-id="57f50-3716">DL</span></span> 
- <span data-ttu-id="57f50-3717">DOB</span><span class="sxs-lookup"><span data-stu-id="57f50-3717">DOB</span></span> 
- <span data-ttu-id="57f50-3718">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="57f50-3718">Birthdate</span></span> 
- <span data-ttu-id="57f50-3719">Geburtstag</span><span class="sxs-lookup"><span data-stu-id="57f50-3719">Birthday</span></span> 
- <span data-ttu-id="57f50-3720">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="57f50-3720">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="57f50-3721">US-Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="57f50-3721">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="57f50-3722">Format</span><span class="sxs-lookup"><span data-stu-id="57f50-3722">Format</span></span>

<span data-ttu-id="57f50-3723">9 Ziffern in formatiertem oder unformatiertem Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3723">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="57f50-3724">Wenn ein SSN vor Mitte 2011 ausgegeben wird, weist es eine starke Formatierung auf, bei der bestimmte Teile der Zahl in bestimmte Bereiche fallen müssen, um gültig zu sein (aber keine Prüfsumme).</span><span class="sxs-lookup"><span data-stu-id="57f50-3724">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="57f50-3725">Muster</span><span class="sxs-lookup"><span data-stu-id="57f50-3725">Pattern</span></span>

<span data-ttu-id="57f50-3726">Vier Funktionen suchen nach Sozialversicherungsnummern in vier verschiedenen Mustern:</span><span class="sxs-lookup"><span data-stu-id="57f50-3726">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="57f50-3727">Func_ssn findet Sozialversicherungsnummern mit starker Formatierung vor 2011, die mit Bindestrichen oder Leerzeichen formatiert sind (DDD-DD-dddd oder DDD DD dddd)</span><span class="sxs-lookup"><span data-stu-id="57f50-3727">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="57f50-3728">Func_unformatted_ssn findet Sozialversicherungsnummern mit starker Formatierung vor 2011, die als neun aufeinanderfolgende Ziffern (ddddddddd) unformatiert sind.</span><span class="sxs-lookup"><span data-stu-id="57f50-3728">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="57f50-3729">Func_randomized_formatted_ssn findet Post-2011-Sozialversicherungsnummern, die mit Bindestrichen oder Leerzeichen formatiert sind (DDD-DD-dddd oder DDD DD dddd)</span><span class="sxs-lookup"><span data-stu-id="57f50-3729">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="57f50-3730">Func_randomized_unformatted_ssn findet Post-2011-Sozialversicherungsnummern, die als neun aufeinanderfolgende Ziffern (ddddddddd) unformatiert sind.</span><span class="sxs-lookup"><span data-stu-id="57f50-3730">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="57f50-3731">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="57f50-3731">Checksum</span></span>

<span data-ttu-id="57f50-3732">Nein</span><span class="sxs-lookup"><span data-stu-id="57f50-3732">No</span></span>


### <a name="definition"></a><span data-ttu-id="57f50-3733">Definition</span><span class="sxs-lookup"><span data-stu-id="57f50-3733">Definition</span></span>

<span data-ttu-id="57f50-3734">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3735">Die Funktion Func_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3735">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3736">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3736">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="57f50-3737">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-3737">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="57f50-3738">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="57f50-3738">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="57f50-3739">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3739">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3740">Die Funktion Func_unformatted_ssn findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3740">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3741">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3741">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="57f50-3742">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-3742">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="57f50-3743">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="57f50-3743">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="57f50-3744">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3744">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3745">Die Funktion Func_randomized_formatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3745">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3746">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3746">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="57f50-3747">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-3747">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="57f50-3748">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="57f50-3748">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="57f50-3749">Eine DLP-Richtlinie ist zu 55 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="57f50-3749">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3750">Die Funktion Func_randomized_unformatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3750">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3751">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3751">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="57f50-3752">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="57f50-3752">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="57f50-3753">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="57f50-3753">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="57f50-3754">Eine DLP-Richtlinie ist 40% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Sie in einer Nähe von 300 Zeichen:</span><span class="sxs-lookup"><span data-stu-id="57f50-3754">A DLP policy is 40% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="57f50-3755">Die Funktion Func_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3755">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3756">Die Funktion Func_unformatted_ssn findet keine Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3756">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3757">Die Funktion Func_randomized_unformatted_ssn findet keine Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3757">The function Func_randomized_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3758">Ein Schlüsselwort aus Keyword_ssn wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3758">A keyword from Keyword_ssn is not found.</span></span>
 
<span data-ttu-id="57f50-3759">Oder</span><span class="sxs-lookup"><span data-stu-id="57f50-3759">Or</span></span>

- <span data-ttu-id="57f50-3760">Die Funktion Func_randomized_formatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3760">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3761">Die Funktion Func_unformatted_ssn findet keine Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3761">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3762">Die Funktion Func_randomized_unformatted_ssn findet keine Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="57f50-3762">The function Func_randomized_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="57f50-3763">Ein Schlüsselwort aus Keyword_ssn wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="57f50-3763">A keyword from Keyword_ssn is not found.</span></span>

```xml
<!-- U.S. Social Security Number (SSN) -->
  <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Any minMatches="1">
          <Match idRef="Keyword_ssn" />
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="1">
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Any minMatches="1">
          <Match idRef="Keyword_ssn" />
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="1">
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="40">
        <IdMatch idRef="Func_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
          <Match idRef="Func_randomized_unformatted_ssn" />
          <Match idRef="Keyword_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="40">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
          <Match idRef="Func_randomized_unformatted_ssn" />
          <Match idRef="Keyword_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="57f50-3764">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="57f50-3764">Keywords</span></span>

#### <a name="keyword_ssn"></a><span data-ttu-id="57f50-3765">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="57f50-3765">Keyword_ssn</span></span>

- <span data-ttu-id="57f50-3766">Social Security</span><span class="sxs-lookup"><span data-stu-id="57f50-3766">Social Security</span></span> 
- <span data-ttu-id="57f50-3767">Social Security#</span><span class="sxs-lookup"><span data-stu-id="57f50-3767">Social Security#</span></span> 
- <span data-ttu-id="57f50-3768">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="57f50-3768">Soc Sec</span></span> 
- <span data-ttu-id="57f50-3769">SSN</span><span class="sxs-lookup"><span data-stu-id="57f50-3769">SSN</span></span> 
- <span data-ttu-id="57f50-3770">Sozialversicherungsnummern</span><span class="sxs-lookup"><span data-stu-id="57f50-3770">SSNS</span></span> 
- <span data-ttu-id="57f50-3771">SSN #</span><span class="sxs-lookup"><span data-stu-id="57f50-3771">SSN#</span></span> 
- <span data-ttu-id="57f50-3772">SS #</span><span class="sxs-lookup"><span data-stu-id="57f50-3772">SS#</span></span> 
- <span data-ttu-id="57f50-3773">SSID</span><span class="sxs-lookup"><span data-stu-id="57f50-3773">SSID</span></span> 
   

