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
ms.openlocfilehash: 55fa8b6855a9a5bf2c84f6555dd8c8227a2ad9cf
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455267"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="62380-104">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="62380-104">What the sensitive information types look for</span></span>

<span data-ttu-id="62380-105">Data Loss Prevention (DLP) im Office 365 Security &amp; Compliance Center enthält viele vertrauliche Informationstypen, die Sie in ihren DLP-Richtlinien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="62380-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="62380-106">Dieses Thema enthält eine Liste aller dieser vertraulichen Informationstypen und zeigt, was eine DLP-Richtlinie sucht, wenn sie den jeweiligen Typen erkennt.</span><span class="sxs-lookup"><span data-stu-id="62380-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="62380-107">Ein vertraulicher Informationstyp wird durch ein Muster definiert, das durch einen regulären Ausdruck oder eine Funktion identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="62380-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="62380-108">Darüber hinaus können auch belegende Hinweise wie Schlüsselwörter oder Prüfsummen zum Identifizieren eines Typs vertraulicher Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62380-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="62380-109">Beim Auswertungsprozess können auch die Zuverlässigkeitsstufe und die Näherung herangezogen werden.</span><span class="sxs-lookup"><span data-stu-id="62380-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="62380-110">ABA Routing Number (US-Bankleitzahl)</span><span class="sxs-lookup"><span data-stu-id="62380-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-111">Format</span><span class="sxs-lookup"><span data-stu-id="62380-111">Format</span></span>

<span data-ttu-id="62380-112">9 Ziffern in formatiertem oder unformatiertem Muster</span><span class="sxs-lookup"><span data-stu-id="62380-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-113">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-113">Pattern</span></span>

<span data-ttu-id="62380-114">Formatiert</span><span class="sxs-lookup"><span data-stu-id="62380-114">Formatted:</span></span>
- <span data-ttu-id="62380-115">Vier Ziffern, beginnend mit 0, 1, 2, 3, 6, 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="62380-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="62380-116">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-116">A hyphen</span></span>
- <span data-ttu-id="62380-117">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-117">Four digits</span></span>
- <span data-ttu-id="62380-118">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-118">A hyphen</span></span>
- <span data-ttu-id="62380-119">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="62380-119">A digit</span></span>

<span data-ttu-id="62380-120">Unformatiert: 9 aufeinanderfolgende Ziffern beginnend mit 0, 1, 2, 3, 6, 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="62380-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="62380-121">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-121">Checksum</span></span>

<span data-ttu-id="62380-122">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-123">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-123">Definition</span></span>

<span data-ttu-id="62380-124">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-125">Die Funktion Func_aba_routing findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-126">Ein Schlüsselwort aus Keyword_ABA_Routing wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="62380-127">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="62380-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="62380-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="62380-129">ABA</span><span class="sxs-lookup"><span data-stu-id="62380-129">aba</span></span>
- <span data-ttu-id="62380-130">aba #</span><span class="sxs-lookup"><span data-stu-id="62380-130">aba #</span></span>
- <span data-ttu-id="62380-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="62380-131">aba routing #</span></span>
- <span data-ttu-id="62380-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="62380-132">aba routing number</span></span>
- <span data-ttu-id="62380-133">ABA</span><span class="sxs-lookup"><span data-stu-id="62380-133">aba#</span></span>
- <span data-ttu-id="62380-134">abarouting #</span><span class="sxs-lookup"><span data-stu-id="62380-134">abarouting#</span></span>
- <span data-ttu-id="62380-135">aba number</span><span class="sxs-lookup"><span data-stu-id="62380-135">aba number</span></span>
- <span data-ttu-id="62380-136">abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="62380-136">abaroutingnumber</span></span>
- <span data-ttu-id="62380-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="62380-137">american bank association routing #</span></span>
- <span data-ttu-id="62380-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="62380-138">american bank association routing number</span></span>
- <span data-ttu-id="62380-139">americanbankassociationrouting #</span><span class="sxs-lookup"><span data-stu-id="62380-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="62380-140">americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="62380-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="62380-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="62380-141">bank routing number</span></span>
- <span data-ttu-id="62380-142">bankrouting #</span><span class="sxs-lookup"><span data-stu-id="62380-142">bankrouting#</span></span>
- <span data-ttu-id="62380-143">bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="62380-143">bankroutingnumber</span></span>
- <span data-ttu-id="62380-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="62380-144">routing transit number</span></span>
- <span data-ttu-id="62380-145">RTN</span><span class="sxs-lookup"><span data-stu-id="62380-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="62380-146">Argentina National Identity (DNI) Number</span><span class="sxs-lookup"><span data-stu-id="62380-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-147">Format</span><span class="sxs-lookup"><span data-stu-id="62380-147">Format</span></span>

<span data-ttu-id="62380-148">Acht Ziffern, durch Punkte getrennt</span><span class="sxs-lookup"><span data-stu-id="62380-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-149">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-149">Pattern</span></span>

<span data-ttu-id="62380-150">Acht Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-150">Eight digits:</span></span>
- <span data-ttu-id="62380-151">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-151">Two digits</span></span>
- <span data-ttu-id="62380-152">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="62380-152">A period</span></span>
- <span data-ttu-id="62380-153">Drei Ziffern </span><span class="sxs-lookup"><span data-stu-id="62380-153">Three digits</span></span>
- <span data-ttu-id="62380-154">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="62380-154">A period</span></span>
- <span data-ttu-id="62380-155">Drei Ziffern </span><span class="sxs-lookup"><span data-stu-id="62380-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-156">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-156">Checksum</span></span>

<span data-ttu-id="62380-157">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-158">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-158">Definition</span></span>

<span data-ttu-id="62380-159">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-160">Der reguläre Ausdruck Regex_argentina_national_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-161">Ein Schlüsselwort aus Keyword_argentina_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-162">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="62380-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="62380-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="62380-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="62380-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="62380-165">Identität</span><span class="sxs-lookup"><span data-stu-id="62380-165">Identity</span></span> 
- <span data-ttu-id="62380-166">Identifizierung nationaler Identitätsausweis</span><span class="sxs-lookup"><span data-stu-id="62380-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="62380-167">DNI</span><span class="sxs-lookup"><span data-stu-id="62380-167">DNI</span></span> 
- <span data-ttu-id="62380-168">NIC National Registry of persons</span><span class="sxs-lookup"><span data-stu-id="62380-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="62380-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="62380-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="62380-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="62380-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="62380-171">Identidad</span><span class="sxs-lookup"><span data-stu-id="62380-171">Identidad</span></span> 
- <span data-ttu-id="62380-172">Identificación</span><span class="sxs-lookup"><span data-stu-id="62380-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="62380-173">Australische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="62380-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-174">Format</span><span class="sxs-lookup"><span data-stu-id="62380-174">Format</span></span>

<span data-ttu-id="62380-175">6-10 Stellen mit oder ohne Bankfilialnummer</span><span class="sxs-lookup"><span data-stu-id="62380-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-176">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-176">Pattern</span></span>

<span data-ttu-id="62380-177">Kontonummer hat 6-10 Stellen.</span><span class="sxs-lookup"><span data-stu-id="62380-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="62380-178">Australische Bankleitzahl:</span><span class="sxs-lookup"><span data-stu-id="62380-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="62380-179">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-179">Three digits</span></span> 
- <span data-ttu-id="62380-180">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-180">A hyphen</span></span> 
- <span data-ttu-id="62380-181">Drei Stellen</span><span class="sxs-lookup"><span data-stu-id="62380-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-182">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-182">Checksum</span></span>

<span data-ttu-id="62380-183">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-184">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-184">Definition</span></span>

<span data-ttu-id="62380-185">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-186">Der reguläre Ausdruck Regex_australia_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="62380-187">Ein Schlüsselwort aus Keyword_australia_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="62380-188">Der reguläre Ausdruck Regex_australia_bank_account_number_bsb findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="62380-189">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-190">Der reguläre Ausdruck Regex_australia_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="62380-191">Ein Schlüsselwort aus Keyword_australia_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-192">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="62380-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="62380-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="62380-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="62380-194">swift bank code</span></span>
- <span data-ttu-id="62380-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="62380-195">correspondent bank</span></span>
- <span data-ttu-id="62380-196">base currency</span><span class="sxs-lookup"><span data-stu-id="62380-196">base currency</span></span>
- <span data-ttu-id="62380-197">usa account</span><span class="sxs-lookup"><span data-stu-id="62380-197">usa account</span></span>
- <span data-ttu-id="62380-198">holder address</span><span class="sxs-lookup"><span data-stu-id="62380-198">holder address</span></span>
- <span data-ttu-id="62380-199">bank address</span><span class="sxs-lookup"><span data-stu-id="62380-199">bank address</span></span>
- <span data-ttu-id="62380-200">information account</span><span class="sxs-lookup"><span data-stu-id="62380-200">information account</span></span>
- <span data-ttu-id="62380-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="62380-201">fund transfers</span></span>
- <span data-ttu-id="62380-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="62380-202">bank charges</span></span>
- <span data-ttu-id="62380-203">bank details</span><span class="sxs-lookup"><span data-stu-id="62380-203">bank details</span></span>
- <span data-ttu-id="62380-204">banking information</span><span class="sxs-lookup"><span data-stu-id="62380-204">banking information</span></span>
- <span data-ttu-id="62380-205">full names</span><span class="sxs-lookup"><span data-stu-id="62380-205">full names</span></span>
- <span data-ttu-id="62380-206">IAEO</span><span class="sxs-lookup"><span data-stu-id="62380-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="62380-207">Australische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-208">Format</span><span class="sxs-lookup"><span data-stu-id="62380-208">Format</span></span>

<span data-ttu-id="62380-209">Neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-210">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-210">Pattern</span></span>

<span data-ttu-id="62380-211">Neun Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="62380-212">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="62380-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="62380-213">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-213">Two digits</span></span> 
- <span data-ttu-id="62380-214">Fünf Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="62380-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="62380-215">ODER</span><span class="sxs-lookup"><span data-stu-id="62380-215">OR</span></span>

- <span data-ttu-id="62380-216">1-2 optionale Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="62380-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="62380-217">4 bis 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-217">4-9 digits</span></span>

<span data-ttu-id="62380-218">ODER</span><span class="sxs-lookup"><span data-stu-id="62380-218">OR</span></span>

- <span data-ttu-id="62380-219">Neun Ziffern oder Buchstaben (Groß-/Kleinschreibung irrelevant)</span><span class="sxs-lookup"><span data-stu-id="62380-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-220">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-220">Checksum</span></span>

<span data-ttu-id="62380-221">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-222">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-222">Definition</span></span>

<span data-ttu-id="62380-223">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-224">Der reguläre Ausdruck Regex_australia_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-225">Ein Schlüsselwort aus Keyword_australia_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="62380-226">Es wurde kein Schlüsselwort aus Keyword_australia_drivers_license_number_exclusions gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-227">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="62380-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="62380-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="62380-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="62380-229">international driving permits</span></span>
- <span data-ttu-id="62380-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="62380-230">australian automobile association</span></span>
- <span data-ttu-id="62380-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="62380-231">international driving permit</span></span>
- <span data-ttu-id="62380-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="62380-232">DriverLicence</span></span>
- <span data-ttu-id="62380-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="62380-233">DriverLicences</span></span>
- <span data-ttu-id="62380-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="62380-234">Driver Lic</span></span>
- <span data-ttu-id="62380-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="62380-235">Driver Licence</span></span>
- <span data-ttu-id="62380-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="62380-236">Driver Licences</span></span>
- <span data-ttu-id="62380-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="62380-237">DriversLic</span></span>
- <span data-ttu-id="62380-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="62380-238">DriversLicence</span></span>
- <span data-ttu-id="62380-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="62380-239">DriversLicences</span></span>
- <span data-ttu-id="62380-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="62380-240">Drivers Lic</span></span>
- <span data-ttu-id="62380-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="62380-241">Drivers Lics</span></span>
- <span data-ttu-id="62380-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="62380-242">Drivers Licence</span></span>
- <span data-ttu-id="62380-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="62380-243">Drivers Licences</span></span>
- <span data-ttu-id="62380-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="62380-244">Driver'Lic</span></span>
- <span data-ttu-id="62380-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="62380-245">Driver'Lics</span></span>
- <span data-ttu-id="62380-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="62380-246">Driver'Licence</span></span>
- <span data-ttu-id="62380-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="62380-247">Driver'Licences</span></span>
- <span data-ttu-id="62380-248">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="62380-248">Driver' Lic</span></span>
- <span data-ttu-id="62380-249">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="62380-249">Driver' Lics</span></span>
- <span data-ttu-id="62380-250">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="62380-250">Driver' Licence</span></span>
- <span data-ttu-id="62380-251">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="62380-251">Driver' Licences</span></span>
- <span data-ttu-id="62380-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="62380-252">Driver'sLic</span></span>
- <span data-ttu-id="62380-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="62380-253">Driver'sLics</span></span>
- <span data-ttu-id="62380-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="62380-254">Driver'sLicence</span></span>
- <span data-ttu-id="62380-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="62380-255">Driver'sLicences</span></span>
- <span data-ttu-id="62380-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="62380-256">Driver's Lic</span></span>
- <span data-ttu-id="62380-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="62380-257">Driver's Lics</span></span>
- <span data-ttu-id="62380-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="62380-258">Driver's Licence</span></span>
- <span data-ttu-id="62380-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="62380-259">Driver's Licences</span></span>
- <span data-ttu-id="62380-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="62380-260">DriverLic#</span></span>
- <span data-ttu-id="62380-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="62380-261">DriverLics#</span></span>
- <span data-ttu-id="62380-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="62380-262">DriverLicence#</span></span>
- <span data-ttu-id="62380-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="62380-263">DriverLicences#</span></span>
- <span data-ttu-id="62380-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-264">Driver Lic#</span></span>
- <span data-ttu-id="62380-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-265">Driver Lics#</span></span>
- <span data-ttu-id="62380-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="62380-266">Driver Licence#</span></span>
- <span data-ttu-id="62380-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="62380-267">Driver Licences#</span></span>
- <span data-ttu-id="62380-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="62380-268">DriversLic#</span></span>
- <span data-ttu-id="62380-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="62380-269">DriversLics#</span></span>
- <span data-ttu-id="62380-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="62380-270">DriversLicence#</span></span>
- <span data-ttu-id="62380-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="62380-271">DriversLicences#</span></span>
- <span data-ttu-id="62380-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-272">Drivers Lic#</span></span>
- <span data-ttu-id="62380-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-273">Drivers Lics#</span></span>
- <span data-ttu-id="62380-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="62380-274">Drivers Licence#</span></span>
- <span data-ttu-id="62380-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="62380-275">Drivers Licences#</span></span>
- <span data-ttu-id="62380-276">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="62380-276">Driver'Lic#</span></span>
- <span data-ttu-id="62380-277">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="62380-277">Driver'Lics#</span></span>
- <span data-ttu-id="62380-278">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="62380-278">Driver'Licence#</span></span>
- <span data-ttu-id="62380-279">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="62380-279">Driver'Licences#</span></span>
- <span data-ttu-id="62380-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-280">Driver' Lic#</span></span>
- <span data-ttu-id="62380-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-281">Driver' Lics#</span></span>
- <span data-ttu-id="62380-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="62380-282">Driver' Licence#</span></span>
- <span data-ttu-id="62380-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="62380-283">Driver' Licences#</span></span>
- <span data-ttu-id="62380-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="62380-284">Driver'sLic#</span></span>
- <span data-ttu-id="62380-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="62380-285">Driver'sLics#</span></span>
- <span data-ttu-id="62380-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="62380-286">Driver'sLicence#</span></span>
- <span data-ttu-id="62380-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="62380-287">Driver'sLicences#</span></span>
- <span data-ttu-id="62380-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-288">Driver's Lic#</span></span>
- <span data-ttu-id="62380-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-289">Driver's Lics#</span></span>
- <span data-ttu-id="62380-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="62380-290">Driver's Licence#</span></span>
- <span data-ttu-id="62380-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="62380-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="62380-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="62380-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="62380-293">aaa</span><span class="sxs-lookup"><span data-stu-id="62380-293">aaa</span></span>
- <span data-ttu-id="62380-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="62380-294">DriverLicense</span></span>
- <span data-ttu-id="62380-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="62380-295">DriverLicenses</span></span>
- <span data-ttu-id="62380-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="62380-296">Driver License</span></span>
- <span data-ttu-id="62380-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-297">Driver Licenses</span></span>
- <span data-ttu-id="62380-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="62380-298">DriversLicense</span></span>
- <span data-ttu-id="62380-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="62380-299">DriversLicenses</span></span>
- <span data-ttu-id="62380-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="62380-300">Drivers License</span></span>
- <span data-ttu-id="62380-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-301">Drivers Licenses</span></span>
- <span data-ttu-id="62380-302">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="62380-302">Driver'License</span></span>
- <span data-ttu-id="62380-303">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-303">Driver'Licenses</span></span>
- <span data-ttu-id="62380-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="62380-304">Driver' License</span></span>
- <span data-ttu-id="62380-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-305">Driver' Licenses</span></span>
- <span data-ttu-id="62380-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="62380-306">Driver'sLicense</span></span>
- <span data-ttu-id="62380-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="62380-307">Driver'sLicenses</span></span>
- <span data-ttu-id="62380-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="62380-308">Driver's License</span></span>
- <span data-ttu-id="62380-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-309">Driver's Licenses</span></span>
- <span data-ttu-id="62380-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="62380-310">DriverLicense#</span></span>
- <span data-ttu-id="62380-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="62380-311">DriverLicenses#</span></span>
- <span data-ttu-id="62380-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="62380-312">Driver License#</span></span>
- <span data-ttu-id="62380-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-313">Driver Licenses#</span></span>
- <span data-ttu-id="62380-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="62380-314">DriversLicense#</span></span>
- <span data-ttu-id="62380-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="62380-315">DriversLicenses#</span></span>
- <span data-ttu-id="62380-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="62380-316">Drivers License#</span></span>
- <span data-ttu-id="62380-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-317">Drivers Licenses#</span></span>
- <span data-ttu-id="62380-318">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="62380-318">Driver'License#</span></span>
- <span data-ttu-id="62380-319">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-319">Driver'Licenses#</span></span>
- <span data-ttu-id="62380-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="62380-320">Driver' License#</span></span>
- <span data-ttu-id="62380-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-321">Driver' Licenses#</span></span>
- <span data-ttu-id="62380-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="62380-322">Driver'sLicense#</span></span>
- <span data-ttu-id="62380-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="62380-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="62380-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="62380-324">Driver's License#</span></span>
- <span data-ttu-id="62380-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="62380-326">Australische Medical Account-Nummer</span><span class="sxs-lookup"><span data-stu-id="62380-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-327">Format</span><span class="sxs-lookup"><span data-stu-id="62380-327">Format</span></span>

<span data-ttu-id="62380-328">10-11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-329">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-329">Pattern</span></span>

<span data-ttu-id="62380-330">10-11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-330">10-11 digits:</span></span>
- <span data-ttu-id="62380-331">Erste Ziffer im Bereich von 2-6</span><span class="sxs-lookup"><span data-stu-id="62380-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="62380-332">Neunte Ziffer ist eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="62380-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="62380-333">Zehnte Ziffer ist die Ausgabeziffer</span><span class="sxs-lookup"><span data-stu-id="62380-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="62380-334">Elfte Ziffer (optional) ist die Einzelziffer</span><span class="sxs-lookup"><span data-stu-id="62380-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-335">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-335">Checksum</span></span>

<span data-ttu-id="62380-336">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-337">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-337">Definition</span></span>

<span data-ttu-id="62380-338">Eine DLP-Richtlinie ist zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-339">Die Funktion Func_australian_medical_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-340">Ein Schlüsselwort aus Keyword_Australia_Medical_Account_Number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="62380-341">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-341">The checksum passes.</span></span>

<span data-ttu-id="62380-342">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-343">Die Funktion Func_australian_medical_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-344">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-345">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="62380-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="62380-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="62380-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="62380-347">bank account details</span></span>
- <span data-ttu-id="62380-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="62380-348">medicare payments</span></span>
- <span data-ttu-id="62380-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="62380-349">mortgage account</span></span>
- <span data-ttu-id="62380-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="62380-350">bank payments</span></span>
- <span data-ttu-id="62380-351">information branch</span><span class="sxs-lookup"><span data-stu-id="62380-351">information branch</span></span>
- <span data-ttu-id="62380-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="62380-352">credit card loan</span></span>
- <span data-ttu-id="62380-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="62380-353">department of human services</span></span>
- <span data-ttu-id="62380-354">local service</span><span class="sxs-lookup"><span data-stu-id="62380-354">local service</span></span>
- <span data-ttu-id="62380-355">Medicare</span><span class="sxs-lookup"><span data-stu-id="62380-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="62380-356">Australische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="62380-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-357">Format</span><span class="sxs-lookup"><span data-stu-id="62380-357">Format</span></span>

<span data-ttu-id="62380-358">Ein Buchstabe gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-359">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-359">Pattern</span></span>

<span data-ttu-id="62380-360">Ein Buchstabe (Groß-/Kleinschreibung irrelevant) gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-361">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-361">Checksum</span></span>

<span data-ttu-id="62380-362">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-363">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-363">Definition</span></span>

<span data-ttu-id="62380-364">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-365">Der reguläre Ausdruck Regex_australia_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-366">Ein Schlüsselwort aus Keyword_passport oder Keyword_australia_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-367">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="62380-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="62380-368">Keyword_passport</span></span>

- <span data-ttu-id="62380-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="62380-369">Passport Number</span></span>
- <span data-ttu-id="62380-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="62380-370">Passport No</span></span>
- <span data-ttu-id="62380-371">Passport#</span><span class="sxs-lookup"><span data-stu-id="62380-371">Passport #</span></span>
- <span data-ttu-id="62380-372">Pass</span><span class="sxs-lookup"><span data-stu-id="62380-372">Passport#</span></span>
- <span data-ttu-id="62380-373">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="62380-373">PassportID</span></span>
- <span data-ttu-id="62380-374">Passportno</span><span class="sxs-lookup"><span data-stu-id="62380-374">Passportno</span></span>
- <span data-ttu-id="62380-375">passportnumber</span><span class="sxs-lookup"><span data-stu-id="62380-375">passportnumber</span></span>
- <span data-ttu-id="62380-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="62380-376">パスポート</span></span>
- <span data-ttu-id="62380-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="62380-377">パスポート番号</span></span>
- <span data-ttu-id="62380-378">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="62380-378">パスポートのNum</span></span>
- <span data-ttu-id="62380-379">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="62380-379">パスポート ＃</span></span> 
- <span data-ttu-id="62380-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="62380-380">Numéro de passeport</span></span>
- <span data-ttu-id="62380-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="62380-381">Passeport n °</span></span>
- <span data-ttu-id="62380-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="62380-382">Passeport Non</span></span>
- <span data-ttu-id="62380-383">Passeport#</span><span class="sxs-lookup"><span data-stu-id="62380-383">Passeport #</span></span>
- <span data-ttu-id="62380-384">Passeport</span><span class="sxs-lookup"><span data-stu-id="62380-384">Passeport#</span></span>
- <span data-ttu-id="62380-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="62380-385">PasseportNon</span></span>
- <span data-ttu-id="62380-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="62380-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="62380-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="62380-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="62380-388">Pass</span><span class="sxs-lookup"><span data-stu-id="62380-388">passport</span></span>
- <span data-ttu-id="62380-389">passport details</span><span class="sxs-lookup"><span data-stu-id="62380-389">passport details</span></span>
- <span data-ttu-id="62380-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="62380-390">immigration and citizenship</span></span>
- <span data-ttu-id="62380-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="62380-391">commonwealth of australia</span></span>
- <span data-ttu-id="62380-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="62380-392">department of immigration</span></span>
- <span data-ttu-id="62380-393">residential address</span><span class="sxs-lookup"><span data-stu-id="62380-393">residential address</span></span>
- <span data-ttu-id="62380-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="62380-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="62380-395">Visa</span><span class="sxs-lookup"><span data-stu-id="62380-395">visa</span></span>
- <span data-ttu-id="62380-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="62380-396">national identity card</span></span>
- <span data-ttu-id="62380-397">passport number</span><span class="sxs-lookup"><span data-stu-id="62380-397">passport number</span></span>
- <span data-ttu-id="62380-398">travel document</span><span class="sxs-lookup"><span data-stu-id="62380-398">travel document</span></span>
- <span data-ttu-id="62380-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="62380-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="62380-400">Australische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="62380-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-401">Format</span><span class="sxs-lookup"><span data-stu-id="62380-401">Format</span></span>

<span data-ttu-id="62380-402">8-9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-403">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-403">Pattern</span></span>

<span data-ttu-id="62380-404">8 bis 9 Ziffern, die in der Regel wie folgt mit Leerzeichen dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="62380-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="62380-405">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-405">Three digits</span></span> 
- <span data-ttu-id="62380-406">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-406">An optional space</span></span> 
- <span data-ttu-id="62380-407">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-407">Three digits</span></span> 
- <span data-ttu-id="62380-408">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-408">An optional space</span></span> 
- <span data-ttu-id="62380-409">2 bis 3 Ziffern, wobei die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="62380-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-410">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-410">Checksum</span></span>

<span data-ttu-id="62380-411">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-412">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-412">Definition</span></span>

<span data-ttu-id="62380-413">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-414">Die Funktion Func_australian_tax_file_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-415">Es wurde kein Schlüsselwort aus Keyword_Australia_Tax_File_Number oder Keyword_number_exclusions gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="62380-416">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-416">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-417">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="62380-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="62380-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="62380-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="62380-419">australian business number</span></span>
- <span data-ttu-id="62380-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="62380-420">marginal tax rate</span></span>
- <span data-ttu-id="62380-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="62380-421">medicare levy</span></span>
- <span data-ttu-id="62380-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="62380-422">portfolio number</span></span>
- <span data-ttu-id="62380-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="62380-423">service veterans</span></span>
- <span data-ttu-id="62380-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="62380-424">withholding tax</span></span>
- <span data-ttu-id="62380-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="62380-425">individual tax return</span></span>
- <span data-ttu-id="62380-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="62380-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="62380-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="62380-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="62380-428">00000000</span><span class="sxs-lookup"><span data-stu-id="62380-428">00000000</span></span>
- <span data-ttu-id="62380-429">11111111</span><span class="sxs-lookup"><span data-stu-id="62380-429">11111111</span></span>
- <span data-ttu-id="62380-430">22222222</span><span class="sxs-lookup"><span data-stu-id="62380-430">22222222</span></span>
- <span data-ttu-id="62380-431">33333333</span><span class="sxs-lookup"><span data-stu-id="62380-431">33333333</span></span>
- <span data-ttu-id="62380-432">44444444</span><span class="sxs-lookup"><span data-stu-id="62380-432">44444444</span></span>
- <span data-ttu-id="62380-433">55555555</span><span class="sxs-lookup"><span data-stu-id="62380-433">55555555</span></span>
- <span data-ttu-id="62380-434">66666666</span><span class="sxs-lookup"><span data-stu-id="62380-434">66666666</span></span>
- <span data-ttu-id="62380-435">77777777</span><span class="sxs-lookup"><span data-stu-id="62380-435">77777777</span></span>
- <span data-ttu-id="62380-436">88888888</span><span class="sxs-lookup"><span data-stu-id="62380-436">88888888</span></span>
- <span data-ttu-id="62380-437">99999999</span><span class="sxs-lookup"><span data-stu-id="62380-437">99999999</span></span>
- <span data-ttu-id="62380-438">000000000</span><span class="sxs-lookup"><span data-stu-id="62380-438">000000000</span></span>
- <span data-ttu-id="62380-439">111111111</span><span class="sxs-lookup"><span data-stu-id="62380-439">111111111</span></span>
- <span data-ttu-id="62380-440">222222222</span><span class="sxs-lookup"><span data-stu-id="62380-440">222222222</span></span>
- <span data-ttu-id="62380-441">333333333</span><span class="sxs-lookup"><span data-stu-id="62380-441">333333333</span></span>
- <span data-ttu-id="62380-442">444444444</span><span class="sxs-lookup"><span data-stu-id="62380-442">444444444</span></span>
- <span data-ttu-id="62380-443">555555555</span><span class="sxs-lookup"><span data-stu-id="62380-443">555555555</span></span>
- <span data-ttu-id="62380-444">666666666</span><span class="sxs-lookup"><span data-stu-id="62380-444">666666666</span></span>
- <span data-ttu-id="62380-445">777777777</span><span class="sxs-lookup"><span data-stu-id="62380-445">777777777</span></span>
- <span data-ttu-id="62380-446">888888888</span><span class="sxs-lookup"><span data-stu-id="62380-446">888888888</span></span>
- <span data-ttu-id="62380-447">999999999</span><span class="sxs-lookup"><span data-stu-id="62380-447">999999999</span></span>
- <span data-ttu-id="62380-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="62380-448">0000000000</span></span>
- <span data-ttu-id="62380-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="62380-449">1111111111</span></span>
- <span data-ttu-id="62380-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="62380-450">2222222222</span></span>
- <span data-ttu-id="62380-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="62380-451">3333333333</span></span>
- <span data-ttu-id="62380-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="62380-452">4444444444</span></span>
- <span data-ttu-id="62380-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="62380-453">5555555555</span></span>
- <span data-ttu-id="62380-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="62380-454">6666666666</span></span>
- <span data-ttu-id="62380-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="62380-455">7777777777</span></span>
- <span data-ttu-id="62380-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="62380-456">8888888888</span></span>
- <span data-ttu-id="62380-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="62380-457">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="62380-458">Belgien – Nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="62380-458">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-459">Format</span><span class="sxs-lookup"><span data-stu-id="62380-459">Format</span></span>

<span data-ttu-id="62380-460">11 Ziffern plus Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-460">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-461">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-461">Pattern</span></span>

<span data-ttu-id="62380-462">11 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="62380-462">11 digits plus delimiters:</span></span>
- <span data-ttu-id="62380-463">Sechs Ziffern und zwei Punkte im Format JJ.MM.TT für das Geburtsdatum </span><span class="sxs-lookup"><span data-stu-id="62380-463">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="62380-464">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-464">A hyphen</span></span> 
- <span data-ttu-id="62380-465">Drei aufeinander folgende Ziffern (ungerade für Männer, gerade für Frauen) </span><span class="sxs-lookup"><span data-stu-id="62380-465">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="62380-466">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="62380-466">A period</span></span> 
- <span data-ttu-id="62380-467">Zwei Ziffern als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="62380-467">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-468">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-468">Checksum</span></span>

<span data-ttu-id="62380-469">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-469">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-470">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-470">Definition</span></span>

<span data-ttu-id="62380-471">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-472">Die Funktion Func_belgium_national_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-472">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-473">Ein Schlüsselwort aus Keyword_belgium_national_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-473">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="62380-474">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-474">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-475">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-475">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="62380-476">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="62380-476">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="62380-477">Identität</span><span class="sxs-lookup"><span data-stu-id="62380-477">Identity</span></span>
- <span data-ttu-id="62380-478">Registrierung</span><span class="sxs-lookup"><span data-stu-id="62380-478">Registration</span></span>
- <span data-ttu-id="62380-479">Identifikations</span><span class="sxs-lookup"><span data-stu-id="62380-479">Identification</span></span> 
- <span data-ttu-id="62380-480">ID</span><span class="sxs-lookup"><span data-stu-id="62380-480">ID</span></span> 
- <span data-ttu-id="62380-481">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="62380-481">Identiteitskaart</span></span>
- <span data-ttu-id="62380-482">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="62380-482">Registratie nummer</span></span> 
- <span data-ttu-id="62380-483">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="62380-483">Identificatie nummer</span></span> 
- <span data-ttu-id="62380-484">Identiteit</span><span class="sxs-lookup"><span data-stu-id="62380-484">Identiteit</span></span>
- <span data-ttu-id="62380-485">Registratie</span><span class="sxs-lookup"><span data-stu-id="62380-485">Registratie</span></span>
- <span data-ttu-id="62380-486">Identificatie</span><span class="sxs-lookup"><span data-stu-id="62380-486">Identificatie</span></span> 
- <span data-ttu-id="62380-487">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="62380-487">Carte d’identité</span></span> 
- <span data-ttu-id="62380-488">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="62380-488">numéro d'immatriculation</span></span>
- <span data-ttu-id="62380-489">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="62380-489">numéro d'identification</span></span>
- <span data-ttu-id="62380-490">identité</span><span class="sxs-lookup"><span data-stu-id="62380-490">identité</span></span> 
- <span data-ttu-id="62380-491">Inschrift</span><span class="sxs-lookup"><span data-stu-id="62380-491">inscription</span></span> 
- <span data-ttu-id="62380-492">Identifikation</span><span class="sxs-lookup"><span data-stu-id="62380-492">Identifikation</span></span>
- <span data-ttu-id="62380-493">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="62380-493">Identifizierung</span></span>
- <span data-ttu-id="62380-494">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-494">Identifikationsnummer</span></span>
- <span data-ttu-id="62380-495">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="62380-495">Personalausweis</span></span>
- <span data-ttu-id="62380-496">Registrierung</span><span class="sxs-lookup"><span data-stu-id="62380-496">Registrierung</span></span>
- <span data-ttu-id="62380-497">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-497">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="62380-498">Brazil CPF Number</span><span class="sxs-lookup"><span data-stu-id="62380-498">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-499">Format</span><span class="sxs-lookup"><span data-stu-id="62380-499">Format</span></span>

<span data-ttu-id="62380-500">11 Ziffern, die eine Prüfziffer umfassen und die formatiert oder unformatiert sein können</span><span class="sxs-lookup"><span data-stu-id="62380-500">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-501">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-501">Pattern</span></span>

<span data-ttu-id="62380-502">Formatiert</span><span class="sxs-lookup"><span data-stu-id="62380-502">Formatted:</span></span>
- <span data-ttu-id="62380-503">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-503">Three digits</span></span> 
- <span data-ttu-id="62380-504">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="62380-504">A period</span></span> 
- <span data-ttu-id="62380-505">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-505">Three digits</span></span> 
- <span data-ttu-id="62380-506">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="62380-506">A period</span></span> 
- <span data-ttu-id="62380-507">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-507">Three digits</span></span> 
- <span data-ttu-id="62380-508">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-508">A hyphen</span></span> 
- <span data-ttu-id="62380-509">Zwei Ziffern, die Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="62380-509">Two digits which are check digits</span></span>

<span data-ttu-id="62380-510">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="62380-510">Unformatted:</span></span>
- <span data-ttu-id="62380-511">11 Ziffern, wobei die letzten beiden Ziffern Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="62380-511">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-512">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-512">Checksum</span></span>

<span data-ttu-id="62380-513">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-513">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-514">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-514">Definition</span></span>

<span data-ttu-id="62380-515">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-515">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-516">Die Funktion Func_brazil_cpf sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-516">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-517">Ein Schlüsselwort aus Keyword_brazil_cpf wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-517">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="62380-518">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-518">The checksum passes.</span></span>

<span data-ttu-id="62380-519">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-519">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-520">Die Funktion Func_brazil_cpf sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-520">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-521">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-521">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-522">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-522">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="62380-523">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="62380-523">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="62380-524">CPF</span><span class="sxs-lookup"><span data-stu-id="62380-524">CPF</span></span>
- <span data-ttu-id="62380-525">Identifikations</span><span class="sxs-lookup"><span data-stu-id="62380-525">Identification</span></span>
- <span data-ttu-id="62380-526">Registrierung</span><span class="sxs-lookup"><span data-stu-id="62380-526">Registration</span></span>
- <span data-ttu-id="62380-527">Umsatz</span><span class="sxs-lookup"><span data-stu-id="62380-527">Revenue</span></span>
- <span data-ttu-id="62380-528">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="62380-528">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="62380-529">Imposto</span><span class="sxs-lookup"><span data-stu-id="62380-529">Imposto</span></span> 
- <span data-ttu-id="62380-530">Identificação</span><span class="sxs-lookup"><span data-stu-id="62380-530">Identificação</span></span> 
- <span data-ttu-id="62380-531">Inscrição</span><span class="sxs-lookup"><span data-stu-id="62380-531">Inscrição</span></span> 
- <span data-ttu-id="62380-532">Receita</span><span class="sxs-lookup"><span data-stu-id="62380-532">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="62380-533">Brasilien – Juristische Personennummer (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="62380-533">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="62380-534">Format</span><span class="sxs-lookup"><span data-stu-id="62380-534">Format</span></span>

<span data-ttu-id="62380-535">14 Ziffern, die eine Registrierungsnummer, eine Zweignummer und Prüfnziffern sowie Trennzeichen umfassen</span><span class="sxs-lookup"><span data-stu-id="62380-535">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-536">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-536">Pattern</span></span>
<span data-ttu-id="62380-537">14 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="62380-537">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="62380-538">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-538">Two digits</span></span> 
- <span data-ttu-id="62380-539">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="62380-539">A period</span></span> 
- <span data-ttu-id="62380-540">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-540">Three digits</span></span> 
- <span data-ttu-id="62380-541">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="62380-541">A period</span></span> 
- <span data-ttu-id="62380-542">Drei Ziffern (diese ersten acht Ziffern sind die Registrierungsnummer) </span><span class="sxs-lookup"><span data-stu-id="62380-542">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="62380-543">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="62380-543">A forward slash</span></span> 
- <span data-ttu-id="62380-544">Vierstellige Zweignummer </span><span class="sxs-lookup"><span data-stu-id="62380-544">Four-digit branch number</span></span> 
- <span data-ttu-id="62380-545">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-545">A hyphen</span></span> 
- <span data-ttu-id="62380-546">Zwei Ziffern, die Prüfziffern sind</span><span class="sxs-lookup"><span data-stu-id="62380-546">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-547">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-547">Checksum</span></span>

<span data-ttu-id="62380-548">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-549">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-549">Definition</span></span>

<span data-ttu-id="62380-550">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-551">Die Funktion Func_brazil_cnpj sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-551">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-552">Ein Schlüsselwort aus Keyword_brazil_cnpj wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-552">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="62380-553">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-553">The checksum passes.</span></span>

<span data-ttu-id="62380-554">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-554">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-555">Die Funktion Func_brazil_cnpj sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-555">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-556">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-556">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-557">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-557">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="62380-558">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="62380-558">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="62380-559">CNPJ</span><span class="sxs-lookup"><span data-stu-id="62380-559">CNPJ</span></span> 
- <span data-ttu-id="62380-560">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="62380-560">CNPJ/MF</span></span> 
- <span data-ttu-id="62380-561">CNPJ-MF</span><span class="sxs-lookup"><span data-stu-id="62380-561">CNPJ-MF</span></span> 
- <span data-ttu-id="62380-562">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="62380-562">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="62380-563">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="62380-563">Taxpayers Registry</span></span> 
- <span data-ttu-id="62380-564">Legal entity</span><span class="sxs-lookup"><span data-stu-id="62380-564">Legal entity</span></span> 
- <span data-ttu-id="62380-565">Legal entities</span><span class="sxs-lookup"><span data-stu-id="62380-565">Legal entities</span></span> 
- <span data-ttu-id="62380-566">Registration Status</span><span class="sxs-lookup"><span data-stu-id="62380-566">Registration Status</span></span> 
- <span data-ttu-id="62380-567">Business</span><span class="sxs-lookup"><span data-stu-id="62380-567">Business</span></span> 
- <span data-ttu-id="62380-568">Company</span><span class="sxs-lookup"><span data-stu-id="62380-568">Company</span></span>
- <span data-ttu-id="62380-569">CNPJ</span><span class="sxs-lookup"><span data-stu-id="62380-569">CNPJ</span></span> 
- <span data-ttu-id="62380-570">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="62380-570">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="62380-571">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="62380-571">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="62380-572">CGC</span><span class="sxs-lookup"><span data-stu-id="62380-572">CGC</span></span> 
- <span data-ttu-id="62380-573">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="62380-573">Pessoa jurídica</span></span> 
- <span data-ttu-id="62380-574">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="62380-574">Pessoas jurídicas</span></span> 
- <span data-ttu-id="62380-575">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="62380-575">Situação cadastral</span></span> 
- <span data-ttu-id="62380-576">Inscrição</span><span class="sxs-lookup"><span data-stu-id="62380-576">Inscrição</span></span> 
- <span data-ttu-id="62380-577">Empresa</span><span class="sxs-lookup"><span data-stu-id="62380-577">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="62380-578">	Brasilien – Personalausweis (RG)</span><span class="sxs-lookup"><span data-stu-id="62380-578">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="62380-579">Format</span><span class="sxs-lookup"><span data-stu-id="62380-579">Format</span></span>

<span data-ttu-id="62380-580">Registro Geral (altes Format): neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-580">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="62380-581">Registro de Identidade (RIC) (neues Format): 11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-581">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-582">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-582">Pattern</span></span>

<span data-ttu-id="62380-583">Registro Geral (altes Format):</span><span class="sxs-lookup"><span data-stu-id="62380-583">Registro Geral (old format):</span></span>
- <span data-ttu-id="62380-584">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-584">Two digits</span></span> 
- <span data-ttu-id="62380-585">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="62380-585">A period</span></span> 
- <span data-ttu-id="62380-586">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-586">Three digits</span></span> 
- <span data-ttu-id="62380-587">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="62380-587">A period</span></span> 
- <span data-ttu-id="62380-588">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-588">Three digits</span></span> 
- <span data-ttu-id="62380-589">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-589">A hyphen</span></span> 
- <span data-ttu-id="62380-590">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="62380-590">One digit which is a check digit</span></span>

<span data-ttu-id="62380-591">Registro de Identidade (RIC) (neues Format):</span><span class="sxs-lookup"><span data-stu-id="62380-591">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="62380-592">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-592">10 digits</span></span> 
- <span data-ttu-id="62380-593">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-593">A hyphen</span></span> 
- <span data-ttu-id="62380-594">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="62380-594">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-595">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-595">Checksum</span></span>

<span data-ttu-id="62380-596">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-596">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-597">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-597">Definition</span></span>

<span data-ttu-id="62380-598">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-598">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-599">Die Funktion Func_brazil_rg sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-599">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-600">Ein Schlüsselwort aus Keyword_brazil_rg wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-600">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="62380-601">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-601">The checksum passes.</span></span>

<span data-ttu-id="62380-602">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-602">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-603">Die Funktion Func_brazil_rg sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-603">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-604">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-604">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-605">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-605">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="62380-606">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="62380-606">Keyword_brazil_rg</span></span>

<span data-ttu-id="62380-607">Cédula de identidade Identity Card National ID número de rregistro Registro de Iidentidade Registro Geral RG (dieses Schlüsselwort wird Groß-/Kleinschreibung beachtet) RIC (bei diesem Schlüsselwort wird die Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="62380-607">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="62380-608">Kanadische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="62380-608">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-609">Format</span><span class="sxs-lookup"><span data-stu-id="62380-609">Format</span></span>

<span data-ttu-id="62380-610">Sieben oder zwölf Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-610">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-611">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-611">Pattern</span></span>

<span data-ttu-id="62380-612">Eine kanadische Kontonummer umfasst sieben oder zwölf Ziffern.</span><span class="sxs-lookup"><span data-stu-id="62380-612">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="62380-613">Eine kanadische Bankkontonummer setzt sich wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="62380-613">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="62380-614">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-614">Five digits</span></span> 
- <span data-ttu-id="62380-615">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-615">A hyphen</span></span> 
- <span data-ttu-id="62380-616">Drei Ziffern oder</span><span class="sxs-lookup"><span data-stu-id="62380-616">Three digits OR</span></span>
- <span data-ttu-id="62380-617">Eine 0 (null) </span><span class="sxs-lookup"><span data-stu-id="62380-617">A zero "0"</span></span> 
- <span data-ttu-id="62380-618">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-618">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-619">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-619">Checksum</span></span>

<span data-ttu-id="62380-620">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-620">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-621">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-621">Definition</span></span>

<span data-ttu-id="62380-622">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-622">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-623">Der reguläre Ausdruck Regex_canada_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-623">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-624">Ein Schlüsselwort aus Keyword_canada_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-624">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="62380-625">Der reguläre Ausdruck Regex_canada_bank_account_transit_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-625">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="62380-626">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-627">Der reguläre Ausdruck Regex_canada_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-627">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-628">Ein Schlüsselwort aus Keyword_canada_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-628">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-629">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-629">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="62380-630">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="62380-630">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="62380-631">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="62380-631">canada savings bonds</span></span>
- <span data-ttu-id="62380-632">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="62380-632">canada revenue agency</span></span>
- <span data-ttu-id="62380-633">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="62380-633">canadian financial institution</span></span>
- <span data-ttu-id="62380-634">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="62380-634">direct deposit form</span></span>
- <span data-ttu-id="62380-635">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="62380-635">canadian citizen</span></span>
- <span data-ttu-id="62380-636">legal representative</span><span class="sxs-lookup"><span data-stu-id="62380-636">legal representative</span></span>
- <span data-ttu-id="62380-637">notary public</span><span class="sxs-lookup"><span data-stu-id="62380-637">notary public</span></span>
- <span data-ttu-id="62380-638">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="62380-638">commissioner for oaths</span></span>
- <span data-ttu-id="62380-639">child care benefit</span><span class="sxs-lookup"><span data-stu-id="62380-639">child care benefit</span></span>
- <span data-ttu-id="62380-640">universal child care</span><span class="sxs-lookup"><span data-stu-id="62380-640">universal child care</span></span>
- <span data-ttu-id="62380-641">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="62380-641">canada child tax benefit</span></span>
- <span data-ttu-id="62380-642">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="62380-642">income tax benefit</span></span>
- <span data-ttu-id="62380-643">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="62380-643">harmonized sales tax</span></span>
- <span data-ttu-id="62380-644">social insurance number</span><span class="sxs-lookup"><span data-stu-id="62380-644">social insurance number</span></span>
- <span data-ttu-id="62380-645">income tax refund</span><span class="sxs-lookup"><span data-stu-id="62380-645">income tax refund</span></span>
- <span data-ttu-id="62380-646">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="62380-646">child tax benefit</span></span>
- <span data-ttu-id="62380-647">territorial payments</span><span class="sxs-lookup"><span data-stu-id="62380-647">territorial payments</span></span>
- <span data-ttu-id="62380-648">institution number</span><span class="sxs-lookup"><span data-stu-id="62380-648">institution number</span></span>
- <span data-ttu-id="62380-649">deposit request</span><span class="sxs-lookup"><span data-stu-id="62380-649">deposit request</span></span>
- <span data-ttu-id="62380-650">banking information</span><span class="sxs-lookup"><span data-stu-id="62380-650">banking information</span></span>
- <span data-ttu-id="62380-651">direct deposit</span><span class="sxs-lookup"><span data-stu-id="62380-651">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="62380-652">Kanadische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-652">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-653">Format</span><span class="sxs-lookup"><span data-stu-id="62380-653">Format</span></span>

<span data-ttu-id="62380-654">Variiert je nach Provinz</span><span class="sxs-lookup"><span data-stu-id="62380-654">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-655">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-655">Pattern</span></span>

<span data-ttu-id="62380-656">Verschiedene Muster in Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec und Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="62380-656">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-657">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-657">Checksum</span></span>

<span data-ttu-id="62380-658">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-658">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-659">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-659">Definition</span></span>

<span data-ttu-id="62380-660">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-660">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-661">Die Funktion Func_[province_name]_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-661">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-662">Ein Schlüsselwort aus Keyword_[province_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-662">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="62380-663">Ein Schlüsselwort aus Keyword_canada_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-663">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-664">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-664">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="62380-665">Keyword_ [province_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="62380-665">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="62380-666">Die Abkürzung für die Provinz, z. B. AB</span><span class="sxs-lookup"><span data-stu-id="62380-666">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="62380-667">Der Name der Provinz, beispielsweise „Alberta“</span><span class="sxs-lookup"><span data-stu-id="62380-667">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="62380-668">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="62380-668">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="62380-669">DL</span><span class="sxs-lookup"><span data-stu-id="62380-669">DL</span></span>
- <span data-ttu-id="62380-670">DLS</span><span class="sxs-lookup"><span data-stu-id="62380-670">DLS</span></span>
- <span data-ttu-id="62380-671">CDL</span><span class="sxs-lookup"><span data-stu-id="62380-671">CDL</span></span>
- <span data-ttu-id="62380-672">CDLS</span><span class="sxs-lookup"><span data-stu-id="62380-672">CDLS</span></span>
- <span data-ttu-id="62380-673">DriverLic</span><span class="sxs-lookup"><span data-stu-id="62380-673">DriverLic</span></span>
- <span data-ttu-id="62380-674">DriverLics</span><span class="sxs-lookup"><span data-stu-id="62380-674">DriverLics</span></span>
- <span data-ttu-id="62380-675">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="62380-675">DriverLicense</span></span>
- <span data-ttu-id="62380-676">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="62380-676">DriverLicenses</span></span>
- <span data-ttu-id="62380-677">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="62380-677">DriverLicence</span></span>
- <span data-ttu-id="62380-678">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="62380-678">DriverLicences</span></span>
- <span data-ttu-id="62380-679">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="62380-679">Driver Lic</span></span>
- <span data-ttu-id="62380-680">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="62380-680">Driver Lics</span></span>
- <span data-ttu-id="62380-681">Driver License</span><span class="sxs-lookup"><span data-stu-id="62380-681">Driver License</span></span>
- <span data-ttu-id="62380-682">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-682">Driver Licenses</span></span>
- <span data-ttu-id="62380-683">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="62380-683">Driver Licence</span></span>
- <span data-ttu-id="62380-684">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="62380-684">Driver Licences</span></span>
- <span data-ttu-id="62380-685">DriversLic</span><span class="sxs-lookup"><span data-stu-id="62380-685">DriversLic</span></span>
- <span data-ttu-id="62380-686">DriversLics</span><span class="sxs-lookup"><span data-stu-id="62380-686">DriversLics</span></span>
- <span data-ttu-id="62380-687">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="62380-687">DriversLicence</span></span>
- <span data-ttu-id="62380-688">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="62380-688">DriversLicences</span></span>
- <span data-ttu-id="62380-689">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="62380-689">DriversLicense</span></span>
- <span data-ttu-id="62380-690">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="62380-690">DriversLicenses</span></span>
- <span data-ttu-id="62380-691">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="62380-691">Drivers Lic</span></span>
- <span data-ttu-id="62380-692">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="62380-692">Drivers Lics</span></span>
- <span data-ttu-id="62380-693">Drivers License</span><span class="sxs-lookup"><span data-stu-id="62380-693">Drivers License</span></span>
- <span data-ttu-id="62380-694">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-694">Drivers Licenses</span></span>
- <span data-ttu-id="62380-695">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="62380-695">Drivers Licence</span></span>
- <span data-ttu-id="62380-696">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="62380-696">Drivers Licences</span></span>
- <span data-ttu-id="62380-697">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="62380-697">Driver'Lic</span></span>
- <span data-ttu-id="62380-698">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="62380-698">Driver'Lics</span></span>
- <span data-ttu-id="62380-699">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="62380-699">Driver'License</span></span>
- <span data-ttu-id="62380-700">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-700">Driver'Licenses</span></span>
- <span data-ttu-id="62380-701">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="62380-701">Driver'Licence</span></span>
- <span data-ttu-id="62380-702">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="62380-702">Driver'Licences</span></span>
- <span data-ttu-id="62380-703">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="62380-703">Driver' Lic</span></span>
- <span data-ttu-id="62380-704">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="62380-704">Driver' Lics</span></span>
- <span data-ttu-id="62380-705">Driver' License</span><span class="sxs-lookup"><span data-stu-id="62380-705">Driver' License</span></span>
- <span data-ttu-id="62380-706">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-706">Driver' Licenses</span></span>
- <span data-ttu-id="62380-707">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="62380-707">Driver' Licence</span></span>
- <span data-ttu-id="62380-708">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="62380-708">Driver' Licences</span></span>
- <span data-ttu-id="62380-709">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="62380-709">Driver'sLic</span></span>
- <span data-ttu-id="62380-710">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="62380-710">Driver'sLics</span></span>
- <span data-ttu-id="62380-711">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="62380-711">Driver'sLicense</span></span>
- <span data-ttu-id="62380-712">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="62380-712">Driver'sLicenses</span></span>
- <span data-ttu-id="62380-713">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="62380-713">Driver'sLicence</span></span>
- <span data-ttu-id="62380-714">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="62380-714">Driver'sLicences</span></span>
- <span data-ttu-id="62380-715">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="62380-715">Driver's Lic</span></span>
- <span data-ttu-id="62380-716">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="62380-716">Driver's Lics</span></span>
- <span data-ttu-id="62380-717">Driver's License</span><span class="sxs-lookup"><span data-stu-id="62380-717">Driver's License</span></span>
- <span data-ttu-id="62380-718">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-718">Driver's Licenses</span></span>
- <span data-ttu-id="62380-719">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="62380-719">Driver's Licence</span></span>
- <span data-ttu-id="62380-720">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="62380-720">Driver's Licences</span></span>
- <span data-ttu-id="62380-721">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="62380-721">Permis de Conduire</span></span>
- <span data-ttu-id="62380-722">id</span><span class="sxs-lookup"><span data-stu-id="62380-722">id</span></span>
- <span data-ttu-id="62380-723">ids</span><span class="sxs-lookup"><span data-stu-id="62380-723">ids</span></span>
- <span data-ttu-id="62380-724">idcard number</span><span class="sxs-lookup"><span data-stu-id="62380-724">idcard number</span></span>
- <span data-ttu-id="62380-725">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="62380-725">idcard numbers</span></span>
- <span data-ttu-id="62380-726">idcard #</span><span class="sxs-lookup"><span data-stu-id="62380-726">idcard #</span></span>
- <span data-ttu-id="62380-727">idcard #s</span><span class="sxs-lookup"><span data-stu-id="62380-727">idcard #s</span></span>
- <span data-ttu-id="62380-728">idcard card</span><span class="sxs-lookup"><span data-stu-id="62380-728">idcard card</span></span>
- <span data-ttu-id="62380-729">idcard cards</span><span class="sxs-lookup"><span data-stu-id="62380-729">idcard cards</span></span>
- <span data-ttu-id="62380-730">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="62380-730">idcard</span></span>
- <span data-ttu-id="62380-731">identification number</span><span class="sxs-lookup"><span data-stu-id="62380-731">identification number</span></span>
- <span data-ttu-id="62380-732">identification numbers</span><span class="sxs-lookup"><span data-stu-id="62380-732">identification numbers</span></span>
- <span data-ttu-id="62380-733">identification #</span><span class="sxs-lookup"><span data-stu-id="62380-733">identification #</span></span>
- <span data-ttu-id="62380-734">identification #s</span><span class="sxs-lookup"><span data-stu-id="62380-734">identification #s</span></span>
- <span data-ttu-id="62380-735">identification card</span><span class="sxs-lookup"><span data-stu-id="62380-735">identification card</span></span>
- <span data-ttu-id="62380-736">identification cards</span><span class="sxs-lookup"><span data-stu-id="62380-736">identification cards</span></span>
- <span data-ttu-id="62380-737">Identifikations</span><span class="sxs-lookup"><span data-stu-id="62380-737">identification</span></span> 
- <span data-ttu-id="62380-738">DL</span><span class="sxs-lookup"><span data-stu-id="62380-738">DL#</span></span>
- <span data-ttu-id="62380-739">DLS</span><span class="sxs-lookup"><span data-stu-id="62380-739">DLS#</span></span> 
- <span data-ttu-id="62380-740">CDL</span><span class="sxs-lookup"><span data-stu-id="62380-740">CDL#</span></span> 
- <span data-ttu-id="62380-741">CDLS</span><span class="sxs-lookup"><span data-stu-id="62380-741">CDLS#</span></span> 
- <span data-ttu-id="62380-742">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="62380-742">DriverLic#</span></span> 
- <span data-ttu-id="62380-743">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="62380-743">DriverLics#</span></span> 
- <span data-ttu-id="62380-744">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="62380-744">DriverLicense#</span></span> 
- <span data-ttu-id="62380-745">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="62380-745">DriverLicenses#</span></span> 
- <span data-ttu-id="62380-746">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="62380-746">DriverLicence#</span></span> 
- <span data-ttu-id="62380-747">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="62380-747">DriverLicences#</span></span> 
- <span data-ttu-id="62380-748">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-748">Driver Lic#</span></span>
- <span data-ttu-id="62380-749">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-749">Driver Lics#</span></span> 
- <span data-ttu-id="62380-750">Driver License#</span><span class="sxs-lookup"><span data-stu-id="62380-750">Driver License#</span></span> 
- <span data-ttu-id="62380-751">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-751">Driver Licenses#</span></span> 
- <span data-ttu-id="62380-752">Driver License#</span><span class="sxs-lookup"><span data-stu-id="62380-752">Driver License#</span></span> 
- <span data-ttu-id="62380-753">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="62380-753">Driver Licences#</span></span> 
- <span data-ttu-id="62380-754">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="62380-754">DriversLic#</span></span> 
- <span data-ttu-id="62380-755">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="62380-755">DriversLics#</span></span> 
- <span data-ttu-id="62380-756">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="62380-756">DriversLicense#</span></span> 
- <span data-ttu-id="62380-757">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="62380-757">DriversLicenses#</span></span> 
- <span data-ttu-id="62380-758">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="62380-758">DriversLicence#</span></span> 
- <span data-ttu-id="62380-759">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="62380-759">DriversLicences#</span></span> 
- <span data-ttu-id="62380-760">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-760">Drivers Lic#</span></span> 
- <span data-ttu-id="62380-761">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-761">Drivers Lics#</span></span> 
- <span data-ttu-id="62380-762">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="62380-762">Drivers License#</span></span> 
- <span data-ttu-id="62380-763">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-763">Drivers Licenses#</span></span> 
- <span data-ttu-id="62380-764">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="62380-764">Drivers Licence#</span></span> 
- <span data-ttu-id="62380-765">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="62380-765">Drivers Licences#</span></span> 
- <span data-ttu-id="62380-766">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="62380-766">Driver'Lic#</span></span> 
- <span data-ttu-id="62380-767">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="62380-767">Driver'Lics#</span></span> 
- <span data-ttu-id="62380-768">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="62380-768">Driver'License#</span></span> 
- <span data-ttu-id="62380-769">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-769">Driver'Licenses#</span></span> 
- <span data-ttu-id="62380-770">Driver'Licence #</span><span class="sxs-lookup"><span data-stu-id="62380-770">Driver'Licence#</span></span> 
- <span data-ttu-id="62380-771">Driver'Licences #</span><span class="sxs-lookup"><span data-stu-id="62380-771">Driver'Licences#</span></span> 
- <span data-ttu-id="62380-772">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-772">Driver' Lic#</span></span> 
- <span data-ttu-id="62380-773">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-773">Driver' Lics#</span></span> 
- <span data-ttu-id="62380-774">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="62380-774">Driver' License#</span></span> 
- <span data-ttu-id="62380-775">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-775">Driver' Licenses#</span></span> 
- <span data-ttu-id="62380-776">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="62380-776">Driver' Licence#</span></span> 
- <span data-ttu-id="62380-777">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="62380-777">Driver' Licences#</span></span> 
- <span data-ttu-id="62380-778">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="62380-778">Driver'sLic#</span></span> 
- <span data-ttu-id="62380-779">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="62380-779">Driver'sLics#</span></span> 
- <span data-ttu-id="62380-780">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="62380-780">Driver'sLicense#</span></span> 
- <span data-ttu-id="62380-781">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="62380-781">Driver'sLicenses#</span></span> 
- <span data-ttu-id="62380-782">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="62380-782">Driver'sLicence#</span></span> 
- <span data-ttu-id="62380-783">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="62380-783">Driver'sLicences#</span></span> 
- <span data-ttu-id="62380-784">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-784">Driver's Lic#</span></span> 
- <span data-ttu-id="62380-785">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-785">Driver's Lics#</span></span> 
- <span data-ttu-id="62380-786">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="62380-786">Driver's License#</span></span> 
- <span data-ttu-id="62380-787">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-787">Driver's Licenses#</span></span> 
- <span data-ttu-id="62380-788">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="62380-788">Driver's Licence#</span></span> 
- <span data-ttu-id="62380-789">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="62380-789">Driver's Licences#</span></span> 
- <span data-ttu-id="62380-790">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="62380-790">Permis de Conduire#</span></span> 
- <span data-ttu-id="62380-791">ID</span><span class="sxs-lookup"><span data-stu-id="62380-791">id#</span></span> 
- <span data-ttu-id="62380-792">IDs</span><span class="sxs-lookup"><span data-stu-id="62380-792">ids#</span></span> 
- <span data-ttu-id="62380-793">idcard card#</span><span class="sxs-lookup"><span data-stu-id="62380-793">idcard card#</span></span> 
- <span data-ttu-id="62380-794">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="62380-794">idcard cards#</span></span> 
- <span data-ttu-id="62380-795">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="62380-795">idcard#</span></span> 
- <span data-ttu-id="62380-796">identification card#</span><span class="sxs-lookup"><span data-stu-id="62380-796">identification card#</span></span> 
- <span data-ttu-id="62380-797">identification cards#</span><span class="sxs-lookup"><span data-stu-id="62380-797">identification cards#</span></span> 
- <span data-ttu-id="62380-798">Identifikations</span><span class="sxs-lookup"><span data-stu-id="62380-798">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="62380-799">Kanadische Health Service-Nummer</span><span class="sxs-lookup"><span data-stu-id="62380-799">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-800">Format</span><span class="sxs-lookup"><span data-stu-id="62380-800">Format</span></span>

<span data-ttu-id="62380-801">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-801">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-802">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-802">Pattern</span></span>

<span data-ttu-id="62380-803">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-803">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-804">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-804">Checksum</span></span>

<span data-ttu-id="62380-805">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-805">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-806">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-806">Definition</span></span>

<span data-ttu-id="62380-807">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-807">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-808">Der reguläre Ausdruck Regex_canada_health_service_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-808">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-809">Ein Schlüsselwort aus Keyword_canada_health_service_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-809">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-810">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-810">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="62380-811">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="62380-811">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="62380-812">personal health number</span><span class="sxs-lookup"><span data-stu-id="62380-812">personal health number</span></span>
- <span data-ttu-id="62380-813">patient information</span><span class="sxs-lookup"><span data-stu-id="62380-813">patient information</span></span>
- <span data-ttu-id="62380-814">health services</span><span class="sxs-lookup"><span data-stu-id="62380-814">health services</span></span>
- <span data-ttu-id="62380-815">speciality services</span><span class="sxs-lookup"><span data-stu-id="62380-815">speciality services</span></span>
- <span data-ttu-id="62380-816">automobile accident</span><span class="sxs-lookup"><span data-stu-id="62380-816">automobile accident</span></span>
- <span data-ttu-id="62380-817">patient hospital</span><span class="sxs-lookup"><span data-stu-id="62380-817">patient hospital</span></span>
- <span data-ttu-id="62380-818">Psychiater</span><span class="sxs-lookup"><span data-stu-id="62380-818">psychiatrist</span></span>
- <span data-ttu-id="62380-819">workers compensation</span><span class="sxs-lookup"><span data-stu-id="62380-819">workers compensation</span></span>
- <span data-ttu-id="62380-820">Disability</span><span class="sxs-lookup"><span data-stu-id="62380-820">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="62380-821">Kanadische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="62380-821">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-822">Format</span><span class="sxs-lookup"><span data-stu-id="62380-822">Format</span></span>

<span data-ttu-id="62380-823">Zwei Großbuchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-823">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-824">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-824">Pattern</span></span>

<span data-ttu-id="62380-825">Zwei Großbuchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-825">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-826">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-826">Checksum</span></span>

<span data-ttu-id="62380-827">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-827">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-828">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-828">Definition</span></span>

<span data-ttu-id="62380-829">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-829">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-830">Der reguläre Ausdruck Regex_canada_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-830">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-831">Ein Schlüsselwort aus Keyword_canada_passport_number oder Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-831">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-832">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-832">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="62380-833">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="62380-833">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="62380-834">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="62380-834">canadian citizenship</span></span>
- <span data-ttu-id="62380-835">canadian passport</span><span class="sxs-lookup"><span data-stu-id="62380-835">canadian passport</span></span>
- <span data-ttu-id="62380-836">passport application</span><span class="sxs-lookup"><span data-stu-id="62380-836">passport application</span></span>
- <span data-ttu-id="62380-837">passport photos</span><span class="sxs-lookup"><span data-stu-id="62380-837">passport photos</span></span>
- <span data-ttu-id="62380-838">certified translator</span><span class="sxs-lookup"><span data-stu-id="62380-838">certified translator</span></span>
- <span data-ttu-id="62380-839">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="62380-839">canadian citizens</span></span>
- <span data-ttu-id="62380-840">processing times</span><span class="sxs-lookup"><span data-stu-id="62380-840">processing times</span></span>
- <span data-ttu-id="62380-841">renewal application</span><span class="sxs-lookup"><span data-stu-id="62380-841">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="62380-842">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="62380-842">Keyword_passport</span></span>

- <span data-ttu-id="62380-843">Passport Number</span><span class="sxs-lookup"><span data-stu-id="62380-843">Passport Number</span></span>
- <span data-ttu-id="62380-844">Passport No</span><span class="sxs-lookup"><span data-stu-id="62380-844">Passport No</span></span>
- <span data-ttu-id="62380-845">Passport#</span><span class="sxs-lookup"><span data-stu-id="62380-845">Passport #</span></span>
- <span data-ttu-id="62380-846">Pass</span><span class="sxs-lookup"><span data-stu-id="62380-846">Passport#</span></span>
- <span data-ttu-id="62380-847">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="62380-847">PassportID</span></span>
- <span data-ttu-id="62380-848">Passportno</span><span class="sxs-lookup"><span data-stu-id="62380-848">Passportno</span></span>
- <span data-ttu-id="62380-849">passportnumber</span><span class="sxs-lookup"><span data-stu-id="62380-849">passportnumber</span></span>
- <span data-ttu-id="62380-850">パスポート</span><span class="sxs-lookup"><span data-stu-id="62380-850">パスポート</span></span>
- <span data-ttu-id="62380-851">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="62380-851">パスポート番号</span></span>
- <span data-ttu-id="62380-852">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="62380-852">パスポートのNum</span></span>
- <span data-ttu-id="62380-853">パスポート #</span><span class="sxs-lookup"><span data-stu-id="62380-853">パスポート＃</span></span>
- <span data-ttu-id="62380-854">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="62380-854">Numéro de passeport</span></span>
- <span data-ttu-id="62380-855">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="62380-855">Passeport n °</span></span>
- <span data-ttu-id="62380-856">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="62380-856">Passeport Non</span></span>
- <span data-ttu-id="62380-857">Passeport#</span><span class="sxs-lookup"><span data-stu-id="62380-857">Passeport #</span></span>
- <span data-ttu-id="62380-858">Passeport</span><span class="sxs-lookup"><span data-stu-id="62380-858">Passeport#</span></span>
- <span data-ttu-id="62380-859">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="62380-859">PasseportNon</span></span>
- <span data-ttu-id="62380-860">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="62380-860">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="62380-861">Kanadische Personal Health Identification-Nummer (PHIN)</span><span class="sxs-lookup"><span data-stu-id="62380-861">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="62380-862">Format</span><span class="sxs-lookup"><span data-stu-id="62380-862">Format</span></span>

<span data-ttu-id="62380-863">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-863">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-864">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-864">Pattern</span></span>

<span data-ttu-id="62380-865">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-865">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-866">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-866">Checksum</span></span>

<span data-ttu-id="62380-867">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-867">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-868">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-868">Definition</span></span>

<span data-ttu-id="62380-869">Eine DLP-Richtlinie ist 75% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: der reguläre Ausdruck Regex_canada_phin findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-869">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="62380-870">Es werden mindestens zwei Schlüsselwörter aus Keyword_canada_phin oder Keyword_canada_provinces gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-870">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-871">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-871">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="62380-872">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="62380-872">Keyword_canada_phin</span></span>

- <span data-ttu-id="62380-873">social insurance number</span><span class="sxs-lookup"><span data-stu-id="62380-873">social insurance number</span></span>
- <span data-ttu-id="62380-874">health information act</span><span class="sxs-lookup"><span data-stu-id="62380-874">health information act</span></span>
- <span data-ttu-id="62380-875">income tax information</span><span class="sxs-lookup"><span data-stu-id="62380-875">income tax information</span></span>
- <span data-ttu-id="62380-876">manitoba health</span><span class="sxs-lookup"><span data-stu-id="62380-876">manitoba health</span></span>
- <span data-ttu-id="62380-877">health registration</span><span class="sxs-lookup"><span data-stu-id="62380-877">health registration</span></span>
- <span data-ttu-id="62380-878">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="62380-878">prescription purchases</span></span>
- <span data-ttu-id="62380-879">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="62380-879">benefit eligibility</span></span>
- <span data-ttu-id="62380-880">personal health</span><span class="sxs-lookup"><span data-stu-id="62380-880">personal health</span></span>
- <span data-ttu-id="62380-881">power of attorney</span><span class="sxs-lookup"><span data-stu-id="62380-881">power of attorney</span></span>
- <span data-ttu-id="62380-882">registration number</span><span class="sxs-lookup"><span data-stu-id="62380-882">registration number</span></span>
- <span data-ttu-id="62380-883">personal health number</span><span class="sxs-lookup"><span data-stu-id="62380-883">personal health number</span></span>
- <span data-ttu-id="62380-884">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="62380-884">practitioner referral</span></span>
- <span data-ttu-id="62380-885">wellness professional</span><span class="sxs-lookup"><span data-stu-id="62380-885">wellness professional</span></span>
- <span data-ttu-id="62380-886">patient referral</span><span class="sxs-lookup"><span data-stu-id="62380-886">patient referral</span></span>
- <span data-ttu-id="62380-887">health and wellness</span><span class="sxs-lookup"><span data-stu-id="62380-887">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="62380-888">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="62380-888">Keyword_canada_provinces</span></span>

- <span data-ttu-id="62380-889">Nunavut</span><span class="sxs-lookup"><span data-stu-id="62380-889">Nunavut</span></span>
- <span data-ttu-id="62380-890">Quebec</span><span class="sxs-lookup"><span data-stu-id="62380-890">Quebec</span></span>
- <span data-ttu-id="62380-891">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="62380-891">Northwest Territories</span></span>
- <span data-ttu-id="62380-892">Ontario</span><span class="sxs-lookup"><span data-stu-id="62380-892">Ontario</span></span>
- <span data-ttu-id="62380-893">British Columbia</span><span class="sxs-lookup"><span data-stu-id="62380-893">British Columbia</span></span>
- <span data-ttu-id="62380-894">Alberta</span><span class="sxs-lookup"><span data-stu-id="62380-894">Alberta</span></span>
- <span data-ttu-id="62380-895">Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="62380-895">Saskatchewan</span></span>
- <span data-ttu-id="62380-896">Manitoba</span><span class="sxs-lookup"><span data-stu-id="62380-896">Manitoba</span></span>
- <span data-ttu-id="62380-897">Yukon</span><span class="sxs-lookup"><span data-stu-id="62380-897">Yukon</span></span>
- <span data-ttu-id="62380-898">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="62380-898">Newfoundland and Labrador</span></span>
- <span data-ttu-id="62380-899">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="62380-899">New Brunswick</span></span>
- <span data-ttu-id="62380-900">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="62380-900">Nova Scotia</span></span>
- <span data-ttu-id="62380-901">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="62380-901">Prince Edward Island</span></span>
- <span data-ttu-id="62380-902">Kanada</span><span class="sxs-lookup"><span data-stu-id="62380-902">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="62380-903">Kanadische Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-903">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-904">Format</span><span class="sxs-lookup"><span data-stu-id="62380-904">Format</span></span>

<span data-ttu-id="62380-905">Neun Ziffern mit optionalen Bindestrichen oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-905">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-906">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-906">Pattern</span></span>

<span data-ttu-id="62380-907">Formatiert</span><span class="sxs-lookup"><span data-stu-id="62380-907">Formatted:</span></span>
- <span data-ttu-id="62380-908">Drei Ziffern </span><span class="sxs-lookup"><span data-stu-id="62380-908">Three digits</span></span> 
- <span data-ttu-id="62380-909">Ein Bindestrich oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-909">A hyphen or space</span></span> 
- <span data-ttu-id="62380-910">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-910">Three digits</span></span> 
- <span data-ttu-id="62380-911">Ein Bindestrich oder Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-911">A hyphen or space</span></span> 
- <span data-ttu-id="62380-912">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-912">Three digits</span></span>

<span data-ttu-id="62380-913">Unformatiert: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-913">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-914">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-914">Checksum</span></span>

<span data-ttu-id="62380-915">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-915">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-916">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-916">Definition</span></span>

<span data-ttu-id="62380-917">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-917">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-918">Die Funktion Func_canadian_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-918">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-919">Mindestens zwei dieser eine beliebige Kombination der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="62380-919">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="62380-920">Ein Schlüsselwort aus Keyword_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-920">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="62380-921">Ein Schlüsselwort aus Keyword_sin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-921">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="62380-922">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="62380-922">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="62380-923">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-923">The checksum passes.</span></span>

<span data-ttu-id="62380-924">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-924">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-925">Die Funktion Func_unformatted_canadian_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-925">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-926">Ein Schlüsselwort aus Keyword_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-926">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="62380-927">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-927">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-928">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-928">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="62380-929">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="62380-929">Keyword_sin</span></span>

- <span data-ttu-id="62380-930">sin</span><span class="sxs-lookup"><span data-stu-id="62380-930">sin</span></span> 
- <span data-ttu-id="62380-931">social insurance</span><span class="sxs-lookup"><span data-stu-id="62380-931">social insurance</span></span> 
- <span data-ttu-id="62380-932">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="62380-932">numero d'assurance sociale</span></span> 
- <span data-ttu-id="62380-933">Todsünden</span><span class="sxs-lookup"><span data-stu-id="62380-933">sins</span></span> 
- <span data-ttu-id="62380-934">SSN</span><span class="sxs-lookup"><span data-stu-id="62380-934">ssn</span></span> 
- <span data-ttu-id="62380-935">SSNs</span><span class="sxs-lookup"><span data-stu-id="62380-935">ssns</span></span> 
- <span data-ttu-id="62380-936">social security</span><span class="sxs-lookup"><span data-stu-id="62380-936">social security</span></span> 
- <span data-ttu-id="62380-937">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="62380-937">numero d'assurance social</span></span> 
- <span data-ttu-id="62380-938">national identification number</span><span class="sxs-lookup"><span data-stu-id="62380-938">national identification number</span></span> 
- <span data-ttu-id="62380-939">national id</span><span class="sxs-lookup"><span data-stu-id="62380-939">national id</span></span> 
- <span data-ttu-id="62380-940">Sünde</span><span class="sxs-lookup"><span data-stu-id="62380-940">sin#</span></span> 
- <span data-ttu-id="62380-941">soc ins</span><span class="sxs-lookup"><span data-stu-id="62380-941">soc ins</span></span> 
- <span data-ttu-id="62380-942">social ins</span><span class="sxs-lookup"><span data-stu-id="62380-942">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="62380-943">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="62380-943">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="62380-944">driver's license</span><span class="sxs-lookup"><span data-stu-id="62380-944">driver's license</span></span> 
- <span data-ttu-id="62380-945">drivers license</span><span class="sxs-lookup"><span data-stu-id="62380-945">drivers license</span></span> 
- <span data-ttu-id="62380-946">driver's licence</span><span class="sxs-lookup"><span data-stu-id="62380-946">driver's licence</span></span> 
- <span data-ttu-id="62380-947">drivers licence</span><span class="sxs-lookup"><span data-stu-id="62380-947">drivers licence</span></span> 
- <span data-ttu-id="62380-948">DOB</span><span class="sxs-lookup"><span data-stu-id="62380-948">DOB</span></span> 
- <span data-ttu-id="62380-949">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="62380-949">Birthdate</span></span> 
- <span data-ttu-id="62380-950">Geburtstag</span><span class="sxs-lookup"><span data-stu-id="62380-950">Birthday</span></span> 
- <span data-ttu-id="62380-951">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="62380-951">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="62380-952">	Chile Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="62380-952">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-953">Format</span><span class="sxs-lookup"><span data-stu-id="62380-953">Format</span></span>

<span data-ttu-id="62380-954">7-8 Ziffern Plus Trennzeichen eine Prüfziffer oder ein Buchstaben</span><span class="sxs-lookup"><span data-stu-id="62380-954">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-955">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-955">Pattern</span></span>

<span data-ttu-id="62380-956">7-8 Ziffern plus Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="62380-956">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="62380-957">1-2 Ziffern </span><span class="sxs-lookup"><span data-stu-id="62380-957">1-2 digits</span></span> 
- <span data-ttu-id="62380-958">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="62380-958">A period</span></span> 
- <span data-ttu-id="62380-959">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-959">Three digits</span></span> 
- <span data-ttu-id="62380-960">Ein Punkt </span><span class="sxs-lookup"><span data-stu-id="62380-960">A period</span></span> 
- <span data-ttu-id="62380-961">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-961">Three digits</span></span> 
- <span data-ttu-id="62380-962">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-962">A dash</span></span> 
- <span data-ttu-id="62380-963">Eine Ziffer oder ein Buchstabe (Groß-/Kleinschreibung nicht unterschieden), die bzw. der eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="62380-963">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-964">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-964">Checksum</span></span>

<span data-ttu-id="62380-965">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-966">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-966">Definition</span></span>

<span data-ttu-id="62380-967">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-967">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-968">Die Funktion Func_chile_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-968">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-969">Ein Schlüsselwort aus Keyword_chile_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-969">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="62380-970">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-970">The checksum passes.</span></span>

<span data-ttu-id="62380-971">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-971">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-972">Die Funktion Func_chile_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-972">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-973">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-973">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-974">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-974">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="62380-975">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="62380-975">Keyword_chile_id_card</span></span>

- <span data-ttu-id="62380-976">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="62380-976">National Identification Number</span></span> 
- <span data-ttu-id="62380-977">Identity card</span><span class="sxs-lookup"><span data-stu-id="62380-977">Identity card</span></span> 
- <span data-ttu-id="62380-978">ID</span><span class="sxs-lookup"><span data-stu-id="62380-978">ID</span></span> 
- <span data-ttu-id="62380-979">Identifikations</span><span class="sxs-lookup"><span data-stu-id="62380-979">Identification</span></span> 
- <span data-ttu-id="62380-980">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="62380-980">Rol Único Nacional</span></span> 
- <span data-ttu-id="62380-981">FÜHREN</span><span class="sxs-lookup"><span data-stu-id="62380-981">RUN</span></span> 
- <span data-ttu-id="62380-982">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="62380-982">Rol Único Tributario</span></span> 
- <span data-ttu-id="62380-983">RUT</span><span class="sxs-lookup"><span data-stu-id="62380-983">RUT</span></span> 
- <span data-ttu-id="62380-984">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="62380-984">Cédula de Identidad</span></span> 
- <span data-ttu-id="62380-985">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="62380-985">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="62380-986">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="62380-986">Tarjeta de identificación</span></span> 
- <span data-ttu-id="62380-987">Identificación</span><span class="sxs-lookup"><span data-stu-id="62380-987">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="62380-988">	China (PRC) – Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="62380-988">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-989">Format</span><span class="sxs-lookup"><span data-stu-id="62380-989">Format</span></span>

<span data-ttu-id="62380-990">18 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-990">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-991">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-991">Pattern</span></span>

<span data-ttu-id="62380-992">18 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-992">18 digits:</span></span>
- <span data-ttu-id="62380-993">Sechs Ziffern, die einen Adresscode angeben </span><span class="sxs-lookup"><span data-stu-id="62380-993">Six digits which are an address code</span></span> 
- <span data-ttu-id="62380-994">Acht Ziffern im Fomat JJJJMMTT, wobei es sich um das Geburtsdatum handelt </span><span class="sxs-lookup"><span data-stu-id="62380-994">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="62380-995">Drei Ziffern, die ein Reihenfolgencode sind </span><span class="sxs-lookup"><span data-stu-id="62380-995">Three digits which are an order code</span></span> 
- <span data-ttu-id="62380-996">Eine Ziffer als Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="62380-996">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-997">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-997">Checksum</span></span>

<span data-ttu-id="62380-998">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-998">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-999">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-999">Definition</span></span>

<span data-ttu-id="62380-1000">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1000">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1001">Die Funktion Func_china_resident_id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-1001">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1002">Ein Schlüsselwort aus Keyword_china_resident_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1002">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="62380-1003">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1003">The checksum passes.</span></span>

<span data-ttu-id="62380-1004">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1005">Die Funktion Func_china_resident_id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-1005">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1006">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1006">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-1007">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1007">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="62380-1008">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="62380-1008">Keyword_china_resident_id</span></span>

- <span data-ttu-id="62380-1009">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="62380-1009">Resident Identity Card</span></span> 
- <span data-ttu-id="62380-1010">PRC</span><span class="sxs-lookup"><span data-stu-id="62380-1010">PRC</span></span> 
- <span data-ttu-id="62380-1011">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="62380-1011">National Identification Card</span></span> 
- <span data-ttu-id="62380-1012">身份证</span><span class="sxs-lookup"><span data-stu-id="62380-1012">身份证</span></span> 
- <span data-ttu-id="62380-1013">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="62380-1013">居民 身份证</span></span> 
- <span data-ttu-id="62380-1014">居民身份证</span><span class="sxs-lookup"><span data-stu-id="62380-1014">居民身份证</span></span> 
- <span data-ttu-id="62380-1015">鉴定</span><span class="sxs-lookup"><span data-stu-id="62380-1015">鉴定</span></span> 
- <span data-ttu-id="62380-1016">身分證</span><span class="sxs-lookup"><span data-stu-id="62380-1016">身分證</span></span> 
- <span data-ttu-id="62380-1017">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="62380-1017">居民 身份證</span></span>
- <span data-ttu-id="62380-1018">鑑定</span><span class="sxs-lookup"><span data-stu-id="62380-1018">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="62380-1019">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="62380-1019">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1020">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1020">Format</span></span>

<span data-ttu-id="62380-1021">16 Ziffern, die formatiert oder unformatiert (dddddddddddddddd) werden können und den Luhn-Test bestehen müssen.</span><span class="sxs-lookup"><span data-stu-id="62380-1021">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1022">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1022">Pattern</span></span>

<span data-ttu-id="62380-1023">Sehr komplexe und robuste Muster, die Karten aller wichtigen Marken weltweit, einschließlich Visa, MasterCard, Discover-Karte, JCB, American Express, Geschenkgutscheine und Restaurantkarten erkennen.</span><span class="sxs-lookup"><span data-stu-id="62380-1023">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1024">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1024">Checksum</span></span>

<span data-ttu-id="62380-1025">Ja, die Luhn-Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1025">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1026">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1026">Definition</span></span>

<span data-ttu-id="62380-1027">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1027">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1028">Die Funktion Func_credit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-1028">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1029">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="62380-1029">One of the following is true:</span></span>
    - <span data-ttu-id="62380-1030">Ein Schlüsselwort aus Keyword_cc_verification wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1030">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="62380-1031">Ein Schlüsselwort aus Keyword_cc_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1031">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="62380-1032">Die Funktion Func_expiration_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="62380-1032">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="62380-1033">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1033">The checksum passes.</span></span>

<span data-ttu-id="62380-1034">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1034">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1035">Die Funktion Func_credit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-1035">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1036">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1036">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-1037">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1037">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="62380-1038">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="62380-1038">Keyword_cc_verification</span></span>

- <span data-ttu-id="62380-1039">card verification</span><span class="sxs-lookup"><span data-stu-id="62380-1039">card verification</span></span>
- <span data-ttu-id="62380-1040">card identification number</span><span class="sxs-lookup"><span data-stu-id="62380-1040">card identification number</span></span>
- <span data-ttu-id="62380-1041">CVN</span><span class="sxs-lookup"><span data-stu-id="62380-1041">cvn</span></span>
- <span data-ttu-id="62380-1042">cid</span><span class="sxs-lookup"><span data-stu-id="62380-1042">cid</span></span>
- <span data-ttu-id="62380-1043">CVC2</span><span class="sxs-lookup"><span data-stu-id="62380-1043">cvc2</span></span>
- <span data-ttu-id="62380-1044">CVV2</span><span class="sxs-lookup"><span data-stu-id="62380-1044">cvv2</span></span>
- <span data-ttu-id="62380-1045">pin block</span><span class="sxs-lookup"><span data-stu-id="62380-1045">pin block</span></span>
- <span data-ttu-id="62380-1046">security code</span><span class="sxs-lookup"><span data-stu-id="62380-1046">security code</span></span>
- <span data-ttu-id="62380-1047">security number</span><span class="sxs-lookup"><span data-stu-id="62380-1047">security number</span></span>
- <span data-ttu-id="62380-1048">security no</span><span class="sxs-lookup"><span data-stu-id="62380-1048">security no</span></span>
- <span data-ttu-id="62380-1049">issue number</span><span class="sxs-lookup"><span data-stu-id="62380-1049">issue number</span></span>
- <span data-ttu-id="62380-1050">issue no</span><span class="sxs-lookup"><span data-stu-id="62380-1050">issue no</span></span>
- <span data-ttu-id="62380-1051">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="62380-1051">cryptogramme</span></span>
- <span data-ttu-id="62380-1052">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="62380-1052">numéro de sécurité</span></span>
- <span data-ttu-id="62380-1053">numero de securite</span><span class="sxs-lookup"><span data-stu-id="62380-1053">numero de securite</span></span>
- <span data-ttu-id="62380-1054">Kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1054">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="62380-1055">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1055">kreditkartenprufnummer</span></span>
- <span data-ttu-id="62380-1056">Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="62380-1056">prüfziffer</span></span>
- <span data-ttu-id="62380-1057">prufziffer</span><span class="sxs-lookup"><span data-stu-id="62380-1057">prufziffer</span></span>
- <span data-ttu-id="62380-1058">Sicherheitskode</span><span class="sxs-lookup"><span data-stu-id="62380-1058">sicherheits Kode</span></span>
- <span data-ttu-id="62380-1059">Sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="62380-1059">sicherheitscode</span></span>
- <span data-ttu-id="62380-1060">Sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1060">sicherheitsnummer</span></span>
- <span data-ttu-id="62380-1061">Verfalldatum</span><span class="sxs-lookup"><span data-stu-id="62380-1061">verfalldatum</span></span>
- <span data-ttu-id="62380-1062">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="62380-1062">codice di verifica</span></span>
- <span data-ttu-id="62380-1063">COD.</span><span class="sxs-lookup"><span data-stu-id="62380-1063">cod.</span></span> <span data-ttu-id="62380-1064">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="62380-1064">sicurezza</span></span>
- <span data-ttu-id="62380-1065">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="62380-1065">cod sicurezza</span></span>
- <span data-ttu-id="62380-1066">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="62380-1066">n autorizzazione</span></span>
- <span data-ttu-id="62380-1067">Código</span><span class="sxs-lookup"><span data-stu-id="62380-1067">código</span></span>
- <span data-ttu-id="62380-1068">codigo</span><span class="sxs-lookup"><span data-stu-id="62380-1068">codigo</span></span>
- <span data-ttu-id="62380-1069">COD.</span><span class="sxs-lookup"><span data-stu-id="62380-1069">cod.</span></span> <span data-ttu-id="62380-1070">SEG</span><span class="sxs-lookup"><span data-stu-id="62380-1070">seg</span></span>
- <span data-ttu-id="62380-1071">cod seg</span><span class="sxs-lookup"><span data-stu-id="62380-1071">cod seg</span></span>
- <span data-ttu-id="62380-1072">código de segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1072">código de segurança</span></span>
- <span data-ttu-id="62380-1073">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="62380-1073">codigo de seguranca</span></span>
- <span data-ttu-id="62380-1074">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1074">codigo de segurança</span></span>
- <span data-ttu-id="62380-1075">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="62380-1075">código de seguranca</span></span>
- <span data-ttu-id="62380-1076">cód.</span><span class="sxs-lookup"><span data-stu-id="62380-1076">cód.</span></span> <span data-ttu-id="62380-1077">Segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1077">segurança</span></span>
- <span data-ttu-id="62380-1078">COD.</span><span class="sxs-lookup"><span data-stu-id="62380-1078">cod.</span></span> <span data-ttu-id="62380-1079">Seguranca COD.</span><span class="sxs-lookup"><span data-stu-id="62380-1079">seguranca cod.</span></span> <span data-ttu-id="62380-1080">Segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1080">segurança</span></span>
- <span data-ttu-id="62380-1081">cód.</span><span class="sxs-lookup"><span data-stu-id="62380-1081">cód.</span></span> <span data-ttu-id="62380-1082">Seguranca</span><span class="sxs-lookup"><span data-stu-id="62380-1082">seguranca</span></span>
- <span data-ttu-id="62380-1083">cód segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1083">cód segurança</span></span>
- <span data-ttu-id="62380-1084">COD Seguranca COD Segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1084">cod seguranca cod segurança</span></span>
- <span data-ttu-id="62380-1085">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="62380-1085">cód seguranca</span></span>
- <span data-ttu-id="62380-1086">número de verificação</span><span class="sxs-lookup"><span data-stu-id="62380-1086">número de verificação</span></span>
- <span data-ttu-id="62380-1087">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="62380-1087">numero de verificacao</span></span>
- <span data-ttu-id="62380-1088">Ablauf</span><span class="sxs-lookup"><span data-stu-id="62380-1088">ablauf</span></span>
- <span data-ttu-id="62380-1089">Gültig bis</span><span class="sxs-lookup"><span data-stu-id="62380-1089">gültig bis</span></span>
- <span data-ttu-id="62380-1090">Gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="62380-1090">gültigkeitsdatum</span></span>
- <span data-ttu-id="62380-1091">Gultig bis</span><span class="sxs-lookup"><span data-stu-id="62380-1091">gultig bis</span></span>
- <span data-ttu-id="62380-1092">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="62380-1092">gultigkeitsdatum</span></span>
- <span data-ttu-id="62380-1093">scadenza</span><span class="sxs-lookup"><span data-stu-id="62380-1093">scadenza</span></span>
- <span data-ttu-id="62380-1094">data scad</span><span class="sxs-lookup"><span data-stu-id="62380-1094">data scad</span></span>
- <span data-ttu-id="62380-1095">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="62380-1095">fecha de expiracion</span></span>
- <span data-ttu-id="62380-1096">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="62380-1096">fecha de venc</span></span>
- <span data-ttu-id="62380-1097">vencimiento</span><span class="sxs-lookup"><span data-stu-id="62380-1097">vencimiento</span></span>
- <span data-ttu-id="62380-1098">válido hasta</span><span class="sxs-lookup"><span data-stu-id="62380-1098">válido hasta</span></span>
- <span data-ttu-id="62380-1099">valido hasta</span><span class="sxs-lookup"><span data-stu-id="62380-1099">valido hasta</span></span>
- <span data-ttu-id="62380-1100">VTO</span><span class="sxs-lookup"><span data-stu-id="62380-1100">vto</span></span>
- <span data-ttu-id="62380-1101">data de expiração</span><span class="sxs-lookup"><span data-stu-id="62380-1101">data de expiração</span></span>
- <span data-ttu-id="62380-1102">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="62380-1102">data de expiracao</span></span>
- <span data-ttu-id="62380-1103">data em que expira</span><span class="sxs-lookup"><span data-stu-id="62380-1103">data em que expira</span></span>
- <span data-ttu-id="62380-1104">validade</span><span class="sxs-lookup"><span data-stu-id="62380-1104">validade</span></span>
- <span data-ttu-id="62380-1105">Valor</span><span class="sxs-lookup"><span data-stu-id="62380-1105">valor</span></span>
- <span data-ttu-id="62380-1106">vencimento</span><span class="sxs-lookup"><span data-stu-id="62380-1106">vencimento</span></span>
- <span data-ttu-id="62380-1107">Venc</span><span class="sxs-lookup"><span data-stu-id="62380-1107">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="62380-1108">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="62380-1108">Keyword_cc_name</span></span>

- <span data-ttu-id="62380-1109">Amex</span><span class="sxs-lookup"><span data-stu-id="62380-1109">amex</span></span>
- <span data-ttu-id="62380-1110">american express</span><span class="sxs-lookup"><span data-stu-id="62380-1110">american express</span></span>
- <span data-ttu-id="62380-1111">AmericanExpress</span><span class="sxs-lookup"><span data-stu-id="62380-1111">americanexpress</span></span>
- <span data-ttu-id="62380-1112">Visa</span><span class="sxs-lookup"><span data-stu-id="62380-1112">Visa</span></span>
- <span data-ttu-id="62380-1113">Card</span><span class="sxs-lookup"><span data-stu-id="62380-1113">mastercard</span></span>
- <span data-ttu-id="62380-1114">master card</span><span class="sxs-lookup"><span data-stu-id="62380-1114">master card</span></span>
- <span data-ttu-id="62380-1115">MC</span><span class="sxs-lookup"><span data-stu-id="62380-1115">mc</span></span> 
- <span data-ttu-id="62380-1116">MasterCards gesichert</span><span class="sxs-lookup"><span data-stu-id="62380-1116">mastercards</span></span>
- <span data-ttu-id="62380-1117">master cards</span><span class="sxs-lookup"><span data-stu-id="62380-1117">master cards</span></span>
- <span data-ttu-id="62380-1118">diner's Club</span><span class="sxs-lookup"><span data-stu-id="62380-1118">diner's Club</span></span>
- <span data-ttu-id="62380-1119">diners club</span><span class="sxs-lookup"><span data-stu-id="62380-1119">diners club</span></span>
- <span data-ttu-id="62380-1120">DinersClub</span><span class="sxs-lookup"><span data-stu-id="62380-1120">dinersclub</span></span>
- <span data-ttu-id="62380-1121">discover card</span><span class="sxs-lookup"><span data-stu-id="62380-1121">discover card</span></span>
- <span data-ttu-id="62380-1122">discovercard</span><span class="sxs-lookup"><span data-stu-id="62380-1122">discovercard</span></span>
- <span data-ttu-id="62380-1123">discover cards</span><span class="sxs-lookup"><span data-stu-id="62380-1123">discover cards</span></span>
- <span data-ttu-id="62380-1124">JCB</span><span class="sxs-lookup"><span data-stu-id="62380-1124">JCB</span></span>
- <span data-ttu-id="62380-1125">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="62380-1125">japanese card bureau</span></span>
- <span data-ttu-id="62380-1126">carte blanche</span><span class="sxs-lookup"><span data-stu-id="62380-1126">carte blanche</span></span>
- <span data-ttu-id="62380-1127">CarteBlanche</span><span class="sxs-lookup"><span data-stu-id="62380-1127">carteblanche</span></span>
- <span data-ttu-id="62380-1128">credit card</span><span class="sxs-lookup"><span data-stu-id="62380-1128">credit card</span></span>
- <span data-ttu-id="62380-1129">CC</span><span class="sxs-lookup"><span data-stu-id="62380-1129">cc#</span></span>
- <span data-ttu-id="62380-1130">cc #:</span><span class="sxs-lookup"><span data-stu-id="62380-1130">cc#:</span></span>
- <span data-ttu-id="62380-1131">expiration date</span><span class="sxs-lookup"><span data-stu-id="62380-1131">expiration date</span></span>
- <span data-ttu-id="62380-1132">exp date</span><span class="sxs-lookup"><span data-stu-id="62380-1132">exp date</span></span>
- <span data-ttu-id="62380-1133">expiry date</span><span class="sxs-lookup"><span data-stu-id="62380-1133">expiry date</span></span>
- <span data-ttu-id="62380-1134">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="62380-1134">date d’expiration</span></span>
- <span data-ttu-id="62380-1135">date d'exp</span><span class="sxs-lookup"><span data-stu-id="62380-1135">date d'exp</span></span>
- <span data-ttu-id="62380-1136">date expiration</span><span class="sxs-lookup"><span data-stu-id="62380-1136">date expiration</span></span>
- <span data-ttu-id="62380-1137">bank card</span><span class="sxs-lookup"><span data-stu-id="62380-1137">bank card</span></span>
- <span data-ttu-id="62380-1138">Bankcard</span><span class="sxs-lookup"><span data-stu-id="62380-1138">bankcard</span></span>
- <span data-ttu-id="62380-1139">card number</span><span class="sxs-lookup"><span data-stu-id="62380-1139">card number</span></span>
- <span data-ttu-id="62380-1140">card num</span><span class="sxs-lookup"><span data-stu-id="62380-1140">card num</span></span>
- <span data-ttu-id="62380-1141">cardNumber</span><span class="sxs-lookup"><span data-stu-id="62380-1141">cardnumber</span></span>
- <span data-ttu-id="62380-1142">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="62380-1142">cardnumbers</span></span>
- <span data-ttu-id="62380-1143">card numbers</span><span class="sxs-lookup"><span data-stu-id="62380-1143">card numbers</span></span>
- <span data-ttu-id="62380-1144">CreditCard</span><span class="sxs-lookup"><span data-stu-id="62380-1144">creditcard</span></span>
- <span data-ttu-id="62380-1145">credit cards</span><span class="sxs-lookup"><span data-stu-id="62380-1145">credit cards</span></span>
- <span data-ttu-id="62380-1146">creditCards</span><span class="sxs-lookup"><span data-stu-id="62380-1146">creditcards</span></span>
- <span data-ttu-id="62380-1147">CCN</span><span class="sxs-lookup"><span data-stu-id="62380-1147">ccn</span></span>
- <span data-ttu-id="62380-1148">card holder</span><span class="sxs-lookup"><span data-stu-id="62380-1148">card holder</span></span>
- <span data-ttu-id="62380-1149">Karteninhaber</span><span class="sxs-lookup"><span data-stu-id="62380-1149">cardholder</span></span>
- <span data-ttu-id="62380-1150">card holders</span><span class="sxs-lookup"><span data-stu-id="62380-1150">card holders</span></span>
- <span data-ttu-id="62380-1151">Inhaber</span><span class="sxs-lookup"><span data-stu-id="62380-1151">cardholders</span></span>
- <span data-ttu-id="62380-1152">check card</span><span class="sxs-lookup"><span data-stu-id="62380-1152">check card</span></span>
- <span data-ttu-id="62380-1153">checkcard</span><span class="sxs-lookup"><span data-stu-id="62380-1153">checkcard</span></span>
- <span data-ttu-id="62380-1154">check cards</span><span class="sxs-lookup"><span data-stu-id="62380-1154">check cards</span></span>
- <span data-ttu-id="62380-1155">checkcards</span><span class="sxs-lookup"><span data-stu-id="62380-1155">checkcards</span></span>
- <span data-ttu-id="62380-1156">debit card</span><span class="sxs-lookup"><span data-stu-id="62380-1156">debit card</span></span>
- <span data-ttu-id="62380-1157">Debitkarte</span><span class="sxs-lookup"><span data-stu-id="62380-1157">debitcard</span></span>
- <span data-ttu-id="62380-1158">debit cards</span><span class="sxs-lookup"><span data-stu-id="62380-1158">debit cards</span></span>
- <span data-ttu-id="62380-1159">debitcards</span><span class="sxs-lookup"><span data-stu-id="62380-1159">debitcards</span></span>
- <span data-ttu-id="62380-1160">atm card</span><span class="sxs-lookup"><span data-stu-id="62380-1160">atm card</span></span>
- <span data-ttu-id="62380-1161">atmcard</span><span class="sxs-lookup"><span data-stu-id="62380-1161">atmcard</span></span>
- <span data-ttu-id="62380-1162">atm cards</span><span class="sxs-lookup"><span data-stu-id="62380-1162">atm cards</span></span>
- <span data-ttu-id="62380-1163">atmcards</span><span class="sxs-lookup"><span data-stu-id="62380-1163">atmcards</span></span>
- <span data-ttu-id="62380-1164">enroute</span><span class="sxs-lookup"><span data-stu-id="62380-1164">enroute</span></span>
- <span data-ttu-id="62380-1165">en route</span><span class="sxs-lookup"><span data-stu-id="62380-1165">en route</span></span>
- <span data-ttu-id="62380-1166">card type</span><span class="sxs-lookup"><span data-stu-id="62380-1166">card type</span></span>
- <span data-ttu-id="62380-1167">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="62380-1167">carte bancaire</span></span>
- <span data-ttu-id="62380-1168">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="62380-1168">carte de crédit</span></span>
- <span data-ttu-id="62380-1169">carte de credit</span><span class="sxs-lookup"><span data-stu-id="62380-1169">carte de credit</span></span>
- <span data-ttu-id="62380-1170">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="62380-1170">numéro de carte</span></span>
- <span data-ttu-id="62380-1171">numero de carte</span><span class="sxs-lookup"><span data-stu-id="62380-1171">numero de carte</span></span>
- <span data-ttu-id="62380-1172">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="62380-1172">nº de la carte</span></span>
- <span data-ttu-id="62380-1173">nº de carte</span><span class="sxs-lookup"><span data-stu-id="62380-1173">nº de carte</span></span>
- <span data-ttu-id="62380-1174">Kreditkarte</span><span class="sxs-lookup"><span data-stu-id="62380-1174">kreditkarte</span></span>
- <span data-ttu-id="62380-1175">Karte</span><span class="sxs-lookup"><span data-stu-id="62380-1175">karte</span></span>
- <span data-ttu-id="62380-1176">Karteninhaber</span><span class="sxs-lookup"><span data-stu-id="62380-1176">karteninhaber</span></span>
- <span data-ttu-id="62380-1177">Karteninhabers</span><span class="sxs-lookup"><span data-stu-id="62380-1177">karteninhabers</span></span>
- <span data-ttu-id="62380-1178">Kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="62380-1178">kreditkarteninhaber</span></span>
- <span data-ttu-id="62380-1179">Kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="62380-1179">kreditkarteninstitut</span></span>
- <span data-ttu-id="62380-1180">Kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="62380-1180">kreditkartentyp</span></span>
- <span data-ttu-id="62380-1181">Eigentümername</span><span class="sxs-lookup"><span data-stu-id="62380-1181">eigentümername</span></span>
- <span data-ttu-id="62380-1182">Kartennr</span><span class="sxs-lookup"><span data-stu-id="62380-1182">kartennr</span></span> 
- <span data-ttu-id="62380-1183">Kartennummer</span><span class="sxs-lookup"><span data-stu-id="62380-1183">kartennummer</span></span>
- <span data-ttu-id="62380-1184">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="62380-1184">kreditkartennummer</span></span>
- <span data-ttu-id="62380-1185">Kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="62380-1185">kreditkarten-nummer</span></span>
- <span data-ttu-id="62380-1186">carta di credito</span><span class="sxs-lookup"><span data-stu-id="62380-1186">carta di credito</span></span>
- <span data-ttu-id="62380-1187">carta credito</span><span class="sxs-lookup"><span data-stu-id="62380-1187">carta credito</span></span>
- <span data-ttu-id="62380-1188">Carta</span><span class="sxs-lookup"><span data-stu-id="62380-1188">carta</span></span>
- <span data-ttu-id="62380-1189">n carta</span><span class="sxs-lookup"><span data-stu-id="62380-1189">n carta</span></span>
- <span data-ttu-id="62380-1190">Nr.</span><span class="sxs-lookup"><span data-stu-id="62380-1190">nr.</span></span> <span data-ttu-id="62380-1191">Carta</span><span class="sxs-lookup"><span data-stu-id="62380-1191">carta</span></span>
- <span data-ttu-id="62380-1192">nr carta</span><span class="sxs-lookup"><span data-stu-id="62380-1192">nr carta</span></span>
- <span data-ttu-id="62380-1193">numero carta</span><span class="sxs-lookup"><span data-stu-id="62380-1193">numero carta</span></span>
- <span data-ttu-id="62380-1194">numero della carta</span><span class="sxs-lookup"><span data-stu-id="62380-1194">numero della carta</span></span>
- <span data-ttu-id="62380-1195">numero di carta</span><span class="sxs-lookup"><span data-stu-id="62380-1195">numero di carta</span></span>
- <span data-ttu-id="62380-1196">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="62380-1196">tarjeta credito</span></span>
- <span data-ttu-id="62380-1197">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="62380-1197">tarjeta de credito</span></span>
- <span data-ttu-id="62380-1198">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="62380-1198">tarjeta crédito</span></span>
- <span data-ttu-id="62380-1199">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="62380-1199">tarjeta de crédito</span></span>
- <span data-ttu-id="62380-1200">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="62380-1200">tarjeta de atm</span></span>
- <span data-ttu-id="62380-1201">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="62380-1201">tarjeta atm</span></span>
- <span data-ttu-id="62380-1202">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="62380-1202">tarjeta debito</span></span>
- <span data-ttu-id="62380-1203">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="62380-1203">tarjeta de debito</span></span>
- <span data-ttu-id="62380-1204">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="62380-1204">tarjeta débito</span></span>
- <span data-ttu-id="62380-1205">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="62380-1205">tarjeta de débito</span></span>
- <span data-ttu-id="62380-1206">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="62380-1206">nº de tarjeta</span></span>
- <span data-ttu-id="62380-1207">Nein.</span><span class="sxs-lookup"><span data-stu-id="62380-1207">no.</span></span> <span data-ttu-id="62380-1208">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="62380-1208">de tarjeta</span></span>
- <span data-ttu-id="62380-1209">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="62380-1209">no de tarjeta</span></span>
- <span data-ttu-id="62380-1210">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="62380-1210">numero de tarjeta</span></span>
- <span data-ttu-id="62380-1211">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="62380-1211">número de tarjeta</span></span>
- <span data-ttu-id="62380-1212">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="62380-1212">tarjeta no</span></span>
- <span data-ttu-id="62380-1213">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="62380-1213">tarjetahabiente</span></span>
- <span data-ttu-id="62380-1214">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="62380-1214">cartão de crédito</span></span>
- <span data-ttu-id="62380-1215">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="62380-1215">cartão de credito</span></span>
- <span data-ttu-id="62380-1216">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="62380-1216">cartao de crédito</span></span>
- <span data-ttu-id="62380-1217">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="62380-1217">cartao de credito</span></span>
- <span data-ttu-id="62380-1218">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="62380-1218">cartão de débito</span></span>
- <span data-ttu-id="62380-1219">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="62380-1219">cartao de débito</span></span>
- <span data-ttu-id="62380-1220">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="62380-1220">cartão de debito</span></span>
- <span data-ttu-id="62380-1221">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="62380-1221">cartao de debito</span></span>
- <span data-ttu-id="62380-1222">débito automático</span><span class="sxs-lookup"><span data-stu-id="62380-1222">débito automático</span></span>
- <span data-ttu-id="62380-1223">debito automatico</span><span class="sxs-lookup"><span data-stu-id="62380-1223">debito automatico</span></span>
- <span data-ttu-id="62380-1224">número do cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1224">número do cartão</span></span>
- <span data-ttu-id="62380-1225">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1225">numero do cartão</span></span> 
- <span data-ttu-id="62380-1226">número do cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1226">número do cartao</span></span>
- <span data-ttu-id="62380-1227">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1227">numero do cartao</span></span>
- <span data-ttu-id="62380-1228">número de cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1228">número de cartão</span></span>
- <span data-ttu-id="62380-1229">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1229">numero de cartão</span></span>
- <span data-ttu-id="62380-1230">número de cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1230">número de cartao</span></span>
- <span data-ttu-id="62380-1231">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1231">numero de cartao</span></span>
- <span data-ttu-id="62380-1232">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1232">nº do cartão</span></span>
- <span data-ttu-id="62380-1233">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1233">nº do cartao</span></span>
- <span data-ttu-id="62380-1234">nº.</span><span class="sxs-lookup"><span data-stu-id="62380-1234">nº.</span></span> <span data-ttu-id="62380-1235">do cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1235">do cartão</span></span>
- <span data-ttu-id="62380-1236">no do cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1236">no do cartão</span></span>
- <span data-ttu-id="62380-1237">no do cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1237">no do cartao</span></span>
- <span data-ttu-id="62380-1238">Nein.</span><span class="sxs-lookup"><span data-stu-id="62380-1238">no.</span></span> <span data-ttu-id="62380-1239">do cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1239">do cartão</span></span>
- <span data-ttu-id="62380-1240">Nein.</span><span class="sxs-lookup"><span data-stu-id="62380-1240">no.</span></span> <span data-ttu-id="62380-1241">do cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1241">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="62380-1242">	Kroatien – Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1242">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1243">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1243">Format</span></span>

<span data-ttu-id="62380-1244">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1245">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1245">Pattern</span></span>

<span data-ttu-id="62380-1246">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1247">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1247">Checksum</span></span>

<span data-ttu-id="62380-1248">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-1248">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1249">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1249">Definition</span></span>

<span data-ttu-id="62380-1250">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1251">Die Funktion Func_croatia_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-1251">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1252">Ein Schlüsselwort aus Keyword_croatia_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1252">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-1253">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1253">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="62380-1254">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="62380-1254">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="62380-1255">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="62380-1255">Croatian identity card</span></span>
- <span data-ttu-id="62380-1256">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="62380-1256">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="62380-1257">	Croatia Personal Identification (OIB) Number</span><span class="sxs-lookup"><span data-stu-id="62380-1257">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1258">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1258">Format</span></span>

<span data-ttu-id="62380-1259">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1259">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1260">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1260">Pattern</span></span>

<span data-ttu-id="62380-1261">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-1261">11 digits:</span></span>
- <span data-ttu-id="62380-1262">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1262">10 digits</span></span> 
- <span data-ttu-id="62380-1263">Die letzte Ziffer ist eine Prüfziffer für die Zwecke des internationalen Datenaustauschs, die Buchstaben HR werden vor den elf Ziffern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="62380-1263">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1264">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1264">Checksum</span></span>

<span data-ttu-id="62380-1265">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-1265">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1266">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1266">Definition</span></span>

<span data-ttu-id="62380-1267">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1267">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1268">Die Funktion Func_croatia_oib_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-1268">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1269">Ein Schlüsselwort aus Keyword_croatia_oib_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1269">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="62380-1270">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1270">The checksum passes.</span></span>

<span data-ttu-id="62380-1271">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1272">Die Funktion Func_croatia_oib_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-1272">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1273">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1273">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-1274">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1274">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="62380-1275">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="62380-1275">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="62380-1276">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="62380-1276">Personal Identification Number</span></span>
- <span data-ttu-id="62380-1277">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="62380-1277">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="62380-1278">OIB</span><span class="sxs-lookup"><span data-stu-id="62380-1278">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="62380-1279">Tschechische Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1279">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1280">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1280">Format</span></span>

<span data-ttu-id="62380-1281">Neun Ziffern mit optionalem Schrägstrich (altes Format) 10 Ziffern mit optionalem Schrägstrich (neues Format)</span><span class="sxs-lookup"><span data-stu-id="62380-1281">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1282">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1282">Pattern</span></span>

<span data-ttu-id="62380-1283">Neun Ziffern (altes Format):</span><span class="sxs-lookup"><span data-stu-id="62380-1283">Nine digits (old format):</span></span>
- <span data-ttu-id="62380-1284">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1284">Nine digits</span></span>

<span data-ttu-id="62380-1285">ODER</span><span class="sxs-lookup"><span data-stu-id="62380-1285">OR</span></span>

- <span data-ttu-id="62380-1286">Sechs Ziffern, die das Geburtsdatum darstellen</span><span class="sxs-lookup"><span data-stu-id="62380-1286">Six digits that represent date of birth</span></span>
- <span data-ttu-id="62380-1287">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="62380-1287">A forward slash</span></span>
- <span data-ttu-id="62380-1288">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1288">Three digits</span></span>

<span data-ttu-id="62380-1289">10 Ziffern (neues Format):</span><span class="sxs-lookup"><span data-stu-id="62380-1289">10 digits (new format):</span></span>
- <span data-ttu-id="62380-1290">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1290">10 digits</span></span>

<span data-ttu-id="62380-1291">ODER</span><span class="sxs-lookup"><span data-stu-id="62380-1291">OR</span></span>

- <span data-ttu-id="62380-1292">Sechs Ziffern, die das Geburtsdatum darstellen</span><span class="sxs-lookup"><span data-stu-id="62380-1292">Six digits that represent date of birth</span></span>
- <span data-ttu-id="62380-1293">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="62380-1293">A forward slash</span></span> 
- <span data-ttu-id="62380-1294">Vier Ziffern, wobei die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="62380-1294">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1295">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1295">Checksum</span></span>

<span data-ttu-id="62380-1296">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-1296">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1297">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1297">Definition</span></span>

<span data-ttu-id="62380-1298">Eine DLP-Richtlinie ist 85% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: die Funktion Func_czech_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-1298">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="62380-1299">Ein Schlüsselwort aus Keyword_czech_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1299">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="62380-1300">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1300">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="62380-1301">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1301">Keywords</span></span>

- <span data-ttu-id="62380-1302">Tschechische Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1302">czech personal identity number</span></span>
- <span data-ttu-id="62380-1303">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="62380-1303">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="62380-1304">	Dänemark – Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1304">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1305">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1305">Format</span></span>

<span data-ttu-id="62380-1306">10 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="62380-1306">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1307">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1307">Pattern</span></span>

<span data-ttu-id="62380-1308">10 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-1308">10 digits:</span></span>
- <span data-ttu-id="62380-1309">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="62380-1309">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="62380-1310">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-1310">A hyphen</span></span> 
- <span data-ttu-id="62380-1311">Vier Ziffern, bei denen die letzte Ziffer eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="62380-1311">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1312">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1312">Checksum</span></span>

<span data-ttu-id="62380-1313">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-1313">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1314">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1314">Definition</span></span>

<span data-ttu-id="62380-1315">Eine DLP-Richtlinie ist 75% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: der reguläre Ausdruck Regex_denmark_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-1315">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="62380-1316">Ein Schlüsselwort aus Keyword_denmark_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1316">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="62380-1317">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1317">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-1318">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1318">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="62380-1319">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="62380-1319">Keyword_denmark_id</span></span>

- <span data-ttu-id="62380-1320">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="62380-1320">Personal Identification Number</span></span>
- <span data-ttu-id="62380-1321">CPR</span><span class="sxs-lookup"><span data-stu-id="62380-1321">CPR</span></span>
- <span data-ttu-id="62380-1322">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="62380-1322">Det Centrale Personregister</span></span>
- <span data-ttu-id="62380-1323">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="62380-1323">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="62380-1324">Drug Enforcement Agency (DEA)-Nummer</span><span class="sxs-lookup"><span data-stu-id="62380-1324">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1325">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1325">Format</span></span>

<span data-ttu-id="62380-1326">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1326">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1327">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1327">Pattern</span></span>

<span data-ttu-id="62380-1328">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="62380-1328">Pattern must include all of the following:</span></span>
- <span data-ttu-id="62380-1329">Einen Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) aus der folgenden Gruppe möglicher Buchstaben: abcdefghjklmnprstux, was einem Registrantencode entspricht</span><span class="sxs-lookup"><span data-stu-id="62380-1329">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="62380-1330">Ein Buchstabe (bei dem die Groß-und Kleinschreibung nicht beachtet wird), der dem ersten Buchstaben des Nachnamens des Registrants entspricht</span><span class="sxs-lookup"><span data-stu-id="62380-1330">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="62380-1331">Sieben Ziffern, von denen die letzte die Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="62380-1331">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1332">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1332">Checksum</span></span>

<span data-ttu-id="62380-1333">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-1333">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1334">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1334">Definition</span></span>

<span data-ttu-id="62380-1335">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1335">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1336">Die Funktion Func_dea_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-1336">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1337">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1337">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-1338">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1338">Keywords</span></span>

<span data-ttu-id="62380-1339">None</span><span class="sxs-lookup"><span data-stu-id="62380-1339">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="62380-1340">EU Debit Card-Nummer</span><span class="sxs-lookup"><span data-stu-id="62380-1340">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1341">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1341">Format</span></span>

<span data-ttu-id="62380-1342">16 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1342">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1343">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1343">Pattern</span></span>

<span data-ttu-id="62380-1344">Sehr komplexes und robustes Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1344">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1345">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1345">Checksum</span></span>

<span data-ttu-id="62380-1346">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-1346">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1347">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1347">Definition</span></span>

<span data-ttu-id="62380-1348">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1348">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1349">Die Funktion Func_eu_debit_card findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-1349">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1350">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="62380-1350">At least one of the following is true:</span></span>
    - <span data-ttu-id="62380-1351">Ein Schlüsselwort aus Keyword_eu_debit_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1351">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="62380-1352">Ein Schlüsselwort aus Keyword_card_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1352">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="62380-1353">Ein Schlüsselwort aus Keyword_card_security_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1353">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="62380-1354">Ein Schlüsselwort aus Keyword_card_expiration_terms_dict wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1354">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="62380-1355">Die Funktion Func_expiration_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="62380-1355">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="62380-1356">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1356">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-1357">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1357">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="62380-1358">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="62380-1358">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="62380-1359">account number</span><span class="sxs-lookup"><span data-stu-id="62380-1359">account number</span></span> 
- <span data-ttu-id="62380-1360">card number</span><span class="sxs-lookup"><span data-stu-id="62380-1360">card number</span></span> 
- <span data-ttu-id="62380-1361">card no.</span><span class="sxs-lookup"><span data-stu-id="62380-1361">card no.</span></span> 
- <span data-ttu-id="62380-1362">security number</span><span class="sxs-lookup"><span data-stu-id="62380-1362">security number</span></span> 
- <span data-ttu-id="62380-1363">CC</span><span class="sxs-lookup"><span data-stu-id="62380-1363">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="62380-1364">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="62380-1364">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="62380-1365">acct nbr</span><span class="sxs-lookup"><span data-stu-id="62380-1365">acct nbr</span></span> 
- <span data-ttu-id="62380-1366">acct num</span><span class="sxs-lookup"><span data-stu-id="62380-1366">acct num</span></span> 
- <span data-ttu-id="62380-1367">acct no</span><span class="sxs-lookup"><span data-stu-id="62380-1367">acct no</span></span> 
- <span data-ttu-id="62380-1368">american express</span><span class="sxs-lookup"><span data-stu-id="62380-1368">american express</span></span> 
- <span data-ttu-id="62380-1369">AmericanExpress</span><span class="sxs-lookup"><span data-stu-id="62380-1369">americanexpress</span></span> 
- <span data-ttu-id="62380-1370">americano espresso</span><span class="sxs-lookup"><span data-stu-id="62380-1370">americano espresso</span></span> 
- <span data-ttu-id="62380-1371">Amex</span><span class="sxs-lookup"><span data-stu-id="62380-1371">amex</span></span> 
- <span data-ttu-id="62380-1372">atm card</span><span class="sxs-lookup"><span data-stu-id="62380-1372">atm card</span></span> 
- <span data-ttu-id="62380-1373">atm cards</span><span class="sxs-lookup"><span data-stu-id="62380-1373">atm cards</span></span> 
- <span data-ttu-id="62380-1374">atm kaart</span><span class="sxs-lookup"><span data-stu-id="62380-1374">atm kaart</span></span> 
- <span data-ttu-id="62380-1375">atmcard</span><span class="sxs-lookup"><span data-stu-id="62380-1375">atmcard</span></span> 
- <span data-ttu-id="62380-1376">atmcards</span><span class="sxs-lookup"><span data-stu-id="62380-1376">atmcards</span></span> 
- <span data-ttu-id="62380-1377">atmkaart</span><span class="sxs-lookup"><span data-stu-id="62380-1377">atmkaart</span></span> 
- <span data-ttu-id="62380-1378">atmkaarten</span><span class="sxs-lookup"><span data-stu-id="62380-1378">atmkaarten</span></span> 
- <span data-ttu-id="62380-1379">Bancontact</span><span class="sxs-lookup"><span data-stu-id="62380-1379">bancontact</span></span> 
- <span data-ttu-id="62380-1380">bank card</span><span class="sxs-lookup"><span data-stu-id="62380-1380">bank card</span></span> 
- <span data-ttu-id="62380-1381">bankkaart</span><span class="sxs-lookup"><span data-stu-id="62380-1381">bankkaart</span></span> 
- <span data-ttu-id="62380-1382">card holder</span><span class="sxs-lookup"><span data-stu-id="62380-1382">card holder</span></span> 
- <span data-ttu-id="62380-1383">card holders</span><span class="sxs-lookup"><span data-stu-id="62380-1383">card holders</span></span> 
- <span data-ttu-id="62380-1384">card num</span><span class="sxs-lookup"><span data-stu-id="62380-1384">card num</span></span> 
- <span data-ttu-id="62380-1385">card number</span><span class="sxs-lookup"><span data-stu-id="62380-1385">card number</span></span> 
- <span data-ttu-id="62380-1386">card numbers</span><span class="sxs-lookup"><span data-stu-id="62380-1386">card numbers</span></span> 
- <span data-ttu-id="62380-1387">card type</span><span class="sxs-lookup"><span data-stu-id="62380-1387">card type</span></span> 
- <span data-ttu-id="62380-1388">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="62380-1388">cardano numerico</span></span> 
- <span data-ttu-id="62380-1389">Karteninhaber</span><span class="sxs-lookup"><span data-stu-id="62380-1389">cardholder</span></span> 
- <span data-ttu-id="62380-1390">Inhaber</span><span class="sxs-lookup"><span data-stu-id="62380-1390">cardholders</span></span> 
- <span data-ttu-id="62380-1391">cardNumber</span><span class="sxs-lookup"><span data-stu-id="62380-1391">cardnumber</span></span> 
- <span data-ttu-id="62380-1392">cardnumbers</span><span class="sxs-lookup"><span data-stu-id="62380-1392">cardnumbers</span></span> 
- <span data-ttu-id="62380-1393">carta bianca</span><span class="sxs-lookup"><span data-stu-id="62380-1393">carta bianca</span></span> 
- <span data-ttu-id="62380-1394">carta credito</span><span class="sxs-lookup"><span data-stu-id="62380-1394">carta credito</span></span> 
- <span data-ttu-id="62380-1395">carta di credito</span><span class="sxs-lookup"><span data-stu-id="62380-1395">carta di credito</span></span> 
- <span data-ttu-id="62380-1396">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="62380-1396">cartao de credito</span></span> 
- <span data-ttu-id="62380-1397">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="62380-1397">cartao de crédito</span></span> 
- <span data-ttu-id="62380-1398">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="62380-1398">cartao de debito</span></span> 
- <span data-ttu-id="62380-1399">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="62380-1399">cartao de débito</span></span> 
- <span data-ttu-id="62380-1400">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="62380-1400">carte bancaire</span></span> 
- <span data-ttu-id="62380-1401">carte blanche</span><span class="sxs-lookup"><span data-stu-id="62380-1401">carte blanche</span></span> 
- <span data-ttu-id="62380-1402">carte bleue</span><span class="sxs-lookup"><span data-stu-id="62380-1402">carte bleue</span></span> 
- <span data-ttu-id="62380-1403">carte de credit</span><span class="sxs-lookup"><span data-stu-id="62380-1403">carte de credit</span></span> 
- <span data-ttu-id="62380-1404">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="62380-1404">carte de crédit</span></span> 
- <span data-ttu-id="62380-1405">carte di credito</span><span class="sxs-lookup"><span data-stu-id="62380-1405">carte di credito</span></span> 
- <span data-ttu-id="62380-1406">CarteBlanche</span><span class="sxs-lookup"><span data-stu-id="62380-1406">carteblanche</span></span> 
- <span data-ttu-id="62380-1407">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="62380-1407">cartão de credito</span></span> 
- <span data-ttu-id="62380-1408">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="62380-1408">cartão de crédito</span></span> 
- <span data-ttu-id="62380-1409">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="62380-1409">cartão de debito</span></span> 
- <span data-ttu-id="62380-1410">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="62380-1410">cartão de débito</span></span> 
- <span data-ttu-id="62380-1411">cb</span><span class="sxs-lookup"><span data-stu-id="62380-1411">cb</span></span> 
- <span data-ttu-id="62380-1412">CCN</span><span class="sxs-lookup"><span data-stu-id="62380-1412">ccn</span></span> 
- <span data-ttu-id="62380-1413">check card</span><span class="sxs-lookup"><span data-stu-id="62380-1413">check card</span></span> 
- <span data-ttu-id="62380-1414">check cards</span><span class="sxs-lookup"><span data-stu-id="62380-1414">check cards</span></span> 
- <span data-ttu-id="62380-1415">checkcard</span><span class="sxs-lookup"><span data-stu-id="62380-1415">checkcard</span></span>
- <span data-ttu-id="62380-1416">checkcards</span><span class="sxs-lookup"><span data-stu-id="62380-1416">checkcards</span></span> 
- <span data-ttu-id="62380-1417">chequekaart</span><span class="sxs-lookup"><span data-stu-id="62380-1417">chequekaart</span></span> 
- <span data-ttu-id="62380-1418">Cirrus</span><span class="sxs-lookup"><span data-stu-id="62380-1418">cirrus</span></span> 
- <span data-ttu-id="62380-1419">Cirrus-EDC-Maestro</span><span class="sxs-lookup"><span data-stu-id="62380-1419">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="62380-1420">controlekaart</span><span class="sxs-lookup"><span data-stu-id="62380-1420">controlekaart</span></span> 
- <span data-ttu-id="62380-1421">controlekaarten</span><span class="sxs-lookup"><span data-stu-id="62380-1421">controlekaarten</span></span> 
- <span data-ttu-id="62380-1422">credit card</span><span class="sxs-lookup"><span data-stu-id="62380-1422">credit card</span></span> 
- <span data-ttu-id="62380-1423">credit cards</span><span class="sxs-lookup"><span data-stu-id="62380-1423">credit cards</span></span> 
- <span data-ttu-id="62380-1424">CreditCard</span><span class="sxs-lookup"><span data-stu-id="62380-1424">creditcard</span></span> 
- <span data-ttu-id="62380-1425">creditCards</span><span class="sxs-lookup"><span data-stu-id="62380-1425">creditcards</span></span> 
- <span data-ttu-id="62380-1426">debetkaart</span><span class="sxs-lookup"><span data-stu-id="62380-1426">debetkaart</span></span> 
- <span data-ttu-id="62380-1427">debetkaarten</span><span class="sxs-lookup"><span data-stu-id="62380-1427">debetkaarten</span></span> 
- <span data-ttu-id="62380-1428">debit card</span><span class="sxs-lookup"><span data-stu-id="62380-1428">debit card</span></span> 
- <span data-ttu-id="62380-1429">debit cards</span><span class="sxs-lookup"><span data-stu-id="62380-1429">debit cards</span></span> 
- <span data-ttu-id="62380-1430">Debitkarte</span><span class="sxs-lookup"><span data-stu-id="62380-1430">debitcard</span></span> 
- <span data-ttu-id="62380-1431">debitcards</span><span class="sxs-lookup"><span data-stu-id="62380-1431">debitcards</span></span> 
- <span data-ttu-id="62380-1432">debito automatico</span><span class="sxs-lookup"><span data-stu-id="62380-1432">debito automatico</span></span> 
- <span data-ttu-id="62380-1433">diners club</span><span class="sxs-lookup"><span data-stu-id="62380-1433">diners club</span></span> 
- <span data-ttu-id="62380-1434">DinersClub</span><span class="sxs-lookup"><span data-stu-id="62380-1434">dinersclub</span></span> 
- <span data-ttu-id="62380-1435">Entdecken</span><span class="sxs-lookup"><span data-stu-id="62380-1435">discover</span></span> 
- <span data-ttu-id="62380-1436">discover card</span><span class="sxs-lookup"><span data-stu-id="62380-1436">discover card</span></span> 
- <span data-ttu-id="62380-1437">discover cards</span><span class="sxs-lookup"><span data-stu-id="62380-1437">discover cards</span></span> 
- <span data-ttu-id="62380-1438">discovercard</span><span class="sxs-lookup"><span data-stu-id="62380-1438">discovercard</span></span> 
- <span data-ttu-id="62380-1439">discovercards</span><span class="sxs-lookup"><span data-stu-id="62380-1439">discovercards</span></span> 
- <span data-ttu-id="62380-1440">débito automático</span><span class="sxs-lookup"><span data-stu-id="62380-1440">débito automático</span></span>
- <span data-ttu-id="62380-1441">EDC</span><span class="sxs-lookup"><span data-stu-id="62380-1441">edc</span></span> 
- <span data-ttu-id="62380-1442">Eigentümername</span><span class="sxs-lookup"><span data-stu-id="62380-1442">eigentümername</span></span> 
- <span data-ttu-id="62380-1443">european debit card</span><span class="sxs-lookup"><span data-stu-id="62380-1443">european debit card</span></span> 
- <span data-ttu-id="62380-1444">hoofdkaart</span><span class="sxs-lookup"><span data-stu-id="62380-1444">hoofdkaart</span></span> 
- <span data-ttu-id="62380-1445">hoofdkaarten</span><span class="sxs-lookup"><span data-stu-id="62380-1445">hoofdkaarten</span></span> 
- <span data-ttu-id="62380-1446">in viaggio</span><span class="sxs-lookup"><span data-stu-id="62380-1446">in viaggio</span></span> 
- <span data-ttu-id="62380-1447">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="62380-1447">japanese card bureau</span></span> 
- <span data-ttu-id="62380-1448">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="62380-1448">japanse kaartdienst</span></span> 
- <span data-ttu-id="62380-1449">JCB</span><span class="sxs-lookup"><span data-stu-id="62380-1449">jcb</span></span> 
- <span data-ttu-id="62380-1450">Kaart</span><span class="sxs-lookup"><span data-stu-id="62380-1450">kaart</span></span> 
- <span data-ttu-id="62380-1451">kaart num</span><span class="sxs-lookup"><span data-stu-id="62380-1451">kaart num</span></span> 
- <span data-ttu-id="62380-1452">kaartaantal</span><span class="sxs-lookup"><span data-stu-id="62380-1452">kaartaantal</span></span> 
- <span data-ttu-id="62380-1453">kaartaantallen</span><span class="sxs-lookup"><span data-stu-id="62380-1453">kaartaantallen</span></span> 
- <span data-ttu-id="62380-1454">kaarthouder</span><span class="sxs-lookup"><span data-stu-id="62380-1454">kaarthouder</span></span> 
- <span data-ttu-id="62380-1455">kaarthouders</span><span class="sxs-lookup"><span data-stu-id="62380-1455">kaarthouders</span></span> 
- <span data-ttu-id="62380-1456">Karte</span><span class="sxs-lookup"><span data-stu-id="62380-1456">karte</span></span>  
- <span data-ttu-id="62380-1457">Karteninhaber</span><span class="sxs-lookup"><span data-stu-id="62380-1457">karteninhaber</span></span> 
- <span data-ttu-id="62380-1458">Karteninhabers</span><span class="sxs-lookup"><span data-stu-id="62380-1458">karteninhabers</span></span>
- <span data-ttu-id="62380-1459">Kartennr</span><span class="sxs-lookup"><span data-stu-id="62380-1459">kartennr</span></span> 
- <span data-ttu-id="62380-1460">Kartennummer</span><span class="sxs-lookup"><span data-stu-id="62380-1460">kartennummer</span></span> 
- <span data-ttu-id="62380-1461">Kreditkarte</span><span class="sxs-lookup"><span data-stu-id="62380-1461">kreditkarte</span></span> 
- <span data-ttu-id="62380-1462">Kreditkarten-Nummer</span><span class="sxs-lookup"><span data-stu-id="62380-1462">kreditkarten-nummer</span></span> 
- <span data-ttu-id="62380-1463">Kreditkarteninhaber</span><span class="sxs-lookup"><span data-stu-id="62380-1463">kreditkarteninhaber</span></span> 
- <span data-ttu-id="62380-1464">Kreditkarteninstitut</span><span class="sxs-lookup"><span data-stu-id="62380-1464">kreditkarteninstitut</span></span> 
- <span data-ttu-id="62380-1465">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="62380-1465">kreditkartennummer</span></span> 
- <span data-ttu-id="62380-1466">Kreditkartentyp</span><span class="sxs-lookup"><span data-stu-id="62380-1466">kreditkartentyp</span></span> 
- <span data-ttu-id="62380-1467">Maestro</span><span class="sxs-lookup"><span data-stu-id="62380-1467">maestro</span></span> 
- <span data-ttu-id="62380-1468">master card</span><span class="sxs-lookup"><span data-stu-id="62380-1468">master card</span></span> 
- <span data-ttu-id="62380-1469">master cards</span><span class="sxs-lookup"><span data-stu-id="62380-1469">master cards</span></span> 
- <span data-ttu-id="62380-1470">Card</span><span class="sxs-lookup"><span data-stu-id="62380-1470">mastercard</span></span> 
- <span data-ttu-id="62380-1471">MasterCards gesichert</span><span class="sxs-lookup"><span data-stu-id="62380-1471">mastercards</span></span> 
- <span data-ttu-id="62380-1472">MC</span><span class="sxs-lookup"><span data-stu-id="62380-1472">mc</span></span> 
- <span data-ttu-id="62380-1473">mister cash</span><span class="sxs-lookup"><span data-stu-id="62380-1473">mister cash</span></span> 
- <span data-ttu-id="62380-1474">n carta</span><span class="sxs-lookup"><span data-stu-id="62380-1474">n carta</span></span> 
- <span data-ttu-id="62380-1475">Carta</span><span class="sxs-lookup"><span data-stu-id="62380-1475">carta</span></span> 
- <span data-ttu-id="62380-1476">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="62380-1476">no de tarjeta</span></span> 
- <span data-ttu-id="62380-1477">no do cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1477">no do cartao</span></span> 
- <span data-ttu-id="62380-1478">no do cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1478">no do cartão</span></span> 
- <span data-ttu-id="62380-1479">Nein.</span><span class="sxs-lookup"><span data-stu-id="62380-1479">no.</span></span> <span data-ttu-id="62380-1480">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="62380-1480">de tarjeta</span></span> 
- <span data-ttu-id="62380-1481">Nein.</span><span class="sxs-lookup"><span data-stu-id="62380-1481">no.</span></span> <span data-ttu-id="62380-1482">do cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1482">do cartao</span></span> 
- <span data-ttu-id="62380-1483">Nein.</span><span class="sxs-lookup"><span data-stu-id="62380-1483">no.</span></span> <span data-ttu-id="62380-1484">do cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1484">do cartão</span></span> 
- <span data-ttu-id="62380-1485">nr carta</span><span class="sxs-lookup"><span data-stu-id="62380-1485">nr carta</span></span> 
- <span data-ttu-id="62380-1486">Nr.</span><span class="sxs-lookup"><span data-stu-id="62380-1486">nr.</span></span> <span data-ttu-id="62380-1487">Carta</span><span class="sxs-lookup"><span data-stu-id="62380-1487">carta</span></span> 
- <span data-ttu-id="62380-1488">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="62380-1488">numeri di scheda</span></span> 
- <span data-ttu-id="62380-1489">numero carta</span><span class="sxs-lookup"><span data-stu-id="62380-1489">numero carta</span></span> 
- <span data-ttu-id="62380-1490">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1490">numero de cartao</span></span> 
- <span data-ttu-id="62380-1491">numero de carte</span><span class="sxs-lookup"><span data-stu-id="62380-1491">numero de carte</span></span> 
- <span data-ttu-id="62380-1492">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1492">numero de cartão</span></span> 
- <span data-ttu-id="62380-1493">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="62380-1493">numero de tarjeta</span></span>
- <span data-ttu-id="62380-1494">numero della carta</span><span class="sxs-lookup"><span data-stu-id="62380-1494">numero della carta</span></span> 
- <span data-ttu-id="62380-1495">numero di carta</span><span class="sxs-lookup"><span data-stu-id="62380-1495">numero di carta</span></span> 
- <span data-ttu-id="62380-1496">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="62380-1496">numero di scheda</span></span> 
- <span data-ttu-id="62380-1497">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1497">numero do cartao</span></span> 
- <span data-ttu-id="62380-1498">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1498">numero do cartão</span></span> 
- <span data-ttu-id="62380-1499">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="62380-1499">numéro de carte</span></span> 
- <span data-ttu-id="62380-1500">nº carta</span><span class="sxs-lookup"><span data-stu-id="62380-1500">nº carta</span></span> 
- <span data-ttu-id="62380-1501">nº de carte</span><span class="sxs-lookup"><span data-stu-id="62380-1501">nº de carte</span></span> 
- <span data-ttu-id="62380-1502">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="62380-1502">nº de la carte</span></span> 
- <span data-ttu-id="62380-1503">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="62380-1503">nº de tarjeta</span></span> 
- <span data-ttu-id="62380-1504">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1504">nº do cartao</span></span> 
- <span data-ttu-id="62380-1505">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1505">nº do cartão</span></span> 
- <span data-ttu-id="62380-1506">nº.</span><span class="sxs-lookup"><span data-stu-id="62380-1506">nº.</span></span> <span data-ttu-id="62380-1507">do cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1507">do cartão</span></span> 
- <span data-ttu-id="62380-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1508">número de cartao</span></span> 
- <span data-ttu-id="62380-1509">número de cartão</span><span class="sxs-lookup"><span data-stu-id="62380-1509">número de cartão</span></span> 
- <span data-ttu-id="62380-1510">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="62380-1510">número de tarjeta</span></span> 
- <span data-ttu-id="62380-1511">número do cartao</span><span class="sxs-lookup"><span data-stu-id="62380-1511">número do cartao</span></span> 
- <span data-ttu-id="62380-1512">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="62380-1512">scheda dell'assegno</span></span> 
- <span data-ttu-id="62380-1513">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="62380-1513">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="62380-1514">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="62380-1514">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="62380-1515">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="62380-1515">scheda della banca</span></span> 
- <span data-ttu-id="62380-1516">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="62380-1516">scheda di controllo</span></span> 
- <span data-ttu-id="62380-1517">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="62380-1517">scheda di debito</span></span> 
- <span data-ttu-id="62380-1518">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="62380-1518">scheda matrice</span></span> 
- <span data-ttu-id="62380-1519">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="62380-1519">schede dell'atmosfera</span></span> 
- <span data-ttu-id="62380-1520">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="62380-1520">schede di controllo</span></span> 
- <span data-ttu-id="62380-1521">schede di debito</span><span class="sxs-lookup"><span data-stu-id="62380-1521">schede di debito</span></span> 
- <span data-ttu-id="62380-1522">schede matrici</span><span class="sxs-lookup"><span data-stu-id="62380-1522">schede matrici</span></span> 
- <span data-ttu-id="62380-1523">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="62380-1523">scoprono la scheda</span></span> 
- <span data-ttu-id="62380-1524">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="62380-1524">scoprono le schede</span></span> 
- <span data-ttu-id="62380-1525">Solo</span><span class="sxs-lookup"><span data-stu-id="62380-1525">solo</span></span> 
- <span data-ttu-id="62380-1526">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="62380-1526">supporti di scheda</span></span> 
- <span data-ttu-id="62380-1527">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="62380-1527">supporto di scheda</span></span> 
- <span data-ttu-id="62380-1528">Wechseln</span><span class="sxs-lookup"><span data-stu-id="62380-1528">switch</span></span> 
- <span data-ttu-id="62380-1529">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="62380-1529">tarjeta atm</span></span> 
- <span data-ttu-id="62380-1530">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="62380-1530">tarjeta credito</span></span> 
- <span data-ttu-id="62380-1531">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="62380-1531">tarjeta de atm</span></span> 
- <span data-ttu-id="62380-1532">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="62380-1532">tarjeta de credito</span></span> 
- <span data-ttu-id="62380-1533">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="62380-1533">tarjeta de debito</span></span> 
- <span data-ttu-id="62380-1534">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="62380-1534">tarjeta debito</span></span> 
- <span data-ttu-id="62380-1535">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="62380-1535">tarjeta no</span></span>
- <span data-ttu-id="62380-1536">tarjetahabiente</span><span class="sxs-lookup"><span data-stu-id="62380-1536">tarjetahabiente</span></span> 
- <span data-ttu-id="62380-1537">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="62380-1537">tipo della scheda</span></span> 
- <span data-ttu-id="62380-1538">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="62380-1538">ufficio giapponese della</span></span> 
- <span data-ttu-id="62380-1539">Scheda</span><span class="sxs-lookup"><span data-stu-id="62380-1539">scheda</span></span> 
- <span data-ttu-id="62380-1540">v pay</span><span class="sxs-lookup"><span data-stu-id="62380-1540">v pay</span></span> 
- <span data-ttu-id="62380-1541">v-Pay</span><span class="sxs-lookup"><span data-stu-id="62380-1541">v-pay</span></span> 
- <span data-ttu-id="62380-1542">Visa</span><span class="sxs-lookup"><span data-stu-id="62380-1542">visa</span></span> 
- <span data-ttu-id="62380-1543">visa plus</span><span class="sxs-lookup"><span data-stu-id="62380-1543">visa plus</span></span> 
- <span data-ttu-id="62380-1544">visa electron</span><span class="sxs-lookup"><span data-stu-id="62380-1544">visa electron</span></span> 
- <span data-ttu-id="62380-1545">Visto</span><span class="sxs-lookup"><span data-stu-id="62380-1545">visto</span></span> 
- <span data-ttu-id="62380-1546">Visum</span><span class="sxs-lookup"><span data-stu-id="62380-1546">visum</span></span> 
- <span data-ttu-id="62380-1547">vpay</span><span class="sxs-lookup"><span data-stu-id="62380-1547">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="62380-1548">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="62380-1548">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="62380-1549">card identification number</span><span class="sxs-lookup"><span data-stu-id="62380-1549">card identification number</span></span>
- <span data-ttu-id="62380-1550">card verification</span><span class="sxs-lookup"><span data-stu-id="62380-1550">card verification</span></span> 
- <span data-ttu-id="62380-1551">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="62380-1551">cardi la verifica</span></span> 
- <span data-ttu-id="62380-1552">cid</span><span class="sxs-lookup"><span data-stu-id="62380-1552">cid</span></span> 
- <span data-ttu-id="62380-1553">cod seg</span><span class="sxs-lookup"><span data-stu-id="62380-1553">cod seg</span></span> 
- <span data-ttu-id="62380-1554">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="62380-1554">cod seguranca</span></span> 
- <span data-ttu-id="62380-1555">cod segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1555">cod segurança</span></span> 
- <span data-ttu-id="62380-1556">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="62380-1556">cod sicurezza</span></span> 
- <span data-ttu-id="62380-1557">COD.</span><span class="sxs-lookup"><span data-stu-id="62380-1557">cod.</span></span> <span data-ttu-id="62380-1558">SEG</span><span class="sxs-lookup"><span data-stu-id="62380-1558">seg</span></span> 
- <span data-ttu-id="62380-1559">COD.</span><span class="sxs-lookup"><span data-stu-id="62380-1559">cod.</span></span> <span data-ttu-id="62380-1560">Seguranca</span><span class="sxs-lookup"><span data-stu-id="62380-1560">seguranca</span></span> 
- <span data-ttu-id="62380-1561">COD.</span><span class="sxs-lookup"><span data-stu-id="62380-1561">cod.</span></span> <span data-ttu-id="62380-1562">Segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1562">segurança</span></span> 
- <span data-ttu-id="62380-1563">COD.</span><span class="sxs-lookup"><span data-stu-id="62380-1563">cod.</span></span> <span data-ttu-id="62380-1564">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="62380-1564">sicurezza</span></span> 
- <span data-ttu-id="62380-1565">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="62380-1565">codice di sicurezza</span></span> 
- <span data-ttu-id="62380-1566">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="62380-1566">codice di verifica</span></span> 
- <span data-ttu-id="62380-1567">codigo</span><span class="sxs-lookup"><span data-stu-id="62380-1567">codigo</span></span> 
- <span data-ttu-id="62380-1568">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="62380-1568">codigo de seguranca</span></span> 
- <span data-ttu-id="62380-1569">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1569">codigo de segurança</span></span> 
- <span data-ttu-id="62380-1570">crittogramma</span><span class="sxs-lookup"><span data-stu-id="62380-1570">crittogramma</span></span> 
- <span data-ttu-id="62380-1571">Kryptogramm</span><span class="sxs-lookup"><span data-stu-id="62380-1571">cryptogram</span></span> 
- <span data-ttu-id="62380-1572">cryptogramme</span><span class="sxs-lookup"><span data-stu-id="62380-1572">cryptogramme</span></span> 
- <span data-ttu-id="62380-1573">CV2</span><span class="sxs-lookup"><span data-stu-id="62380-1573">cv2</span></span> 
- <span data-ttu-id="62380-1574">CVC</span><span class="sxs-lookup"><span data-stu-id="62380-1574">cvc</span></span> 
- <span data-ttu-id="62380-1575">CVC2</span><span class="sxs-lookup"><span data-stu-id="62380-1575">cvc2</span></span> 
- <span data-ttu-id="62380-1576">CVN</span><span class="sxs-lookup"><span data-stu-id="62380-1576">cvn</span></span> 
- <span data-ttu-id="62380-1577">CVV</span><span class="sxs-lookup"><span data-stu-id="62380-1577">cvv</span></span> 
- <span data-ttu-id="62380-1578">CVV2</span><span class="sxs-lookup"><span data-stu-id="62380-1578">cvv2</span></span> 
- <span data-ttu-id="62380-1579">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="62380-1579">cód seguranca</span></span> 
- <span data-ttu-id="62380-1580">cód segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1580">cód segurança</span></span> 
- <span data-ttu-id="62380-1581">cód.</span><span class="sxs-lookup"><span data-stu-id="62380-1581">cód.</span></span> <span data-ttu-id="62380-1582">Seguranca</span><span class="sxs-lookup"><span data-stu-id="62380-1582">seguranca</span></span> 
- <span data-ttu-id="62380-1583">cód.</span><span class="sxs-lookup"><span data-stu-id="62380-1583">cód.</span></span> <span data-ttu-id="62380-1584">Segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1584">segurança</span></span> 
- <span data-ttu-id="62380-1585">Código</span><span class="sxs-lookup"><span data-stu-id="62380-1585">código</span></span> 
- <span data-ttu-id="62380-1586">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="62380-1586">código de seguranca</span></span> 
- <span data-ttu-id="62380-1587">código de segurança</span><span class="sxs-lookup"><span data-stu-id="62380-1587">código de segurança</span></span> 
- <span data-ttu-id="62380-1588">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="62380-1588">de kaart controle</span></span> 
- <span data-ttu-id="62380-1589">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="62380-1589">geeft nr uit</span></span> 
- <span data-ttu-id="62380-1590">issue no</span><span class="sxs-lookup"><span data-stu-id="62380-1590">issue no</span></span> 
- <span data-ttu-id="62380-1591">issue number</span><span class="sxs-lookup"><span data-stu-id="62380-1591">issue number</span></span> 
- <span data-ttu-id="62380-1592">kaartidentificatienummer</span><span class="sxs-lookup"><span data-stu-id="62380-1592">kaartidentificatienummer</span></span> 
- <span data-ttu-id="62380-1593">kreditkartenprufnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1593">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="62380-1594">Kreditkartenprüfnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1594">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="62380-1595">kwestieaantal</span><span class="sxs-lookup"><span data-stu-id="62380-1595">kwestieaantal</span></span> 
- <span data-ttu-id="62380-1596">Nein.</span><span class="sxs-lookup"><span data-stu-id="62380-1596">no.</span></span> <span data-ttu-id="62380-1597">Dell ' edizione</span><span class="sxs-lookup"><span data-stu-id="62380-1597">dell'edizione</span></span> 
- <span data-ttu-id="62380-1598">Nein.</span><span class="sxs-lookup"><span data-stu-id="62380-1598">no.</span></span> <span data-ttu-id="62380-1599">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="62380-1599">di sicurezza</span></span> 
- <span data-ttu-id="62380-1600">numero de securite</span><span class="sxs-lookup"><span data-stu-id="62380-1600">numero de securite</span></span> 
- <span data-ttu-id="62380-1601">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="62380-1601">numero de verificacao</span></span> 
- <span data-ttu-id="62380-1602">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="62380-1602">numero dell'edizione</span></span> 
- <span data-ttu-id="62380-1603">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="62380-1603">numero di identificazione della</span></span> 
- <span data-ttu-id="62380-1604">Scheda</span><span class="sxs-lookup"><span data-stu-id="62380-1604">scheda</span></span> 
- <span data-ttu-id="62380-1605">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="62380-1605">numero di sicurezza</span></span> 
- <span data-ttu-id="62380-1606">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="62380-1606">numero van veiligheid</span></span> 
- <span data-ttu-id="62380-1607">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="62380-1607">numéro de sécurité</span></span> 
- <span data-ttu-id="62380-1608">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="62380-1608">nº autorizzazione</span></span> 
- <span data-ttu-id="62380-1609">número de verificação</span><span class="sxs-lookup"><span data-stu-id="62380-1609">número de verificação</span></span> 
- <span data-ttu-id="62380-1610">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="62380-1610">perno il blocco</span></span> 
- <span data-ttu-id="62380-1611">pin block</span><span class="sxs-lookup"><span data-stu-id="62380-1611">pin block</span></span> 
- <span data-ttu-id="62380-1612">prufziffer</span><span class="sxs-lookup"><span data-stu-id="62380-1612">prufziffer</span></span> 
- <span data-ttu-id="62380-1613">Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="62380-1613">prüfziffer</span></span> 
- <span data-ttu-id="62380-1614">security code</span><span class="sxs-lookup"><span data-stu-id="62380-1614">security code</span></span> 
- <span data-ttu-id="62380-1615">security no</span><span class="sxs-lookup"><span data-stu-id="62380-1615">security no</span></span> 
- <span data-ttu-id="62380-1616">security number</span><span class="sxs-lookup"><span data-stu-id="62380-1616">security number</span></span> 
- <span data-ttu-id="62380-1617">Sicherheitskode</span><span class="sxs-lookup"><span data-stu-id="62380-1617">sicherheits kode</span></span> 
- <span data-ttu-id="62380-1618">Sicherheitscode</span><span class="sxs-lookup"><span data-stu-id="62380-1618">sicherheitscode</span></span> 
- <span data-ttu-id="62380-1619">Sicherheitsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1619">sicherheitsnummer</span></span> 
- <span data-ttu-id="62380-1620">speldblok</span><span class="sxs-lookup"><span data-stu-id="62380-1620">speldblok</span></span> 
- <span data-ttu-id="62380-1621">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="62380-1621">veiligheid nr</span></span> 
- <span data-ttu-id="62380-1622">veiligheidsaantal</span><span class="sxs-lookup"><span data-stu-id="62380-1622">veiligheidsaantal</span></span> 
- <span data-ttu-id="62380-1623">veiligheidscode</span><span class="sxs-lookup"><span data-stu-id="62380-1623">veiligheidscode</span></span> 
- <span data-ttu-id="62380-1624">veiligheidsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1624">veiligheidsnummer</span></span> 
- <span data-ttu-id="62380-1625">Verfalldatum</span><span class="sxs-lookup"><span data-stu-id="62380-1625">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="62380-1626">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="62380-1626">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="62380-1627">Ablauf</span><span class="sxs-lookup"><span data-stu-id="62380-1627">ablauf</span></span> 
- <span data-ttu-id="62380-1628">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="62380-1628">data de expiracao</span></span> 
- <span data-ttu-id="62380-1629">data de expiração</span><span class="sxs-lookup"><span data-stu-id="62380-1629">data de expiração</span></span> 
- <span data-ttu-id="62380-1630">data del exp</span><span class="sxs-lookup"><span data-stu-id="62380-1630">data del exp</span></span> 
- <span data-ttu-id="62380-1631">data di exp</span><span class="sxs-lookup"><span data-stu-id="62380-1631">data di exp</span></span> 
- <span data-ttu-id="62380-1632">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="62380-1632">data di scadenza</span></span> 
- <span data-ttu-id="62380-1633">data em que expira</span><span class="sxs-lookup"><span data-stu-id="62380-1633">data em que expira</span></span> 
- <span data-ttu-id="62380-1634">data scad</span><span class="sxs-lookup"><span data-stu-id="62380-1634">data scad</span></span> 
- <span data-ttu-id="62380-1635">data scadenza</span><span class="sxs-lookup"><span data-stu-id="62380-1635">data scadenza</span></span> 
- <span data-ttu-id="62380-1636">date de validité</span><span class="sxs-lookup"><span data-stu-id="62380-1636">date de validité</span></span> 
- <span data-ttu-id="62380-1637">datum afloop</span><span class="sxs-lookup"><span data-stu-id="62380-1637">datum afloop</span></span> 
- <span data-ttu-id="62380-1638">datum van exp</span><span class="sxs-lookup"><span data-stu-id="62380-1638">datum van exp</span></span> 
- <span data-ttu-id="62380-1639">de afloop</span><span class="sxs-lookup"><span data-stu-id="62380-1639">de afloop</span></span> 
- <span data-ttu-id="62380-1640">Espira</span><span class="sxs-lookup"><span data-stu-id="62380-1640">espira</span></span> 
- <span data-ttu-id="62380-1641">Espira</span><span class="sxs-lookup"><span data-stu-id="62380-1641">espira</span></span> 
- <span data-ttu-id="62380-1642">exp date</span><span class="sxs-lookup"><span data-stu-id="62380-1642">exp date</span></span> 
- <span data-ttu-id="62380-1643">exp datum</span><span class="sxs-lookup"><span data-stu-id="62380-1643">exp datum</span></span> 
- <span data-ttu-id="62380-1644">Ablauf</span><span class="sxs-lookup"><span data-stu-id="62380-1644">expiration</span></span> 
- <span data-ttu-id="62380-1645">läuft</span><span class="sxs-lookup"><span data-stu-id="62380-1645">expire</span></span> 
- <span data-ttu-id="62380-1646">abläuft</span><span class="sxs-lookup"><span data-stu-id="62380-1646">expires</span></span> 
- <span data-ttu-id="62380-1647">Ablauf</span><span class="sxs-lookup"><span data-stu-id="62380-1647">expiry</span></span> 
- <span data-ttu-id="62380-1648">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="62380-1648">fecha de expiracion</span></span> 
- <span data-ttu-id="62380-1649">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="62380-1649">fecha de venc</span></span> 
- <span data-ttu-id="62380-1650">Gultig bis</span><span class="sxs-lookup"><span data-stu-id="62380-1650">gultig bis</span></span> 
- <span data-ttu-id="62380-1651">gultigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="62380-1651">gultigkeitsdatum</span></span> 
- <span data-ttu-id="62380-1652">Gültig bis</span><span class="sxs-lookup"><span data-stu-id="62380-1652">gültig bis</span></span> 
- <span data-ttu-id="62380-1653">Gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="62380-1653">gültigkeitsdatum</span></span> 
- <span data-ttu-id="62380-1654">la scadenza</span><span class="sxs-lookup"><span data-stu-id="62380-1654">la scadenza</span></span> 
- <span data-ttu-id="62380-1655">scadenza</span><span class="sxs-lookup"><span data-stu-id="62380-1655">scadenza</span></span> 
- <span data-ttu-id="62380-1656">valable</span><span class="sxs-lookup"><span data-stu-id="62380-1656">valable</span></span> 
- <span data-ttu-id="62380-1657">validade</span><span class="sxs-lookup"><span data-stu-id="62380-1657">validade</span></span> 
- <span data-ttu-id="62380-1658">valido hasta</span><span class="sxs-lookup"><span data-stu-id="62380-1658">valido hasta</span></span> 
- <span data-ttu-id="62380-1659">Valor</span><span class="sxs-lookup"><span data-stu-id="62380-1659">valor</span></span> 
- <span data-ttu-id="62380-1660">venc</span><span class="sxs-lookup"><span data-stu-id="62380-1660">venc</span></span> 
- <span data-ttu-id="62380-1661">vencimento</span><span class="sxs-lookup"><span data-stu-id="62380-1661">vencimento</span></span> 
- <span data-ttu-id="62380-1662">vencimiento</span><span class="sxs-lookup"><span data-stu-id="62380-1662">vencimiento</span></span> 
- <span data-ttu-id="62380-1663">verloopt</span><span class="sxs-lookup"><span data-stu-id="62380-1663">verloopt</span></span> 
- <span data-ttu-id="62380-1664">vervaldag</span><span class="sxs-lookup"><span data-stu-id="62380-1664">vervaldag</span></span> 
- <span data-ttu-id="62380-1665">vervaldatum</span><span class="sxs-lookup"><span data-stu-id="62380-1665">vervaldatum</span></span> 
- <span data-ttu-id="62380-1666">VTO</span><span class="sxs-lookup"><span data-stu-id="62380-1666">vto</span></span> 
- <span data-ttu-id="62380-1667">válido hasta</span><span class="sxs-lookup"><span data-stu-id="62380-1667">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="62380-1668">EU-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1668">EU Driver's License Number</span></span>

<span data-ttu-id="62380-1669">Weitere Informationen finden Sie unter [sicherheitsTyp für die EU-Treiber Lizenznummer](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="62380-1669">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="62380-1670">Nationale IdentifikationsNummer der EU</span><span class="sxs-lookup"><span data-stu-id="62380-1670">EU National Identification Number</span></span>

<span data-ttu-id="62380-1671">Weitere Informationen finden Sie unter [sensibler informationsTyp der EU-nationalen Identifikationsnummer](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="62380-1671">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="62380-1672">EU-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="62380-1672">EU Passport Number</span></span>

<span data-ttu-id="62380-1673">Weitere Informationen finden Sie unter Sicherheitstyp für die [EU-Passport-Nummer](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="62380-1673">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="62380-1674">EU-sozialVersicherungsNummer oder entsprechende ID</span><span class="sxs-lookup"><span data-stu-id="62380-1674">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="62380-1675">Weitere Informationen finden Sie unter [EU-Sozialversicherungsnummer oder entsprechende ID-vertraulicher Informationstyp](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="62380-1675">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="62380-1676">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="62380-1676">EU Tax Identification Number</span></span>

<span data-ttu-id="62380-1677">Weitere Informationen finden Sie unter Sicherheitstyp für die [EU-Steuernummer](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="62380-1677">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="62380-1678">Finland National ID (Finnischer Personalausweis)</span><span class="sxs-lookup"><span data-stu-id="62380-1678">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="62380-1679">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1679">Format</span></span>

<span data-ttu-id="62380-1680">Sechs Ziffern plus ein Zeichen, das ein Jahrhundert angibt, plus drei Ziffern plus einer Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="62380-1680">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1681">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1681">Pattern</span></span>

<span data-ttu-id="62380-1682">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="62380-1682">Pattern must include all of the following:</span></span>
- <span data-ttu-id="62380-1683">Sechs Ziffern im Format TTMMJJ, die ein Geburtsdatum darstellen</span><span class="sxs-lookup"><span data-stu-id="62380-1683">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="62380-1684">Jahrhundertkennzeichnung (entweder „-“, „+“ oder „a“)</span><span class="sxs-lookup"><span data-stu-id="62380-1684">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="62380-1685">Dreistellige persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1685">Three-digit personal identification number</span></span> 
- <span data-ttu-id="62380-1686">Eine Ziffer oder ein Buchstabe (Groß-/Kleinschreibung irrelevant), die bzw. der eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="62380-1686">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1687">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1687">Checksum</span></span>

<span data-ttu-id="62380-1688">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-1688">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1689">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1689">Definition</span></span>

<span data-ttu-id="62380-1690">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1690">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1691">Die Funktion Func_finnish_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-1691">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1692">Ein Schlüsselwort aus Keyword_finnish_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1692">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="62380-1693">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1693">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-1694">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1694">Keywords</span></span>

- <span data-ttu-id="62380-1695">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="62380-1695">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="62380-1696">Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="62380-1696">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="62380-1697">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="62380-1697">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="62380-1698">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="62380-1698">Personbeteckning</span></span>
- <span data-ttu-id="62380-1699">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="62380-1699">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="62380-1700">Finnland – Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1700">Finland Passport Number</span></span>

<span data-ttu-id="62380-1701">Format-Kombination aus neun Buchstaben und Ziffern Muster Kombination aus neun Buchstaben und Ziffern: zwei Buchstaben (ohne Berücksichtigung von Groß-/Kleinschreibung) siebenstellige prüfSumme keine Definition eine DLP-Richtlinie ist 75% sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn innerhalb eines Nähe von 300 Zeichen: der reguläre Ausdruck Regex_finland_passport_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-1701">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="62380-1702">Ein Schlüsselwort aus Keyword_finland_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1702">A keyword from Keyword_finland_passport_number is found.</span></span>
<span data-ttu-id="62380-1703"><!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="62380-1703"></span></span>
<span data-ttu-id="62380-1704">Schlüsselwörter Keyword_finland_passport_number Passport Passi</span><span class="sxs-lookup"><span data-stu-id="62380-1704">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="62380-1705">Französische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1705">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1706">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1706">Format</span></span>

<span data-ttu-id="62380-1707">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1707">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1708">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1708">Pattern</span></span>

<span data-ttu-id="62380-1709">12 Ziffern mit Validierung, um ähnliche Muster ( z. B. französische Telefonnummern) auszuschließen</span><span class="sxs-lookup"><span data-stu-id="62380-1709">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1710">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1710">Checksum</span></span>

<span data-ttu-id="62380-1711">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-1711">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1712">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1712">Definition</span></span>

<span data-ttu-id="62380-1713">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1713">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1714">Die Funktion Func_french_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-1714">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1715">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="62380-1715">At least one of the following is true:</span></span>
- <span data-ttu-id="62380-1716">Ein Schlüsselwort aus Keyword_french_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1716">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="62380-1717">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="62380-1717">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-1718">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1718">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="62380-1719">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="62380-1719">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="62380-1720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="62380-1720">drivers licence</span></span>
- <span data-ttu-id="62380-1721">drivers license</span><span class="sxs-lookup"><span data-stu-id="62380-1721">drivers license</span></span>
- <span data-ttu-id="62380-1722">Führerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1722">driving licence</span></span>
- <span data-ttu-id="62380-1723">driving license</span><span class="sxs-lookup"><span data-stu-id="62380-1723">driving license</span></span>
- <span data-ttu-id="62380-1724">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="62380-1724">permis de conduire</span></span>
- <span data-ttu-id="62380-1725">licence number</span><span class="sxs-lookup"><span data-stu-id="62380-1725">licence number</span></span>
- <span data-ttu-id="62380-1726">license number</span><span class="sxs-lookup"><span data-stu-id="62380-1726">license number</span></span>
- <span data-ttu-id="62380-1727">licence numbers</span><span class="sxs-lookup"><span data-stu-id="62380-1727">licence numbers</span></span>
- <span data-ttu-id="62380-1728">license numbers</span><span class="sxs-lookup"><span data-stu-id="62380-1728">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="62380-1729">Französische Carte nationale d'identité (CNI)</span><span class="sxs-lookup"><span data-stu-id="62380-1729">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="62380-1730">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1730">Format</span></span>

<span data-ttu-id="62380-1731">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1731">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1732">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1732">Pattern</span></span>

<span data-ttu-id="62380-1733">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1733">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1734">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1734">Checksum</span></span>

<span data-ttu-id="62380-1735">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-1735">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1736">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1736">Definition</span></span>

<span data-ttu-id="62380-1737">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1737">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1738">Der reguläre Ausdruck Regex_france_cni findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-1738">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-1739">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1739">Keywords</span></span>

<span data-ttu-id="62380-1740">None</span><span class="sxs-lookup"><span data-stu-id="62380-1740">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="62380-1741">Französische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1741">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1742">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1742">Format</span></span>

<span data-ttu-id="62380-1743">Neun Ziffern und Buchstaben</span><span class="sxs-lookup"><span data-stu-id="62380-1743">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1744">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1744">Pattern</span></span>

<span data-ttu-id="62380-1745">Neun Ziffern und Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="62380-1745">Nine digits and letters:</span></span>
- <span data-ttu-id="62380-1746">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1746">Two digits</span></span> 
- <span data-ttu-id="62380-1747">Zwei Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="62380-1747">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="62380-1748">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1748">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1749">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1749">Checksum</span></span>

<span data-ttu-id="62380-1750">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-1750">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1751">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1751">Definition</span></span>

<span data-ttu-id="62380-1752">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1752">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1753">Die Funktion Func_fr_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-1753">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1754">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1754">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-1755">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1755">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="62380-1756">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="62380-1756">Keyword_passport</span></span>

- <span data-ttu-id="62380-1757">Passport Number</span><span class="sxs-lookup"><span data-stu-id="62380-1757">Passport Number</span></span>
- <span data-ttu-id="62380-1758">Passport No</span><span class="sxs-lookup"><span data-stu-id="62380-1758">Passport No</span></span>
- <span data-ttu-id="62380-1759">Passport#</span><span class="sxs-lookup"><span data-stu-id="62380-1759">Passport #</span></span>
- <span data-ttu-id="62380-1760">Pass</span><span class="sxs-lookup"><span data-stu-id="62380-1760">Passport#</span></span>
- <span data-ttu-id="62380-1761">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="62380-1761">PassportID</span></span>
- <span data-ttu-id="62380-1762">Passportno</span><span class="sxs-lookup"><span data-stu-id="62380-1762">Passportno</span></span>
- <span data-ttu-id="62380-1763">passportnumber</span><span class="sxs-lookup"><span data-stu-id="62380-1763">passportnumber</span></span>
- <span data-ttu-id="62380-1764">パスポート</span><span class="sxs-lookup"><span data-stu-id="62380-1764">パスポート</span></span>
- <span data-ttu-id="62380-1765">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="62380-1765">パスポート番号</span></span>
- <span data-ttu-id="62380-1766">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="62380-1766">パスポートのNum</span></span>
- <span data-ttu-id="62380-1767">パスポート ＃</span><span class="sxs-lookup"><span data-stu-id="62380-1767">パスポート ＃</span></span> 
- <span data-ttu-id="62380-1768">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="62380-1768">Numéro de passeport</span></span>
- <span data-ttu-id="62380-1769">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="62380-1769">Passeport n °</span></span>
- <span data-ttu-id="62380-1770">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="62380-1770">Passeport Non</span></span>
- <span data-ttu-id="62380-1771">Passeport#</span><span class="sxs-lookup"><span data-stu-id="62380-1771">Passeport #</span></span>
- <span data-ttu-id="62380-1772">Passeport</span><span class="sxs-lookup"><span data-stu-id="62380-1772">Passeport#</span></span>
- <span data-ttu-id="62380-1773">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="62380-1773">PasseportNon</span></span>
- <span data-ttu-id="62380-1774">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="62380-1774">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="62380-1775">Französische Sozialversicherungsnummer (INSEE)</span><span class="sxs-lookup"><span data-stu-id="62380-1775">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="62380-1776">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1776">Format</span></span>

<span data-ttu-id="62380-1777">15 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1777">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1778">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1778">Pattern</span></span>

<span data-ttu-id="62380-1779">Muss einem von zwei Mustern entsprechen:</span><span class="sxs-lookup"><span data-stu-id="62380-1779">Must match one of two patterns:</span></span>
- <span data-ttu-id="62380-1780">13 Ziffern gefolgt von einem Leerzeichen, gefolgt von zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1780">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="62380-1781">oder</span><span class="sxs-lookup"><span data-stu-id="62380-1781">or</span></span>
- <span data-ttu-id="62380-1782">15 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1782">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1783">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1783">Checksum</span></span>

<span data-ttu-id="62380-1784">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-1784">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1785">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1785">Definition</span></span>

<span data-ttu-id="62380-1786">Eine DLP-Richtlinie ist zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1786">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1787">Die Funktion Func_french_insee oder Func_fr_insee sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-1787">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1788">Ein Schlüsselwort aus Keyword_fr_insee wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1788">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="62380-1789">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1789">The checksum passes.</span></span>

<span data-ttu-id="62380-1790">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1790">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1791">Die Funktion Func_french_insee oder Func_fr_insee sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-1791">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1792">Es wurde kein Schlüsselwort aus Keyword_fr_insee gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1792">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="62380-1793">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1793">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-1794">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1794">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="62380-1795">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="62380-1795">Keyword_fr_insee</span></span>

- <span data-ttu-id="62380-1796">INSEE</span><span class="sxs-lookup"><span data-stu-id="62380-1796">insee</span></span>
- <span data-ttu-id="62380-1797">securité sociale</span><span class="sxs-lookup"><span data-stu-id="62380-1797">securité sociale</span></span>
- <span data-ttu-id="62380-1798">securite sociale</span><span class="sxs-lookup"><span data-stu-id="62380-1798">securite sociale</span></span>
- <span data-ttu-id="62380-1799">national id</span><span class="sxs-lookup"><span data-stu-id="62380-1799">national id</span></span>
- <span data-ttu-id="62380-1800">national identification</span><span class="sxs-lookup"><span data-stu-id="62380-1800">national identification</span></span>
- <span data-ttu-id="62380-1801">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="62380-1801">numéro d'identité</span></span>
- <span data-ttu-id="62380-1802">no d'identité</span><span class="sxs-lookup"><span data-stu-id="62380-1802">no d'identité</span></span>
- <span data-ttu-id="62380-1803">Nein.</span><span class="sxs-lookup"><span data-stu-id="62380-1803">no.</span></span> <span data-ttu-id="62380-1804">d ' identité</span><span class="sxs-lookup"><span data-stu-id="62380-1804">d'identité</span></span>
- <span data-ttu-id="62380-1805">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="62380-1805">numero d'identite</span></span>
- <span data-ttu-id="62380-1806">no d'identite</span><span class="sxs-lookup"><span data-stu-id="62380-1806">no d'identite</span></span>
- <span data-ttu-id="62380-1807">Nein.</span><span class="sxs-lookup"><span data-stu-id="62380-1807">no.</span></span> <span data-ttu-id="62380-1808">d'identite</span><span class="sxs-lookup"><span data-stu-id="62380-1808">d'identite</span></span>
- <span data-ttu-id="62380-1809">social security number</span><span class="sxs-lookup"><span data-stu-id="62380-1809">social security number</span></span>
- <span data-ttu-id="62380-1810">social security code</span><span class="sxs-lookup"><span data-stu-id="62380-1810">social security code</span></span>
- <span data-ttu-id="62380-1811">social insurance number</span><span class="sxs-lookup"><span data-stu-id="62380-1811">social insurance number</span></span>
- <span data-ttu-id="62380-1812">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="62380-1812">le numéro d'identification nationale</span></span>
- <span data-ttu-id="62380-1813">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="62380-1813">d'identité nationale</span></span>
- <span data-ttu-id="62380-1814">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="62380-1814">numéro de sécurité sociale</span></span>
- <span data-ttu-id="62380-1815">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="62380-1815">le code de la sécurité sociale</span></span>
- <span data-ttu-id="62380-1816">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="62380-1816">numéro d'assurance sociale</span></span>
- <span data-ttu-id="62380-1817">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="62380-1817">numéro de sécu</span></span>
- <span data-ttu-id="62380-1818">code sécu</span><span class="sxs-lookup"><span data-stu-id="62380-1818">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="62380-1819">Deutsche Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1819">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1820">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1820">Format</span></span>

<span data-ttu-id="62380-1821">Kombination von 11 Ziffern und Buchstaben</span><span class="sxs-lookup"><span data-stu-id="62380-1821">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1822">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1822">Pattern</span></span>

<span data-ttu-id="62380-1823">11 Zahlen und Buchstaben (ohne Beachtung der Groß-/Kleinschreibung):</span><span class="sxs-lookup"><span data-stu-id="62380-1823">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="62380-1824">Eine Ziffer oder ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="62380-1824">A digit or letter</span></span> 
- <span data-ttu-id="62380-1825">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1825">Two digits</span></span> 
- <span data-ttu-id="62380-1826">Sechs Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="62380-1826">Six digits or letters</span></span> 
- <span data-ttu-id="62380-1827">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="62380-1827">A digit</span></span> 
- <span data-ttu-id="62380-1828">Eine Ziffer oder ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="62380-1828">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1829">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1829">Checksum</span></span>

<span data-ttu-id="62380-1830">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-1830">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1831">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1831">Definition</span></span>

<span data-ttu-id="62380-1832">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1833">Die Funktion Func_german_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-1833">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1834">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="62380-1834">At least one of the following is true:</span></span>
    - <span data-ttu-id="62380-1835">Ein Schlüsselwort aus Keyword_german_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1835">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="62380-1836">Ein Schlüsselwort aus Keyword_german_drivers_license_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1836">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="62380-1837">Ein Schlüsselwort aus Keyword_german_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1837">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="62380-1838">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1838">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-1839">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1839">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="62380-1840">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="62380-1840">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="62380-1841">Führerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1841">Führerschein</span></span>
- <span data-ttu-id="62380-1842">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1842">Fuhrerschein</span></span>
- <span data-ttu-id="62380-1843">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1843">Fuehrerschein</span></span>
- <span data-ttu-id="62380-1844">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1844">Führerscheinnummer</span></span>
- <span data-ttu-id="62380-1845">Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1845">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="62380-1846">Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1846">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="62380-1847">Führerschein-</span><span class="sxs-lookup"><span data-stu-id="62380-1847">Führerschein-</span></span> 
- <span data-ttu-id="62380-1848">Fuhrerschein-</span><span class="sxs-lookup"><span data-stu-id="62380-1848">Fuhrerschein-</span></span> 
- <span data-ttu-id="62380-1849">Fuehrerschein-</span><span class="sxs-lookup"><span data-stu-id="62380-1849">Fuehrerschein-</span></span> 
- <span data-ttu-id="62380-1850">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="62380-1850">FührerscheinnummerNr</span></span>
- <span data-ttu-id="62380-1851">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="62380-1851">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="62380-1852">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="62380-1852">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="62380-1853">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="62380-1853">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="62380-1854">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="62380-1854">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="62380-1855">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="62380-1855">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="62380-1856">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="62380-1856">Führerschein- Nr</span></span>
- <span data-ttu-id="62380-1857">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="62380-1857">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="62380-1858">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="62380-1858">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="62380-1859">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="62380-1859">Führerschein- Klasse</span></span> 
- <span data-ttu-id="62380-1860">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="62380-1860">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="62380-1861">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="62380-1861">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="62380-1862">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="62380-1862">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="62380-1863">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="62380-1863">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="62380-1864">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="62380-1864">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="62380-1865">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="62380-1865">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="62380-1866">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="62380-1866">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="62380-1867">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="62380-1867">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="62380-1868">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="62380-1868">Führerschein- Nr</span></span> 
- <span data-ttu-id="62380-1869">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="62380-1869">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="62380-1870">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="62380-1870">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="62380-1871">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="62380-1871">Führerschein- Klasse</span></span> 
- <span data-ttu-id="62380-1872">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="62380-1872">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="62380-1873">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="62380-1873">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="62380-1874">DL</span><span class="sxs-lookup"><span data-stu-id="62380-1874">DL</span></span> 
- <span data-ttu-id="62380-1875">DLS</span><span class="sxs-lookup"><span data-stu-id="62380-1875">DLS</span></span>
- <span data-ttu-id="62380-1876">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="62380-1876">Driv Lic</span></span> 
- <span data-ttu-id="62380-1877">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="62380-1877">Driv Licen</span></span> 
- <span data-ttu-id="62380-1878">Driv License</span><span class="sxs-lookup"><span data-stu-id="62380-1878">Driv License</span></span>
- <span data-ttu-id="62380-1879">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-1879">Driv Licenses</span></span> 
- <span data-ttu-id="62380-1880">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="62380-1880">Driv Licence</span></span> 
- <span data-ttu-id="62380-1881">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="62380-1881">Driv Licences</span></span> 
- <span data-ttu-id="62380-1882">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="62380-1882">Driv Lic</span></span> 
- <span data-ttu-id="62380-1883">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="62380-1883">Driver Licen</span></span> 
- <span data-ttu-id="62380-1884">Driver License</span><span class="sxs-lookup"><span data-stu-id="62380-1884">Driver License</span></span> 
- <span data-ttu-id="62380-1885">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-1885">Driver Licenses</span></span> 
- <span data-ttu-id="62380-1886">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="62380-1886">Driver Licence</span></span> 
- <span data-ttu-id="62380-1887">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="62380-1887">Driver Licences</span></span> 
- <span data-ttu-id="62380-1888">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="62380-1888">Drivers Lic</span></span> 
- <span data-ttu-id="62380-1889">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="62380-1889">Drivers Licen</span></span> 
- <span data-ttu-id="62380-1890">Drivers License</span><span class="sxs-lookup"><span data-stu-id="62380-1890">Drivers License</span></span> 
- <span data-ttu-id="62380-1891">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-1891">Drivers Licenses</span></span> 
- <span data-ttu-id="62380-1892">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="62380-1892">Drivers Licence</span></span> 
- <span data-ttu-id="62380-1893">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="62380-1893">Drivers Licences</span></span> 
- <span data-ttu-id="62380-1894">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="62380-1894">Driver's Lic</span></span> 
- <span data-ttu-id="62380-1895">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="62380-1895">Driver's Licen</span></span> 
- <span data-ttu-id="62380-1896">Driver's License</span><span class="sxs-lookup"><span data-stu-id="62380-1896">Driver's License</span></span> 
- <span data-ttu-id="62380-1897">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-1897">Driver's Licenses</span></span> 
- <span data-ttu-id="62380-1898">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="62380-1898">Driver's Licence</span></span> 
- <span data-ttu-id="62380-1899">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="62380-1899">Driver's Licences</span></span> 
- <span data-ttu-id="62380-1900">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="62380-1900">Driving Lic</span></span> 
- <span data-ttu-id="62380-1901">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="62380-1901">Driving Licen</span></span> 
- <span data-ttu-id="62380-1902">Driving License</span><span class="sxs-lookup"><span data-stu-id="62380-1902">Driving License</span></span> 
- <span data-ttu-id="62380-1903">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-1903">Driving Licenses</span></span> 
- <span data-ttu-id="62380-1904">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="62380-1904">Driving Licence</span></span> 
- <span data-ttu-id="62380-1905">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="62380-1905">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="62380-1906">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="62380-1906">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="62380-1907">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1907">Nr-Führerschein</span></span> 
- <span data-ttu-id="62380-1908">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1908">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="62380-1909">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1909">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="62380-1910">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1910">No-Führerschein</span></span> 
- <span data-ttu-id="62380-1911">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1911">No-Fuhrerschein</span></span> 
- <span data-ttu-id="62380-1912">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1912">No-Fuehrerschein</span></span> 
- <span data-ttu-id="62380-1913">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1913">N-Führerschein</span></span> 
- <span data-ttu-id="62380-1914">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1914">N-Fuhrerschein</span></span> 
- <span data-ttu-id="62380-1915">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1915">N-Fuehrerschein</span></span>
- <span data-ttu-id="62380-1916">Nr-Führerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1916">Nr-Führerschein</span></span> 
- <span data-ttu-id="62380-1917">Nr-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1917">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="62380-1918">Nr-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1918">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="62380-1919">No-Führerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1919">No-Führerschein</span></span> 
- <span data-ttu-id="62380-1920">No-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1920">No-Fuhrerschein</span></span> 
- <span data-ttu-id="62380-1921">No-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1921">No-Fuehrerschein</span></span> 
- <span data-ttu-id="62380-1922">N-Führerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1922">N-Führerschein</span></span> 
- <span data-ttu-id="62380-1923">N-Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1923">N-Fuhrerschein</span></span> 
- <span data-ttu-id="62380-1924">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="62380-1924">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="62380-1925">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="62380-1925">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="62380-1926">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="62380-1926">ausstellungsdatum</span></span>
- <span data-ttu-id="62380-1927">Ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="62380-1927">ausstellungsort</span></span>
- <span data-ttu-id="62380-1928">Ausstellende Behöde</span><span class="sxs-lookup"><span data-stu-id="62380-1928">ausstellende behöde</span></span>
- <span data-ttu-id="62380-1929">Ausstellende Behorde</span><span class="sxs-lookup"><span data-stu-id="62380-1929">ausstellende behorde</span></span>
- <span data-ttu-id="62380-1930">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="62380-1930">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="62380-1931">Deutsche Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1931">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1932">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1932">Format</span></span>

<span data-ttu-id="62380-1933">10 Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="62380-1933">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1934">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1934">Pattern</span></span>

<span data-ttu-id="62380-1935">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="62380-1935">Pattern must include all of the following:</span></span>
- <span data-ttu-id="62380-1936">Das erste Zeichen ist eine Ziffer oder ein Buchstabe aus dieser Gruppe (C, F, G, H, J, K)</span><span class="sxs-lookup"><span data-stu-id="62380-1936">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="62380-1937">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1937">Three digits</span></span> 
- <span data-ttu-id="62380-1938">Fünf Ziffern oder Buchstaben aus dieser Gruppe (C -H, J-N, P, R, T, V-Z)</span><span class="sxs-lookup"><span data-stu-id="62380-1938">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="62380-1939">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="62380-1939">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1940">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1940">Checksum</span></span>

<span data-ttu-id="62380-1941">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-1941">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1942">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1942">Definition</span></span>

<span data-ttu-id="62380-1943">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1943">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1944">Die Funktion Func_german_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-1944">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1945">Ein Schlüsselwort aus einer der fünf Schlüsselwortlisten wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1945">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="62380-1946">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1946">The checksum passes.</span></span>

<span data-ttu-id="62380-1947">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1947">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1948">Die Funktion Func_german_passport_data findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-1948">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1949">Ein Schlüsselwort aus einer der fünf Schlüsselwortlisten wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1949">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="62380-1950">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-1950">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-1951">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1951">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="62380-1952">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="62380-1952">Keyword_german_passport</span></span>

- <span data-ttu-id="62380-1953">Reisepass</span><span class="sxs-lookup"><span data-stu-id="62380-1953">reisepass</span></span>
- <span data-ttu-id="62380-1954">reisepasse</span><span class="sxs-lookup"><span data-stu-id="62380-1954">reisepasse</span></span>
- <span data-ttu-id="62380-1955">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1955">reisepassnummer</span></span>
- <span data-ttu-id="62380-1956">Pass</span><span class="sxs-lookup"><span data-stu-id="62380-1956">passport</span></span>
- <span data-ttu-id="62380-1957">Pässe</span><span class="sxs-lookup"><span data-stu-id="62380-1957">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="62380-1958">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="62380-1958">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="62380-1959">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="62380-1959">geburtsdatum</span></span>
- <span data-ttu-id="62380-1960">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="62380-1960">ausstellungsdatum</span></span>
- <span data-ttu-id="62380-1961">Ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="62380-1961">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="62380-1962">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="62380-1962">Keyword_german_passport_number</span></span>

<span data-ttu-id="62380-1963">No-Reisepass Nr-Reisepass</span><span class="sxs-lookup"><span data-stu-id="62380-1963">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="62380-1964">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="62380-1964">Keyword_german_passport1</span></span>

<span data-ttu-id="62380-1965">Reisepass-Nr</span><span class="sxs-lookup"><span data-stu-id="62380-1965">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="62380-1966">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="62380-1966">Keyword_german_passport2</span></span>

<span data-ttu-id="62380-1967">bnationalit. t</span><span class="sxs-lookup"><span data-stu-id="62380-1967">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="62380-1968">Deutsche Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1968">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-1969">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1969">Format</span></span>

<span data-ttu-id="62380-1970">Seit dem 1. November 2010: neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1970">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="62380-1971">Vom 1. April 1987 bis 31. Oktober 2010:10 Stellen</span><span class="sxs-lookup"><span data-stu-id="62380-1971">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1972">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1972">Pattern</span></span>

<span data-ttu-id="62380-1973">Seit 1. November 2010:</span><span class="sxs-lookup"><span data-stu-id="62380-1973">Since 1 November 2010:</span></span>
- <span data-ttu-id="62380-1974">Ein Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="62380-1974">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="62380-1975">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1975">Eight digits</span></span>

<span data-ttu-id="62380-1976">Vom 1. April 1987 bis 31. Oktober 2010:</span><span class="sxs-lookup"><span data-stu-id="62380-1976">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="62380-1977">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-1977">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-1978">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-1978">Checksum</span></span>

<span data-ttu-id="62380-1979">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-1979">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-1980">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-1980">Definition</span></span>

<span data-ttu-id="62380-1981">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-1981">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-1982">Der reguläre Ausdruck Regex_germany_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-1982">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-1983">Ein Schlüsselwort aus Keyword_germany_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-1983">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-1984">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-1984">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="62380-1985">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="62380-1985">Keyword_germany_id_card</span></span>

- <span data-ttu-id="62380-1986">Identity Card</span><span class="sxs-lookup"><span data-stu-id="62380-1986">Identity Card</span></span>
- <span data-ttu-id="62380-1987">ID</span><span class="sxs-lookup"><span data-stu-id="62380-1987">ID</span></span>
- <span data-ttu-id="62380-1988">Identifikations</span><span class="sxs-lookup"><span data-stu-id="62380-1988">Identification</span></span>
- <span data-ttu-id="62380-1989">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="62380-1989">Personalausweis</span></span>
- <span data-ttu-id="62380-1990">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-1990">Identifizierungsnummer</span></span>
- <span data-ttu-id="62380-1991">Ausweis</span><span class="sxs-lookup"><span data-stu-id="62380-1991">Ausweis</span></span>
- <span data-ttu-id="62380-1992">Identifikation</span><span class="sxs-lookup"><span data-stu-id="62380-1992">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="62380-1993">Griechenland – Personalausweis</span><span class="sxs-lookup"><span data-stu-id="62380-1993">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="62380-1994">Format</span><span class="sxs-lookup"><span data-stu-id="62380-1994">Format</span></span>

<span data-ttu-id="62380-1995">Kombination von 7-8 Buchstaben und Zahlen plus einem Gedankenstrich</span><span class="sxs-lookup"><span data-stu-id="62380-1995">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-1996">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-1996">Pattern</span></span>

<span data-ttu-id="62380-1997">Sieben Buchstaben und Zahlen (altes Format):</span><span class="sxs-lookup"><span data-stu-id="62380-1997">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="62380-1998">Ein Buchstabe (jeder Buchstabe des griechischen Alphabets) </span><span class="sxs-lookup"><span data-stu-id="62380-1998">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="62380-1999">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-1999">A dash</span></span> 
- <span data-ttu-id="62380-2000">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2000">Six digits</span></span>

<span data-ttu-id="62380-2001">Acht Buchstaben und Zahlen (neues Format):</span><span class="sxs-lookup"><span data-stu-id="62380-2001">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="62380-2002">Zwei Buchstaben, deren Großbuchstabe sowohl im griechischen als auch lateinischen Alphabet (ABEZHIKMNOPTYX) vorkommt </span><span class="sxs-lookup"><span data-stu-id="62380-2002">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="62380-2003">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-2003">A dash</span></span> 
- <span data-ttu-id="62380-2004">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2004">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2005">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2005">Checksum</span></span>

<span data-ttu-id="62380-2006">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2006">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2007">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2007">Definition</span></span>

<span data-ttu-id="62380-2008">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2008">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2009">Der reguläre Ausdruck Regex_greece_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2009">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2010">Ein Schlüsselwort aus Keyword_greece_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2010">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2011">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2011">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="62380-2012">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="62380-2012">Keyword_greece_id_card</span></span>

- <span data-ttu-id="62380-2013">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="62380-2013">Greek identity Card</span></span>
- <span data-ttu-id="62380-2014">Tautotita</span><span class="sxs-lookup"><span data-stu-id="62380-2014">Tautotita</span></span>
- <span data-ttu-id="62380-2015">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="62380-2015">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="62380-2016">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="62380-2016">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="62380-2017">Hongkong (HKID) - Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2017">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2018">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2018">Format</span></span>

<span data-ttu-id="62380-2019">Kombination aus 8-9Buchstaben und Zahlen sowie optionale Klammern um das letzte Zeichen</span><span class="sxs-lookup"><span data-stu-id="62380-2019">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2020">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2020">Pattern</span></span>

<span data-ttu-id="62380-2021">Kombination aus Buchstaben 8-9 Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="62380-2021">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="62380-2022">1-2 Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="62380-2022">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="62380-2023">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2023">Six digits</span></span> 
- <span data-ttu-id="62380-2024">Das letzte Zeichen (eine Ziffer oder der Buchstabe A), bei dem es sich um die Prüfziffer handelt, die optional in Klammern eingeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="62380-2024">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2025">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2025">Checksum</span></span>

<span data-ttu-id="62380-2026">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2026">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2027">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2027">Definition</span></span>

<span data-ttu-id="62380-2028">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2028">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2029">Die Funktion Func_hong_kong_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2029">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2030">Ein Schlüsselwort aus Keyword_hong_kong_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2030">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="62380-2031">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2031">The checksum passes.</span></span>

<span data-ttu-id="62380-2032">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2032">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2033">Die Funktion Func_hong_kong_id_card sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2033">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2034">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2034">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2035">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2035">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="62380-2036">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="62380-2036">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="62380-2037">Hongkong-Identitätskarte</span><span class="sxs-lookup"><span data-stu-id="62380-2037">hong kong identity card</span></span>
- <span data-ttu-id="62380-2038">HKIDC</span><span class="sxs-lookup"><span data-stu-id="62380-2038">HKIDC</span></span>
- <span data-ttu-id="62380-2039">id card</span><span class="sxs-lookup"><span data-stu-id="62380-2039">id card</span></span>
- <span data-ttu-id="62380-2040">identity card</span><span class="sxs-lookup"><span data-stu-id="62380-2040">identity card</span></span>
- <span data-ttu-id="62380-2041">HK-Identitätskarte</span><span class="sxs-lookup"><span data-stu-id="62380-2041">hk identity card</span></span>
- <span data-ttu-id="62380-2042">Hongkong-ID</span><span class="sxs-lookup"><span data-stu-id="62380-2042">hong kong id</span></span>
- <span data-ttu-id="62380-2043">香港身份證</span><span class="sxs-lookup"><span data-stu-id="62380-2043">香港身份證</span></span>
- <span data-ttu-id="62380-2044">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="62380-2044">香港永久性居民身份證</span></span>
- <span data-ttu-id="62380-2045">身份證</span><span class="sxs-lookup"><span data-stu-id="62380-2045">身份證</span></span>
- <span data-ttu-id="62380-2046">身份証</span><span class="sxs-lookup"><span data-stu-id="62380-2046">身份証</span></span>
- <span data-ttu-id="62380-2047">身分證</span><span class="sxs-lookup"><span data-stu-id="62380-2047">身分證</span></span>
- <span data-ttu-id="62380-2048">身分証</span><span class="sxs-lookup"><span data-stu-id="62380-2048">身分証</span></span>
- <span data-ttu-id="62380-2049">香港身份証</span><span class="sxs-lookup"><span data-stu-id="62380-2049">香港身份証</span></span>
- <span data-ttu-id="62380-2050">香港身分證</span><span class="sxs-lookup"><span data-stu-id="62380-2050">香港身分證</span></span>
- <span data-ttu-id="62380-2051">香港身分証</span><span class="sxs-lookup"><span data-stu-id="62380-2051">香港身分証</span></span>
- <span data-ttu-id="62380-2052">香港身份證</span><span class="sxs-lookup"><span data-stu-id="62380-2052">香港身份證</span></span>
- <span data-ttu-id="62380-2053">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="62380-2053">香港居民身份證</span></span>
- <span data-ttu-id="62380-2054">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="62380-2054">香港居民身份証</span></span>
- <span data-ttu-id="62380-2055">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="62380-2055">香港居民身分證</span></span>
- <span data-ttu-id="62380-2056">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="62380-2056">香港居民身分証</span></span>
- <span data-ttu-id="62380-2057">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="62380-2057">香港永久性居民身份証</span></span>
- <span data-ttu-id="62380-2058">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="62380-2058">香港永久性居民身分證</span></span>
- <span data-ttu-id="62380-2059">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="62380-2059">香港永久性居民身分証</span></span>
- <span data-ttu-id="62380-2060">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="62380-2060">香港永久性居民身份證</span></span>
- <span data-ttu-id="62380-2061">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="62380-2061">香港非永久性居民身份證</span></span>
- <span data-ttu-id="62380-2062">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="62380-2062">香港非永久性居民身份証</span></span>
- <span data-ttu-id="62380-2063">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="62380-2063">香港非永久性居民身分證</span></span>
- <span data-ttu-id="62380-2064">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="62380-2064">香港非永久性居民身分証</span></span>
- <span data-ttu-id="62380-2065">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="62380-2065">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="62380-2066">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="62380-2066">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="62380-2067">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="62380-2067">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="62380-2068">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="62380-2068">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="62380-2069">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="62380-2069">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="62380-2070">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="62380-2070">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="62380-2071">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="62380-2071">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="62380-2072">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="62380-2072">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="62380-2073">Indien – Permanente Kontonummer</span><span class="sxs-lookup"><span data-stu-id="62380-2073">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="62380-2074">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2074">Format</span></span>

<span data-ttu-id="62380-2075">10 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2075">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2076">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2076">Pattern</span></span>

<span data-ttu-id="62380-2077">10 Buchstaben oder Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2077">10 letters or digits:</span></span>
- <span data-ttu-id="62380-2078">Fünf Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="62380-2078">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="62380-2079">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2079">Four digits</span></span> 
- <span data-ttu-id="62380-2080">Ein Buchstabe, der eine alphabetische Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="62380-2080">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2081">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2081">Checksum</span></span>

<span data-ttu-id="62380-2082">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2083">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2083">Definition</span></span>

<span data-ttu-id="62380-2084">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2084">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2085">Der reguläre Ausdruck Regex_india_permanent_account_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2085">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2086">Ein Schlüsselwort aus Keyword_india_permanent_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2086">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="62380-2087">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2087">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2088">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2088">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="62380-2089">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="62380-2089">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="62380-2090">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="62380-2090">Permanent Account Number</span></span> 
- <span data-ttu-id="62380-2091">SCHWENKEN</span><span class="sxs-lookup"><span data-stu-id="62380-2091">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="62380-2092">Indien - Eindeutige Identifikationsnummer (Aadhaar)</span><span class="sxs-lookup"><span data-stu-id="62380-2092">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2093">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2093">Format</span></span>

<span data-ttu-id="62380-2094">12 Ziffern mit optionalen Leerzeichen oder Bindestrichen</span><span class="sxs-lookup"><span data-stu-id="62380-2094">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2095">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2095">Pattern</span></span>

<span data-ttu-id="62380-2096">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2096">12 digits:</span></span>
- <span data-ttu-id="62380-2097">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2097">Four digits</span></span> 
- <span data-ttu-id="62380-2098">Eine optionales Leerzeichen oder ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-2098">An optional space or dash</span></span> 
- <span data-ttu-id="62380-2099">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2099">Four digits</span></span> 
- <span data-ttu-id="62380-2100">Eine optionales Leerzeichen oder ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-2100">An optional space or dash</span></span> 
- <span data-ttu-id="62380-2101">Die letzte Ziffer, die eine Prüfziffer ist</span><span class="sxs-lookup"><span data-stu-id="62380-2101">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2102">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2102">Checksum</span></span>

<span data-ttu-id="62380-2103">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2103">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2104">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2104">Definition</span></span>

<span data-ttu-id="62380-2105">Eine DLP-Richtlinie ist 85% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: die Funktion Func_india_aadhaar findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2105">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="62380-2106">Ein Schlüsselwort aus Keyword_india_aadhar wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2106">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="62380-2107">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2107">The checksum passes.</span></span>
<span data-ttu-id="62380-2108">Eine DLP-Richtlinie ist 75% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: die Funktion Func_india_aadhaar findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2108">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="62380-2109">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2109">The checksum passes.</span></span>
<span data-ttu-id="62380-2110"><!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="62380-2110"></span></span>

### <a name="keywords"></a><span data-ttu-id="62380-2111">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2111">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="62380-2112">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="62380-2112">Keyword_india_aadhar</span></span>
- <span data-ttu-id="62380-2113">Aadhar</span><span class="sxs-lookup"><span data-stu-id="62380-2113">Aadhar</span></span>
- <span data-ttu-id="62380-2114">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="62380-2114">Aadhaar</span></span>
- <span data-ttu-id="62380-2115">UID</span><span class="sxs-lookup"><span data-stu-id="62380-2115">UID</span></span>
- <span data-ttu-id="62380-2116">आधार</span><span class="sxs-lookup"><span data-stu-id="62380-2116">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="62380-2117">Indonesien – Perosonalausweisnummer (KTP)</span><span class="sxs-lookup"><span data-stu-id="62380-2117">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2118">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2118">Format</span></span>

<span data-ttu-id="62380-2119">16 Ziffern mit optionalen Punkten</span><span class="sxs-lookup"><span data-stu-id="62380-2119">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2120">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2120">Pattern</span></span>

<span data-ttu-id="62380-2121">16 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2121">16 digits:</span></span>
- <span data-ttu-id="62380-2122">Zweistelliger Provinzcode </span><span class="sxs-lookup"><span data-stu-id="62380-2122">Two-digit province code</span></span> 
- <span data-ttu-id="62380-2123">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="62380-2123">A period (optional)</span></span> 
- <span data-ttu-id="62380-2124">Zweistelliger Regency- oder Stadtcode </span><span class="sxs-lookup"><span data-stu-id="62380-2124">Two-digit regency or city code</span></span> 
- <span data-ttu-id="62380-2125">Zweistelliger Subdistrict-Code </span><span class="sxs-lookup"><span data-stu-id="62380-2125">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="62380-2126">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="62380-2126">A period (optional)</span></span> 
- <span data-ttu-id="62380-2127">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="62380-2127">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="62380-2128">Ein Punkt (optional) </span><span class="sxs-lookup"><span data-stu-id="62380-2128">A period (optional)</span></span> 
- <span data-ttu-id="62380-2129">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2129">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2130">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2130">Checksum</span></span>

<span data-ttu-id="62380-2131">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2131">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2132">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2132">Definition</span></span>

<span data-ttu-id="62380-2133">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2133">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2134">Der reguläre Ausdruck Regex_indonesia_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2134">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2135">Ein Schlüsselwort aus Keyword_indonesia_id_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2135">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="62380-2136">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2137">Der reguläre Ausdruck Regex_indonesia_id_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2137">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2138">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2138">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="62380-2139">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="62380-2139">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="62380-2140">KTP</span><span class="sxs-lookup"><span data-stu-id="62380-2140">KTP</span></span>
- <span data-ttu-id="62380-2141">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="62380-2141">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="62380-2142">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="62380-2142">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="62380-2143">International Banking Account Number (IBAN)</span><span class="sxs-lookup"><span data-stu-id="62380-2143">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="62380-2144">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2144">Format</span></span>

<span data-ttu-id="62380-2145">Ländercode (zwei Buchstaben) plus Prüfziffern (zwei Ziffern) plus BBAN-Nummer (bis zu 30 Zeichen)</span><span class="sxs-lookup"><span data-stu-id="62380-2145">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2146">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2146">Pattern</span></span>

<span data-ttu-id="62380-2147">Das Muster muss Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="62380-2147">Pattern must include all of the following:</span></span>

- <span data-ttu-id="62380-2148">Ländercode aus zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="62380-2148">Two-letter country code</span></span>
- <span data-ttu-id="62380-2149">Zwei Prüfziffern (gefolgt von einem optionalen Leerzeichen)</span><span class="sxs-lookup"><span data-stu-id="62380-2149">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="62380-2150">1-7 Gruppen von vier Buchstaben oder Ziffern (können durch Leerzeichengetrennt werden)</span><span class="sxs-lookup"><span data-stu-id="62380-2150">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="62380-2151">1 bis 3 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2151">1-3 letters or digits</span></span>

<span data-ttu-id="62380-2152">Das Format für jedes Land ist geringfügig unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="62380-2152">The format for each country is slightly different.</span></span> <span data-ttu-id="62380-2153">Der Typ der vertraulichen IBAN-Informationen umfasst diese 60 Länder:</span><span class="sxs-lookup"><span data-stu-id="62380-2153">The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="62380-2154">AD, AE, Al, at, AZ, BA, be, BG, BH, ch, CR, CY, CZ, de, DK, Do, EE, es, fi, FO, Fr, GB, ge, GI, GL, GR, HR, HU, IE, IL, is, IT, kW, KZ, LB, Li, LU , NL, No, PL, PT, RO, RS, Sa, SE, Si, SK, SM, TN, TR, VG</span><span class="sxs-lookup"><span data-stu-id="62380-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2155">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2155">Checksum</span></span>

<span data-ttu-id="62380-2156">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2156">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2157">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2157">Definition</span></span>

<span data-ttu-id="62380-2158">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2158">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2159">Die Funktion Func_iban findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2159">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2160">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2160">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2161">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2161">Keywords</span></span>

<span data-ttu-id="62380-2162">None</span><span class="sxs-lookup"><span data-stu-id="62380-2162">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="62380-2163">IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="62380-2163">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="62380-2164">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2164">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="62380-2165">IPv4</span><span class="sxs-lookup"><span data-stu-id="62380-2165">IPv4:</span></span>
<span data-ttu-id="62380-2166">Komplexes Muster, das formatierte (Punkte) und unformatierte (keine Punkte) Versionen der IPv4-Adressen angibt</span><span class="sxs-lookup"><span data-stu-id="62380-2166">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="62380-2167">IPv6</span><span class="sxs-lookup"><span data-stu-id="62380-2167">IPv6:</span></span>
<span data-ttu-id="62380-2168"> Komplexes Muster, das formatierte IPv6-Nummern angibt (schließt Doppelpunkte ein)</span><span class="sxs-lookup"><span data-stu-id="62380-2168">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2169">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2169">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2170">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2170">Checksum</span></span>

<span data-ttu-id="62380-2171">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2172">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2172">Definition</span></span>

<span data-ttu-id="62380-2173">Für IPv6 ist eine DLP-Richtlinie zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2173">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2174">Der reguläre Ausdruck Regex_ipv6_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2174">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2175">Es wurde kein Schlüsselwort aus Keyword_ipaddress gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2175">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="62380-2176">Für IPv4 ist eine DLP-Richtlinie zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2176">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2177">Der reguläre Ausdruck Regex_ipv4_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2177">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2178">Ein Schlüsselwort aus Keyword_ipaddress wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2178">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="62380-2179">Für IPv6 ist eine DLP-Richtlinie zu 95 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2179">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2180">Der reguläre Ausdruck Regex_ipv6_address findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2180">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2181">Es wurde kein Schlüsselwort aus Keyword_ipaddress gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2181">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2182">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2182">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="62380-2183">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="62380-2183">Keyword_ipaddress</span></span>

- <span data-ttu-id="62380-2184">IP (bei diesem Schlüsselwort wird die Groß-/Kleinschreibung unterschieden)</span><span class="sxs-lookup"><span data-stu-id="62380-2184">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="62380-2185">ip address</span><span class="sxs-lookup"><span data-stu-id="62380-2185">ip address</span></span> 
- <span data-ttu-id="62380-2186">IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="62380-2186">ip addresses</span></span>
- <span data-ttu-id="62380-2187">internet protocol</span><span class="sxs-lookup"><span data-stu-id="62380-2187">internet protocol</span></span>
- <span data-ttu-id="62380-2188">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="62380-2188">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="62380-2189">Internationale Klassifikation von Krankheiten (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="62380-2189">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="62380-2190">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2190">Format</span></span>

<span data-ttu-id="62380-2191">Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="62380-2191">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2192">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2192">Pattern</span></span>

<span data-ttu-id="62380-2193">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="62380-2193">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2194">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2194">Checksum</span></span>

<span data-ttu-id="62380-2195">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2195">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2196">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2196">Definition</span></span>

<span data-ttu-id="62380-2197">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2197">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2198">Ein Schlüsselwort aus Dictionary_icd_10_cm wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2198">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="62380-2199">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2199">Keywords</span></span>

<span data-ttu-id="62380-2200">Ein beliebiger Begriff aus dem Dictionary_icd_10_cm-Stichwort Wörterbuch, das auf der [internationalen Klassifikation der Krankheiten, der zehnTen Revision, der klinischen Modifikation (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604)basiert.</span><span class="sxs-lookup"><span data-stu-id="62380-2200">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="62380-2201">Dieser Typ sucht nur nach dem Begriff, nicht nach den Versicherungs Codes.</span><span class="sxs-lookup"><span data-stu-id="62380-2201">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="62380-2202">Internationale Klassifikation von Krankheiten (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="62380-2202">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="62380-2203">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2203">Format</span></span>

<span data-ttu-id="62380-2204">Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="62380-2204">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2205">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2205">Pattern</span></span>

<span data-ttu-id="62380-2206">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="62380-2206">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2207">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2207">Checksum</span></span>

<span data-ttu-id="62380-2208">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2208">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2209">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2209">Definition</span></span>

<span data-ttu-id="62380-2210">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2210">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2211">Ein Schlüsselwort aus Dictionary_icd_9_cm wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2211">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2212">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2212">Keywords</span></span>

<span data-ttu-id="62380-2213">Ein beliebiger Begriff aus dem Dictionary_icd_9_cm-Stichwort Wörterbuch, das auf der [internationalen Klassifikation der Krankheiten, der neunTen Revision, der klinischen Modifikation (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605)basiert.</span><span class="sxs-lookup"><span data-stu-id="62380-2213">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="62380-2214">Dieser Typ sucht nur nach dem Begriff, nicht nach den Versicherungs Codes.</span><span class="sxs-lookup"><span data-stu-id="62380-2214">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="62380-2215">Irland – Personal Public Service-Nummer (PPS)</span><span class="sxs-lookup"><span data-stu-id="62380-2215">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2216">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2216">Format</span></span>

<span data-ttu-id="62380-2217">Altes Format (bis 31. Dez 2012):</span><span class="sxs-lookup"><span data-stu-id="62380-2217">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="62380-2218">Sieben Ziffern, gefolgt von 1-2 Buchstaben </span><span class="sxs-lookup"><span data-stu-id="62380-2218">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="62380-2219">Neues Format (1 Jan 2013 und nachher):</span><span class="sxs-lookup"><span data-stu-id="62380-2219">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="62380-2220">Sieben Ziffern, gefolgt von zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="62380-2220">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2221">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2221">Pattern</span></span>

<span data-ttu-id="62380-2222">Altes Format (bis 31. Dez 2012):</span><span class="sxs-lookup"><span data-stu-id="62380-2222">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="62380-2223">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="62380-2223">Seven digits</span></span> 
- <span data-ttu-id="62380-2224">1-2 Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="62380-2224">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="62380-2225">Neues Format (1 Jan 2013 und nachher):</span><span class="sxs-lookup"><span data-stu-id="62380-2225">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="62380-2226">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="62380-2226">Seven digits</span></span> 
- <span data-ttu-id="62380-2227">Ein Buchstabe (Groß-/Kleinschreibung irrelevant), wobei es sich um eine alphabetische Prüfziffer handelt </span><span class="sxs-lookup"><span data-stu-id="62380-2227">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="62380-2228">Die Buchstaben "A" oder "H" (Groß-/Kleinschreibung irrelevant)</span><span class="sxs-lookup"><span data-stu-id="62380-2228">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2229">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2229">Checksum</span></span>

<span data-ttu-id="62380-2230">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2230">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2231">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2231">Definition</span></span>

<span data-ttu-id="62380-2232">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2232">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2233">Die Funktion Func_ireland_pps sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2233">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2234">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="62380-2234">One of the following is true:</span></span>
    - <span data-ttu-id="62380-2235">Ein Schlüsselwort aus Keyword_ireland_pps wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2235">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="62380-2236">Die Funktion Func_eu_date findet ein Datum in das richtige Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="62380-2236">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="62380-2237">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2237">The checksum passes.</span></span>

<span data-ttu-id="62380-2238">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2238">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2239">Die Funktion Func_ireland_pps sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2239">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2240">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2240">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2241">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2241">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="62380-2242">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="62380-2242">Keyword_ireland_pps</span></span>

- <span data-ttu-id="62380-2243">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="62380-2243">Personal Public Service Number</span></span> 
- <span data-ttu-id="62380-2244">PPS Number</span><span class="sxs-lookup"><span data-stu-id="62380-2244">PPS Number</span></span> 
- <span data-ttu-id="62380-2245">PPS Num</span><span class="sxs-lookup"><span data-stu-id="62380-2245">PPS Num</span></span> 
- <span data-ttu-id="62380-2246">PPS No.</span><span class="sxs-lookup"><span data-stu-id="62380-2246">PPS No.</span></span> 
- <span data-ttu-id="62380-2247">PPS #</span><span class="sxs-lookup"><span data-stu-id="62380-2247">PPS #</span></span> 
- <span data-ttu-id="62380-2248">PPS</span><span class="sxs-lookup"><span data-stu-id="62380-2248">PPS#</span></span> 
- <span data-ttu-id="62380-2249">PPSN</span><span class="sxs-lookup"><span data-stu-id="62380-2249">PPSN</span></span> 
- <span data-ttu-id="62380-2250">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="62380-2250">Public Services Card</span></span> 
- <span data-ttu-id="62380-2251">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="62380-2251">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="62380-2252">Uimh.</span><span class="sxs-lookup"><span data-stu-id="62380-2252">Uimh.</span></span> <span data-ttu-id="62380-2253">PSP</span><span class="sxs-lookup"><span data-stu-id="62380-2253">PSP</span></span> 
- <span data-ttu-id="62380-2254">PSP</span><span class="sxs-lookup"><span data-stu-id="62380-2254">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="62380-2255">Israelische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="62380-2255">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2256">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2256">Format</span></span>

<span data-ttu-id="62380-2257">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2257">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2258">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2258">Pattern</span></span>

<span data-ttu-id="62380-2259">Formatiert</span><span class="sxs-lookup"><span data-stu-id="62380-2259">Formatted:</span></span>
- <span data-ttu-id="62380-2260">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2260">Two digits</span></span> 
- <span data-ttu-id="62380-2261">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-2261">A dash</span></span> 
- <span data-ttu-id="62380-2262">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2262">Three digits</span></span> 
- <span data-ttu-id="62380-2263">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-2263">A dash</span></span> 
- <span data-ttu-id="62380-2264">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2264">Eight digits</span></span>

<span data-ttu-id="62380-2265">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="62380-2265">Unformatted:</span></span>
- <span data-ttu-id="62380-2266">	13 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2266">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2267">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2267">Checksum</span></span>

<span data-ttu-id="62380-2268">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2269">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2269">Definition</span></span>

<span data-ttu-id="62380-2270">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2271">Der reguläre Ausdruck Regex_israel_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2271">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2272">Ein Schlüsselwort aus Keyword_israel_bank_account_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2272">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2273">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2273">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="62380-2274">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="62380-2274">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="62380-2275">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="62380-2275">Bank Account Number</span></span> 
- <span data-ttu-id="62380-2276">Bank Account</span><span class="sxs-lookup"><span data-stu-id="62380-2276">Bank Account</span></span> 
- <span data-ttu-id="62380-2277">Account Number</span><span class="sxs-lookup"><span data-stu-id="62380-2277">Account Number</span></span> 
- <span data-ttu-id="62380-2278">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="62380-2278">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="62380-2279">Israelische Ausweis-ID</span><span class="sxs-lookup"><span data-stu-id="62380-2279">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="62380-2280">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2280">Format</span></span>

<span data-ttu-id="62380-2281">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2281">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2282">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2282">Pattern</span></span>

<span data-ttu-id="62380-2283">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2283">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2284">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2284">Checksum</span></span>

<span data-ttu-id="62380-2285">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2285">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2286">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2286">Definition</span></span>

<span data-ttu-id="62380-2287">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2288">Die Funktion Func_israeli_national_id_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2288">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2289">Ein Schlüsselwort aus Keyword_Israel_National_ID wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2289">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="62380-2290">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2290">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2291">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2291">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="62380-2292">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="62380-2292">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="62380-2293">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="62380-2293">מספר זהות</span></span> 
- <span data-ttu-id="62380-2294">National ID Number</span><span class="sxs-lookup"><span data-stu-id="62380-2294">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="62380-2295">Italienische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2295">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2296">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2296">Format</span></span>

<span data-ttu-id="62380-2297">Eine Kombination von 10 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2297">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2298">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2298">Pattern</span></span>

- <span data-ttu-id="62380-2299">Eine Kombination aus 10 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2299">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="62380-2300">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="62380-2300">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="62380-2301">Der Buchstabe „A“ oder „W“ (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="62380-2301">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="62380-2302">Sieben Buchstaben (ohne Beachtung der Groß-/Kleinschreibung), Ziffern oder der Unterstrich</span><span class="sxs-lookup"><span data-stu-id="62380-2302">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="62380-2303">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="62380-2303">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2304">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2304">Checksum</span></span>

<span data-ttu-id="62380-2305">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2305">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2306">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2306">Definition</span></span>

<span data-ttu-id="62380-2307">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2308">Der reguläre Ausdruck Regex_italy_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2308">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2309">Ein Schlüsselwort aus Keyword_italy_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2309">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2310">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2310">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="62380-2311">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="62380-2311">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="62380-2312">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="62380-2312">numero di patente di guida</span></span> 
- <span data-ttu-id="62380-2313">patente di guida</span><span class="sxs-lookup"><span data-stu-id="62380-2313">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="62380-2314">Japanische Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="62380-2314">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2315">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2315">Format</span></span>

<span data-ttu-id="62380-2316">Sieben oder acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2316">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2317">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2317">Pattern</span></span>

<span data-ttu-id="62380-2318">Bankkontonummer:</span><span class="sxs-lookup"><span data-stu-id="62380-2318">Bank account number:</span></span>
- <span data-ttu-id="62380-2319">Sieben oder acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2319">Seven or eight digits</span></span>
- <span data-ttu-id="62380-2320">Niederlassungscode der Bank:</span><span class="sxs-lookup"><span data-stu-id="62380-2320">Bank account branch code:</span></span>
- <span data-ttu-id="62380-2321">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2321">Four digits</span></span> 
- <span data-ttu-id="62380-2322">Ein Leerzeichen oder ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="62380-2322">A space or dash (optional)</span></span> 
- <span data-ttu-id="62380-2323">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2323">Three digits</span></span>

<span data-ttu-id="62380-2324">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2324">Checksum</span></span>

<span data-ttu-id="62380-2325">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2325">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2326">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2326">Definition</span></span>

<span data-ttu-id="62380-2327">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2327">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2328">Die Funktion Func_jp_bank_account findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2328">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2329">Ein Schlüsselwort aus Keyword_jp_bank_account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2329">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="62380-2330">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="62380-2330">One of the following is true:</span></span>
- <span data-ttu-id="62380-2331">Die Funktion Func_jp_bank_account_branch_code findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2331">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2332">Ein Schlüsselwort aus Keyword_jp_bank_branch_code wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2332">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="62380-2333">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2333">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2334">Die Funktion Func_jp_bank_account findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2334">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2335">Ein Schlüsselwort aus Keyword_jp_bank_account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2335">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2336">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2336">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="62380-2337">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="62380-2337">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="62380-2338">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="62380-2338">Checking Account Number</span></span> 
- <span data-ttu-id="62380-2339">Checking Account</span><span class="sxs-lookup"><span data-stu-id="62380-2339">Checking Account</span></span> 
- <span data-ttu-id="62380-2340">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="62380-2340">Checking Account #</span></span> 
- <span data-ttu-id="62380-2341">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="62380-2341">Checking Acct Number</span></span> 
- <span data-ttu-id="62380-2342">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="62380-2342">Checking Acct #</span></span> 
- <span data-ttu-id="62380-2343">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="62380-2343">Checking Acct No.</span></span> 
- <span data-ttu-id="62380-2344">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="62380-2344">Checking Account No.</span></span> 
- <span data-ttu-id="62380-2345">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="62380-2345">Bank Account Number</span></span> 
- <span data-ttu-id="62380-2346">Bank Account</span><span class="sxs-lookup"><span data-stu-id="62380-2346">Bank Account</span></span> 
- <span data-ttu-id="62380-2347">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="62380-2347">Bank Account #</span></span> 
- <span data-ttu-id="62380-2348">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="62380-2348">Bank Acct Number</span></span> 
- <span data-ttu-id="62380-2349">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="62380-2349">Bank Acct #</span></span> 
- <span data-ttu-id="62380-2350">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="62380-2350">Bank Acct No.</span></span> 
- <span data-ttu-id="62380-2351">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="62380-2351">Bank Account No.</span></span> 
- <span data-ttu-id="62380-2352">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="62380-2352">Savings Account Number</span></span> 
- <span data-ttu-id="62380-2353">Savings Account</span><span class="sxs-lookup"><span data-stu-id="62380-2353">Savings Account</span></span> 
- <span data-ttu-id="62380-2354">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="62380-2354">Savings Account #</span></span> 
- <span data-ttu-id="62380-2355">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="62380-2355">Savings Acct Number</span></span> 
- <span data-ttu-id="62380-2356">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="62380-2356">Savings Acct #</span></span> 
- <span data-ttu-id="62380-2357">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="62380-2357">Savings Acct No.</span></span> 
- <span data-ttu-id="62380-2358">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="62380-2358">Savings Account No.</span></span> 
- <span data-ttu-id="62380-2359">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="62380-2359">Debit Account Number</span></span> 
- <span data-ttu-id="62380-2360">Debit Account</span><span class="sxs-lookup"><span data-stu-id="62380-2360">Debit Account</span></span> 
- <span data-ttu-id="62380-2361">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="62380-2361">Debit Account #</span></span> 
- <span data-ttu-id="62380-2362">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="62380-2362">Debit Acct Number</span></span> 
- <span data-ttu-id="62380-2363">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="62380-2363">Debit Acct #</span></span> 
- <span data-ttu-id="62380-2364">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="62380-2364">Debit Acct No.</span></span> 
- <span data-ttu-id="62380-2365">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="62380-2365">Debit Account No.</span></span> 
- <span data-ttu-id="62380-2366">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="62380-2366">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="62380-2367">#アカウントの確認. 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="62380-2367">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="62380-2368">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="62380-2368">＃勘定の確認</span></span> 
- <span data-ttu-id="62380-2369">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="62380-2369">勘定番号の確認</span></span> 
- <span data-ttu-id="62380-2370">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="62380-2370">口座番号の確認</span></span> 
- <span data-ttu-id="62380-2371">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="62380-2371">銀行口座番号</span></span> 
- <span data-ttu-id="62380-2372">銀行口座</span><span class="sxs-lookup"><span data-stu-id="62380-2372">銀行口座</span></span> 
- <span data-ttu-id="62380-2373">銀行口座 #</span><span class="sxs-lookup"><span data-stu-id="62380-2373">銀行口座＃</span></span> 
- <span data-ttu-id="62380-2374">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="62380-2374">銀行の勘定番号</span></span> 
- <span data-ttu-id="62380-2375">銀行のacct #</span><span class="sxs-lookup"><span data-stu-id="62380-2375">銀行のacct＃</span></span> 
- <span data-ttu-id="62380-2376">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="62380-2376">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="62380-2377">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="62380-2377">銀行口座番号</span></span>
- <span data-ttu-id="62380-2378">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="62380-2378">普通預金口座番号</span></span> 
- <span data-ttu-id="62380-2379">預金口座</span><span class="sxs-lookup"><span data-stu-id="62380-2379">預金口座</span></span> 
- <span data-ttu-id="62380-2380">貯蓄口座 #</span><span class="sxs-lookup"><span data-stu-id="62380-2380">貯蓄口座＃</span></span> 
- <span data-ttu-id="62380-2381">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="62380-2381">貯蓄勘定の数</span></span> 
- <span data-ttu-id="62380-2382">貯蓄勘定 #</span><span class="sxs-lookup"><span data-stu-id="62380-2382">貯蓄勘定＃</span></span> 
- <span data-ttu-id="62380-2383">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="62380-2383">貯蓄勘定番号</span></span> 
- <span data-ttu-id="62380-2384">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="62380-2384">普通預金口座番号</span></span> 
- <span data-ttu-id="62380-2385">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="62380-2385">引き落とし口座番号</span></span> 
- <span data-ttu-id="62380-2386">口座番号</span><span class="sxs-lookup"><span data-stu-id="62380-2386">口座番号</span></span> 
- <span data-ttu-id="62380-2387">口座番号 #</span><span class="sxs-lookup"><span data-stu-id="62380-2387">口座番号＃</span></span> 
- <span data-ttu-id="62380-2388">デビットのacct番号</span><span class="sxs-lookup"><span data-stu-id="62380-2388">デビットのacct番号</span></span> 
- <span data-ttu-id="62380-2389">デビット勘定 #</span><span class="sxs-lookup"><span data-stu-id="62380-2389">デビット勘定＃</span></span> 
- <span data-ttu-id="62380-2390">デビットACCTの番号</span><span class="sxs-lookup"><span data-stu-id="62380-2390">デビットACCTの番号</span></span> 
- <span data-ttu-id="62380-2391">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="62380-2391">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="62380-2392">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="62380-2392">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="62380-2393">Otemachi</span><span class="sxs-lookup"><span data-stu-id="62380-2393">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="62380-2394">Japanische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2394">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2395">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2395">Format</span></span>

<span data-ttu-id="62380-2396">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2396">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2397">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2397">Pattern</span></span>

<span data-ttu-id="62380-2398">12 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2398">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2399">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2399">Checksum</span></span>

<span data-ttu-id="62380-2400">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2400">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2401">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2401">Definition</span></span>

<span data-ttu-id="62380-2402">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2402">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2403">Die Funktion Func_jp_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2403">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2404">Ein Schlüsselwort aus Keyword_jp_drivers_license_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2404">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2405">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2405">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="62380-2406">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="62380-2406">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="62380-2407">DL</span><span class="sxs-lookup"><span data-stu-id="62380-2407">dl#</span></span> 
- <span data-ttu-id="62380-2408">DL</span><span class="sxs-lookup"><span data-stu-id="62380-2408">DL＃</span></span> 
- <span data-ttu-id="62380-2409">DLS</span><span class="sxs-lookup"><span data-stu-id="62380-2409">dls#</span></span> 
- <span data-ttu-id="62380-2410">DLS</span><span class="sxs-lookup"><span data-stu-id="62380-2410">DLS＃</span></span> 
- <span data-ttu-id="62380-2411">driver license</span><span class="sxs-lookup"><span data-stu-id="62380-2411">driver license</span></span> 
- <span data-ttu-id="62380-2412">driver licenses</span><span class="sxs-lookup"><span data-stu-id="62380-2412">driver licenses</span></span> 
- <span data-ttu-id="62380-2413">drivers license</span><span class="sxs-lookup"><span data-stu-id="62380-2413">drivers license</span></span> 
- <span data-ttu-id="62380-2414">driver's license</span><span class="sxs-lookup"><span data-stu-id="62380-2414">driver's license</span></span> 
- <span data-ttu-id="62380-2415">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="62380-2415">drivers licenses</span></span> 
- <span data-ttu-id="62380-2416">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="62380-2416">driver's licenses</span></span> 
- <span data-ttu-id="62380-2417">driving licence</span><span class="sxs-lookup"><span data-stu-id="62380-2417">driving licence</span></span> 
- <span data-ttu-id="62380-2418">lic</span><span class="sxs-lookup"><span data-stu-id="62380-2418">lic#</span></span> 
- <span data-ttu-id="62380-2419">LIC</span><span class="sxs-lookup"><span data-stu-id="62380-2419">LIC＃</span></span> 
- <span data-ttu-id="62380-2420">LiCS</span><span class="sxs-lookup"><span data-stu-id="62380-2420">lics#</span></span> 
- <span data-ttu-id="62380-2421">state id</span><span class="sxs-lookup"><span data-stu-id="62380-2421">state id</span></span> 
- <span data-ttu-id="62380-2422">state identification</span><span class="sxs-lookup"><span data-stu-id="62380-2422">state identification</span></span> 
- <span data-ttu-id="62380-2423">state identification number</span><span class="sxs-lookup"><span data-stu-id="62380-2423">state identification number</span></span> 
- <span data-ttu-id="62380-2424">低所得国 #</span><span class="sxs-lookup"><span data-stu-id="62380-2424">低所得国＃</span></span> 
- <span data-ttu-id="62380-2425">免許証</span><span class="sxs-lookup"><span data-stu-id="62380-2425">免許証</span></span> 
- <span data-ttu-id="62380-2426">状態ID</span><span class="sxs-lookup"><span data-stu-id="62380-2426">状態ID</span></span>
- <span data-ttu-id="62380-2427">状態の識別</span><span class="sxs-lookup"><span data-stu-id="62380-2427">状態の識別</span></span> 
- <span data-ttu-id="62380-2428">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="62380-2428">状態の識別番号</span></span> 
- <span data-ttu-id="62380-2429">運転免許</span><span class="sxs-lookup"><span data-stu-id="62380-2429">運転免許</span></span> 
- <span data-ttu-id="62380-2430">運転免許証</span><span class="sxs-lookup"><span data-stu-id="62380-2430">運転免許証</span></span> 
- <span data-ttu-id="62380-2431">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="62380-2431">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="62380-2432">Japanische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2432">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2433">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2433">Format</span></span>

<span data-ttu-id="62380-2434">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2434">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2435">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2435">Pattern</span></span>

<span data-ttu-id="62380-2436">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2436">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2437">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2437">Checksum</span></span>

<span data-ttu-id="62380-2438">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2438">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2439">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2439">Definition</span></span>

<span data-ttu-id="62380-2440">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2441">Die Funktion Func_jp_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2441">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2442">Ein Schlüsselwort aus Keyword_jp_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2442">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2443">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2443">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="62380-2444">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="62380-2444">Keyword_jp_passport</span></span>

- <span data-ttu-id="62380-2445">パスポート</span><span class="sxs-lookup"><span data-stu-id="62380-2445">パスポート</span></span> 
- <span data-ttu-id="62380-2446">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="62380-2446">パスポート番号</span></span> 
- <span data-ttu-id="62380-2447">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="62380-2447">パスポートのNum</span></span> 
- <span data-ttu-id="62380-2448">パスポート #</span><span class="sxs-lookup"><span data-stu-id="62380-2448">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="62380-2449">Japanische Einwohnerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2449">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2450">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2450">Format</span></span>

<span data-ttu-id="62380-2451">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2451">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2452">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2452">Pattern</span></span>

<span data-ttu-id="62380-2453">11 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2453">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2454">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2454">Checksum</span></span>

<span data-ttu-id="62380-2455">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2455">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2456">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2456">Definition</span></span>

<span data-ttu-id="62380-2457">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2458">Die Funktion Func_jp_resident_registration_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2458">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2459">Ein Schlüsselwort aus Keyword_jp_resident_registration_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2459">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2460">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2460">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="62380-2461">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="62380-2461">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="62380-2462">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="62380-2462">Resident Registration Number</span></span>
- <span data-ttu-id="62380-2463">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="62380-2463">Resident Register Number</span></span> 
- <span data-ttu-id="62380-2464">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="62380-2464">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="62380-2465">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="62380-2465">Resident Registration No.</span></span> 
- <span data-ttu-id="62380-2466">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="62380-2466">Resident Register No.</span></span> 
- <span data-ttu-id="62380-2467">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="62380-2467">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="62380-2468">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="62380-2468">Basic Resident Register No.</span></span> 
- <span data-ttu-id="62380-2469">住民登録番号, 登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="62380-2469">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="62380-2470">住民基本登録番号, 登録番号</span><span class="sxs-lookup"><span data-stu-id="62380-2470">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="62380-2471">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="62380-2471">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="62380-2472">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="62380-2472">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="62380-2473">Japanische Sozialversicherungsnummer (SIN)</span><span class="sxs-lookup"><span data-stu-id="62380-2473">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="62380-2474">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2474">Format</span></span>

<span data-ttu-id="62380-2475">7-12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2475">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2476">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2476">Pattern</span></span>

<span data-ttu-id="62380-2477">7 bis 12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2477">7-12 digits:</span></span>
- <span data-ttu-id="62380-2478">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2478">Four digits</span></span> 
- <span data-ttu-id="62380-2479">Ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="62380-2479">A hyphen (optional)</span></span> 
- <span data-ttu-id="62380-2480">Sechs Ziffern oder</span><span class="sxs-lookup"><span data-stu-id="62380-2480">Six digits OR</span></span>
- <span data-ttu-id="62380-2481">7-12 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2481">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2482">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2482">Checksum</span></span>

<span data-ttu-id="62380-2483">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2483">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2484">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2484">Definition</span></span>

<span data-ttu-id="62380-2485">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2485">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2486">Die Funktion Func_jp_sin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2486">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2487">Ein Schlüsselwort aus Keyword_jp_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2487">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="62380-2488">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2488">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2489">Die Funktion Func_jp_sin_pre_1997 findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2489">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2490">Ein Schlüsselwort aus Keyword_jp_sin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2490">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2491">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2491">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="62380-2492">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="62380-2492">Keyword_jp_sin</span></span>

- <span data-ttu-id="62380-2493">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="62380-2493">Social Insurance No.</span></span> 
- <span data-ttu-id="62380-2494">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="62380-2494">Social Insurance Num</span></span> 
- <span data-ttu-id="62380-2495">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="62380-2495">Social Insurance Number</span></span> 
- <span data-ttu-id="62380-2496">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="62380-2496">社会保険のテンキー</span></span> 
- <span data-ttu-id="62380-2497">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="62380-2497">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="62380-2498">Nummer der japanischen Residenzkarte</span><span class="sxs-lookup"><span data-stu-id="62380-2498">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2499">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2499">Format</span></span>

<span data-ttu-id="62380-2500">12 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2500">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2501">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2501">Pattern</span></span>

<span data-ttu-id="62380-2502">12 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2502">12 letters and digits:</span></span>
- <span data-ttu-id="62380-2503">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="62380-2503">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="62380-2504">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2504">Eight digits</span></span> 
- <span data-ttu-id="62380-2505">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="62380-2505">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2506">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2506">Checksum</span></span>

<span data-ttu-id="62380-2507">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2507">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2508">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2508">Definition</span></span>

<span data-ttu-id="62380-2509">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2509">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2510">Der reguläre Ausdruck Regex_jp_residence_card_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2510">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2511">Ein Schlüsselwort aus Keyword_jp_residence_card_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2511">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2512">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2512">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="62380-2513">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="62380-2513">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="62380-2514">Nummer der Residenzkarte</span><span class="sxs-lookup"><span data-stu-id="62380-2514">Residence card number</span></span>
- <span data-ttu-id="62380-2515">Aufenthaltskarte Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2515">Residence card no</span></span>
- <span data-ttu-id="62380-2516">Residenzkarte #</span><span class="sxs-lookup"><span data-stu-id="62380-2516">Residence card #</span></span>
- <span data-ttu-id="62380-2517">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="62380-2517">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="62380-2518">Malaysia -ID-Kartennummer</span><span class="sxs-lookup"><span data-stu-id="62380-2518">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2519">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2519">Format</span></span>

<span data-ttu-id="62380-2520">12 Ziffern mit optionalen Bindestrichen</span><span class="sxs-lookup"><span data-stu-id="62380-2520">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2521">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2521">Pattern</span></span>

<span data-ttu-id="62380-2522">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2522">12 digits:</span></span>
- <span data-ttu-id="62380-2523">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="62380-2523">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="62380-2524">Ein Bindestrich (optional) </span><span class="sxs-lookup"><span data-stu-id="62380-2524">A dash (optional)</span></span> 
- <span data-ttu-id="62380-2525">Zwei Buchstaben als Code für den Geburtsort </span><span class="sxs-lookup"><span data-stu-id="62380-2525">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="62380-2526">Ein Bindestrich (optional) </span><span class="sxs-lookup"><span data-stu-id="62380-2526">A dash (optional)</span></span> 
- <span data-ttu-id="62380-2527">Drei beliebige Ziffern </span><span class="sxs-lookup"><span data-stu-id="62380-2527">Three random digits</span></span> 
- <span data-ttu-id="62380-2528">Einstelliger Code für das Geschlecht</span><span class="sxs-lookup"><span data-stu-id="62380-2528">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2529">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2529">Checksum</span></span>

<span data-ttu-id="62380-2530">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2530">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2531">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2531">Definition</span></span>

<span data-ttu-id="62380-2532">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2532">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2533">Der reguläre Ausdruck Regex_malaysia_id_card_number findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2533">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2534">Ein Schlüsselwort aus Keyword_malaysia_id_card_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2534">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2535">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2535">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="62380-2536">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="62380-2536">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="62380-2537">digitale Anwendungs Karte</span><span class="sxs-lookup"><span data-stu-id="62380-2537">digital application card</span></span>
- <span data-ttu-id="62380-2538">i/c</span><span class="sxs-lookup"><span data-stu-id="62380-2538">i/c</span></span>
- <span data-ttu-id="62380-2539">i/c Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2539">i/c no</span></span>
- <span data-ttu-id="62380-2540">IC</span><span class="sxs-lookup"><span data-stu-id="62380-2540">ic</span></span>
- <span data-ttu-id="62380-2541">IC Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2541">ic no</span></span>
- <span data-ttu-id="62380-2542">id card</span><span class="sxs-lookup"><span data-stu-id="62380-2542">id card</span></span>
- <span data-ttu-id="62380-2543">Identitätskarte</span><span class="sxs-lookup"><span data-stu-id="62380-2543">identification Card</span></span>
- <span data-ttu-id="62380-2544">identity card</span><span class="sxs-lookup"><span data-stu-id="62380-2544">identity card</span></span>
- <span data-ttu-id="62380-2545">k/p</span><span class="sxs-lookup"><span data-stu-id="62380-2545">k/p</span></span>
- <span data-ttu-id="62380-2546">k/p Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2546">k/p no</span></span>
- <span data-ttu-id="62380-2547">Kad akuan Diri</span><span class="sxs-lookup"><span data-stu-id="62380-2547">kad akuan diri</span></span>
- <span data-ttu-id="62380-2548">Kad aplikasi Digital</span><span class="sxs-lookup"><span data-stu-id="62380-2548">kad aplikasi digital</span></span>
- <span data-ttu-id="62380-2549">Kad Einführung in Malaysia</span><span class="sxs-lookup"><span data-stu-id="62380-2549">kad pengenalan malaysia</span></span>
- <span data-ttu-id="62380-2550">KP</span><span class="sxs-lookup"><span data-stu-id="62380-2550">kp</span></span>
- <span data-ttu-id="62380-2551">KP Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2551">kp no</span></span>
- <span data-ttu-id="62380-2552">MyKAD</span><span class="sxs-lookup"><span data-stu-id="62380-2552">mykad</span></span>
- <span data-ttu-id="62380-2553">mykas</span><span class="sxs-lookup"><span data-stu-id="62380-2553">mykas</span></span>
- <span data-ttu-id="62380-2554">mykid</span><span class="sxs-lookup"><span data-stu-id="62380-2554">mykid</span></span>
- <span data-ttu-id="62380-2555">mypr</span><span class="sxs-lookup"><span data-stu-id="62380-2555">mypr</span></span>
- <span data-ttu-id="62380-2556">mytentera</span><span class="sxs-lookup"><span data-stu-id="62380-2556">mytentera</span></span>
- <span data-ttu-id="62380-2557">Malaysia-Identitätskarte</span><span class="sxs-lookup"><span data-stu-id="62380-2557">malaysia identity card</span></span>
- <span data-ttu-id="62380-2558">malaysischer Identitätsausweis</span><span class="sxs-lookup"><span data-stu-id="62380-2558">malaysian identity card</span></span>
- <span data-ttu-id="62380-2559">NRIC</span><span class="sxs-lookup"><span data-stu-id="62380-2559">nric</span></span>
- <span data-ttu-id="62380-2560">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="62380-2560">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="62380-2561">Niederlande – Bürgerdienstnummer (BSN)</span><span class="sxs-lookup"><span data-stu-id="62380-2561">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2562">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2562">Format</span></span>

<span data-ttu-id="62380-2563">8-9 Ziffern mit optionalen Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-2563">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2564">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2564">Pattern</span></span>

<span data-ttu-id="62380-2565">8-9 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2565">8-9 digits:</span></span>
- <span data-ttu-id="62380-2566">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2566">Three digits</span></span> 
- <span data-ttu-id="62380-2567">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="62380-2567">A space (optional)</span></span> 
- <span data-ttu-id="62380-2568">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2568">Three digits</span></span> 
- <span data-ttu-id="62380-2569">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="62380-2569">A space (optional)</span></span> 
- <span data-ttu-id="62380-2570">2-3 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2570">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2571">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2571">Checksum</span></span>

<span data-ttu-id="62380-2572">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2572">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2573">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2573">Definition</span></span>

<span data-ttu-id="62380-2574">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2574">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2575">Die Funktion Func_netherlands_bsn sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2575">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2576">Ein Schlüsselwort aus Keyword_netherlands_bsn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2576">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="62380-2577">Die Funktion Func_eu_date2 findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="62380-2577">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="62380-2578">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2578">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2579">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2579">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="62380-2580">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="62380-2580">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="62380-2581">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="62380-2581">Citizen service number</span></span> 
- <span data-ttu-id="62380-2582">BSN</span><span class="sxs-lookup"><span data-stu-id="62380-2582">BSN</span></span> 
- <span data-ttu-id="62380-2583">Burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="62380-2583">Burgerservicenummer</span></span> 
- <span data-ttu-id="62380-2584">Sofinummer</span><span class="sxs-lookup"><span data-stu-id="62380-2584">Sofinummer</span></span> 
- <span data-ttu-id="62380-2585">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="62380-2585">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="62380-2586">Persoonsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2586">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="62380-2587">Neuseeländische Gesundheitsministeriumsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2587">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2588">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2588">Format</span></span>

<span data-ttu-id="62380-2589">Drei Buchstaben, ein Leerzeichen (optional) und vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2589">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2590">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2590">Pattern</span></span>

<span data-ttu-id="62380-2591">Drei Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) ein Leerzeichen (optional) vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2591">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2592">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2592">Checksum</span></span>

<span data-ttu-id="62380-2593">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2593">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2594">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2594">Definition</span></span>

<span data-ttu-id="62380-2595">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2596">Die Funktion Func_new_zealand_ministry_of_health_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2596">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2597">Ein Schlüsselwort aus Keyword_nz_terms wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2597">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="62380-2598">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2598">The checksum passes.</span></span>

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

<span data-ttu-id="62380-2599">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2599">Keywords</span></span>

<span data-ttu-id="62380-2600">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="62380-2600">Keyword_nz_terms</span></span>

- <span data-ttu-id="62380-2601">NHI</span><span class="sxs-lookup"><span data-stu-id="62380-2601">NHI</span></span> 
- <span data-ttu-id="62380-2602">New Zealand</span><span class="sxs-lookup"><span data-stu-id="62380-2602">New Zealand</span></span> 
- <span data-ttu-id="62380-2603">Integrität</span><span class="sxs-lookup"><span data-stu-id="62380-2603">Health</span></span> 
- <span data-ttu-id="62380-2604">Flusses zur Gewährung</span><span class="sxs-lookup"><span data-stu-id="62380-2604">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="62380-2605">Norwegen – Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2605">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2606">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2606">Format</span></span>

<span data-ttu-id="62380-2607">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2607">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2608">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2608">Pattern</span></span>

<span data-ttu-id="62380-2609">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2609">11 digits:</span></span>
- <span data-ttu-id="62380-2610">Sechs Ziffern im Format TTMMJJ, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="62380-2610">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="62380-2611">Dreistellige individuelle Zahl </span><span class="sxs-lookup"><span data-stu-id="62380-2611">Three-digit individual number</span></span> 
- <span data-ttu-id="62380-2612">Zwei Prüfziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2612">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2613">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2613">Checksum</span></span>

<span data-ttu-id="62380-2614">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2614">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2615">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2615">Definition</span></span>

<span data-ttu-id="62380-2616">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2616">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2617">Die Funktion Func_norway_id_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2617">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2618">Ein Schlüsselwort aus Keyword_norway_id_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2618">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="62380-2619">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2619">The checksum passes.</span></span>
- <span data-ttu-id="62380-2620">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2620">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2621">Die Funktion Func_norway_id_numbe sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2621">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2622">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2622">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2623">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2623">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="62380-2624">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="62380-2624">Keyword_norway_id_number</span></span>

- <span data-ttu-id="62380-2625">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="62380-2625">Personal identification number</span></span>
- <span data-ttu-id="62380-2626">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="62380-2626">Norwegian ID Number</span></span>
- <span data-ttu-id="62380-2627">ID Number</span><span class="sxs-lookup"><span data-stu-id="62380-2627">ID Number</span></span>
- <span data-ttu-id="62380-2628">Identifikations</span><span class="sxs-lookup"><span data-stu-id="62380-2628">Identification</span></span>
- <span data-ttu-id="62380-2629">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="62380-2629">Personnummer</span></span>
- <span data-ttu-id="62380-2630">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2630">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="62380-2631">Philippinen – Vereinheitlichte Mehrzweck-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="62380-2631">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2632">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2632">Format</span></span>

<span data-ttu-id="62380-2633">12 Ziffern, durch Bindestriche getrennt</span><span class="sxs-lookup"><span data-stu-id="62380-2633">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2634">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2634">Pattern</span></span>

<span data-ttu-id="62380-2635">12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2635">12 digits:</span></span>
- <span data-ttu-id="62380-2636">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2636">Four digits</span></span> 
- <span data-ttu-id="62380-2637">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-2637">A hyphen</span></span> 
- <span data-ttu-id="62380-2638">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="62380-2638">Seven digits</span></span> 
- <span data-ttu-id="62380-2639">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-2639">A hyphen</span></span> 
- <span data-ttu-id="62380-2640">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="62380-2640">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2641">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2641">Checksum</span></span>

<span data-ttu-id="62380-2642">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2642">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2643">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2643">Definition</span></span>

<span data-ttu-id="62380-2644">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2644">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2645">Der reguläre Ausdruck Regex_philippines_unified_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2645">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2646">Ein Schlüsselwort aus Keyword_philippines_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2646">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2647">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2647">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="62380-2648">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="62380-2648">Keyword_philippines_id</span></span>

- <span data-ttu-id="62380-2649">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="62380-2649">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="62380-2650">UMID</span><span class="sxs-lookup"><span data-stu-id="62380-2650">UMID</span></span> 
- <span data-ttu-id="62380-2651">Identity Card</span><span class="sxs-lookup"><span data-stu-id="62380-2651">Identity Card</span></span> 
- <span data-ttu-id="62380-2652">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="62380-2652">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="62380-2653">Polen Personalausweis</span><span class="sxs-lookup"><span data-stu-id="62380-2653">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="62380-2654">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2654">Format</span></span>

<span data-ttu-id="62380-2655">Drei Buchstaben und sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2655">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2656">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2656">Pattern</span></span>

<span data-ttu-id="62380-2657">Drei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2657">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2658">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2658">Checksum</span></span>

<span data-ttu-id="62380-2659">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2659">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2660">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2660">Definition</span></span>

<span data-ttu-id="62380-2661">Eine DLP-Richtlinie ist 75% sicher, dass Sie diese Art von vertraulichen Informationen erkannt hat, wenn in einer Nähe von 300 Zeichen: die Funktion Func_polish_national_id findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2661">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="62380-2662">Ein Schlüsselwort aus Keyword_polish_national_id_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2662">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="62380-2663">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2663">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2664">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2664">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="62380-2665">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="62380-2665">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="62380-2666">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="62380-2666">Dowód osobisty</span></span>
- <span data-ttu-id="62380-2667">Numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="62380-2667">Numer dowodu osobistego</span></span>
- <span data-ttu-id="62380-2668">Nazwa i Numer dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="62380-2668">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="62380-2669">Nazwa i Nr dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="62380-2669">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="62380-2670">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="62380-2670">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="62380-2671">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="62380-2671">Dowód Tożsamości</span></span>
- <span data-ttu-id="62380-2672">Dow.</span><span class="sxs-lookup"><span data-stu-id="62380-2672">dow.</span></span> <span data-ttu-id="62380-2673">OS.</span><span class="sxs-lookup"><span data-stu-id="62380-2673">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="62380-2674">Polnische ID-Karte (PESEL)</span><span class="sxs-lookup"><span data-stu-id="62380-2674">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="62380-2675">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2675">Format</span></span>

<span data-ttu-id="62380-2676">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2676">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2677">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2677">Pattern</span></span>

<span data-ttu-id="62380-2678">11 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2678">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2679">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2679">Checksum</span></span>

<span data-ttu-id="62380-2680">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2680">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2681">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2681">Definition</span></span>

<span data-ttu-id="62380-2682">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2682">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2683">Die Funktion Func_pesel_identification_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2683">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2684">Ein Schlüsselwort aus Keyword_pesel_identification_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2684">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="62380-2685">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2685">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2686">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2686">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="62380-2687">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="62380-2687">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="62380-2688">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="62380-2688">Nr PESEL</span></span>
- <span data-ttu-id="62380-2689">PESEL</span><span class="sxs-lookup"><span data-stu-id="62380-2689">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="62380-2690">Polen Reisepass</span><span class="sxs-lookup"><span data-stu-id="62380-2690">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="62380-2691">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2691">Format</span></span>

<span data-ttu-id="62380-2692">Zwei Buchstaben und sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2692">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2693">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2693">Pattern</span></span>

<span data-ttu-id="62380-2694">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2694">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2695">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2695">Checksum</span></span>

<span data-ttu-id="62380-2696">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2696">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2697">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2697">Definition</span></span>

<span data-ttu-id="62380-2698">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2698">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2699">Die Funktion Func_polish_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2699">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2700">Ein Schlüsselwort aus Keyword_polish_national_id_passport_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2700">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="62380-2701">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2701">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2702">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2702">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="62380-2703">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="62380-2703">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="62380-2704">Numer paszportu</span><span class="sxs-lookup"><span data-stu-id="62380-2704">Numer paszportu</span></span>
- <span data-ttu-id="62380-2705">Nr.</span><span class="sxs-lookup"><span data-stu-id="62380-2705">Nr.</span></span> <span data-ttu-id="62380-2706">Paszportu</span><span class="sxs-lookup"><span data-stu-id="62380-2706">Paszportu</span></span>
- <span data-ttu-id="62380-2707">Paszport</span><span class="sxs-lookup"><span data-stu-id="62380-2707">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="62380-2708">Portugal – Bürgerkartennummer</span><span class="sxs-lookup"><span data-stu-id="62380-2708">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2709">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2709">Format</span></span>

<span data-ttu-id="62380-2710">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2710">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2711">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2711">Pattern</span></span>

<span data-ttu-id="62380-2712">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2712">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2713">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2713">Checksum</span></span>

<span data-ttu-id="62380-2714">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2714">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2715">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2715">Definition</span></span>

<span data-ttu-id="62380-2716">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2716">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2717">Der reguläre Ausdruck Regex_portugal_citizen_card findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2717">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2718">Ein Schlüsselwort aus Keyword_portugal_citizen_card wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2718">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2719">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2719">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="62380-2720">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="62380-2720">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="62380-2721">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="62380-2721">Citizen Card</span></span>
- <span data-ttu-id="62380-2722">National ID Card</span><span class="sxs-lookup"><span data-stu-id="62380-2722">National ID Card</span></span>
- <span data-ttu-id="62380-2723">CC</span><span class="sxs-lookup"><span data-stu-id="62380-2723">CC</span></span>
- <span data-ttu-id="62380-2724">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="62380-2724">Cartão de Cidadão</span></span>
- <span data-ttu-id="62380-2725">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="62380-2725">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="62380-2726">Saudi-Arabische Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2726">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="62380-2727">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2727">Format</span></span>

<span data-ttu-id="62380-2728">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2728">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2729">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2729">Pattern</span></span>

<span data-ttu-id="62380-2730">10 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2730">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2731">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2731">Checksum</span></span>

<span data-ttu-id="62380-2732">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2732">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2733">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2733">Definition</span></span>

<span data-ttu-id="62380-2734">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2734">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2735">Der reguläre Ausdruck Regex_saudi_arabia_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2735">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2736">Ein Schlüsselwort aus Keyword_saudi_arabia_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2736">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2737">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2737">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="62380-2738">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="62380-2738">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="62380-2739">Identification Card</span><span class="sxs-lookup"><span data-stu-id="62380-2739">Identification Card</span></span> 
- <span data-ttu-id="62380-2740">I card number</span><span class="sxs-lookup"><span data-stu-id="62380-2740">I card number</span></span> 
- <span data-ttu-id="62380-2741">ID number</span><span class="sxs-lookup"><span data-stu-id="62380-2741">ID number</span></span> 
- <span data-ttu-id="62380-2742">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="62380-2742">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="62380-2743">Singapur – National Registration Identity Card-Nummer (NRIC)</span><span class="sxs-lookup"><span data-stu-id="62380-2743">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2744">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2744">Format</span></span>

<span data-ttu-id="62380-2745">Neun Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2745">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2746">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2746">Pattern</span></span>

- <span data-ttu-id="62380-2747">Neun Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2747">Nine letters and digits:</span></span>
- <span data-ttu-id="62380-2748">Die Buchstaben "F", "G", "S" oder "T" (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="62380-2748">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="62380-2749">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="62380-2749">Seven digits</span></span> 
- <span data-ttu-id="62380-2750">Eine alphabetische Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="62380-2750">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2751">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2751">Checksum</span></span>

<span data-ttu-id="62380-2752">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2752">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2753">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2753">Definition</span></span>

<span data-ttu-id="62380-2754">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2754">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2755">Der reguläre Ausdruck Regex_singapore_nric findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2755">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2756">Ein Schlüsselwort aus Keyword_singapore_nric wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2756">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="62380-2757">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2757">The checksum passes.</span></span>

<span data-ttu-id="62380-2758">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2758">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2759">Der reguläre Ausdruck Regex_singapore_nric findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2759">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2760">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2760">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2761">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2761">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="62380-2762">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="62380-2762">Keyword_singapore_nric</span></span>

- <span data-ttu-id="62380-2763">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="62380-2763">National Registration Identity Card</span></span> 
- <span data-ttu-id="62380-2764">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="62380-2764">Identity Card Number</span></span> 
- <span data-ttu-id="62380-2765">NRIC</span><span class="sxs-lookup"><span data-stu-id="62380-2765">NRIC</span></span> 
- <span data-ttu-id="62380-2766">IC</span><span class="sxs-lookup"><span data-stu-id="62380-2766">IC</span></span> 
- <span data-ttu-id="62380-2767">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="62380-2767">Foreign Identification Number</span></span> 
- <span data-ttu-id="62380-2768">FIN</span><span class="sxs-lookup"><span data-stu-id="62380-2768">FIN</span></span> 
- <span data-ttu-id="62380-2769">身份证</span><span class="sxs-lookup"><span data-stu-id="62380-2769">身份证</span></span> 
- <span data-ttu-id="62380-2770">身份證</span><span class="sxs-lookup"><span data-stu-id="62380-2770">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="62380-2771">Südafrika – Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2771">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2772">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2772">Format</span></span>

<span data-ttu-id="62380-2773">13 Ziffern, die Leerzeichen enthalten können</span><span class="sxs-lookup"><span data-stu-id="62380-2773">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2774">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2774">Pattern</span></span>

<span data-ttu-id="62380-2775">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2775">13 digits:</span></span>
- <span data-ttu-id="62380-2776">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="62380-2776">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="62380-2777">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2777">Four digits</span></span> 
- <span data-ttu-id="62380-2778">Ein einstelliger Citizenship-Indikator </span><span class="sxs-lookup"><span data-stu-id="62380-2778">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="62380-2779">Die Ziffer "8" oder "9" </span><span class="sxs-lookup"><span data-stu-id="62380-2779">The digit "8" or "9"</span></span> 
- <span data-ttu-id="62380-2780">Eine Ziffer als Prüfsummenziffer</span><span class="sxs-lookup"><span data-stu-id="62380-2780">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2781">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2781">Checksum</span></span>

<span data-ttu-id="62380-2782">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2782">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2783">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2783">Definition</span></span>

<span data-ttu-id="62380-2784">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2785">Die Funktion Func_south_africa_identification_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2785">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2786">Ein Schlüsselwort aus Keyword_south_africa_identification_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2786">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="62380-2787">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2787">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2788">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2788">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="62380-2789">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="62380-2789">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="62380-2790">Identity card</span><span class="sxs-lookup"><span data-stu-id="62380-2790">Identity card</span></span>
- <span data-ttu-id="62380-2791">ID</span><span class="sxs-lookup"><span data-stu-id="62380-2791">ID</span></span>
- <span data-ttu-id="62380-2792">Identifikations</span><span class="sxs-lookup"><span data-stu-id="62380-2792">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="62380-2793">Südkorea – Einwohnerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2793">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2794">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2794">Format</span></span>

<span data-ttu-id="62380-2795">13 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="62380-2795">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2796">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2796">Pattern</span></span>

<span data-ttu-id="62380-2797">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2797">13 digits:</span></span>
- <span data-ttu-id="62380-2798">Sechs Ziffern im Format JJMMTT, die das Geburtsdatum angeben </span><span class="sxs-lookup"><span data-stu-id="62380-2798">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="62380-2799">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="62380-2799">A hyphen</span></span> 
- <span data-ttu-id="62380-2800">Eine Ziffer, die durch das Jahrhundert und das Geschlecht bestimmt wird </span><span class="sxs-lookup"><span data-stu-id="62380-2800">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="62380-2801">Vierstelliger Code für die Geburtsregion </span><span class="sxs-lookup"><span data-stu-id="62380-2801">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="62380-2802">Eine Ziffer, um Personen zu unterscheiden, für die die vorhergehenden Zahlen identisch sind </span><span class="sxs-lookup"><span data-stu-id="62380-2802">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="62380-2803">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="62380-2803">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2804">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2804">Checksum</span></span>

<span data-ttu-id="62380-2805">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2805">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2806">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2806">Definition</span></span>

<span data-ttu-id="62380-2807">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2807">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2808">Die Funktion Func_south_korea_resident_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2808">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2809">Ein Schlüsselwort aus Keyword_south_korea_resident_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2809">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="62380-2810">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2810">The checksum passes.</span></span>

<span data-ttu-id="62380-2811">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2811">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2812">Die Funktion Func_south_korea_resident_number sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2812">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2813">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2813">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2814">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2814">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="62380-2815">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="62380-2815">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="62380-2816">National ID card</span><span class="sxs-lookup"><span data-stu-id="62380-2816">National ID card</span></span> 
- <span data-ttu-id="62380-2817">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="62380-2817">Citizen's Registration Number</span></span> 
- <span data-ttu-id="62380-2818">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="62380-2818">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="62380-2819">RRN</span><span class="sxs-lookup"><span data-stu-id="62380-2819">RRN</span></span> 
- <span data-ttu-id="62380-2820">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="62380-2820">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="62380-2821">Spanische Sozialversicherungsnummer (SSN)</span><span class="sxs-lookup"><span data-stu-id="62380-2821">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="62380-2822">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2822">Format</span></span>

<span data-ttu-id="62380-2823">11-12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2823">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2824">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2824">Pattern</span></span>

<span data-ttu-id="62380-2825">11-12 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2825">11-12 digits:</span></span>
- <span data-ttu-id="62380-2826">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2826">Two digits</span></span> 
- <span data-ttu-id="62380-2827">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="62380-2827">A forward slash (optional)</span></span> 
- <span data-ttu-id="62380-2828">7 bis 8 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2828">7-8 digits</span></span> 
- <span data-ttu-id="62380-2829">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="62380-2829">A forward slash (optional)</span></span> 
- <span data-ttu-id="62380-2830">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2830">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2831">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2831">Checksum</span></span>

<span data-ttu-id="62380-2832">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2832">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2833">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2833">Definition</span></span>

<span data-ttu-id="62380-2834">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2834">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2835">Die Funktion Func_spanish_social_security_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2835">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2836">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2836">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2837">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2837">Keywords</span></span>

<span data-ttu-id="62380-2838">None</span><span class="sxs-lookup"><span data-stu-id="62380-2838">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="62380-2839">Schwedische Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2839">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="62380-2840">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2840">Format</span></span>

<span data-ttu-id="62380-2841">10 oder 12 Ziffern und ein optionales Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-2841">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2842">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2842">Pattern</span></span>

<span data-ttu-id="62380-2843">10 oder 12 Ziffern und ein optionals Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="62380-2843">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="62380-2844">2 bis 4 Ziffern (optional)</span><span class="sxs-lookup"><span data-stu-id="62380-2844">2-4 digits (optional)</span></span> 
- <span data-ttu-id="62380-2845">Sechs Ziffern im Datumsformat JJMMTT</span><span class="sxs-lookup"><span data-stu-id="62380-2845">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="62380-2846">Trennzeichen „-“ oder „+“ (optional) und</span><span class="sxs-lookup"><span data-stu-id="62380-2846">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="62380-2847">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2847">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2848">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2848">Checksum</span></span>

<span data-ttu-id="62380-2849">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2849">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2850">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2850">Definition</span></span>

<span data-ttu-id="62380-2851">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2851">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2852">Die Funktion Func_swedish_national_identifier findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2852">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2853">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2853">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2854">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2854">Keywords</span></span>

<span data-ttu-id="62380-2855">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2855">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="62380-2856">Schwedische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2856">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2857">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2857">Format</span></span>

<span data-ttu-id="62380-2858">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2858">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2859">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2859">Pattern</span></span>

<span data-ttu-id="62380-2860">Acht aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2860">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2861">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2861">Checksum</span></span>

<span data-ttu-id="62380-2862">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2862">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2863">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2863">Definition</span></span>

<span data-ttu-id="62380-2864">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2864">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2865">Der reguläre Ausdruck Regex_sweden_passport_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2865">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2866">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="62380-2866">One of the following is true:</span></span>
    - <span data-ttu-id="62380-2867">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2867">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="62380-2868">Ein Schlüsselwort aus Keyword_sweden_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2868">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-2869">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2869">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="62380-2870">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="62380-2870">Keyword_sweden_passport</span></span>

- <span data-ttu-id="62380-2871">visa requirements</span><span class="sxs-lookup"><span data-stu-id="62380-2871">visa requirements</span></span> 
- <span data-ttu-id="62380-2872">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="62380-2872">Alien Registration Card</span></span> 
- <span data-ttu-id="62380-2873">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="62380-2873">Schengen visas</span></span> 
- <span data-ttu-id="62380-2874">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="62380-2874">Schengen visa</span></span> 
- <span data-ttu-id="62380-2875">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="62380-2875">Visa Processing</span></span> 
- <span data-ttu-id="62380-2876">Visa Type</span><span class="sxs-lookup"><span data-stu-id="62380-2876">Visa Type</span></span> 
- <span data-ttu-id="62380-2877">Single Entry</span><span class="sxs-lookup"><span data-stu-id="62380-2877">Single Entry</span></span> 
- <span data-ttu-id="62380-2878">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="62380-2878">Multiple Entry</span></span> 
- <span data-ttu-id="62380-2879">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="62380-2879">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="62380-2880">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="62380-2880">Keyword_passport</span></span>

- <span data-ttu-id="62380-2881">Passport Number</span><span class="sxs-lookup"><span data-stu-id="62380-2881">Passport Number</span></span> 
- <span data-ttu-id="62380-2882">Passport No</span><span class="sxs-lookup"><span data-stu-id="62380-2882">Passport No</span></span> 
- <span data-ttu-id="62380-2883">Passport#</span><span class="sxs-lookup"><span data-stu-id="62380-2883">Passport #</span></span> 
- <span data-ttu-id="62380-2884">Pass</span><span class="sxs-lookup"><span data-stu-id="62380-2884">Passport#</span></span> 
- <span data-ttu-id="62380-2885">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="62380-2885">PassportID</span></span> 
- <span data-ttu-id="62380-2886">Passportno</span><span class="sxs-lookup"><span data-stu-id="62380-2886">Passportno</span></span> 
- <span data-ttu-id="62380-2887">passportnumber</span><span class="sxs-lookup"><span data-stu-id="62380-2887">passportnumber</span></span> 
- <span data-ttu-id="62380-2888">パスポート</span><span class="sxs-lookup"><span data-stu-id="62380-2888">パスポート</span></span> 
- <span data-ttu-id="62380-2889">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="62380-2889">パスポート番号</span></span> 
- <span data-ttu-id="62380-2890">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="62380-2890">パスポートのNum</span></span> 
- <span data-ttu-id="62380-2891">パスポート #</span><span class="sxs-lookup"><span data-stu-id="62380-2891">パスポート＃</span></span> 
- <span data-ttu-id="62380-2892">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="62380-2892">Numéro de passeport</span></span> 
- <span data-ttu-id="62380-2893">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="62380-2893">Passeport n °</span></span> 
- <span data-ttu-id="62380-2894">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="62380-2894">Passeport Non</span></span> 
- <span data-ttu-id="62380-2895">Passeport#</span><span class="sxs-lookup"><span data-stu-id="62380-2895">Passeport #</span></span> 
- <span data-ttu-id="62380-2896">Passeport</span><span class="sxs-lookup"><span data-stu-id="62380-2896">Passeport#</span></span> 
- <span data-ttu-id="62380-2897">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="62380-2897">PasseportNon</span></span> 
- <span data-ttu-id="62380-2898">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="62380-2898">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="62380-2899">SWIFT-Code</span><span class="sxs-lookup"><span data-stu-id="62380-2899">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="62380-2900">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2900">Format</span></span>

<span data-ttu-id="62380-2901">Vier Buchstaben, gefolgt von 5-31 Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2901">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2902">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2902">Pattern</span></span>

<span data-ttu-id="62380-2903">Vier Buchstaben, gefolgt von 5 bis 31 Buchstaben oder Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2903">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="62380-2904">Vier Buchstaben für den Bankcode (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="62380-2904">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="62380-2905">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-2905">An optional space</span></span> 
- <span data-ttu-id="62380-2906">4 bis 28 Buchstaben oder Ziffern (BBAN, Basic Bank Account Number)</span><span class="sxs-lookup"><span data-stu-id="62380-2906">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="62380-2907">Ein optionales Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-2907">An optional space</span></span> 
- <span data-ttu-id="62380-2908">1 bis 3 Buchstaben oder Ziffern (Rest des BBAN)</span><span class="sxs-lookup"><span data-stu-id="62380-2908">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2909">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2909">Checksum</span></span>

<span data-ttu-id="62380-2910">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2910">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2911">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2911">Definition</span></span>

<span data-ttu-id="62380-2912">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2913">Der reguläre Ausdruck Regex_swift findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2913">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2914">Ein Schlüsselwort aus Keyword_swift wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2914">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2915">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2915">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="62380-2916">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="62380-2916">Keyword_swift</span></span>

- <span data-ttu-id="62380-2917">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="62380-2917">international organization for standardization 9362</span></span> 
- <span data-ttu-id="62380-2918">iso 9362</span><span class="sxs-lookup"><span data-stu-id="62380-2918">iso 9362</span></span> 
- <span data-ttu-id="62380-2919">ISO9362</span><span class="sxs-lookup"><span data-stu-id="62380-2919">iso9362</span></span> 
- <span data-ttu-id="62380-2920">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="62380-2920">swift\#</span></span> 
- <span data-ttu-id="62380-2921">Swiftcode</span><span class="sxs-lookup"><span data-stu-id="62380-2921">swiftcode</span></span> 
- <span data-ttu-id="62380-2922">swiftnumber</span><span class="sxs-lookup"><span data-stu-id="62380-2922">swiftnumber</span></span> 
- <span data-ttu-id="62380-2923">swiftroutingnumber</span><span class="sxs-lookup"><span data-stu-id="62380-2923">swiftroutingnumber</span></span> 
- <span data-ttu-id="62380-2924">swift code</span><span class="sxs-lookup"><span data-stu-id="62380-2924">swift code</span></span> 
- <span data-ttu-id="62380-2925">swift number #</span><span class="sxs-lookup"><span data-stu-id="62380-2925">swift number #</span></span> 
- <span data-ttu-id="62380-2926">swift routing number</span><span class="sxs-lookup"><span data-stu-id="62380-2926">swift routing number</span></span> 
- <span data-ttu-id="62380-2927">bic number</span><span class="sxs-lookup"><span data-stu-id="62380-2927">bic number</span></span> 
- <span data-ttu-id="62380-2928">bic code</span><span class="sxs-lookup"><span data-stu-id="62380-2928">bic code</span></span> 
- <span data-ttu-id="62380-2929">BIC\#</span><span class="sxs-lookup"><span data-stu-id="62380-2929">bic \#</span></span> 
- <span data-ttu-id="62380-2930">BIC\#</span><span class="sxs-lookup"><span data-stu-id="62380-2930">bic\#</span></span> 
- <span data-ttu-id="62380-2931">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="62380-2931">bank identifier code</span></span> 
- <span data-ttu-id="62380-2932">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="62380-2932">標準化9362</span></span> 
- <span data-ttu-id="62380-2933">迅速 #</span><span class="sxs-lookup"><span data-stu-id="62380-2933">迅速＃</span></span> 
- <span data-ttu-id="62380-2934">SWIFTコード</span><span class="sxs-lookup"><span data-stu-id="62380-2934">SWIFTコード</span></span> 
- <span data-ttu-id="62380-2935">SWIFT番号</span><span class="sxs-lookup"><span data-stu-id="62380-2935">SWIFT番号</span></span> 
- <span data-ttu-id="62380-2936">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="62380-2936">迅速なルーティング番号</span></span> 
- <span data-ttu-id="62380-2937">BIC番号</span><span class="sxs-lookup"><span data-stu-id="62380-2937">BIC番号</span></span> 
- <span data-ttu-id="62380-2938">BICコード</span><span class="sxs-lookup"><span data-stu-id="62380-2938">BICコード</span></span> 
- <span data-ttu-id="62380-2939">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="62380-2939">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="62380-2940">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="62380-2940">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="62380-2941">rapide\#</span><span class="sxs-lookup"><span data-stu-id="62380-2941">rapide \#</span></span> 
- <span data-ttu-id="62380-2942">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="62380-2942">code SWIFT</span></span> 
- <span data-ttu-id="62380-2943">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="62380-2943">le numéro de swift</span></span> 
- <span data-ttu-id="62380-2944">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="62380-2944">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="62380-2945">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="62380-2945">le numéro BIC</span></span> 
- <span data-ttu-id="62380-2946">\#BIC</span><span class="sxs-lookup"><span data-stu-id="62380-2946">\# BIC</span></span> 
- <span data-ttu-id="62380-2947">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="62380-2947">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="62380-2948">Taiwanesicher Personalausweis</span><span class="sxs-lookup"><span data-stu-id="62380-2948">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="62380-2949">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2949">Format</span></span>

<span data-ttu-id="62380-2950">Ein Buchstabe (auf Englisch) gefolgt von neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2950">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2951">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2951">Pattern</span></span>

<span data-ttu-id="62380-2952">Ein Buchstabe (Englisch), gefolgt von neun Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-2952">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="62380-2953">Ein Buchstabe (Englisch, Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="62380-2953">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="62380-2954">Die Ziffer 1 oder 2</span><span class="sxs-lookup"><span data-stu-id="62380-2954">The digit "1" or "2"</span></span> 
- <span data-ttu-id="62380-2955">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2955">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2956">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2956">Checksum</span></span>

<span data-ttu-id="62380-2957">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-2957">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2958">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2958">Definition</span></span>

<span data-ttu-id="62380-2959">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2959">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2960">Die Funktion Func_taiwanese_national_id findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-2960">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2961">Ein Schlüsselwort aus Keyword_taiwanese_national_id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2961">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="62380-2962">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-2962">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2963">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2963">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="62380-2964">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="62380-2964">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="62380-2965">身份證字號</span><span class="sxs-lookup"><span data-stu-id="62380-2965">身份證字號</span></span> 
- <span data-ttu-id="62380-2966">身份證</span><span class="sxs-lookup"><span data-stu-id="62380-2966">身份證</span></span> 
- <span data-ttu-id="62380-2967">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="62380-2967">身份證號碼</span></span> 
- <span data-ttu-id="62380-2968">身份證號</span><span class="sxs-lookup"><span data-stu-id="62380-2968">身份證號</span></span> 
- <span data-ttu-id="62380-2969">身分證字號</span><span class="sxs-lookup"><span data-stu-id="62380-2969">身分證字號</span></span> 
- <span data-ttu-id="62380-2970">身分證</span><span class="sxs-lookup"><span data-stu-id="62380-2970">身分證</span></span> 
- <span data-ttu-id="62380-2971">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="62380-2971">身分證號碼</span></span> 
- <span data-ttu-id="62380-2972">身份證號</span><span class="sxs-lookup"><span data-stu-id="62380-2972">身份證號</span></span> 
- <span data-ttu-id="62380-2973">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="62380-2973">身分證統一編號</span></span> 
- <span data-ttu-id="62380-2974">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="62380-2974">國民身分證統一編號</span></span> 
- <span data-ttu-id="62380-2975">簽名</span><span class="sxs-lookup"><span data-stu-id="62380-2975">簽名</span></span> 
- <span data-ttu-id="62380-2976">蓋章</span><span class="sxs-lookup"><span data-stu-id="62380-2976">蓋章</span></span> 
- <span data-ttu-id="62380-2977">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="62380-2977">簽名或蓋章</span></span> 
- <span data-ttu-id="62380-2978">簽章</span><span class="sxs-lookup"><span data-stu-id="62380-2978">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="62380-2979">	Taiwan – Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="62380-2979">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-2980">Format</span><span class="sxs-lookup"><span data-stu-id="62380-2980">Format</span></span>

- <span data-ttu-id="62380-2981">Biometrische Passnummer: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2981">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="62380-2982">Nicht-biometrische Passnummer: neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2982">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-2983">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-2983">Pattern</span></span>
<span data-ttu-id="62380-2984">Biometrische Passnummer:</span><span class="sxs-lookup"><span data-stu-id="62380-2984">Biometric passport number:</span></span>
- <span data-ttu-id="62380-2985">Die Ziffer "3" </span><span class="sxs-lookup"><span data-stu-id="62380-2985">The digit "3"</span></span> 
- <span data-ttu-id="62380-2986">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2986">Eight digits</span></span>

<span data-ttu-id="62380-2987">Nicht-biometrische Passport-Nummer:</span><span class="sxs-lookup"><span data-stu-id="62380-2987">Non-biometric passport number:</span></span>
- <span data-ttu-id="62380-2988">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-2988">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-2989">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-2989">Checksum</span></span>

<span data-ttu-id="62380-2990">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-2990">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-2991">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-2991">Definition</span></span>

<span data-ttu-id="62380-2992">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-2992">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-2993">Der reguläre Ausdruck Regex_taiwan_passport findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-2993">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-2994">Ein Schlüsselwort aus Keyword_taiwan_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-2994">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-2995">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-2995">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="62380-2996">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="62380-2996">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="62380-2997">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="62380-2997">ROC passport number</span></span> 
- <span data-ttu-id="62380-2998">Passport number</span><span class="sxs-lookup"><span data-stu-id="62380-2998">Passport number</span></span> 
- <span data-ttu-id="62380-2999">Passport no</span><span class="sxs-lookup"><span data-stu-id="62380-2999">Passport no</span></span> 
- <span data-ttu-id="62380-3000">Passport Num</span><span class="sxs-lookup"><span data-stu-id="62380-3000">Passport Num</span></span> 
- <span data-ttu-id="62380-3001">Passport #</span><span class="sxs-lookup"><span data-stu-id="62380-3001">Passport #</span></span> 
- <span data-ttu-id="62380-3002">护照</span><span class="sxs-lookup"><span data-stu-id="62380-3002">护照</span></span> 
- <span data-ttu-id="62380-3003">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="62380-3003">中華民國護照</span></span> 
- <span data-ttu-id="62380-3004">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="62380-3004">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="62380-3005">Taiwan – Einwohnerzertifikatsnummer (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="62380-3005">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-3006">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3006">Format</span></span>

<span data-ttu-id="62380-3007">10 Buchstaben und Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3007">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3008">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3008">Pattern</span></span>

<span data-ttu-id="62380-3009">10 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-3009">10 letters and digits:</span></span>
- <span data-ttu-id="62380-3010">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant) </span><span class="sxs-lookup"><span data-stu-id="62380-3010">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="62380-3011">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3011">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3012">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3012">Checksum</span></span>

<span data-ttu-id="62380-3013">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-3013">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-3014">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3014">Definition</span></span>

<span data-ttu-id="62380-3015">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3015">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3016">Der reguläre Ausdruck Regex_taiwan_resident_certificate findet Inhalte, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-3016">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3017">Ein Schlüsselwort aus Keyword_taiwan_resident_certificate wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3017">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-3018">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3018">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="62380-3019">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="62380-3019">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="62380-3020">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="62380-3020">Resident Certificate</span></span> 
- <span data-ttu-id="62380-3021">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="62380-3021">Resident Cert</span></span> 
- <span data-ttu-id="62380-3022">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="62380-3022">Resident Cert.</span></span> 
- <span data-ttu-id="62380-3023">Identification card</span><span class="sxs-lookup"><span data-stu-id="62380-3023">Identification card</span></span> 
- <span data-ttu-id="62380-3024">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="62380-3024">Alien Resident Certificate</span></span> 
- <span data-ttu-id="62380-3025">Bogens</span><span class="sxs-lookup"><span data-stu-id="62380-3025">ARC</span></span> 
- <span data-ttu-id="62380-3026">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="62380-3026">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="62380-3027">TARC</span><span class="sxs-lookup"><span data-stu-id="62380-3027">TARC</span></span> 
- <span data-ttu-id="62380-3028">居留證</span><span class="sxs-lookup"><span data-stu-id="62380-3028">居留證</span></span> 
- <span data-ttu-id="62380-3029">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="62380-3029">外僑居留證</span></span> 
- <span data-ttu-id="62380-3030">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="62380-3030">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="62380-3031">Thai-Populations Identifizierungs Code</span><span class="sxs-lookup"><span data-stu-id="62380-3031">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="62380-3032">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3032">Format</span></span>

<span data-ttu-id="62380-3033">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3033">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3034">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3034">Pattern</span></span>

<span data-ttu-id="62380-3035">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-3035">13 digits:</span></span>
- <span data-ttu-id="62380-3036">Die erste Ziffer ist 0 oder 9.</span><span class="sxs-lookup"><span data-stu-id="62380-3036">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="62380-3037">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3037">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3038">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3038">Checksum</span></span>

<span data-ttu-id="62380-3039">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-3039">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-3040">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3040">Definition</span></span>

<span data-ttu-id="62380-3041">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3041">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3042">Die Funktion Func_Thai_Citizen_Id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-3042">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3043">Ein Schlüsselwort aus Keyword_Thai_Citizen_Id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3043">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="62380-3044">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3044">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3045">Die Funktion Func_Thai_Citizen_Id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-3045">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-3046">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3046">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="62380-3047">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="62380-3047">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="62380-3048">ID Number</span><span class="sxs-lookup"><span data-stu-id="62380-3048">ID Number</span></span>
- <span data-ttu-id="62380-3049">IdentifikationsNummer</span><span class="sxs-lookup"><span data-stu-id="62380-3049">Identification Number</span></span>
- <span data-ttu-id="62380-3050">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="62380-3050">บัตรประชาชน</span></span>
- <span data-ttu-id="62380-3051">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="62380-3051">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="62380-3052">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="62380-3052">บัตรประชาชน</span></span>
- <span data-ttu-id="62380-3053">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="62380-3053">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="62380-3054">Türkische nationale IdentifikationsNummer</span><span class="sxs-lookup"><span data-stu-id="62380-3054">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-3055">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3055">Format</span></span>

<span data-ttu-id="62380-3056">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3056">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3057">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3057">Pattern</span></span>

<span data-ttu-id="62380-3058">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3058">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3059">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3059">Checksum</span></span>

<span data-ttu-id="62380-3060">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-3061">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3061">Definition</span></span>

<span data-ttu-id="62380-3062">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3063">Die Funktion Func_Turkish_National_Id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-3063">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3064">Ein Schlüsselwort aus Keyword_Turkish_National_Id wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3064">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="62380-3065">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3065">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3066">Die Funktion Func_Turkish_National_Id sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-3066">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-3067">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3067">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="62380-3068">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="62380-3068">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="62380-3069">TC KİMLİK Nein</span><span class="sxs-lookup"><span data-stu-id="62380-3069">TC Kimlik No</span></span>
- <span data-ttu-id="62380-3070">TC KİMLİK numarası</span><span class="sxs-lookup"><span data-stu-id="62380-3070">TC Kimlik numarası</span></span>
- <span data-ttu-id="62380-3071">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="62380-3071">Vatandaşlık numarası</span></span>
- <span data-ttu-id="62380-3072">Vatandaşlık Nein</span><span class="sxs-lookup"><span data-stu-id="62380-3072">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="62380-p141">Britische Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-3075">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3075">Format</span></span>

<span data-ttu-id="62380-3076">Kombination aus 18 Buchstaben und Ziffern im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="62380-3076">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3077">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3077">Pattern</span></span>

<span data-ttu-id="62380-3078">18 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="62380-3078">18 letters and digits:</span></span>
- <span data-ttu-id="62380-3079">Fünf Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) oder die Ziffer 9 anstelle eines Buchstabens</span><span class="sxs-lookup"><span data-stu-id="62380-3079">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="62380-3080">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="62380-3080">One digit</span></span> 
- <span data-ttu-id="62380-3081">Fünf Ziffern im Datumsformat TTMMJ für das Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="62380-3081">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="62380-3082">Zwei Buchstaben (ohne Beachtung der Groß-/Kleinschreibung) oder die Ziffer 9 anstelle eines Buchstabens</span><span class="sxs-lookup"><span data-stu-id="62380-3082">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="62380-3083">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3083">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3084">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3084">Checksum</span></span>

<span data-ttu-id="62380-3085">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-3085">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-3086">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3086">Definition</span></span>

<span data-ttu-id="62380-3087">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3087">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3088">Die Funktion Func_uk_drivers_license findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3088">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3089">Ein Schlüsselwort aus Keyword_uk_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3089">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="62380-3090">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-3090">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-3091">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3091">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="62380-3092">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="62380-3092">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="62380-3093">DVLA</span><span class="sxs-lookup"><span data-stu-id="62380-3093">DVLA</span></span> 
- <span data-ttu-id="62380-3094">light vans</span><span class="sxs-lookup"><span data-stu-id="62380-3094">light vans</span></span> 
- <span data-ttu-id="62380-3095">Quads entwickelt</span><span class="sxs-lookup"><span data-stu-id="62380-3095">quadbikes</span></span> 
- <span data-ttu-id="62380-3096">motor cars</span><span class="sxs-lookup"><span data-stu-id="62380-3096">motor cars</span></span> 
- <span data-ttu-id="62380-3097">125cc</span><span class="sxs-lookup"><span data-stu-id="62380-3097">125cc</span></span> 
- <span data-ttu-id="62380-3098">Beiwagen</span><span class="sxs-lookup"><span data-stu-id="62380-3098">sidecar</span></span> 
- <span data-ttu-id="62380-3099">Dreiräder</span><span class="sxs-lookup"><span data-stu-id="62380-3099">tricycles</span></span> 
- <span data-ttu-id="62380-3100">Motorrad</span><span class="sxs-lookup"><span data-stu-id="62380-3100">motorcycles</span></span> 
- <span data-ttu-id="62380-3101">photocard licence</span><span class="sxs-lookup"><span data-stu-id="62380-3101">photocard licence</span></span> 
- <span data-ttu-id="62380-3102">learner drivers</span><span class="sxs-lookup"><span data-stu-id="62380-3102">learner drivers</span></span> 
- <span data-ttu-id="62380-3103">licence holder</span><span class="sxs-lookup"><span data-stu-id="62380-3103">licence holder</span></span> 
- <span data-ttu-id="62380-3104">licence holders</span><span class="sxs-lookup"><span data-stu-id="62380-3104">licence holders</span></span> 
- <span data-ttu-id="62380-3105">driving licences</span><span class="sxs-lookup"><span data-stu-id="62380-3105">driving licences</span></span> 
- <span data-ttu-id="62380-3106">driving licence</span><span class="sxs-lookup"><span data-stu-id="62380-3106">driving licence</span></span> 
- <span data-ttu-id="62380-3107">dual control car</span><span class="sxs-lookup"><span data-stu-id="62380-3107">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="62380-p142">Britische Wählerverzeichnisnummer</span><span class="sxs-lookup"><span data-stu-id="62380-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-3110">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3110">Format</span></span>

<span data-ttu-id="62380-3111">Zwei Buchstaben gefolgt von 1-4 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3111">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3112">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3112">Pattern</span></span>

<span data-ttu-id="62380-3113">Zwei Buchstaben (Groß-/Kleinschreibung irrelevant), gefolgt von 1-4 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3113">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3114">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3114">Checksum</span></span>

<span data-ttu-id="62380-3115">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-3115">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-3116">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3116">Definition</span></span>

<span data-ttu-id="62380-3117">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3118">Der reguläre Ausdruck Regex_uk_electoral findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3118">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3119">Ein Schlüsselwort aus Keyword_uk_electoral wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3119">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-3120">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3120">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="62380-3121">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="62380-3121">Keyword_uk_electoral</span></span>

- <span data-ttu-id="62380-3122">council nomination</span><span class="sxs-lookup"><span data-stu-id="62380-3122">council nomination</span></span> 
- <span data-ttu-id="62380-3123">nomination form</span><span class="sxs-lookup"><span data-stu-id="62380-3123">nomination form</span></span> 
- <span data-ttu-id="62380-3124">electoral register</span><span class="sxs-lookup"><span data-stu-id="62380-3124">electoral register</span></span> 
- <span data-ttu-id="62380-3125">electoral roll</span><span class="sxs-lookup"><span data-stu-id="62380-3125">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="62380-p143">Britische National Health Service-Nummer</span><span class="sxs-lookup"><span data-stu-id="62380-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-3128">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3128">Format</span></span>

<span data-ttu-id="62380-3129">10-17 Ziffern, durch Leerzeichen getrennt</span><span class="sxs-lookup"><span data-stu-id="62380-3129">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3130">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3130">Pattern</span></span>

<span data-ttu-id="62380-3131">10 bis 17 Stellen:</span><span class="sxs-lookup"><span data-stu-id="62380-3131">10-17 digits:</span></span>
- <span data-ttu-id="62380-3132">3 oder 10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3132">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="62380-3133">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-3133">A space</span></span> 
- <span data-ttu-id="62380-3134">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3134">Three digits</span></span> 
- <span data-ttu-id="62380-3135">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="62380-3135">A space</span></span> 
- <span data-ttu-id="62380-3136">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3136">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3137">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3137">Checksum</span></span>

<span data-ttu-id="62380-3138">Ja</span><span class="sxs-lookup"><span data-stu-id="62380-3138">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="62380-3139">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3139">Definition</span></span>

<span data-ttu-id="62380-3140">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3140">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3141">Die Funktion Func_uk_nhs_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3141">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3142">Eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="62380-3142">One of the following is true:</span></span>
    - <span data-ttu-id="62380-3143">Ein Schlüsselwort aus Keyword_uk_nhs_number wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3143">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="62380-3144">Ein Schlüsselwort aus Keyword_uk_nhs_number1 wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3144">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="62380-3145">Ein Schlüsselwort aus Keyword_uk_nhs_number_dob wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3145">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="62380-3146">Die Prüfsumme stimmt.</span><span class="sxs-lookup"><span data-stu-id="62380-3146">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-3147">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3147">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="62380-3148">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="62380-3148">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="62380-3149">national health service</span><span class="sxs-lookup"><span data-stu-id="62380-3149">national health service</span></span> 
- <span data-ttu-id="62380-3150">NHS</span><span class="sxs-lookup"><span data-stu-id="62380-3150">nhs</span></span> 
- <span data-ttu-id="62380-3151">health services authority</span><span class="sxs-lookup"><span data-stu-id="62380-3151">health services authority</span></span> 
- <span data-ttu-id="62380-3152">health authority</span><span class="sxs-lookup"><span data-stu-id="62380-3152">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="62380-3153">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="62380-3153">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="62380-3154">patient id</span><span class="sxs-lookup"><span data-stu-id="62380-3154">patient id</span></span> 
- <span data-ttu-id="62380-3155">patient identification</span><span class="sxs-lookup"><span data-stu-id="62380-3155">patient identification</span></span> 
- <span data-ttu-id="62380-3156">patient no</span><span class="sxs-lookup"><span data-stu-id="62380-3156">patient no</span></span> 
- <span data-ttu-id="62380-3157">patient number</span><span class="sxs-lookup"><span data-stu-id="62380-3157">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="62380-3158">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="62380-3158">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="62380-3159">GP</span><span class="sxs-lookup"><span data-stu-id="62380-3159">GP</span></span> 
- <span data-ttu-id="62380-3160">DOB</span><span class="sxs-lookup"><span data-stu-id="62380-3160">DOB</span></span> 
- <span data-ttu-id="62380-3161">D. O. B</span><span class="sxs-lookup"><span data-stu-id="62380-3161">D.O.B</span></span> 
- <span data-ttu-id="62380-3162">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="62380-3162">Date of Birth</span></span> 
- <span data-ttu-id="62380-3163">Birth Date</span><span class="sxs-lookup"><span data-stu-id="62380-3163">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="62380-p144">Britische nationale Versicherungsnummer (NINO)</span><span class="sxs-lookup"><span data-stu-id="62380-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="62380-3166">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3166">Format</span></span>

<span data-ttu-id="62380-3167">7 Zeichen oder 9 Zeichen voneinander getrennt durch Leerzeichen oder Bindestriche</span><span class="sxs-lookup"><span data-stu-id="62380-3167">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3168">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3168">Pattern</span></span>

<span data-ttu-id="62380-3169">Zwei mögliche Muster:</span><span class="sxs-lookup"><span data-stu-id="62380-3169">Two possible patterns:</span></span>

- <span data-ttu-id="62380-3170">Zwei Buchstaben (gültige NINOs verwenden nur bestimmte Zeichen in diesem Präfix, die dieses Muster validiert; Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="62380-3170">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="62380-3171">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3171">Six digits</span></span>
- <span data-ttu-id="62380-3172">Entweder "A", "B", "C" oder "'D" (wie das Präfix, nur bestimmte Zeichen sind im Suffix zulässig; Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="62380-3172">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="62380-3173">ODER</span><span class="sxs-lookup"><span data-stu-id="62380-3173">OR</span></span>

- <span data-ttu-id="62380-3174">Zwei Buchstaben</span><span class="sxs-lookup"><span data-stu-id="62380-3174">Two letters</span></span>
- <span data-ttu-id="62380-3175">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-3175">A space or dash</span></span>
- <span data-ttu-id="62380-3176">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3176">Two digits</span></span>
- <span data-ttu-id="62380-3177">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-3177">A space or dash</span></span>
- <span data-ttu-id="62380-3178">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3178">Two digits</span></span>
- <span data-ttu-id="62380-3179">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-3179">A space or dash</span></span>
- <span data-ttu-id="62380-3180">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3180">Two digits</span></span>
- <span data-ttu-id="62380-3181">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-3181">A space or dash</span></span>
- <span data-ttu-id="62380-3182">Entweder "A", "B", "C" oder "'D"</span><span class="sxs-lookup"><span data-stu-id="62380-3182">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3183">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3183">Checksum</span></span>

<span data-ttu-id="62380-3184">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-3184">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-3185">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3185">Definition</span></span>

<span data-ttu-id="62380-3186">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3186">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3187">Die Funktion Func_uk_nino findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3187">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3188">Ein Schlüsselwort aus Keyword_uk_nino wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3188">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="62380-3189">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3190">Die Funktion Func_uk_nino findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3190">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3191">Es wurde kein Schlüsselwort aus Keyword_uk_nino gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3191">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-3192">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3192">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="62380-3193">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="62380-3193">Keyword_uk_nino</span></span>

- <span data-ttu-id="62380-3194">national insurance number</span><span class="sxs-lookup"><span data-stu-id="62380-3194">national insurance number</span></span> 
- <span data-ttu-id="62380-3195">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="62380-3195">national insurance contributions</span></span> 
- <span data-ttu-id="62380-3196">protection act</span><span class="sxs-lookup"><span data-stu-id="62380-3196">protection act</span></span> 
- <span data-ttu-id="62380-3197">Versicherung</span><span class="sxs-lookup"><span data-stu-id="62380-3197">insurance</span></span> 
- <span data-ttu-id="62380-3198">social security number</span><span class="sxs-lookup"><span data-stu-id="62380-3198">social security number</span></span> 
- <span data-ttu-id="62380-3199">insurance application</span><span class="sxs-lookup"><span data-stu-id="62380-3199">insurance application</span></span> 
- <span data-ttu-id="62380-3200">medical application</span><span class="sxs-lookup"><span data-stu-id="62380-3200">medical application</span></span> 
- <span data-ttu-id="62380-3201">social insurance</span><span class="sxs-lookup"><span data-stu-id="62380-3201">social insurance</span></span> 
- <span data-ttu-id="62380-3202">medical attention</span><span class="sxs-lookup"><span data-stu-id="62380-3202">medical attention</span></span> 
- <span data-ttu-id="62380-3203">social security</span><span class="sxs-lookup"><span data-stu-id="62380-3203">social security</span></span> 
- <span data-ttu-id="62380-3204">great britain</span><span class="sxs-lookup"><span data-stu-id="62380-3204">great britain</span></span> 
- <span data-ttu-id="62380-3205">Versicherung</span><span class="sxs-lookup"><span data-stu-id="62380-3205">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="62380-p145">US-amerikanische/britische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="62380-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-3208">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3208">Format</span></span>

<span data-ttu-id="62380-3209">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3209">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3210">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3210">Pattern</span></span>

<span data-ttu-id="62380-3211">Neun aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3211">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3212">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3212">Checksum</span></span>

<span data-ttu-id="62380-3213">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-3213">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-3214">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3214">Definition</span></span>

<span data-ttu-id="62380-3215">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3215">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3216">Die Funktion Func_usa_uk_passport findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3216">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3217">Ein Schlüsselwort aus Keyword_passport wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3217">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-3218">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3218">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="62380-3219">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="62380-3219">Keyword_passport</span></span>

- <span data-ttu-id="62380-3220">Passport Number</span><span class="sxs-lookup"><span data-stu-id="62380-3220">Passport Number</span></span> 
- <span data-ttu-id="62380-3221">Passport No</span><span class="sxs-lookup"><span data-stu-id="62380-3221">Passport No</span></span> 
- <span data-ttu-id="62380-3222">Passport#</span><span class="sxs-lookup"><span data-stu-id="62380-3222">Passport #</span></span> 
- <span data-ttu-id="62380-3223">Pass</span><span class="sxs-lookup"><span data-stu-id="62380-3223">Passport#</span></span> 
- <span data-ttu-id="62380-3224">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="62380-3224">PassportID</span></span> 
- <span data-ttu-id="62380-3225">Passportno</span><span class="sxs-lookup"><span data-stu-id="62380-3225">Passportno</span></span> 
- <span data-ttu-id="62380-3226">passportnumber</span><span class="sxs-lookup"><span data-stu-id="62380-3226">passportnumber</span></span> 
- <span data-ttu-id="62380-3227">パスポート</span><span class="sxs-lookup"><span data-stu-id="62380-3227">パスポート</span></span> 
- <span data-ttu-id="62380-3228">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="62380-3228">パスポート番号</span></span> 
- <span data-ttu-id="62380-3229">パスポートのNum</span><span class="sxs-lookup"><span data-stu-id="62380-3229">パスポートのNum</span></span> 
- <span data-ttu-id="62380-3230">パスポート #</span><span class="sxs-lookup"><span data-stu-id="62380-3230">パスポート＃</span></span> 
- <span data-ttu-id="62380-3231">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="62380-3231">Numéro de passeport</span></span> 
- <span data-ttu-id="62380-3232">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="62380-3232">Passeport n °</span></span> 
- <span data-ttu-id="62380-3233">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="62380-3233">Passeport Non</span></span> 
- <span data-ttu-id="62380-3234">Passeport#</span><span class="sxs-lookup"><span data-stu-id="62380-3234">Passeport #</span></span> 
- <span data-ttu-id="62380-3235">Passeport</span><span class="sxs-lookup"><span data-stu-id="62380-3235">Passeport#</span></span> 
- <span data-ttu-id="62380-3236">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="62380-3236">PasseportNon</span></span> 
- <span data-ttu-id="62380-3237">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="62380-3237">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="62380-3238">US-Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="62380-3238">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-3239">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3239">Format</span></span>

<span data-ttu-id="62380-3240">8-17 Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3240">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3241">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3241">Pattern</span></span>

<span data-ttu-id="62380-3242">8-17 aufeinanderfolgende Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3242">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3243">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3243">Checksum</span></span>

<span data-ttu-id="62380-3244">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-3244">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-3245">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3245">Definition</span></span>

<span data-ttu-id="62380-3246">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3247">Der reguläre Ausdruck Regex_usa_bank_account_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3247">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3248">Ein Schlüsselwort aus Keyword_usa_Bank_Account wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3248">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="62380-3249">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3249">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="62380-3250">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="62380-3250">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="62380-3251">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="62380-3251">Checking Account Number</span></span> 
- <span data-ttu-id="62380-3252">Checking Account</span><span class="sxs-lookup"><span data-stu-id="62380-3252">Checking Account</span></span> 
- <span data-ttu-id="62380-3253">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="62380-3253">Checking Account #</span></span> 
- <span data-ttu-id="62380-3254">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="62380-3254">Checking Acct Number</span></span> 
- <span data-ttu-id="62380-3255">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="62380-3255">Checking Acct #</span></span> 
- <span data-ttu-id="62380-3256">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="62380-3256">Checking Acct No.</span></span> 
- <span data-ttu-id="62380-3257">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="62380-3257">Checking Account No.</span></span> 
- <span data-ttu-id="62380-3258">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="62380-3258">Bank Account Number</span></span> 
- <span data-ttu-id="62380-3259">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="62380-3259">Bank Account #</span></span> 
- <span data-ttu-id="62380-3260">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="62380-3260">Bank Acct Number</span></span> 
- <span data-ttu-id="62380-3261">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="62380-3261">Bank Acct #</span></span> 
- <span data-ttu-id="62380-3262">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="62380-3262">Bank Acct No.</span></span> 
- <span data-ttu-id="62380-3263">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="62380-3263">Bank Account No.</span></span> 
- <span data-ttu-id="62380-3264">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="62380-3264">Savings Account Number</span></span> 
- <span data-ttu-id="62380-3265">Savings Account</span><span class="sxs-lookup"><span data-stu-id="62380-3265">Savings Account.</span></span> 
- <span data-ttu-id="62380-3266">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="62380-3266">Savings Account #</span></span> 
- <span data-ttu-id="62380-3267">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="62380-3267">Savings Acct Number</span></span> 
- <span data-ttu-id="62380-3268">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="62380-3268">Savings Acct #</span></span> 
- <span data-ttu-id="62380-3269">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="62380-3269">Savings Acct No.</span></span> 
- <span data-ttu-id="62380-3270">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="62380-3270">Savings Account No.</span></span> 
- <span data-ttu-id="62380-3271">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="62380-3271">Debit Account Number</span></span> 
- <span data-ttu-id="62380-3272">Debit Account</span><span class="sxs-lookup"><span data-stu-id="62380-3272">Debit Account</span></span> 
- <span data-ttu-id="62380-3273">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="62380-3273">Debit Account #</span></span> 
- <span data-ttu-id="62380-3274">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="62380-3274">Debit Acct Number</span></span> 
- <span data-ttu-id="62380-3275">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="62380-3275">Debit Acct #</span></span> 
- <span data-ttu-id="62380-3276">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="62380-3276">Debit Acct No.</span></span> 
- <span data-ttu-id="62380-3277">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="62380-3277">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="62380-3278">US-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="62380-3278">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="62380-3279">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3279">Format</span></span>

<span data-ttu-id="62380-3280">Abhängig vom Bundesstaat</span><span class="sxs-lookup"><span data-stu-id="62380-3280">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3281">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3281">Pattern</span></span>

<span data-ttu-id="62380-3282">Abhängig vom Bundesstaat – am Beispiel für New York:</span><span class="sxs-lookup"><span data-stu-id="62380-3282">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="62380-3283">Neun Ziffern, die wie DDD DDD DDD formatiert sind, stimmen überein.</span><span class="sxs-lookup"><span data-stu-id="62380-3283">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="62380-3284">Neun Ziffern wie ddddddddd werden nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-3284">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3285">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3285">Checksum</span></span>

<span data-ttu-id="62380-3286">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-3287">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3287">Definition</span></span>

<span data-ttu-id="62380-3288">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3289">Die Funktion Func_new_york_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3289">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3290">Ein Schlüsselwort aus Keyword_[state_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3290">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="62380-3291">Ein Schlüsselwort aus Keyword_us_drivers_license wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3291">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="62380-3292">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3292">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3293">Die Funktion Func_new_york_drivers_license_number findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3293">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3294">Ein Schlüsselwort aus Keyword_[state_name]_drivers_license_name wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3294">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="62380-3295">Ein Schlüsselwort aus Keyword_us_drivers_license_abbreviations wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3295">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="62380-3296">Es wurde kein Schlüsselwort aus Keyword_us_drivers_license gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3296">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-3297">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3297">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="62380-3298">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="62380-3298">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="62380-3299">DL</span><span class="sxs-lookup"><span data-stu-id="62380-3299">DL</span></span> 
- <span data-ttu-id="62380-3300">DLS</span><span class="sxs-lookup"><span data-stu-id="62380-3300">DLS</span></span> 
- <span data-ttu-id="62380-3301">CDL</span><span class="sxs-lookup"><span data-stu-id="62380-3301">CDL</span></span> 
- <span data-ttu-id="62380-3302">CDLS</span><span class="sxs-lookup"><span data-stu-id="62380-3302">CDLS</span></span> 
- <span data-ttu-id="62380-3303">ID</span><span class="sxs-lookup"><span data-stu-id="62380-3303">ID</span></span> 
- <span data-ttu-id="62380-3304">IDs</span><span class="sxs-lookup"><span data-stu-id="62380-3304">IDs</span></span> 
- <span data-ttu-id="62380-3305">DL</span><span class="sxs-lookup"><span data-stu-id="62380-3305">DL#</span></span> 
- <span data-ttu-id="62380-3306">DLS</span><span class="sxs-lookup"><span data-stu-id="62380-3306">DLS#</span></span> 
- <span data-ttu-id="62380-3307">CDL</span><span class="sxs-lookup"><span data-stu-id="62380-3307">CDL#</span></span> 
- <span data-ttu-id="62380-3308">CDLS</span><span class="sxs-lookup"><span data-stu-id="62380-3308">CDLS#</span></span> 
- <span data-ttu-id="62380-3309">ID</span><span class="sxs-lookup"><span data-stu-id="62380-3309">ID#</span></span>
- <span data-ttu-id="62380-3310">IDs</span><span class="sxs-lookup"><span data-stu-id="62380-3310">IDs#</span></span> 
- <span data-ttu-id="62380-3311">ID number</span><span class="sxs-lookup"><span data-stu-id="62380-3311">ID number</span></span> 
- <span data-ttu-id="62380-3312">ID numbers</span><span class="sxs-lookup"><span data-stu-id="62380-3312">ID numbers</span></span> 
- <span data-ttu-id="62380-3313">LIC</span><span class="sxs-lookup"><span data-stu-id="62380-3313">LIC</span></span> 
- <span data-ttu-id="62380-3314">LIC</span><span class="sxs-lookup"><span data-stu-id="62380-3314">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="62380-3315">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="62380-3315">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="62380-3316">DriverLic</span><span class="sxs-lookup"><span data-stu-id="62380-3316">DriverLic</span></span> 
- <span data-ttu-id="62380-3317">DriverLics</span><span class="sxs-lookup"><span data-stu-id="62380-3317">DriverLics</span></span> 
- <span data-ttu-id="62380-3318">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="62380-3318">DriverLicense</span></span> 
- <span data-ttu-id="62380-3319">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="62380-3319">DriverLicenses</span></span> 
- <span data-ttu-id="62380-3320">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="62380-3320">Driver Lic</span></span> 
- <span data-ttu-id="62380-3321">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="62380-3321">Driver Lics</span></span> 
- <span data-ttu-id="62380-3322">Driver License</span><span class="sxs-lookup"><span data-stu-id="62380-3322">Driver License</span></span> 
- <span data-ttu-id="62380-3323">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-3323">Driver Licenses</span></span> 
- <span data-ttu-id="62380-3324">DriversLic</span><span class="sxs-lookup"><span data-stu-id="62380-3324">DriversLic</span></span> 
- <span data-ttu-id="62380-3325">DriversLics</span><span class="sxs-lookup"><span data-stu-id="62380-3325">DriversLics</span></span> 
- <span data-ttu-id="62380-3326">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="62380-3326">DriversLicense</span></span> 
- <span data-ttu-id="62380-3327">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="62380-3327">DriversLicenses</span></span> 
- <span data-ttu-id="62380-3328">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="62380-3328">Drivers Lic</span></span> 
- <span data-ttu-id="62380-3329">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="62380-3329">Drivers Lics</span></span> 
- <span data-ttu-id="62380-3330">Drivers License</span><span class="sxs-lookup"><span data-stu-id="62380-3330">Drivers License</span></span> 
- <span data-ttu-id="62380-3331">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-3331">Drivers Licenses</span></span> 
- <span data-ttu-id="62380-3332">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="62380-3332">Driver'Lic</span></span> 
- <span data-ttu-id="62380-3333">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="62380-3333">Driver'Lics</span></span> 
- <span data-ttu-id="62380-3334">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="62380-3334">Driver'License</span></span> 
- <span data-ttu-id="62380-3335">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-3335">Driver'Licenses</span></span> 
- <span data-ttu-id="62380-3336">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="62380-3336">Driver' Lic</span></span> 
- <span data-ttu-id="62380-3337">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="62380-3337">Driver' Lics</span></span> 
- <span data-ttu-id="62380-3338">Driver' License</span><span class="sxs-lookup"><span data-stu-id="62380-3338">Driver' License</span></span> 
- <span data-ttu-id="62380-3339">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-3339">Driver' Licenses</span></span>
- <span data-ttu-id="62380-3340">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="62380-3340">Driver'sLic</span></span> 
- <span data-ttu-id="62380-3341">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="62380-3341">Driver'sLics</span></span> 
- <span data-ttu-id="62380-3342">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="62380-3342">Driver'sLicense</span></span> 
- <span data-ttu-id="62380-3343">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="62380-3343">Driver'sLicenses</span></span> 
- <span data-ttu-id="62380-3344">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="62380-3344">Driver's Lic</span></span> 
- <span data-ttu-id="62380-3345">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="62380-3345">Driver's Lics</span></span> 
- <span data-ttu-id="62380-3346">Driver's License</span><span class="sxs-lookup"><span data-stu-id="62380-3346">Driver's License</span></span> 
- <span data-ttu-id="62380-3347">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-3347">Driver's Licenses</span></span> 
- <span data-ttu-id="62380-3348">identification number</span><span class="sxs-lookup"><span data-stu-id="62380-3348">identification number</span></span> 
- <span data-ttu-id="62380-3349">identification numbers</span><span class="sxs-lookup"><span data-stu-id="62380-3349">identification numbers</span></span> 
- <span data-ttu-id="62380-3350">identification#</span><span class="sxs-lookup"><span data-stu-id="62380-3350">identification #</span></span> 
- <span data-ttu-id="62380-3351">id card</span><span class="sxs-lookup"><span data-stu-id="62380-3351">id card</span></span> 
- <span data-ttu-id="62380-3352">id cards</span><span class="sxs-lookup"><span data-stu-id="62380-3352">id cards</span></span> 
- <span data-ttu-id="62380-3353">identification card</span><span class="sxs-lookup"><span data-stu-id="62380-3353">identification card</span></span> 
- <span data-ttu-id="62380-3354">identification cards</span><span class="sxs-lookup"><span data-stu-id="62380-3354">identification cards</span></span> 
- <span data-ttu-id="62380-3355">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="62380-3355">DriverLic#</span></span> 
- <span data-ttu-id="62380-3356">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="62380-3356">DriverLics#</span></span> 
- <span data-ttu-id="62380-3357">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="62380-3357">DriverLicense#</span></span> 
- <span data-ttu-id="62380-3358">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="62380-3358">DriverLicenses#</span></span> 
- <span data-ttu-id="62380-3359">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-3359">Driver Lic#</span></span> 
- <span data-ttu-id="62380-3360">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-3360">Driver Lics#</span></span> 
- <span data-ttu-id="62380-3361">Driver License#</span><span class="sxs-lookup"><span data-stu-id="62380-3361">Driver License#</span></span> 
- <span data-ttu-id="62380-3362">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-3362">Driver Licenses#</span></span> 
- <span data-ttu-id="62380-3363">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="62380-3363">DriversLic#</span></span> 
- <span data-ttu-id="62380-3364">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="62380-3364">DriversLics#</span></span> 
- <span data-ttu-id="62380-3365">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="62380-3365">DriversLicense#</span></span> 
- <span data-ttu-id="62380-3366">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="62380-3366">DriversLicenses#</span></span> 
- <span data-ttu-id="62380-3367">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-3367">Drivers Lic#</span></span> 
- <span data-ttu-id="62380-3368">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-3368">Drivers Lics#</span></span> 
- <span data-ttu-id="62380-3369">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="62380-3369">Drivers License#</span></span> 
- <span data-ttu-id="62380-3370">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-3370">Drivers Licenses#</span></span> 
- <span data-ttu-id="62380-3371">Driver'Lic #</span><span class="sxs-lookup"><span data-stu-id="62380-3371">Driver'Lic#</span></span> 
- <span data-ttu-id="62380-3372">Driver'Lics #</span><span class="sxs-lookup"><span data-stu-id="62380-3372">Driver'Lics#</span></span> 
- <span data-ttu-id="62380-3373">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="62380-3373">Driver'License#</span></span> 
- <span data-ttu-id="62380-3374">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="62380-3374">Driver'Licenses#</span></span> 
- <span data-ttu-id="62380-3375">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-3375">Driver' Lic#</span></span> 
- <span data-ttu-id="62380-3376">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-3376">Driver' Lics#</span></span> 
- <span data-ttu-id="62380-3377">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="62380-3377">Driver' License#</span></span> 
- <span data-ttu-id="62380-3378">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-3378">Driver' Licenses#</span></span> 
- <span data-ttu-id="62380-3379">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="62380-3379">Driver'sLic#</span></span> 
- <span data-ttu-id="62380-3380">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="62380-3380">Driver'sLics#</span></span> 
- <span data-ttu-id="62380-3381">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="62380-3381">Driver'sLicense#</span></span> 
- <span data-ttu-id="62380-3382">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="62380-3382">Driver'sLicenses#</span></span> 
- <span data-ttu-id="62380-3383">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="62380-3383">Driver's Lic#</span></span> 
- <span data-ttu-id="62380-3384">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="62380-3384">Driver's Lics#</span></span> 
- <span data-ttu-id="62380-3385">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="62380-3385">Driver's License#</span></span> 
- <span data-ttu-id="62380-3386">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="62380-3386">Driver's Licenses#</span></span> 
- <span data-ttu-id="62380-3387">id card#</span><span class="sxs-lookup"><span data-stu-id="62380-3387">id card#</span></span> 
- <span data-ttu-id="62380-3388">id cards#</span><span class="sxs-lookup"><span data-stu-id="62380-3388">id cards#</span></span> 
- <span data-ttu-id="62380-3389">identification card#</span><span class="sxs-lookup"><span data-stu-id="62380-3389">identification card#</span></span> 
- <span data-ttu-id="62380-3390">identification cards#</span><span class="sxs-lookup"><span data-stu-id="62380-3390">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="62380-3391">Keyword_ [state_name] _drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="62380-3391">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="62380-3392">Abkürzung für Bundesstaat (z. B. „NY“)</span><span class="sxs-lookup"><span data-stu-id="62380-3392">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="62380-3393">Name des Bundesstaats (z. B. „New York“)</span><span class="sxs-lookup"><span data-stu-id="62380-3393">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="62380-3394">US-Steueridentifikationsnummer (ITIN)</span><span class="sxs-lookup"><span data-stu-id="62380-3394">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="62380-3395">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3395">Format</span></span>

<span data-ttu-id="62380-3396">Neun Ziffern, die mit "9" beginnen und "7" oder "8" als vierte Ziffer enthalten, optional mit Leerzeichen oder Bindestrichen formatiert</span><span class="sxs-lookup"><span data-stu-id="62380-3396">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3397">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3397">Pattern</span></span>

<span data-ttu-id="62380-3398">Formatiert</span><span class="sxs-lookup"><span data-stu-id="62380-3398">Formatted:</span></span>
- <span data-ttu-id="62380-3399">Die Ziffer 9</span><span class="sxs-lookup"><span data-stu-id="62380-3399">The digit "9"</span></span> 
- <span data-ttu-id="62380-3400">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3400">Two digits</span></span> 
- <span data-ttu-id="62380-3401">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-3401">A space or dash</span></span> 
- <span data-ttu-id="62380-3402">Eine 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="62380-3402">A "7" or "8"</span></span> 
- <span data-ttu-id="62380-3403">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="62380-3403">A digit</span></span> 
- <span data-ttu-id="62380-3404">Ein Leerzeichen oder ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="62380-3404">A space, or dash</span></span> 
- <span data-ttu-id="62380-3405">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3405">Four digits</span></span>

<span data-ttu-id="62380-3406">Unformatiert</span><span class="sxs-lookup"><span data-stu-id="62380-3406">Unformatted:</span></span>
- <span data-ttu-id="62380-3407">Die Ziffer 9</span><span class="sxs-lookup"><span data-stu-id="62380-3407">The digit "9"</span></span> 
- <span data-ttu-id="62380-3408">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3408">Two digits</span></span> 
- <span data-ttu-id="62380-3409">Eine 7 oder 8</span><span class="sxs-lookup"><span data-stu-id="62380-3409">A "7" or "8"</span></span> 
- <span data-ttu-id="62380-3410">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="62380-3410">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3411">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3411">Checksum</span></span>

<span data-ttu-id="62380-3412">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-3412">No</span></span>

### <a name="definition"></a><span data-ttu-id="62380-3413">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3413">Definition</span></span>

<span data-ttu-id="62380-3414">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3415">Die Funktion Func_formatted_itin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3415">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3416">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="62380-3416">At least one of the following is true:</span></span>
    - <span data-ttu-id="62380-3417">Ein Schlüsselwort aus Keyword_itin wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3417">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="62380-3418">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="62380-3418">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="62380-3419">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="62380-3419">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="62380-3420">Ein Schlüsselwort aus Keyword_itin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3420">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="62380-3421">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3421">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3422">Die Funktion Func_unformatted_itin findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3422">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3423">Mindestens eine der folgenden Bedingungen trifft zu:</span><span class="sxs-lookup"><span data-stu-id="62380-3423">At least one of the following is true:</span></span>
    - <span data-ttu-id="62380-3424">Ein Schlüsselwort aus Keyword_itin_collaborative wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3424">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="62380-3425">Die Funktion Func_us_address findet eine Adresse im richtigen Format.</span><span class="sxs-lookup"><span data-stu-id="62380-3425">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="62380-3426">Die Funktion Func_us_date findet ein Datum im richtigen Datumsformat.</span><span class="sxs-lookup"><span data-stu-id="62380-3426">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-3427">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3427">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="62380-3428">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="62380-3428">Keyword_itin</span></span>

- <span data-ttu-id="62380-3429">Steuer</span><span class="sxs-lookup"><span data-stu-id="62380-3429">taxpayer</span></span> 
- <span data-ttu-id="62380-3430">tax id</span><span class="sxs-lookup"><span data-stu-id="62380-3430">tax id</span></span> 
- <span data-ttu-id="62380-3431">tax identification</span><span class="sxs-lookup"><span data-stu-id="62380-3431">tax identification</span></span> 
- <span data-ttu-id="62380-3432">Itin</span><span class="sxs-lookup"><span data-stu-id="62380-3432">itin</span></span> 
- <span data-ttu-id="62380-3433">SSN</span><span class="sxs-lookup"><span data-stu-id="62380-3433">ssn</span></span> 
- <span data-ttu-id="62380-3434">Zinn</span><span class="sxs-lookup"><span data-stu-id="62380-3434">tin</span></span> 
- <span data-ttu-id="62380-3435">social security</span><span class="sxs-lookup"><span data-stu-id="62380-3435">social security</span></span> 
- <span data-ttu-id="62380-3436">tax payer</span><span class="sxs-lookup"><span data-stu-id="62380-3436">tax payer</span></span> 
- <span data-ttu-id="62380-3437">itins</span><span class="sxs-lookup"><span data-stu-id="62380-3437">itins</span></span> 
- <span data-ttu-id="62380-3438">getaxit</span><span class="sxs-lookup"><span data-stu-id="62380-3438">taxid</span></span> 
- <span data-ttu-id="62380-3439">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="62380-3439">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="62380-3440">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="62380-3440">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="62380-3441">License</span><span class="sxs-lookup"><span data-stu-id="62380-3441">License</span></span> 
- <span data-ttu-id="62380-3442">DL</span><span class="sxs-lookup"><span data-stu-id="62380-3442">DL</span></span> 
- <span data-ttu-id="62380-3443">DOB</span><span class="sxs-lookup"><span data-stu-id="62380-3443">DOB</span></span> 
- <span data-ttu-id="62380-3444">Geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="62380-3444">Birthdate</span></span> 
- <span data-ttu-id="62380-3445">Geburtstag</span><span class="sxs-lookup"><span data-stu-id="62380-3445">Birthday</span></span> 
- <span data-ttu-id="62380-3446">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="62380-3446">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="62380-3447">US-Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="62380-3447">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="62380-3448">Format</span><span class="sxs-lookup"><span data-stu-id="62380-3448">Format</span></span>

<span data-ttu-id="62380-3449">9 Ziffern in formatiertem oder unformatiertem Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3449">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="62380-3450">Wenn vor Mitte 2011 ausgegeben wird, hat eine SSN eine starke Formatierung, bei der bestimmte Teile der Nummer in bestimmte Bereiche eingehen müssen, um gültig zu sein (es gibt jedoch keine Prüfsumme).</span><span class="sxs-lookup"><span data-stu-id="62380-3450">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="62380-3451">Muster</span><span class="sxs-lookup"><span data-stu-id="62380-3451">Pattern</span></span>

<span data-ttu-id="62380-3452">Vier Funktionen suchen nach SSNs in vier verschiedenen Mustern:</span><span class="sxs-lookup"><span data-stu-id="62380-3452">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="62380-3453">Func_ssn findet SSNs mit einer starken Formatierung vor 2011, die mit Bindestrichen oder Leerzeichen (DDD-DD-dddd oder DDD DD dddd) formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="62380-3453">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="62380-3454">Func_unformatted_ssn findet SSNs mit einer starken Formatierung vor 2011, die unformatiert sind, als neun aufeinanderfolgende Ziffern (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="62380-3454">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="62380-3455">Func_randomized_formatted_ssn findet Post-2011 SSNs, die mit Bindestrichen oder Leerzeichen (DDD-DD-dddd oder DDD DD dddd) formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="62380-3455">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="62380-3456">Func_randomized_unformatted_ssn findet Post-2011 SSNs, die unformatiert sind, als neun aufeinanderfolgende Ziffern (ddddddddd)</span><span class="sxs-lookup"><span data-stu-id="62380-3456">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="62380-3457">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="62380-3457">Checksum</span></span>

<span data-ttu-id="62380-3458">Nein</span><span class="sxs-lookup"><span data-stu-id="62380-3458">No</span></span>


### <a name="definition"></a><span data-ttu-id="62380-3459">Definition</span><span class="sxs-lookup"><span data-stu-id="62380-3459">Definition</span></span>

<span data-ttu-id="62380-3460">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3461">Die Funktion Func_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3461">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3462">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3462">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="62380-3463">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3463">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3464">Die Funktion Func_unformatted_ssn sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62380-3464">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3465">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3465">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="62380-3466">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3466">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3467">Die Funktion Func_randomized_formatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3467">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3468">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3468">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="62380-3469">Die Funktion Func_ssn findet keine Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3469">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="62380-3470">Eine DLP-Richtlinie ist zu 55 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="62380-3470">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="62380-3471">Die Funktion Func_randomized_unformatted_ssn findet Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3471">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="62380-3472">Ein Schlüsselwort aus Keyword_ssn wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="62380-3472">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="62380-3473">Die Funktion Func_unformatted_ssn findet keine Inhalte, die dem Muster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="62380-3473">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="62380-3474">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="62380-3474">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="62380-3475">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="62380-3475">Keyword_ssn</span></span>

- <span data-ttu-id="62380-3476">Social Security</span><span class="sxs-lookup"><span data-stu-id="62380-3476">Social Security</span></span> 
- <span data-ttu-id="62380-3477">Social Security#</span><span class="sxs-lookup"><span data-stu-id="62380-3477">Social Security#</span></span> 
- <span data-ttu-id="62380-3478">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="62380-3478">Soc Sec</span></span> 
- <span data-ttu-id="62380-3479">SSN</span><span class="sxs-lookup"><span data-stu-id="62380-3479">SSN</span></span> 
- <span data-ttu-id="62380-3480">SSNS</span><span class="sxs-lookup"><span data-stu-id="62380-3480">SSNS</span></span> 
- <span data-ttu-id="62380-3481">SSN</span><span class="sxs-lookup"><span data-stu-id="62380-3481">SSN#</span></span> 
- <span data-ttu-id="62380-3482">SS</span><span class="sxs-lookup"><span data-stu-id="62380-3482">SS#</span></span> 
- <span data-ttu-id="62380-3483">SSID</span><span class="sxs-lookup"><span data-stu-id="62380-3483">SSID</span></span> 
   

