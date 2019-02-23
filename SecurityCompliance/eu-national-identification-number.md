---
title: Nationale IdentifikationsNummer der EU
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 2ea971bf-9434-4b61-b825-2bbd28ae6064
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp EU National Identification Number erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 9a85fd6954f39de348874e03268a2e19ae47366c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220635"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="e7729-104">Nationale IdentifikationsNummer der EU</span><span class="sxs-lookup"><span data-stu-id="e7729-104">EU National Identification Number</span></span>

<span data-ttu-id="e7729-p102">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp EU National Identification Number erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="e7729-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="e7729-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="e7729-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="e7729-108">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-108">Format</span></span>

<span data-ttu-id="e7729-109">Eine 24-Zeichen-Kombination aus Buchstaben, Ziffern und Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="e7729-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-110">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-110">Pattern</span></span>

<span data-ttu-id="e7729-111">24 Zeichen:</span><span class="sxs-lookup"><span data-stu-id="e7729-111">24 characters:</span></span>
  
-  <span data-ttu-id="e7729-112">22 Buchstaben (Groß-/Kleinschreibung nicht beachtet), Ziffern, Schrägstriche, Schrägstriche oder Pluszeichen</span><span class="sxs-lookup"><span data-stu-id="e7729-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="e7729-113">Zwei Buchstaben (ohne Unterscheidung nach Groß-/Kleinschreibung), Ziffern, Schrägstriche, Schrägstriche, Pluszeichen oder Gleichheitszeichen</span><span class="sxs-lookup"><span data-stu-id="e7729-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-114">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-114">Checksum</span></span>

<span data-ttu-id="e7729-115">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e7729-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-116">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-116">Definition</span></span>

<span data-ttu-id="e7729-117">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-118">Der reguläre Ausdruck `Regex_austria_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-119">Ein Schlüsselwort `Keywords_austria_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-120">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="e7729-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="e7729-122">Österreichische Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-122">austrian identity number</span></span>
  
<span data-ttu-id="e7729-123">nationale Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-123">national identity number</span></span>
  
<span data-ttu-id="e7729-124">Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-124">identity number</span></span>
  
<span data-ttu-id="e7729-125">
national id</span><span class="sxs-lookup"><span data-stu-id="e7729-125">national id</span></span>
  
<span data-ttu-id="e7729-126">Personalausweis Republik Österreich</span><span class="sxs-lookup"><span data-stu-id="e7729-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="e7729-127">Belgien</span><span class="sxs-lookup"><span data-stu-id="e7729-127">Belgium</span></span>

<span data-ttu-id="e7729-128">Weitere Informationen finden Sie im Abschnitt "belgische nationale Rufnummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e7729-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="e7729-129">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="e7729-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="e7729-130">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-130">Format</span></span>

<span data-ttu-id="e7729-131">Zehn Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e7729-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-132">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-132">Pattern</span></span>

<span data-ttu-id="e7729-133">Zehn Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e7729-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="e7729-134">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="e7729-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="e7729-135">Zwei Ziffern, die der Geburts Reihenfolge entsprechen</span><span class="sxs-lookup"><span data-stu-id="e7729-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="e7729-136">Eine Ziffer, die dem Geschlecht entspricht: eine gerade Ziffer für männliche und eine ungerade Ziffer für weiblich</span><span class="sxs-lookup"><span data-stu-id="e7729-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="e7729-137">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e7729-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-138">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-138">Checksum</span></span>

<span data-ttu-id="e7729-139">Ja</span><span class="sxs-lookup"><span data-stu-id="e7729-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-140">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-140">Definition</span></span>

<span data-ttu-id="e7729-141">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-142">Die Funktion `Func_bulgaria_national_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-143">Ein Schlüsselwort `Keywords_bulgaria_national_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="e7729-144">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-145">Die Funktion `Func_bulgaria_national_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_national_number" />
          <Match idRef="Keywords_bulgaria_national_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-146">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="e7729-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="e7729-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="e7729-148">EGN</span><span class="sxs-lookup"><span data-stu-id="e7729-148">egn</span></span>
  
<span data-ttu-id="e7729-149">EGN</span><span class="sxs-lookup"><span data-stu-id="e7729-149">egn#</span></span>
  
<span data-ttu-id="e7729-150">Bulgarische Nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-150">bulgarian national number</span></span>
  
<span data-ttu-id="e7729-151">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-151">national number</span></span>
  
<span data-ttu-id="e7729-152">social security number
</span><span class="sxs-lookup"><span data-stu-id="e7729-152">social security number</span></span>
  
<span data-ttu-id="e7729-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="e7729-153">nationalnumber#</span></span>
  
<span data-ttu-id="e7729-154">SSN</span><span class="sxs-lookup"><span data-stu-id="e7729-154">ssn#</span></span>
  
<span data-ttu-id="e7729-155">SSN</span><span class="sxs-lookup"><span data-stu-id="e7729-155">ssn</span></span>
  
<span data-ttu-id="e7729-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="e7729-156">nationalnumber</span></span>
  
<span data-ttu-id="e7729-157">BNN</span><span class="sxs-lookup"><span data-stu-id="e7729-157">bnn#</span></span>
  
<span data-ttu-id="e7729-158">BNN</span><span class="sxs-lookup"><span data-stu-id="e7729-158">bnn</span></span>
  
<span data-ttu-id="e7729-159">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-159">personal id number</span></span>
  
<span data-ttu-id="e7729-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e7729-160">personalidnumber#</span></span>
  
<span data-ttu-id="e7729-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="e7729-161">единен граждански номер</span></span>
  
<span data-ttu-id="e7729-162">edinn grazhdanski Nomer</span><span class="sxs-lookup"><span data-stu-id="e7729-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="e7729-163">егн</span><span class="sxs-lookup"><span data-stu-id="e7729-163">егн</span></span>
  
<span data-ttu-id="e7729-164">егн #</span><span class="sxs-lookup"><span data-stu-id="e7729-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="e7729-165">Kroatien</span><span class="sxs-lookup"><span data-stu-id="e7729-165">Croatia</span></span>

<span data-ttu-id="e7729-166">Weitere Informationen finden Sie im Abschnitt "Croatia Identity Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e7729-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="e7729-167">Zypern</span><span class="sxs-lookup"><span data-stu-id="e7729-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="e7729-168">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-168">Format</span></span>

<span data-ttu-id="e7729-169">Zehn Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e7729-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-170">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-170">Pattern</span></span>

 <span data-ttu-id="e7729-171">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="e7729-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="e7729-172">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-172">Checksum</span></span>

<span data-ttu-id="e7729-173">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e7729-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-174">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-174">Definition</span></span>

<span data-ttu-id="e7729-175">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-176">Der reguläre Ausdruck `Regex_cyprus_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-177">Ein Schlüsselwort `Keywords_cyprus_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-178">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="e7729-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="e7729-180">ID-Kartennummer</span><span class="sxs-lookup"><span data-stu-id="e7729-180">id card number</span></span>
  
<span data-ttu-id="e7729-181">nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-181">national identification number</span></span>
  
<span data-ttu-id="e7729-182">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-182">personal id number</span></span>
  
<span data-ttu-id="e7729-183">Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-183">identity card number</span></span>
  
<span data-ttu-id="e7729-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="e7729-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="e7729-185">Tschechien</span><span class="sxs-lookup"><span data-stu-id="e7729-185">Czech Republic</span></span>

<span data-ttu-id="e7729-186">Weitere Informationen finden Sie im Abschnitt "Czech National Identity Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e7729-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="e7729-187">Dänemark</span><span class="sxs-lookup"><span data-stu-id="e7729-187">Denmark</span></span>

<span data-ttu-id="e7729-188">Weitere Informationen finden Sie im Abschnitt "Denmark Personal Identification Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e7729-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="e7729-189">Estland</span><span class="sxs-lookup"><span data-stu-id="e7729-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="e7729-190">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-190">Format</span></span>

<span data-ttu-id="e7729-191">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e7729-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-192">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-192">Pattern</span></span>

<span data-ttu-id="e7729-193">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e7729-193">11 digits:</span></span>
  
- <span data-ttu-id="e7729-194">Eine Ziffer, die dem Geschlecht und dem Jahrhundert der Geburt entspricht (ungerade Zahl, gerade Zahl weiblich; 1-2:19. Jahrhundert; 3-4:20. Jahrhundert; 5-6:21st Century)</span><span class="sxs-lookup"><span data-stu-id="e7729-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="e7729-195">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="e7729-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="e7729-196">Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am selben Datum geboren wurden</span><span class="sxs-lookup"><span data-stu-id="e7729-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="e7729-197">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e7729-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-198">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-198">Checksum</span></span>

<span data-ttu-id="e7729-199">Ja</span><span class="sxs-lookup"><span data-stu-id="e7729-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-200">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-200">Definition</span></span>

<span data-ttu-id="e7729-201">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-202">Die Funktion `Func_estonia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-203">Ein Schlüsselwort `Keywords_estonia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="e7729-204">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-205">Die Funktion `Func_estonia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
          <Match idRef="Keywords_estonia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-206">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="e7729-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="e7729-208">persönlicher Identifizierungscode</span><span class="sxs-lookup"><span data-stu-id="e7729-208">personal identification code</span></span>
  
<span data-ttu-id="e7729-209">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-209">personal identification number</span></span>
  
<span data-ttu-id="e7729-210">nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-210">national identification number</span></span>
  
<span data-ttu-id="e7729-211">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-211">national number</span></span>
  
<span data-ttu-id="e7729-212">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-212">personal id number</span></span>
  
<span data-ttu-id="e7729-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e7729-213">personalidnumber#</span></span>
  
<span data-ttu-id="e7729-214">IK</span><span class="sxs-lookup"><span data-stu-id="e7729-214">ik</span></span>
  
<span data-ttu-id="e7729-215">Isikukood</span><span class="sxs-lookup"><span data-stu-id="e7729-215">isikukood</span></span>
  
<span data-ttu-id="e7729-216">ID-Kaart</span><span class="sxs-lookup"><span data-stu-id="e7729-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="e7729-217">Finnland</span><span class="sxs-lookup"><span data-stu-id="e7729-217">Finland</span></span>

<span data-ttu-id="e7729-218">Weitere Informationen finden Sie im Abschnitt "Finland National ID" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e7729-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="e7729-219">Frankreich</span><span class="sxs-lookup"><span data-stu-id="e7729-219">France</span></span>

<span data-ttu-id="e7729-220">Weitere Informationen finden Sie im Abschnitt "France National ID Card (CNI)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e7729-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="e7729-221">Deutschland</span><span class="sxs-lookup"><span data-stu-id="e7729-221">Germany</span></span>

<span data-ttu-id="e7729-222">Weitere Informationen finden Sie im Abschnitt "Deutschland PersonalausweisNummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e7729-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="e7729-223">Griechenland</span><span class="sxs-lookup"><span data-stu-id="e7729-223">Greece</span></span>

<span data-ttu-id="e7729-224">Weitere Informationen finden Sie im Abschnitt "GriechenLand National ID Card" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e7729-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="e7729-225">Ungarn</span><span class="sxs-lookup"><span data-stu-id="e7729-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="e7729-226">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-226">Format</span></span>

<span data-ttu-id="e7729-227">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e7729-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-228">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-228">Pattern</span></span>

<span data-ttu-id="e7729-229">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e7729-229">11 digits:</span></span>
  
-  <span data-ttu-id="e7729-230">Eine Ziffer, die dem Geschlecht entspricht (1-männlich, 2-weiblich, andere Zahlen sind auch für Bürger möglich, die vor 1900 oder Bürger mit doppelter Staatsbürgerschaft geboren wurden)</span><span class="sxs-lookup"><span data-stu-id="e7729-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="e7729-231">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="e7729-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="e7729-232">Drei Ziffern, die einer Seriennummer entsprechen</span><span class="sxs-lookup"><span data-stu-id="e7729-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="e7729-233">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e7729-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-234">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-234">Checksum</span></span>

<span data-ttu-id="e7729-235">Ja</span><span class="sxs-lookup"><span data-stu-id="e7729-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-236">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-236">Definition</span></span>

<span data-ttu-id="e7729-237">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-238">Die Funktion `Func_hungary_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-239">Ein Schlüsselwort `Keywords_hungary_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="e7729-240">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-241">Die Funktion `Func_hungary_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
          <Match idRef="Keywords_hungary_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-242">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="e7729-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="e7729-244">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-244">personal identification number</span></span>
  
<span data-ttu-id="e7729-245">identification number
</span><span class="sxs-lookup"><span data-stu-id="e7729-245">identification number</span></span>
  
<span data-ttu-id="e7729-246">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-246">personal id number</span></span>
  
<span data-ttu-id="e7729-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="e7729-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="e7729-248">Irland</span><span class="sxs-lookup"><span data-stu-id="e7729-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="e7729-249">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-249">Format</span></span>

<span data-ttu-id="e7729-250">Eine neunstellige Kombination aus Buchstaben, Ziffern und einem Leerzeichen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-251">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-251">Pattern</span></span>

<span data-ttu-id="e7729-252">Eine neunstellige Kombination aus Buchstaben, Ziffern und einem Leerzeichen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="e7729-253">Vom 01. Januar 2013 bis jetzt:</span><span class="sxs-lookup"><span data-stu-id="e7729-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="e7729-254">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="e7729-254">Seven digits</span></span> 
    
- <span data-ttu-id="e7729-255">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e7729-255">One check digit</span></span>
    
- <span data-ttu-id="e7729-256">Ein Leerzeichen oder der Großbuchstabe "W" (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="e7729-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="e7729-257">Vor 01. Januar 2013:</span><span class="sxs-lookup"><span data-stu-id="e7729-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="e7729-258">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="e7729-258">Seven digits</span></span> 
    
- <span data-ttu-id="e7729-259">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e7729-259">One check digit</span></span>
    
- <span data-ttu-id="e7729-260">Ein Leerzeichen oder ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="e7729-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-261">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-261">Checksum</span></span>

<span data-ttu-id="e7729-262">Ja</span><span class="sxs-lookup"><span data-stu-id="e7729-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-263">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-263">Definition</span></span>

<span data-ttu-id="e7729-264">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-265">Die Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e7729-266">Ein Schlüsselwort aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-266">A keyword from is found.</span></span>
    
<span data-ttu-id="e7729-267">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-268">Die Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-268">The function finds content that matches the pattern.</span></span>
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
          <Match idRef="Keywords_ireland_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-269">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="e7729-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="e7729-271">persönliche öffentliche Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-271">personal public service number</span></span>
  
<span data-ttu-id="e7729-272">PPS Nein</span><span class="sxs-lookup"><span data-stu-id="e7729-272">pps no</span></span>
  
<span data-ttu-id="e7729-273">Umsatz-und Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="e7729-274">RSI-No</span><span class="sxs-lookup"><span data-stu-id="e7729-274">rsi no</span></span>
  
<span data-ttu-id="e7729-275">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-275">personal identification number</span></span>
  
<span data-ttu-id="e7729-276">identification number
</span><span class="sxs-lookup"><span data-stu-id="e7729-276">identification number</span></span>
  
<span data-ttu-id="e7729-277">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-277">personal id number</span></span>
  
<span data-ttu-id="e7729-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="e7729-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="e7729-p103">uimh. PSP</span><span class="sxs-lookup"><span data-stu-id="e7729-p103">uimh. psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="e7729-281">Italien</span><span class="sxs-lookup"><span data-stu-id="e7729-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="e7729-282">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-282">Format</span></span>

<span data-ttu-id="e7729-283">Eine 16-stellige Kombination aus Buchstaben und Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-284">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-284">Pattern</span></span>

<span data-ttu-id="e7729-285">Eine 16-stellige Kombination aus Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="e7729-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="e7729-286">Drei Buchstaben, die den ersten drei Konsonanten im Familiennamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="e7729-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="e7729-287">Drei Buchstaben, die dem ersten, dritten und vierten Konsonanten im Vornamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="e7729-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="e7729-288">Zwei Ziffern, die den letzten Ziffern des Geburtsjahrs entsprechen</span><span class="sxs-lookup"><span data-stu-id="e7729-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="e7729-289">Ein Buchstabe, der dem Buchstaben für den Geburtsmonat entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben A bis E, H, L, M, P, R bis T werden verwendet (also Januar ist A und Oktober ist R)</span><span class="sxs-lookup"><span data-stu-id="e7729-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="e7729-290">Zwei Ziffern, die dem Tag des Geburtsmonats entsprechen – zur Unterscheidung zwischen den Geschlechtern wird 40 zum Geburtstag für Frauen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e7729-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="e7729-291">Vier Ziffern, die der Ortskennzahl für die Gemeinde entsprechen, in der die Person geboren wurde (landesweite Codes werden für fremde Länder verwendet)</span><span class="sxs-lookup"><span data-stu-id="e7729-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="e7729-292">Eine Paritäts Ziffer</span><span class="sxs-lookup"><span data-stu-id="e7729-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-293">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-293">Checksum</span></span>

<span data-ttu-id="e7729-294">Ja</span><span class="sxs-lookup"><span data-stu-id="e7729-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-295">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-295">Definition</span></span>

<span data-ttu-id="e7729-296">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-297">Die Funktion `Func_italy_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-298">Ein Schlüsselwort `Keywords_italy_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="e7729-299">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-300">Die Funktion `Func_italy_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
          <Match idRef="Keywords_italy_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-301">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="e7729-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="e7729-303">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="e7729-303">personal code</span></span>
  
<span data-ttu-id="e7729-304">persönliche Codenummer</span><span class="sxs-lookup"><span data-stu-id="e7729-304">personal code number</span></span>
  
<span data-ttu-id="e7729-305">persönliche Zertifikatsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-305">personal certificate number</span></span>
  
<span data-ttu-id="e7729-306">Fiskal Code</span><span class="sxs-lookup"><span data-stu-id="e7729-306">fiscal code</span></span>
  
<span data-ttu-id="e7729-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="e7729-307">personalcodeno#</span></span>
  
<span data-ttu-id="e7729-308">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-308">personal id number</span></span>
  
<span data-ttu-id="e7729-309">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="e7729-309">personal id code</span></span>
  
<span data-ttu-id="e7729-310">codedice personale</span><span class="sxs-lookup"><span data-stu-id="e7729-310">codice personale</span></span>
  
<span data-ttu-id="e7729-311">Numero Bescheinigung personale</span><span class="sxs-lookup"><span data-stu-id="e7729-311">numero certificato personale</span></span>
  
<span data-ttu-id="e7729-312">Numero personale</span><span class="sxs-lookup"><span data-stu-id="e7729-312">numero personale</span></span>
  
<span data-ttu-id="e7729-313">Numero-ID personale</span><span class="sxs-lookup"><span data-stu-id="e7729-313">numero id personale</span></span>
  
<span data-ttu-id="e7729-314">codedice-ID personale</span><span class="sxs-lookup"><span data-stu-id="e7729-314">codice id personale</span></span>
  
<span data-ttu-id="e7729-315">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="e7729-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="e7729-316">Italien</span><span class="sxs-lookup"><span data-stu-id="e7729-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="e7729-317">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-317">Format</span></span>

<span data-ttu-id="e7729-318">11 Ziffern und ein Bindestrich im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="e7729-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-319">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-319">Pattern</span></span>

<span data-ttu-id="e7729-320">11 Ziffern und ein Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="e7729-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="e7729-321">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="e7729-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="e7729-322">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="e7729-322">A hyphen</span></span>
    
- <span data-ttu-id="e7729-323">Eine Ziffer, die dem Jahrhundert der Geburt entspricht ("0" für das 19. Jahrhundert, "1" für das 20. Jahrhundert und "2" für das 21. Jahrhundert)</span><span class="sxs-lookup"><span data-stu-id="e7729-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="e7729-324">Vier Ziffern, nach dem Zufallsprinzip generiert</span><span class="sxs-lookup"><span data-stu-id="e7729-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-325">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-325">Checksum</span></span>

<span data-ttu-id="e7729-326">Ja</span><span class="sxs-lookup"><span data-stu-id="e7729-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-327">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-327">Definition</span></span>

<span data-ttu-id="e7729-328">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-329">Die Funktion `Func_latvia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-330">Ein Schlüsselwort `Keywords_latvia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="e7729-331">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-332">Die Funktion `Func_latvia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
          <Match idRef="Keywords_latvia_eu_national_id_card" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-333">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="e7729-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="e7729-335">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="e7729-335">personal code</span></span>
  
<span data-ttu-id="e7729-336">persönliche Codenummer</span><span class="sxs-lookup"><span data-stu-id="e7729-336">personal code number</span></span>
  
<span data-ttu-id="e7729-337">persönliche Zertifikatsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-337">personal certificate number</span></span>
  
<span data-ttu-id="e7729-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="e7729-338">personalcodeno#</span></span>
  
<span data-ttu-id="e7729-339">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-339">personal id number</span></span>
  
<span data-ttu-id="e7729-340">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="e7729-340">personal id code</span></span>
  
<span data-ttu-id="e7729-341">Personas KODS</span><span class="sxs-lookup"><span data-stu-id="e7729-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="e7729-342">Litauen</span><span class="sxs-lookup"><span data-stu-id="e7729-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="e7729-343">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-343">Format</span></span>

<span data-ttu-id="e7729-344">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e7729-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-345">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-345">Pattern</span></span>

<span data-ttu-id="e7729-346">11 Ziffern ohne Leerzeichen und Abgrenzungen:</span><span class="sxs-lookup"><span data-stu-id="e7729-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="e7729-347">Eine Ziffer, die dem Geschlecht der Person und dem Jahrhundert der Geburt entspricht</span><span class="sxs-lookup"><span data-stu-id="e7729-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="e7729-348">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="e7729-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="e7729-349">Drei Ziffern, die der Seriennummer des Geburtsdatums entsprechen</span><span class="sxs-lookup"><span data-stu-id="e7729-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="e7729-350">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e7729-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-351">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-351">Checksum</span></span>

<span data-ttu-id="e7729-352">Ja</span><span class="sxs-lookup"><span data-stu-id="e7729-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-353">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-353">Definition</span></span>

<span data-ttu-id="e7729-354">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-355">Die Funktion `Func_lithuania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-356">Ein Schlüsselwort `Keywords_lithuania_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="e7729-357">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-358">Die Funktion `Func_lithuania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
          <Match idRef="Keywords_lithuania_eu_national_id_card" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-359">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="e7729-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="e7729-361">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="e7729-361">personal numeric code</span></span>
  
<span data-ttu-id="e7729-362">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-362">unique identification number</span></span>
  
<span data-ttu-id="e7729-363">Citizen-Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-363">citizen service number</span></span>
  
<span data-ttu-id="e7729-364">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-364">unique identity number</span></span>
  
<span data-ttu-id="e7729-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="e7729-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="e7729-366">persönlicher Code.</span><span class="sxs-lookup"><span data-stu-id="e7729-366">personal code.</span></span>
  
<span data-ttu-id="e7729-367">asmeninis skaitmeninis koda</span><span class="sxs-lookup"><span data-stu-id="e7729-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="e7729-368">unikalus identifikavimo Numeris</span><span class="sxs-lookup"><span data-stu-id="e7729-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="e7729-369">piliečio paslaugos Numeris</span><span class="sxs-lookup"><span data-stu-id="e7729-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="e7729-370">unikalus identifikavimo koda</span><span class="sxs-lookup"><span data-stu-id="e7729-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="e7729-371">Mens koda.</span><span class="sxs-lookup"><span data-stu-id="e7729-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="e7729-372">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="e7729-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="e7729-373">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-373">Format</span></span>

<span data-ttu-id="e7729-374">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e7729-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-375">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-375">Pattern</span></span>

<span data-ttu-id="e7729-376">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e7729-376">11 digits</span></span>
  
- <span data-ttu-id="e7729-377">Eine Ziffer, die dem Geschlecht der Person und dem Jahrhundert der Geburt entspricht</span><span class="sxs-lookup"><span data-stu-id="e7729-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="e7729-378">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="e7729-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="e7729-379">Drei Ziffern, die der Seriennummer des Geburtsdatums entsprechen</span><span class="sxs-lookup"><span data-stu-id="e7729-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="e7729-380">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e7729-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-381">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-381">Checksum</span></span>

<span data-ttu-id="e7729-382">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e7729-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-383">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-383">Definition</span></span>

<span data-ttu-id="e7729-384">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-385">Der reguläre Ausdruck `Regex_luxemburg_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-386">Ein Schlüsselwort `Keywords_luxemburg_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-387">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="e7729-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="e7729-389">persönliche ID</span><span class="sxs-lookup"><span data-stu-id="e7729-389">personal id</span></span>
  
<span data-ttu-id="e7729-390">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-390">personal id number</span></span>
  
<span data-ttu-id="e7729-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="e7729-391">personalidno#</span></span>
  
<span data-ttu-id="e7729-392">eindeutige ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-392">unique id number</span></span>
  
<span data-ttu-id="e7729-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e7729-393">personalidnumber#</span></span>
  
<span data-ttu-id="e7729-394">eindeutiger ID-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e7729-394">unique id key</span></span>
  
<span data-ttu-id="e7729-395">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="e7729-395">personal id code</span></span>
  
<span data-ttu-id="e7729-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="e7729-396">uniqueidkey#</span></span>
  
<span data-ttu-id="e7729-397">individueller Code</span><span class="sxs-lookup"><span data-stu-id="e7729-397">individual code</span></span>
  
<span data-ttu-id="e7729-398">einzelne ID</span><span class="sxs-lookup"><span data-stu-id="e7729-398">individual id</span></span>
  
<span data-ttu-id="e7729-399">eindeutige-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="e7729-400">eindeutige-ID</span><span class="sxs-lookup"><span data-stu-id="e7729-400">eindeutige id</span></span>
  
<span data-ttu-id="e7729-401">ID personnelle</span><span class="sxs-lookup"><span data-stu-id="e7729-401">id personnelle</span></span>
  
<span data-ttu-id="e7729-402">Numéro d'identification Personal</span><span class="sxs-lookup"><span data-stu-id="e7729-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="e7729-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="e7729-403">idpersonnelle#</span></span>
  
<span data-ttu-id="e7729-404">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="e7729-405">EINDEUTIGEID #</span><span class="sxs-lookup"><span data-stu-id="e7729-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="e7729-406">Malta</span><span class="sxs-lookup"><span data-stu-id="e7729-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="e7729-407">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-407">Format</span></span>

<span data-ttu-id="e7729-408">Sieben Ziffern gefolgt von einem Buchstaben</span><span class="sxs-lookup"><span data-stu-id="e7729-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-409">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-409">Pattern</span></span>

<span data-ttu-id="e7729-410">Sieben Ziffern gefolgt von einem Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="e7729-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="e7729-411">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="e7729-411">Seven digits</span></span> 
    
- <span data-ttu-id="e7729-412">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="e7729-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-413">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-413">Checksum</span></span>

<span data-ttu-id="e7729-414">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e7729-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-415">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-415">Definition</span></span>

<span data-ttu-id="e7729-416">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-417">Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-418">Ein Schlüsselwort `Keywords_malta_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="e7729-419">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-420">Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
          <Match idRef="Keywords_malta_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-421">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="e7729-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="e7729-423">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="e7729-423">personal numeric code</span></span>
  
<span data-ttu-id="e7729-424">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-424">unique identification number</span></span>
  
<span data-ttu-id="e7729-425">Citizen-Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-425">citizen service number</span></span>
  
<span data-ttu-id="e7729-426">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-426">unique identity number</span></span>
  
<span data-ttu-id="e7729-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="e7729-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="e7729-428">Kodiċi personali</span><span class="sxs-lookup"><span data-stu-id="e7729-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="e7729-429">numru ta ' identifikazzjoni uniku</span><span class="sxs-lookup"><span data-stu-id="e7729-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="e7729-430">numru TAS-servizz taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="e7729-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="e7729-431">numru ta ' identità uniku</span><span class="sxs-lookup"><span data-stu-id="e7729-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="e7729-432">Niederlande</span><span class="sxs-lookup"><span data-stu-id="e7729-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="e7729-433">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-433">Format</span></span>

<span data-ttu-id="e7729-434">Neun Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e7729-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-435">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-435">Pattern</span></span>

<span data-ttu-id="e7729-436">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="e7729-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e7729-437">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-437">Checksum</span></span>

<span data-ttu-id="e7729-438">Ja</span><span class="sxs-lookup"><span data-stu-id="e7729-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-439">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-439">Definition</span></span>

<span data-ttu-id="e7729-440">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-441">Die Funktion `Func_netherlands_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-442">Ein Schlüsselwort aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-442">A keyword from is found.</span></span>
    
<span data-ttu-id="e7729-443">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-444">Die Funktion `Func_netherlands_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
          <Match idRef="Keywords_netherlands_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-445">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="e7729-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="e7729-447">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="e7729-447">personal numeric code</span></span>
  
<span data-ttu-id="e7729-448">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-448">unique identification number</span></span>
  
<span data-ttu-id="e7729-449">Citizen-Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-449">citizen service number</span></span>
  
<span data-ttu-id="e7729-450">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-450">unique identity number</span></span>
  
<span data-ttu-id="e7729-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="e7729-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="e7729-452">BSN</span><span class="sxs-lookup"><span data-stu-id="e7729-452">bsn</span></span>
  
<span data-ttu-id="e7729-453">BSN</span><span class="sxs-lookup"><span data-stu-id="e7729-453">bsn#</span></span>
  
<span data-ttu-id="e7729-454">Persoonlijke-numerieke-Code</span><span class="sxs-lookup"><span data-stu-id="e7729-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="e7729-455">uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="e7729-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="e7729-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="e7729-456">burgerservicenummer</span></span>
  
<span data-ttu-id="e7729-457">uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="e7729-458">Polen</span><span class="sxs-lookup"><span data-stu-id="e7729-458">Poland</span></span>

<span data-ttu-id="e7729-459">Weitere Informationen finden Sie im Abschnitt "polnische National ID (PESEL)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e7729-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="e7729-460">Portugal</span><span class="sxs-lookup"><span data-stu-id="e7729-460">Portugal</span></span>

<span data-ttu-id="e7729-461">Weitere Informationen finden Sie im Abschnitt "portugiesische Bürgerkarten Nummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e7729-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="e7729-462">Rumänien</span><span class="sxs-lookup"><span data-stu-id="e7729-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="e7729-463">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-463">Format</span></span>

<span data-ttu-id="e7729-464">13 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e7729-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-465">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-465">Pattern</span></span>

<span data-ttu-id="e7729-466">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e7729-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e7729-467">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-467">Checksum</span></span>

<span data-ttu-id="e7729-468">Ja</span><span class="sxs-lookup"><span data-stu-id="e7729-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-469">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-469">Definition</span></span>

<span data-ttu-id="e7729-470">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-471">Die Funktion `Func_romania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-472">Ein Schlüsselwort `Keywords_romania_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="e7729-473">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-474">Die Funktion `Func_romania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
          <Match idRef="Keywords_romania_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-475">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="e7729-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="e7729-477">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="e7729-477">personal numeric code</span></span>
  
<span data-ttu-id="e7729-478">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-478">unique identification number</span></span>
  
<span data-ttu-id="e7729-479">CNP</span><span class="sxs-lookup"><span data-stu-id="e7729-479">cnp</span></span>
  
<span data-ttu-id="e7729-480">CNP</span><span class="sxs-lookup"><span data-stu-id="e7729-480">cnp#</span></span>
  
<span data-ttu-id="e7729-481">Anheften</span><span class="sxs-lookup"><span data-stu-id="e7729-481">pin</span></span>
  
<span data-ttu-id="e7729-482">PIN</span><span class="sxs-lookup"><span data-stu-id="e7729-482">pin#</span></span>
  
<span data-ttu-id="e7729-483">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-483">insurance number</span></span>
  
<span data-ttu-id="e7729-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="e7729-484">insurancenumber#</span></span>
  
<span data-ttu-id="e7729-485">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-485">unique identity number</span></span>
  
<span data-ttu-id="e7729-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="e7729-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="e7729-487">COD numerische Personal</span><span class="sxs-lookup"><span data-stu-id="e7729-487">cod numeric personal</span></span>
  
<span data-ttu-id="e7729-488">COD identificare Personal</span><span class="sxs-lookup"><span data-stu-id="e7729-488">cod identificare personal</span></span>
  
<span data-ttu-id="e7729-489">COD Unic identificare</span><span class="sxs-lookup"><span data-stu-id="e7729-489">cod unic identificare</span></span>
  
<span data-ttu-id="e7729-490">număr Personal Unic</span><span class="sxs-lookup"><span data-stu-id="e7729-490">număr personal unic</span></span>
  
<span data-ttu-id="e7729-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="e7729-491">număr identitate</span></span>
  
<span data-ttu-id="e7729-492">număr identificare Personal</span><span class="sxs-lookup"><span data-stu-id="e7729-492">număr identificare personal</span></span>
  
<span data-ttu-id="e7729-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="e7729-493">număridentitate#</span></span>
  
<span data-ttu-id="e7729-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="e7729-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="e7729-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="e7729-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="e7729-496">Slowakei</span><span class="sxs-lookup"><span data-stu-id="e7729-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="e7729-497">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-497">Format</span></span>

<span data-ttu-id="e7729-498">Zehn Ziffern mit einem umgekehrten Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="e7729-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-499">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-499">Pattern</span></span>

<span data-ttu-id="e7729-500">Zehn Ziffern mit einem umgekehrten Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="e7729-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e7729-501">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-501">Checksum</span></span>

<span data-ttu-id="e7729-502">Ja</span><span class="sxs-lookup"><span data-stu-id="e7729-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-503">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-503">Definition</span></span>

<span data-ttu-id="e7729-504">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-505">Die Funktion `Func_slovakia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-506">Ein Schlüsselwort `Keywords_slovakia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="e7729-507">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-508">Die Funktion `Func_slovakia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
          <Match idRef="Keywords_slovakia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-509">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="e7729-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="e7729-511">Geburtsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-511">birth number</span></span>
  
<span data-ttu-id="e7729-512">nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-512">national identification number</span></span>
  
<span data-ttu-id="e7729-513">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-513">personal identification number</span></span>
  
<span data-ttu-id="e7729-514">social security number
</span><span class="sxs-lookup"><span data-stu-id="e7729-514">social security number</span></span>
  
<span data-ttu-id="e7729-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="e7729-515">nationalnumber#</span></span>
  
<span data-ttu-id="e7729-516">SSN</span><span class="sxs-lookup"><span data-stu-id="e7729-516">ssn#</span></span>
  
<span data-ttu-id="e7729-517">SSN</span><span class="sxs-lookup"><span data-stu-id="e7729-517">ssn</span></span>
  
<span data-ttu-id="e7729-518">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-518">national number</span></span>
  
<span data-ttu-id="e7729-519">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-519">personal id number</span></span>
  
<span data-ttu-id="e7729-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="e7729-520">personalidnumber#</span></span>
  
<span data-ttu-id="e7729-521">rč</span><span class="sxs-lookup"><span data-stu-id="e7729-521">rč</span></span>
  
<span data-ttu-id="e7729-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="e7729-522">rodné číslo</span></span>
  
<span data-ttu-id="e7729-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="e7729-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="e7729-524">Slowenien</span><span class="sxs-lookup"><span data-stu-id="e7729-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="e7729-525">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-525">Format</span></span>

<span data-ttu-id="e7729-526">13 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="e7729-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-527">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-527">Pattern</span></span>

<span data-ttu-id="e7729-528">13 Ziffern im angegebenen Muster:</span><span class="sxs-lookup"><span data-stu-id="e7729-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="e7729-529">Sieben Ziffern, die dem Geburtsdatum (DDMMLLL) entsprechen, wobei "LLL" den letzten drei Ziffern des Geburtsjahrs entspricht.</span><span class="sxs-lookup"><span data-stu-id="e7729-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="e7729-530">Zwei Ziffern, die dem Bereich der Geburt entsprechen</span><span class="sxs-lookup"><span data-stu-id="e7729-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="e7729-531">Drei Ziffern, die einer Kombination aus Geschlecht und Seriennummer für Personen entsprechen, die am selben Tag geboren wurden (000-499 für männlich und 500-999 für weiblich)</span><span class="sxs-lookup"><span data-stu-id="e7729-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="e7729-532">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="e7729-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-533">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-533">Checksum</span></span>

<span data-ttu-id="e7729-534">Ja</span><span class="sxs-lookup"><span data-stu-id="e7729-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-535">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-535">Definition</span></span>

<span data-ttu-id="e7729-536">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-537">Die Funktion `Func_slovenia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-538">Ein Schlüsselwort `Keywords_slovenia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="e7729-539">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-540">Die Funktion `Func_slovenia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
          <Match idRef="Keywords_slovenia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-541">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="e7729-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="e7729-543">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="e7729-543">personal numeric code</span></span>
  
<span data-ttu-id="e7729-544">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-544">unique identification number</span></span>
  
<span data-ttu-id="e7729-545">eindeutige Registrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-545">unique registration number</span></span>
  
<span data-ttu-id="e7729-546">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-546">unique identity number</span></span>
  
<span data-ttu-id="e7729-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="e7729-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="e7729-548">eindeutige Master Bürger-Nummer</span><span class="sxs-lookup"><span data-stu-id="e7729-548">unique master citizen number</span></span>
  
<span data-ttu-id="e7729-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="e7729-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="e7729-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="e7729-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="e7729-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="e7729-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="e7729-552">EMŠO</span><span class="sxs-lookup"><span data-stu-id="e7729-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="e7729-553">Spanien</span><span class="sxs-lookup"><span data-stu-id="e7729-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="e7729-554">Format</span><span class="sxs-lookup"><span data-stu-id="e7729-554">Format</span></span>

<span data-ttu-id="e7729-555">Sieben Ziffern gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="e7729-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e7729-556">Muster</span><span class="sxs-lookup"><span data-stu-id="e7729-556">Pattern</span></span>

<span data-ttu-id="e7729-557">Sieben Ziffern gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="e7729-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="e7729-558">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="e7729-558">Seven digits</span></span>
    
- <span data-ttu-id="e7729-559">Eine Ziffer oder ein Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="e7729-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e7729-560">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e7729-560">Checksum</span></span>

<span data-ttu-id="e7729-561">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e7729-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e7729-562">Definition</span><span class="sxs-lookup"><span data-stu-id="e7729-562">Definition</span></span>

<span data-ttu-id="e7729-563">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7729-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e7729-564">Der reguläre Ausdruck `Regex_spain_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e7729-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e7729-565">Ein Schlüsselwort `Keywords_spain_eu_national_id_card"` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="e7729-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="e7729-566">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e7729-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="e7729-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="e7729-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="e7729-568">DNI</span><span class="sxs-lookup"><span data-stu-id="e7729-568">dni</span></span>
  
<span data-ttu-id="e7729-569">nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-569">national identification number</span></span>
  
<span data-ttu-id="e7729-570">nationale Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-570">national identity number</span></span>
  
<span data-ttu-id="e7729-571">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-571">insurance number</span></span>
  
<span data-ttu-id="e7729-572">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-572">personal identification number</span></span>
  
<span data-ttu-id="e7729-573">nationale Identität</span><span class="sxs-lookup"><span data-stu-id="e7729-573">national identity</span></span>
  
<span data-ttu-id="e7729-574">persönliche Identität Nein</span><span class="sxs-lookup"><span data-stu-id="e7729-574">personal identity no</span></span>
  
<span data-ttu-id="e7729-575">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="e7729-575">unique identity number</span></span>
  
<span data-ttu-id="e7729-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="e7729-576">nationalidno#</span></span>
  
<span data-ttu-id="e7729-577">UniqueId</span><span class="sxs-lookup"><span data-stu-id="e7729-577">uniqueid#</span></span>
  
<span data-ttu-id="e7729-578">DNI</span><span class="sxs-lookup"><span data-stu-id="e7729-578">dni#</span></span>
  
<span data-ttu-id="e7729-579">National-Nr.</span><span class="sxs-lookup"><span data-stu-id="e7729-579">nationalid#</span></span>
  
<span data-ttu-id="e7729-580">nie</span><span class="sxs-lookup"><span data-stu-id="e7729-580">nie#</span></span>
  
<span data-ttu-id="e7729-581">nie</span><span class="sxs-lookup"><span data-stu-id="e7729-581">nie</span></span>
  
<span data-ttu-id="e7729-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="e7729-582">nienúmero#</span></span>
  
<span data-ttu-id="e7729-583">nie número</span><span class="sxs-lookup"><span data-stu-id="e7729-583">nie número</span></span>
  
<span data-ttu-id="e7729-584">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="e7729-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="e7729-585">Identidad Único</span><span class="sxs-lookup"><span data-stu-id="e7729-585">identidad único</span></span>
  
<span data-ttu-id="e7729-586">número Nacional Identidad</span><span class="sxs-lookup"><span data-stu-id="e7729-586">número nacional identidad</span></span>
  
<span data-ttu-id="e7729-587">DNI número</span><span class="sxs-lookup"><span data-stu-id="e7729-587">dni número</span></span>
  
<span data-ttu-id="e7729-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="e7729-588">dninúmero#</span></span>
  
<span data-ttu-id="e7729-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="e7729-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="e7729-590">Schweden</span><span class="sxs-lookup"><span data-stu-id="e7729-590">Sweden</span></span>

<span data-ttu-id="e7729-591">Weitere Informationen finden Sie im Abschnitt "schwedische National ID" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e7729-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7729-592">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7729-592">See also</span></span>

[<span data-ttu-id="e7729-593">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="e7729-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

