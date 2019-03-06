---
title: Nationale IdentifikationsNummer der EU
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp EU National Identification Number erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: afae2c3fa54fe5fcd93990cdf5797f5517c46202
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410970"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="9713c-104">Nationale IdentifikationsNummer der EU</span><span class="sxs-lookup"><span data-stu-id="9713c-104">EU National Identification Number</span></span>

<span data-ttu-id="9713c-105">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp EU National Identification Number erkennt.</span><span class="sxs-lookup"><span data-stu-id="9713c-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type.</span></span> <span data-ttu-id="9713c-106">Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="9713c-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="9713c-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="9713c-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="9713c-108">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-108">Format</span></span>

<span data-ttu-id="9713c-109">Eine 24-Zeichen-Kombination aus Buchstaben, Ziffern und Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="9713c-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-110">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-110">Pattern</span></span>

<span data-ttu-id="9713c-111">24 Zeichen:</span><span class="sxs-lookup"><span data-stu-id="9713c-111">24 characters:</span></span>
  
-  <span data-ttu-id="9713c-112">22 Buchstaben (Groß-/Kleinschreibung nicht beachtet), Ziffern, Schrägstriche, Schrägstriche oder Pluszeichen</span><span class="sxs-lookup"><span data-stu-id="9713c-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="9713c-113">Zwei Buchstaben (ohne Unterscheidung nach Groß-/Kleinschreibung), Ziffern, Schrägstriche, Schrägstriche, Pluszeichen oder Gleichheitszeichen</span><span class="sxs-lookup"><span data-stu-id="9713c-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-114">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-114">Checksum</span></span>

<span data-ttu-id="9713c-115">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9713c-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-116">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-116">Definition</span></span>

<span data-ttu-id="9713c-117">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-118">Der reguläre Ausdruck `Regex_austria_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-119">Ein Schlüsselwort `Keywords_austria_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9713c-120">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="9713c-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="9713c-122">Österreichische Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-122">austrian identity number</span></span>
  
<span data-ttu-id="9713c-123">nationale Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-123">national identity number</span></span>
  
<span data-ttu-id="9713c-124">Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-124">identity number</span></span>
  
<span data-ttu-id="9713c-125">national id</span><span class="sxs-lookup"><span data-stu-id="9713c-125">national id</span></span>
  
<span data-ttu-id="9713c-126">Personalausweis Republik Österreich</span><span class="sxs-lookup"><span data-stu-id="9713c-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="9713c-127">Belgien</span><span class="sxs-lookup"><span data-stu-id="9713c-127">Belgium</span></span>

<span data-ttu-id="9713c-128">Weitere Informationen finden Sie im Abschnitt "belgische nationale Rufnummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9713c-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="9713c-129">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="9713c-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="9713c-130">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-130">Format</span></span>

<span data-ttu-id="9713c-131">Zehn Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="9713c-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-132">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-132">Pattern</span></span>

<span data-ttu-id="9713c-133">Zehn Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="9713c-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="9713c-134">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="9713c-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="9713c-135">Zwei Ziffern, die der Geburts Reihenfolge entsprechen</span><span class="sxs-lookup"><span data-stu-id="9713c-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="9713c-136">Eine Ziffer, die dem Geschlecht entspricht: eine gerade Ziffer für männliche und eine ungerade Ziffer für weiblich</span><span class="sxs-lookup"><span data-stu-id="9713c-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="9713c-137">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9713c-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-138">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-138">Checksum</span></span>

<span data-ttu-id="9713c-139">Ja</span><span class="sxs-lookup"><span data-stu-id="9713c-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-140">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-140">Definition</span></span>

<span data-ttu-id="9713c-141">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-142">Die Funktion `Func_bulgaria_national_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-143">Ein Schlüsselwort `Keywords_bulgaria_national_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="9713c-144">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-145">Die Funktion `Func_bulgaria_national_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-146">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="9713c-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="9713c-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="9713c-148">EGN</span><span class="sxs-lookup"><span data-stu-id="9713c-148">egn</span></span>
  
<span data-ttu-id="9713c-149">EGN</span><span class="sxs-lookup"><span data-stu-id="9713c-149">egn#</span></span>
  
<span data-ttu-id="9713c-150">Bulgarische Nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-150">bulgarian national number</span></span>
  
<span data-ttu-id="9713c-151">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-151">national number</span></span>
  
<span data-ttu-id="9713c-152">social security number</span><span class="sxs-lookup"><span data-stu-id="9713c-152">social security number</span></span>
  
<span data-ttu-id="9713c-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="9713c-153">nationalnumber#</span></span>
  
<span data-ttu-id="9713c-154">SSN</span><span class="sxs-lookup"><span data-stu-id="9713c-154">ssn#</span></span>
  
<span data-ttu-id="9713c-155">SSN</span><span class="sxs-lookup"><span data-stu-id="9713c-155">ssn</span></span>
  
<span data-ttu-id="9713c-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="9713c-156">nationalnumber</span></span>
  
<span data-ttu-id="9713c-157">BNN</span><span class="sxs-lookup"><span data-stu-id="9713c-157">bnn#</span></span>
  
<span data-ttu-id="9713c-158">BNN</span><span class="sxs-lookup"><span data-stu-id="9713c-158">bnn</span></span>
  
<span data-ttu-id="9713c-159">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-159">personal id number</span></span>
  
<span data-ttu-id="9713c-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="9713c-160">personalidnumber#</span></span>
  
<span data-ttu-id="9713c-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="9713c-161">единен граждански номер</span></span>
  
<span data-ttu-id="9713c-162">edinn grazhdanski Nomer</span><span class="sxs-lookup"><span data-stu-id="9713c-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="9713c-163">егн</span><span class="sxs-lookup"><span data-stu-id="9713c-163">егн</span></span>
  
<span data-ttu-id="9713c-164">егн #</span><span class="sxs-lookup"><span data-stu-id="9713c-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="9713c-165">Kroatien</span><span class="sxs-lookup"><span data-stu-id="9713c-165">Croatia</span></span>

<span data-ttu-id="9713c-166">Weitere Informationen finden Sie im Abschnitt "Croatia Identity Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9713c-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="9713c-167">Zypern</span><span class="sxs-lookup"><span data-stu-id="9713c-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="9713c-168">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-168">Format</span></span>

<span data-ttu-id="9713c-169">Zehn Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="9713c-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-170">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-170">Pattern</span></span>

 <span data-ttu-id="9713c-171">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="9713c-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="9713c-172">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-172">Checksum</span></span>

<span data-ttu-id="9713c-173">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9713c-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-174">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-174">Definition</span></span>

<span data-ttu-id="9713c-175">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-176">Der reguläre Ausdruck `Regex_cyprus_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-177">Ein Schlüsselwort `Keywords_cyprus_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9713c-178">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="9713c-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="9713c-180">ID-Kartennummer</span><span class="sxs-lookup"><span data-stu-id="9713c-180">id card number</span></span>
  
<span data-ttu-id="9713c-181">national identification number</span><span class="sxs-lookup"><span data-stu-id="9713c-181">national identification number</span></span>
  
<span data-ttu-id="9713c-182">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-182">personal id number</span></span>
  
<span data-ttu-id="9713c-183">Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-183">identity card number</span></span>
  
<span data-ttu-id="9713c-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="9713c-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="9713c-185">Tschechien</span><span class="sxs-lookup"><span data-stu-id="9713c-185">Czech Republic</span></span>

<span data-ttu-id="9713c-186">Weitere Informationen finden Sie im Abschnitt "Czech National Identity Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9713c-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="9713c-187">Dänemark</span><span class="sxs-lookup"><span data-stu-id="9713c-187">Denmark</span></span>

<span data-ttu-id="9713c-188">Weitere Informationen finden Sie im Abschnitt "Denmark Personal Identification Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9713c-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="9713c-189">Estland</span><span class="sxs-lookup"><span data-stu-id="9713c-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="9713c-190">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-190">Format</span></span>

<span data-ttu-id="9713c-191">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="9713c-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-192">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-192">Pattern</span></span>

<span data-ttu-id="9713c-193">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="9713c-193">11 digits:</span></span>
  
- <span data-ttu-id="9713c-194">Eine Ziffer, die dem Geschlecht und dem Jahrhundert der Geburt entspricht (ungerade Zahl, gerade Zahl weiblich; 1-2:19. Jahrhundert; 3-4:20. Jahrhundert; 5-6:21st Century)</span><span class="sxs-lookup"><span data-stu-id="9713c-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="9713c-195">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="9713c-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="9713c-196">Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am selben Datum geboren wurden</span><span class="sxs-lookup"><span data-stu-id="9713c-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="9713c-197">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9713c-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-198">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-198">Checksum</span></span>

<span data-ttu-id="9713c-199">Ja</span><span class="sxs-lookup"><span data-stu-id="9713c-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-200">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-200">Definition</span></span>

<span data-ttu-id="9713c-201">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-202">Die Funktion `Func_estonia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-203">Ein Schlüsselwort `Keywords_estonia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9713c-204">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-205">Die Funktion `Func_estonia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-206">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="9713c-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="9713c-208">persönlicher Identifizierungscode</span><span class="sxs-lookup"><span data-stu-id="9713c-208">personal identification code</span></span>
  
<span data-ttu-id="9713c-209">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-209">personal identification number</span></span>
  
<span data-ttu-id="9713c-210">national identification number</span><span class="sxs-lookup"><span data-stu-id="9713c-210">national identification number</span></span>
  
<span data-ttu-id="9713c-211">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-211">national number</span></span>
  
<span data-ttu-id="9713c-212">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-212">personal id number</span></span>
  
<span data-ttu-id="9713c-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="9713c-213">personalidnumber#</span></span>
  
<span data-ttu-id="9713c-214">IK</span><span class="sxs-lookup"><span data-stu-id="9713c-214">ik</span></span>
  
<span data-ttu-id="9713c-215">Isikukood</span><span class="sxs-lookup"><span data-stu-id="9713c-215">isikukood</span></span>
  
<span data-ttu-id="9713c-216">ID-Kaart</span><span class="sxs-lookup"><span data-stu-id="9713c-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="9713c-217">Finnland</span><span class="sxs-lookup"><span data-stu-id="9713c-217">Finland</span></span>

<span data-ttu-id="9713c-218">Weitere Informationen finden Sie im Abschnitt "Finland National ID" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9713c-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="9713c-219">Frankreich</span><span class="sxs-lookup"><span data-stu-id="9713c-219">France</span></span>

<span data-ttu-id="9713c-220">Weitere Informationen finden Sie im Abschnitt "France National ID Card (CNI)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9713c-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="9713c-221">Deutschland</span><span class="sxs-lookup"><span data-stu-id="9713c-221">Germany</span></span>

<span data-ttu-id="9713c-222">Weitere Informationen finden Sie im Abschnitt "Deutschland PersonalausweisNummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9713c-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="9713c-223">Griechenland</span><span class="sxs-lookup"><span data-stu-id="9713c-223">Greece</span></span>

<span data-ttu-id="9713c-224">Weitere Informationen finden Sie im Abschnitt "GriechenLand National ID Card" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9713c-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="9713c-225">Ungarn</span><span class="sxs-lookup"><span data-stu-id="9713c-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="9713c-226">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-226">Format</span></span>

<span data-ttu-id="9713c-227">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="9713c-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-228">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-228">Pattern</span></span>

<span data-ttu-id="9713c-229">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="9713c-229">11 digits:</span></span>
  
-  <span data-ttu-id="9713c-230">Eine Ziffer, die dem Geschlecht entspricht (1-männlich, 2-weiblich, andere Zahlen sind auch für Bürger möglich, die vor 1900 oder Bürger mit doppelter Staatsbürgerschaft geboren wurden)</span><span class="sxs-lookup"><span data-stu-id="9713c-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="9713c-231">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="9713c-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="9713c-232">Drei Ziffern, die einer Seriennummer entsprechen</span><span class="sxs-lookup"><span data-stu-id="9713c-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="9713c-233">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9713c-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-234">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-234">Checksum</span></span>

<span data-ttu-id="9713c-235">Ja</span><span class="sxs-lookup"><span data-stu-id="9713c-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-236">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-236">Definition</span></span>

<span data-ttu-id="9713c-237">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-238">Die Funktion `Func_hungary_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-239">Ein Schlüsselwort `Keywords_hungary_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9713c-240">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-241">Die Funktion `Func_hungary_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-242">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="9713c-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="9713c-244">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-244">personal identification number</span></span>
  
<span data-ttu-id="9713c-245">identification number</span><span class="sxs-lookup"><span data-stu-id="9713c-245">identification number</span></span>
  
<span data-ttu-id="9713c-246">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-246">personal id number</span></span>
  
<span data-ttu-id="9713c-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="9713c-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="9713c-248">Irland</span><span class="sxs-lookup"><span data-stu-id="9713c-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="9713c-249">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-249">Format</span></span>

<span data-ttu-id="9713c-250">Eine neunstellige Kombination aus Buchstaben, Ziffern und einem Leerzeichen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-251">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-251">Pattern</span></span>

<span data-ttu-id="9713c-252">Eine neunstellige Kombination aus Buchstaben, Ziffern und einem Leerzeichen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="9713c-253">Vom 01. Januar 2013 bis jetzt:</span><span class="sxs-lookup"><span data-stu-id="9713c-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="9713c-254">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="9713c-254">Seven digits</span></span> 
    
- <span data-ttu-id="9713c-255">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9713c-255">One check digit</span></span>
    
- <span data-ttu-id="9713c-256">Ein Leerzeichen oder der Großbuchstabe "W" (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="9713c-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="9713c-257">Vor 01. Januar 2013:</span><span class="sxs-lookup"><span data-stu-id="9713c-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="9713c-258">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="9713c-258">Seven digits</span></span> 
    
- <span data-ttu-id="9713c-259">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9713c-259">One check digit</span></span>
    
- <span data-ttu-id="9713c-260">Ein Leerzeichen oder ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="9713c-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-261">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-261">Checksum</span></span>

<span data-ttu-id="9713c-262">Ja</span><span class="sxs-lookup"><span data-stu-id="9713c-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-263">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-263">Definition</span></span>

<span data-ttu-id="9713c-264">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-265">Die Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="9713c-266">Ein Schlüsselwort aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-266">A keyword from is found.</span></span>
    
<span data-ttu-id="9713c-267">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-268">Die Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-269">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="9713c-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="9713c-271">persönliche öffentliche Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-271">personal public service number</span></span>
  
<span data-ttu-id="9713c-272">PPS Nein</span><span class="sxs-lookup"><span data-stu-id="9713c-272">pps no</span></span>
  
<span data-ttu-id="9713c-273">Umsatz-und Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="9713c-274">RSI-No</span><span class="sxs-lookup"><span data-stu-id="9713c-274">rsi no</span></span>
  
<span data-ttu-id="9713c-275">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-275">personal identification number</span></span>
  
<span data-ttu-id="9713c-276">identification number</span><span class="sxs-lookup"><span data-stu-id="9713c-276">identification number</span></span>
  
<span data-ttu-id="9713c-277">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-277">personal id number</span></span>
  
<span data-ttu-id="9713c-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="9713c-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="9713c-279">uimh.</span><span class="sxs-lookup"><span data-stu-id="9713c-279">uimh.</span></span> <span data-ttu-id="9713c-280">PSP</span><span class="sxs-lookup"><span data-stu-id="9713c-280">psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="9713c-281">Italien</span><span class="sxs-lookup"><span data-stu-id="9713c-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="9713c-282">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-282">Format</span></span>

<span data-ttu-id="9713c-283">Eine 16-stellige Kombination aus Buchstaben und Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-284">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-284">Pattern</span></span>

<span data-ttu-id="9713c-285">Eine 16-stellige Kombination aus Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="9713c-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="9713c-286">Drei Buchstaben, die den ersten drei Konsonanten im Familiennamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="9713c-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="9713c-287">Drei Buchstaben, die dem ersten, dritten und vierten Konsonanten im Vornamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="9713c-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="9713c-288">Zwei Ziffern, die den letzten Ziffern des Geburtsjahrs entsprechen</span><span class="sxs-lookup"><span data-stu-id="9713c-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="9713c-289">Ein Buchstabe, der dem Buchstaben für den Geburtsmonat entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben A bis E, H, L, M, P, R bis T werden verwendet (also Januar ist A und Oktober ist R)</span><span class="sxs-lookup"><span data-stu-id="9713c-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="9713c-290">Zwei Ziffern, die dem Tag des Geburtsmonats entsprechen – zur Unterscheidung zwischen den Geschlechtern wird 40 zum Geburtstag für Frauen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9713c-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="9713c-291">Vier Ziffern, die der Ortskennzahl für die Gemeinde entsprechen, in der die Person geboren wurde (landesweite Codes werden für fremde Länder verwendet)</span><span class="sxs-lookup"><span data-stu-id="9713c-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="9713c-292">Eine Paritäts Ziffer</span><span class="sxs-lookup"><span data-stu-id="9713c-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-293">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-293">Checksum</span></span>

<span data-ttu-id="9713c-294">Ja</span><span class="sxs-lookup"><span data-stu-id="9713c-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-295">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-295">Definition</span></span>

<span data-ttu-id="9713c-296">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-297">Die Funktion `Func_italy_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-298">Ein Schlüsselwort `Keywords_italy_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9713c-299">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-300">Die Funktion `Func_italy_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-301">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="9713c-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="9713c-303">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="9713c-303">personal code</span></span>
  
<span data-ttu-id="9713c-304">persönliche Codenummer</span><span class="sxs-lookup"><span data-stu-id="9713c-304">personal code number</span></span>
  
<span data-ttu-id="9713c-305">persönliche Zertifikatsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-305">personal certificate number</span></span>
  
<span data-ttu-id="9713c-306">Fiskal Code</span><span class="sxs-lookup"><span data-stu-id="9713c-306">fiscal code</span></span>
  
<span data-ttu-id="9713c-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="9713c-307">personalcodeno#</span></span>
  
<span data-ttu-id="9713c-308">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-308">personal id number</span></span>
  
<span data-ttu-id="9713c-309">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="9713c-309">personal id code</span></span>
  
<span data-ttu-id="9713c-310">codedice personale</span><span class="sxs-lookup"><span data-stu-id="9713c-310">codice personale</span></span>
  
<span data-ttu-id="9713c-311">Numero Bescheinigung personale</span><span class="sxs-lookup"><span data-stu-id="9713c-311">numero certificato personale</span></span>
  
<span data-ttu-id="9713c-312">Numero personale</span><span class="sxs-lookup"><span data-stu-id="9713c-312">numero personale</span></span>
  
<span data-ttu-id="9713c-313">Numero-ID personale</span><span class="sxs-lookup"><span data-stu-id="9713c-313">numero id personale</span></span>
  
<span data-ttu-id="9713c-314">codedice-ID personale</span><span class="sxs-lookup"><span data-stu-id="9713c-314">codice id personale</span></span>
  
<span data-ttu-id="9713c-315">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="9713c-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="9713c-316">Italien</span><span class="sxs-lookup"><span data-stu-id="9713c-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="9713c-317">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-317">Format</span></span>

<span data-ttu-id="9713c-318">11 Ziffern und ein Bindestrich im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="9713c-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-319">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-319">Pattern</span></span>

<span data-ttu-id="9713c-320">11 Ziffern und ein Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="9713c-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="9713c-321">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="9713c-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="9713c-322">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="9713c-322">A hyphen</span></span>
    
- <span data-ttu-id="9713c-323">Eine Ziffer, die dem Jahrhundert der Geburt entspricht ("0" für das 19. Jahrhundert, "1" für das 20. Jahrhundert und "2" für das 21. Jahrhundert)</span><span class="sxs-lookup"><span data-stu-id="9713c-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="9713c-324">Vier Ziffern, nach dem Zufallsprinzip generiert</span><span class="sxs-lookup"><span data-stu-id="9713c-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-325">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-325">Checksum</span></span>

<span data-ttu-id="9713c-326">Ja</span><span class="sxs-lookup"><span data-stu-id="9713c-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-327">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-327">Definition</span></span>

<span data-ttu-id="9713c-328">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-329">Die Funktion `Func_latvia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-330">Ein Schlüsselwort `Keywords_latvia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9713c-331">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-332">Die Funktion `Func_latvia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-333">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="9713c-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="9713c-335">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="9713c-335">personal code</span></span>
  
<span data-ttu-id="9713c-336">persönliche Codenummer</span><span class="sxs-lookup"><span data-stu-id="9713c-336">personal code number</span></span>
  
<span data-ttu-id="9713c-337">persönliche Zertifikatsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-337">personal certificate number</span></span>
  
<span data-ttu-id="9713c-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="9713c-338">personalcodeno#</span></span>
  
<span data-ttu-id="9713c-339">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-339">personal id number</span></span>
  
<span data-ttu-id="9713c-340">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="9713c-340">personal id code</span></span>
  
<span data-ttu-id="9713c-341">Personas KODS</span><span class="sxs-lookup"><span data-stu-id="9713c-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="9713c-342">Litauen</span><span class="sxs-lookup"><span data-stu-id="9713c-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="9713c-343">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-343">Format</span></span>

<span data-ttu-id="9713c-344">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="9713c-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-345">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-345">Pattern</span></span>

<span data-ttu-id="9713c-346">11 Ziffern ohne Leerzeichen und Abgrenzungen:</span><span class="sxs-lookup"><span data-stu-id="9713c-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="9713c-347">Eine Ziffer, die dem Geschlecht der Person und dem Jahrhundert der Geburt entspricht</span><span class="sxs-lookup"><span data-stu-id="9713c-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="9713c-348">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="9713c-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="9713c-349">Drei Ziffern, die der Seriennummer des Geburtsdatums entsprechen</span><span class="sxs-lookup"><span data-stu-id="9713c-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="9713c-350">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9713c-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-351">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-351">Checksum</span></span>

<span data-ttu-id="9713c-352">Ja</span><span class="sxs-lookup"><span data-stu-id="9713c-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-353">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-353">Definition</span></span>

<span data-ttu-id="9713c-354">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-355">Die Funktion `Func_lithuania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-356">Ein Schlüsselwort `Keywords_lithuania_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9713c-357">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-358">Die Funktion `Func_lithuania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-359">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="9713c-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="9713c-361">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="9713c-361">personal numeric code</span></span>
  
<span data-ttu-id="9713c-362">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-362">unique identification number</span></span>
  
<span data-ttu-id="9713c-363">Citizen-Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-363">citizen service number</span></span>
  
<span data-ttu-id="9713c-364">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-364">unique identity number</span></span>
  
<span data-ttu-id="9713c-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9713c-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="9713c-366">persönlicher Code.</span><span class="sxs-lookup"><span data-stu-id="9713c-366">personal code.</span></span>
  
<span data-ttu-id="9713c-367">asmeninis skaitmeninis koda</span><span class="sxs-lookup"><span data-stu-id="9713c-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="9713c-368">unikalus identifikavimo Numeris</span><span class="sxs-lookup"><span data-stu-id="9713c-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="9713c-369">piliečio paslaugos Numeris</span><span class="sxs-lookup"><span data-stu-id="9713c-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="9713c-370">unikalus identifikavimo koda</span><span class="sxs-lookup"><span data-stu-id="9713c-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="9713c-371">Mens koda.</span><span class="sxs-lookup"><span data-stu-id="9713c-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="9713c-372">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="9713c-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="9713c-373">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-373">Format</span></span>

<span data-ttu-id="9713c-374">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="9713c-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-375">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-375">Pattern</span></span>

<span data-ttu-id="9713c-376">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="9713c-376">11 digits</span></span>
  
- <span data-ttu-id="9713c-377">Eine Ziffer, die dem Geschlecht der Person und dem Jahrhundert der Geburt entspricht</span><span class="sxs-lookup"><span data-stu-id="9713c-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="9713c-378">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="9713c-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="9713c-379">Drei Ziffern, die der Seriennummer des Geburtsdatums entsprechen</span><span class="sxs-lookup"><span data-stu-id="9713c-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="9713c-380">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9713c-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-381">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-381">Checksum</span></span>

<span data-ttu-id="9713c-382">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9713c-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-383">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-383">Definition</span></span>

<span data-ttu-id="9713c-384">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-385">Der reguläre Ausdruck `Regex_luxemburg_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-386">Ein Schlüsselwort `Keywords_luxemburg_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9713c-387">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="9713c-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="9713c-389">persönliche ID</span><span class="sxs-lookup"><span data-stu-id="9713c-389">personal id</span></span>
  
<span data-ttu-id="9713c-390">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-390">personal id number</span></span>
  
<span data-ttu-id="9713c-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="9713c-391">personalidno#</span></span>
  
<span data-ttu-id="9713c-392">eindeutige ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-392">unique id number</span></span>
  
<span data-ttu-id="9713c-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="9713c-393">personalidnumber#</span></span>
  
<span data-ttu-id="9713c-394">eindeutiger ID-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="9713c-394">unique id key</span></span>
  
<span data-ttu-id="9713c-395">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="9713c-395">personal id code</span></span>
  
<span data-ttu-id="9713c-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="9713c-396">uniqueidkey#</span></span>
  
<span data-ttu-id="9713c-397">individueller Code</span><span class="sxs-lookup"><span data-stu-id="9713c-397">individual code</span></span>
  
<span data-ttu-id="9713c-398">einzelne ID</span><span class="sxs-lookup"><span data-stu-id="9713c-398">individual id</span></span>
  
<span data-ttu-id="9713c-399">eindeutige-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="9713c-400">eindeutige-ID</span><span class="sxs-lookup"><span data-stu-id="9713c-400">eindeutige id</span></span>
  
<span data-ttu-id="9713c-401">ID personnelle</span><span class="sxs-lookup"><span data-stu-id="9713c-401">id personnelle</span></span>
  
<span data-ttu-id="9713c-402">Numéro d'identification Personal</span><span class="sxs-lookup"><span data-stu-id="9713c-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="9713c-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="9713c-403">idpersonnelle#</span></span>
  
<span data-ttu-id="9713c-404">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="9713c-405">EINDEUTIGEID #</span><span class="sxs-lookup"><span data-stu-id="9713c-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="9713c-406">Malta</span><span class="sxs-lookup"><span data-stu-id="9713c-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="9713c-407">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-407">Format</span></span>

<span data-ttu-id="9713c-408">Sieben Ziffern gefolgt von einem Buchstaben</span><span class="sxs-lookup"><span data-stu-id="9713c-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-409">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-409">Pattern</span></span>

<span data-ttu-id="9713c-410">Sieben Ziffern gefolgt von einem Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="9713c-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="9713c-411">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="9713c-411">Seven digits</span></span> 
    
- <span data-ttu-id="9713c-412">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="9713c-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-413">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-413">Checksum</span></span>

<span data-ttu-id="9713c-414">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9713c-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-415">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-415">Definition</span></span>

<span data-ttu-id="9713c-416">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-417">Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-418">Ein Schlüsselwort `Keywords_malta_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9713c-419">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-420">Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-421">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="9713c-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="9713c-423">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="9713c-423">personal numeric code</span></span>
  
<span data-ttu-id="9713c-424">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-424">unique identification number</span></span>
  
<span data-ttu-id="9713c-425">Citizen-Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-425">citizen service number</span></span>
  
<span data-ttu-id="9713c-426">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-426">unique identity number</span></span>
  
<span data-ttu-id="9713c-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9713c-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="9713c-428">Kodiċi personali</span><span class="sxs-lookup"><span data-stu-id="9713c-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="9713c-429">numru ta ' identifikazzjoni uniku</span><span class="sxs-lookup"><span data-stu-id="9713c-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="9713c-430">numru TAS-servizz taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="9713c-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="9713c-431">numru ta ' identità uniku</span><span class="sxs-lookup"><span data-stu-id="9713c-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="9713c-432">Niederlande</span><span class="sxs-lookup"><span data-stu-id="9713c-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="9713c-433">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-433">Format</span></span>

<span data-ttu-id="9713c-434">Neun Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="9713c-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-435">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-435">Pattern</span></span>

<span data-ttu-id="9713c-436">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="9713c-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9713c-437">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-437">Checksum</span></span>

<span data-ttu-id="9713c-438">Ja</span><span class="sxs-lookup"><span data-stu-id="9713c-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-439">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-439">Definition</span></span>

<span data-ttu-id="9713c-440">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-441">Die Funktion `Func_netherlands_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-442">Ein Schlüsselwort aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-442">A keyword from is found.</span></span>
    
<span data-ttu-id="9713c-443">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-444">Die Funktion `Func_netherlands_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-445">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="9713c-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="9713c-447">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="9713c-447">personal numeric code</span></span>
  
<span data-ttu-id="9713c-448">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-448">unique identification number</span></span>
  
<span data-ttu-id="9713c-449">Citizen-Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-449">citizen service number</span></span>
  
<span data-ttu-id="9713c-450">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-450">unique identity number</span></span>
  
<span data-ttu-id="9713c-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9713c-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="9713c-452">BSN</span><span class="sxs-lookup"><span data-stu-id="9713c-452">bsn</span></span>
  
<span data-ttu-id="9713c-453">BSN</span><span class="sxs-lookup"><span data-stu-id="9713c-453">bsn#</span></span>
  
<span data-ttu-id="9713c-454">Persoonlijke-numerieke-Code</span><span class="sxs-lookup"><span data-stu-id="9713c-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="9713c-455">uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="9713c-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="9713c-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="9713c-456">burgerservicenummer</span></span>
  
<span data-ttu-id="9713c-457">uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="9713c-458">Polen</span><span class="sxs-lookup"><span data-stu-id="9713c-458">Poland</span></span>

<span data-ttu-id="9713c-459">Weitere Informationen finden Sie im Abschnitt "polnische National ID (PESEL)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9713c-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="9713c-460">Portugal</span><span class="sxs-lookup"><span data-stu-id="9713c-460">Portugal</span></span>

<span data-ttu-id="9713c-461">Weitere Informationen finden Sie im Abschnitt "portugiesische Bürgerkarten Nummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9713c-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="9713c-462">Rumänien</span><span class="sxs-lookup"><span data-stu-id="9713c-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="9713c-463">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-463">Format</span></span>

<span data-ttu-id="9713c-464">13 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="9713c-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-465">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-465">Pattern</span></span>

<span data-ttu-id="9713c-466">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="9713c-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9713c-467">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-467">Checksum</span></span>

<span data-ttu-id="9713c-468">Ja</span><span class="sxs-lookup"><span data-stu-id="9713c-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-469">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-469">Definition</span></span>

<span data-ttu-id="9713c-470">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-471">Die Funktion `Func_romania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-472">Ein Schlüsselwort `Keywords_romania_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9713c-473">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-474">Die Funktion `Func_romania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-475">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="9713c-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="9713c-477">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="9713c-477">personal numeric code</span></span>
  
<span data-ttu-id="9713c-478">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-478">unique identification number</span></span>
  
<span data-ttu-id="9713c-479">CNP</span><span class="sxs-lookup"><span data-stu-id="9713c-479">cnp</span></span>
  
<span data-ttu-id="9713c-480">CNP</span><span class="sxs-lookup"><span data-stu-id="9713c-480">cnp#</span></span>
  
<span data-ttu-id="9713c-481">PIN</span><span class="sxs-lookup"><span data-stu-id="9713c-481">pin</span></span>
  
<span data-ttu-id="9713c-482">PIN</span><span class="sxs-lookup"><span data-stu-id="9713c-482">pin#</span></span>
  
<span data-ttu-id="9713c-483">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-483">insurance number</span></span>
  
<span data-ttu-id="9713c-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="9713c-484">insurancenumber#</span></span>
  
<span data-ttu-id="9713c-485">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-485">unique identity number</span></span>
  
<span data-ttu-id="9713c-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9713c-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="9713c-487">COD numerische Personal</span><span class="sxs-lookup"><span data-stu-id="9713c-487">cod numeric personal</span></span>
  
<span data-ttu-id="9713c-488">COD identificare Personal</span><span class="sxs-lookup"><span data-stu-id="9713c-488">cod identificare personal</span></span>
  
<span data-ttu-id="9713c-489">COD Unic identificare</span><span class="sxs-lookup"><span data-stu-id="9713c-489">cod unic identificare</span></span>
  
<span data-ttu-id="9713c-490">număr Personal Unic</span><span class="sxs-lookup"><span data-stu-id="9713c-490">număr personal unic</span></span>
  
<span data-ttu-id="9713c-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="9713c-491">număr identitate</span></span>
  
<span data-ttu-id="9713c-492">număr identificare Personal</span><span class="sxs-lookup"><span data-stu-id="9713c-492">număr identificare personal</span></span>
  
<span data-ttu-id="9713c-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="9713c-493">număridentitate#</span></span>
  
<span data-ttu-id="9713c-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="9713c-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="9713c-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="9713c-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="9713c-496">Slowakei</span><span class="sxs-lookup"><span data-stu-id="9713c-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="9713c-497">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-497">Format</span></span>

<span data-ttu-id="9713c-498">Zehn Ziffern mit einem umgekehrten Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="9713c-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-499">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-499">Pattern</span></span>

<span data-ttu-id="9713c-500">Zehn Ziffern mit einem umgekehrten Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="9713c-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9713c-501">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-501">Checksum</span></span>

<span data-ttu-id="9713c-502">Ja</span><span class="sxs-lookup"><span data-stu-id="9713c-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-503">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-503">Definition</span></span>

<span data-ttu-id="9713c-504">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-505">Die Funktion `Func_slovakia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-506">Ein Schlüsselwort `Keywords_slovakia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9713c-507">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-508">Die Funktion `Func_slovakia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-509">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="9713c-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="9713c-511">Geburtsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-511">birth number</span></span>
  
<span data-ttu-id="9713c-512">national identification number</span><span class="sxs-lookup"><span data-stu-id="9713c-512">national identification number</span></span>
  
<span data-ttu-id="9713c-513">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-513">personal identification number</span></span>
  
<span data-ttu-id="9713c-514">social security number</span><span class="sxs-lookup"><span data-stu-id="9713c-514">social security number</span></span>
  
<span data-ttu-id="9713c-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="9713c-515">nationalnumber#</span></span>
  
<span data-ttu-id="9713c-516">SSN</span><span class="sxs-lookup"><span data-stu-id="9713c-516">ssn#</span></span>
  
<span data-ttu-id="9713c-517">SSN</span><span class="sxs-lookup"><span data-stu-id="9713c-517">ssn</span></span>
  
<span data-ttu-id="9713c-518">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-518">national number</span></span>
  
<span data-ttu-id="9713c-519">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-519">personal id number</span></span>
  
<span data-ttu-id="9713c-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="9713c-520">personalidnumber#</span></span>
  
<span data-ttu-id="9713c-521">rč</span><span class="sxs-lookup"><span data-stu-id="9713c-521">rč</span></span>
  
<span data-ttu-id="9713c-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="9713c-522">rodné číslo</span></span>
  
<span data-ttu-id="9713c-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="9713c-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="9713c-524">Slowenien</span><span class="sxs-lookup"><span data-stu-id="9713c-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="9713c-525">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-525">Format</span></span>

<span data-ttu-id="9713c-526">13 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="9713c-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-527">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-527">Pattern</span></span>

<span data-ttu-id="9713c-528">13 Ziffern im angegebenen Muster:</span><span class="sxs-lookup"><span data-stu-id="9713c-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="9713c-529">Sieben Ziffern, die dem Geburtsdatum (DDMMLLL) entsprechen, wobei "LLL" den letzten drei Ziffern des Geburtsjahrs entspricht.</span><span class="sxs-lookup"><span data-stu-id="9713c-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="9713c-530">Zwei Ziffern, die dem Bereich der Geburt entsprechen</span><span class="sxs-lookup"><span data-stu-id="9713c-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="9713c-531">Drei Ziffern, die einer Kombination aus Geschlecht und Seriennummer für Personen entsprechen, die am selben Tag geboren wurden (000-499 für männlich und 500-999 für weiblich)</span><span class="sxs-lookup"><span data-stu-id="9713c-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="9713c-532">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9713c-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-533">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-533">Checksum</span></span>

<span data-ttu-id="9713c-534">Ja</span><span class="sxs-lookup"><span data-stu-id="9713c-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-535">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-535">Definition</span></span>

<span data-ttu-id="9713c-536">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-537">Die Funktion `Func_slovenia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-538">Ein Schlüsselwort `Keywords_slovenia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9713c-539">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-540">Die Funktion `Func_slovenia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9713c-541">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="9713c-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="9713c-543">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="9713c-543">personal numeric code</span></span>
  
<span data-ttu-id="9713c-544">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-544">unique identification number</span></span>
  
<span data-ttu-id="9713c-545">eindeutige Registrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-545">unique registration number</span></span>
  
<span data-ttu-id="9713c-546">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-546">unique identity number</span></span>
  
<span data-ttu-id="9713c-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9713c-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="9713c-548">eindeutige Master Bürger-Nummer</span><span class="sxs-lookup"><span data-stu-id="9713c-548">unique master citizen number</span></span>
  
<span data-ttu-id="9713c-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="9713c-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="9713c-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9713c-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="9713c-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="9713c-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="9713c-552">EMŠO</span><span class="sxs-lookup"><span data-stu-id="9713c-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="9713c-553">Spanien</span><span class="sxs-lookup"><span data-stu-id="9713c-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="9713c-554">Format</span><span class="sxs-lookup"><span data-stu-id="9713c-554">Format</span></span>

<span data-ttu-id="9713c-555">Sieben Ziffern gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="9713c-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9713c-556">Muster</span><span class="sxs-lookup"><span data-stu-id="9713c-556">Pattern</span></span>

<span data-ttu-id="9713c-557">Sieben Ziffern gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="9713c-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="9713c-558">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="9713c-558">Seven digits</span></span>
    
- <span data-ttu-id="9713c-559">Eine Ziffer oder ein Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="9713c-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9713c-560">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9713c-560">Checksum</span></span>

<span data-ttu-id="9713c-561">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9713c-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9713c-562">Definition</span><span class="sxs-lookup"><span data-stu-id="9713c-562">Definition</span></span>

<span data-ttu-id="9713c-563">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9713c-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9713c-564">Der reguläre Ausdruck `Regex_spain_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9713c-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9713c-565">Ein Schlüsselwort `Keywords_spain_eu_national_id_card"` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9713c-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9713c-566">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9713c-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="9713c-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9713c-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="9713c-568">DNI</span><span class="sxs-lookup"><span data-stu-id="9713c-568">dni</span></span>
  
<span data-ttu-id="9713c-569">national identification number</span><span class="sxs-lookup"><span data-stu-id="9713c-569">national identification number</span></span>
  
<span data-ttu-id="9713c-570">nationale Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-570">national identity number</span></span>
  
<span data-ttu-id="9713c-571">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-571">insurance number</span></span>
  
<span data-ttu-id="9713c-572">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-572">personal identification number</span></span>
  
<span data-ttu-id="9713c-573">nationale Identität</span><span class="sxs-lookup"><span data-stu-id="9713c-573">national identity</span></span>
  
<span data-ttu-id="9713c-574">persönliche Identität Nein</span><span class="sxs-lookup"><span data-stu-id="9713c-574">personal identity no</span></span>
  
<span data-ttu-id="9713c-575">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9713c-575">unique identity number</span></span>
  
<span data-ttu-id="9713c-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="9713c-576">nationalidno#</span></span>
  
<span data-ttu-id="9713c-577">UniqueId</span><span class="sxs-lookup"><span data-stu-id="9713c-577">uniqueid#</span></span>
  
<span data-ttu-id="9713c-578">DNI</span><span class="sxs-lookup"><span data-stu-id="9713c-578">dni#</span></span>
  
<span data-ttu-id="9713c-579">National-Nr.</span><span class="sxs-lookup"><span data-stu-id="9713c-579">nationalid#</span></span>
  
<span data-ttu-id="9713c-580">nie</span><span class="sxs-lookup"><span data-stu-id="9713c-580">nie#</span></span>
  
<span data-ttu-id="9713c-581">nie</span><span class="sxs-lookup"><span data-stu-id="9713c-581">nie</span></span>
  
<span data-ttu-id="9713c-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="9713c-582">nienúmero#</span></span>
  
<span data-ttu-id="9713c-583">nie número</span><span class="sxs-lookup"><span data-stu-id="9713c-583">nie número</span></span>
  
<span data-ttu-id="9713c-584">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="9713c-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="9713c-585">Identidad Único</span><span class="sxs-lookup"><span data-stu-id="9713c-585">identidad único</span></span>
  
<span data-ttu-id="9713c-586">número Nacional Identidad</span><span class="sxs-lookup"><span data-stu-id="9713c-586">número nacional identidad</span></span>
  
<span data-ttu-id="9713c-587">DNI número</span><span class="sxs-lookup"><span data-stu-id="9713c-587">dni número</span></span>
  
<span data-ttu-id="9713c-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="9713c-588">dninúmero#</span></span>
  
<span data-ttu-id="9713c-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="9713c-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="9713c-590">Schweden</span><span class="sxs-lookup"><span data-stu-id="9713c-590">Sweden</span></span>

<span data-ttu-id="9713c-591">Weitere Informationen finden Sie im Abschnitt "schwedische National ID" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9713c-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9713c-592">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9713c-592">See also</span></span>

[<span data-ttu-id="9713c-593">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="9713c-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

