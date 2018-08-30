---
title: EU National Identifikationsnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea971bf-9434-4b61-b825-2bbd28ae6064
description: In diesem Thema wird eine Data Loss Prevention (DLP) Richtlinie sieht für beim Erkennen des EU National Identifikationsnummer vertrauliche Informationen-Typs. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 29d2126b937ff46039284a74eb2a84f2ebbacb41
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529392"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="8a0b6-104">EU National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-104">EU National Identification Number</span></span>

<span data-ttu-id="8a0b6-p102">In diesem Thema wird eine Data Loss Prevention (DLP) Richtlinie sieht für beim Erkennen des EU National Identifikationsnummer vertrauliche Informationen-Typs. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="8a0b6-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="8a0b6-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-108">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-108">Format</span></span>

<span data-ttu-id="8a0b6-109">Eine 24 Zeichen Kombination von Buchstaben, Zahlen und Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-110">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-110">Pattern</span></span>

<span data-ttu-id="8a0b6-111">24 Zeichen:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-111">24 characters:</span></span>
  
-  <span data-ttu-id="8a0b6-112">22 Buchstaben (nicht Groß-/Kleinschreibung), Ziffern, umgekehrte Schrägstriche, Schrägstriche oder Pluszeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="8a0b6-113">Zwei Buchstaben (nicht Groß-/Kleinschreibung), Ziffern, umgekehrte Schrägstriche, Schrägstriche, Pluszeichen oder Gleichheitszeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-114">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-114">Checksum</span></span>

<span data-ttu-id="8a0b6-115">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8a0b6-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-116">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-116">Definition</span></span>

<span data-ttu-id="8a0b6-117">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-118">Der reguläre Ausdruck `Regex_austria_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-119">Ein Schlüsselwort aus `Keywords_austria_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8a0b6-120">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="8a0b6-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-122">österreichische Identität Anzahl</span><span class="sxs-lookup"><span data-stu-id="8a0b6-122">austrian identity number</span></span>
  
<span data-ttu-id="8a0b6-123">Anzahl der National Identität</span><span class="sxs-lookup"><span data-stu-id="8a0b6-123">national identity number</span></span>
  
<span data-ttu-id="8a0b6-124">Anzahl der Identität</span><span class="sxs-lookup"><span data-stu-id="8a0b6-124">identity number</span></span>
  
<span data-ttu-id="8a0b6-125">
national id</span><span class="sxs-lookup"><span data-stu-id="8a0b6-125">national id</span></span>
  
<span data-ttu-id="8a0b6-126">Personalausweis Republik österreich</span><span class="sxs-lookup"><span data-stu-id="8a0b6-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="8a0b6-127">Belgien</span><span class="sxs-lookup"><span data-stu-id="8a0b6-127">Belgium</span></span>

<span data-ttu-id="8a0b6-128">Weitere Informationen hierzu finden Sie im Abschnitt "Belgien Vorwahl" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8a0b6-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="8a0b6-129">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="8a0b6-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-130">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-130">Format</span></span>

<span data-ttu-id="8a0b6-131">Zehn Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-132">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-132">Pattern</span></span>

<span data-ttu-id="8a0b6-133">Zehn Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="8a0b6-134">Sechs Ziffern, die das Geburtsdatum (JJMMTT) entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="8a0b6-135">Zwei Ziffern, die die Reihenfolge Geburtsdatum entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="8a0b6-136">Eine Zahl, die das Geschlecht entspricht: eine gerade Zahl für Männlich und eine ungerade Ziffer für Weiblich</span><span class="sxs-lookup"><span data-stu-id="8a0b6-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="8a0b6-137">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-138">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-138">Checksum</span></span>

<span data-ttu-id="8a0b6-139">Ja</span><span class="sxs-lookup"><span data-stu-id="8a0b6-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-140">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-140">Definition</span></span>

<span data-ttu-id="8a0b6-141">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-142">Die Funktion `Func_bulgaria_national_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-143">Ein Schlüsselwort aus `Keywords_bulgaria_national_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="8a0b6-144">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-145">Die Funktion `Func_bulgaria_national_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-146">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="8a0b6-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="8a0b6-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="8a0b6-148">egn</span><span class="sxs-lookup"><span data-stu-id="8a0b6-148">egn</span></span>
  
<span data-ttu-id="8a0b6-149">Egn #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-149">egn#</span></span>
  
<span data-ttu-id="8a0b6-150">Bulgarisch Vorwahl</span><span class="sxs-lookup"><span data-stu-id="8a0b6-150">bulgarian national number</span></span>
  
<span data-ttu-id="8a0b6-151">Vorwahl</span><span class="sxs-lookup"><span data-stu-id="8a0b6-151">national number</span></span>
  
<span data-ttu-id="8a0b6-152">social security number
</span><span class="sxs-lookup"><span data-stu-id="8a0b6-152">social security number</span></span>
  
<span data-ttu-id="8a0b6-153">Nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-153">nationalnumber#</span></span>
  
<span data-ttu-id="8a0b6-154">ssn #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-154">ssn#</span></span>
  
<span data-ttu-id="8a0b6-155">ssn</span><span class="sxs-lookup"><span data-stu-id="8a0b6-155">ssn</span></span>
  
<span data-ttu-id="8a0b6-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="8a0b6-156">nationalnumber</span></span>
  
<span data-ttu-id="8a0b6-157">Bnn #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-157">bnn#</span></span>
  
<span data-ttu-id="8a0b6-158">bnn</span><span class="sxs-lookup"><span data-stu-id="8a0b6-158">bnn</span></span>
  
<span data-ttu-id="8a0b6-159">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-159">personal id number</span></span>
  
<span data-ttu-id="8a0b6-160">Personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-160">personalidnumber#</span></span>
  
<span data-ttu-id="8a0b6-161">ЕДИНЕН ГРАЖДАНСКИ НОМЕР</span><span class="sxs-lookup"><span data-stu-id="8a0b6-161">единен граждански номер</span></span>
  
<span data-ttu-id="8a0b6-162">Edinen Grazhdanski nomer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="8a0b6-163">ЕГН</span><span class="sxs-lookup"><span data-stu-id="8a0b6-163">егн</span></span>
  
<span data-ttu-id="8a0b6-164">ЕГН #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="8a0b6-165">Kroatien</span><span class="sxs-lookup"><span data-stu-id="8a0b6-165">Croatia</span></span>

<span data-ttu-id="8a0b6-166">Weitere Informationen hierzu finden Sie im Abschnitt "Kroatien Identity Number" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8a0b6-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="8a0b6-167">Zypern</span><span class="sxs-lookup"><span data-stu-id="8a0b6-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-168">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-168">Format</span></span>

<span data-ttu-id="8a0b6-169">Zehn Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-170">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-170">Pattern</span></span>

 <span data-ttu-id="8a0b6-171">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="8a0b6-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="8a0b6-172">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-172">Checksum</span></span>

<span data-ttu-id="8a0b6-173">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8a0b6-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-174">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-174">Definition</span></span>

<span data-ttu-id="8a0b6-175">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-176">Der reguläre Ausdruck `Regex_cyprus_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-177">Ein Schlüsselwort aus `Keywords_cyprus_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8a0b6-178">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="8a0b6-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-180">Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-180">id card number</span></span>
  
<span data-ttu-id="8a0b6-181">National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-181">national identification number</span></span>
  
<span data-ttu-id="8a0b6-182">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-182">personal id number</span></span>
  
<span data-ttu-id="8a0b6-183">Identität Card-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-183">identity card number</span></span>
  
<span data-ttu-id="8a0b6-184">ΤΑΥΤΟΤΗΤΑΣ</span><span class="sxs-lookup"><span data-stu-id="8a0b6-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="8a0b6-185">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="8a0b6-185">Czech Republic</span></span>

<span data-ttu-id="8a0b6-186">Weitere Informationen hierzu finden Sie im Abschnitt "Tschechisch National Identity Number" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8a0b6-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="8a0b6-187">Dänemark</span><span class="sxs-lookup"><span data-stu-id="8a0b6-187">Denmark</span></span>

<span data-ttu-id="8a0b6-188">Weitere Informationen hierzu finden Sie im Abschnitt "Dänemark persönliche Identifikationsnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8a0b6-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="8a0b6-189">Estland</span><span class="sxs-lookup"><span data-stu-id="8a0b6-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-190">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-190">Format</span></span>

<span data-ttu-id="8a0b6-191">11 Zahlen ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-192">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-192">Pattern</span></span>

<span data-ttu-id="8a0b6-193">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-193">11 digits:</span></span>
  
- <span data-ttu-id="8a0b6-194">Eine Zahl, die das Geschlecht und Century Geburtsdatum entspricht (ungerade Anzahl Männlich, gerade Anzahl Weiblich; 1 – 2: 19. Century; 3-4: 20. Century; 5-6: 2015)</span><span class="sxs-lookup"><span data-stu-id="8a0b6-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="8a0b6-195">Sechs Ziffern, die das Geburtsdatum (JJMMTT) entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="8a0b6-196">Drei Ziffern, die eine fortlaufende Zahl, die Personen, die an demselben Tag geboren trennt entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="8a0b6-197">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-198">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-198">Checksum</span></span>

<span data-ttu-id="8a0b6-199">Ja</span><span class="sxs-lookup"><span data-stu-id="8a0b6-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-200">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-200">Definition</span></span>

<span data-ttu-id="8a0b6-201">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-202">Die Funktion `Func_estonia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-203">Ein Schlüsselwort aus `Keywords_estonia_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="8a0b6-204">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-205">Die Funktion `Func_estonia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-206">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="8a0b6-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-208">PIN-code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-208">personal identification code</span></span>
  
<span data-ttu-id="8a0b6-209">Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-209">personal identification number</span></span>
  
<span data-ttu-id="8a0b6-210">National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-210">national identification number</span></span>
  
<span data-ttu-id="8a0b6-211">Vorwahl</span><span class="sxs-lookup"><span data-stu-id="8a0b6-211">national number</span></span>
  
<span data-ttu-id="8a0b6-212">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-212">personal id number</span></span>
  
<span data-ttu-id="8a0b6-213">Personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-213">personalidnumber#</span></span>
  
<span data-ttu-id="8a0b6-214">IK</span><span class="sxs-lookup"><span data-stu-id="8a0b6-214">ik</span></span>
  
<span data-ttu-id="8a0b6-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="8a0b6-215">isikukood</span></span>
  
<span data-ttu-id="8a0b6-216">ID-kaart</span><span class="sxs-lookup"><span data-stu-id="8a0b6-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="8a0b6-217">Finnland</span><span class="sxs-lookup"><span data-stu-id="8a0b6-217">Finland</span></span>

<span data-ttu-id="8a0b6-218">Weitere Informationen hierzu finden Sie im Abschnitt "Finnland Personalausweis" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8a0b6-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="8a0b6-219">Frankreich</span><span class="sxs-lookup"><span data-stu-id="8a0b6-219">France</span></span>

<span data-ttu-id="8a0b6-220">Weitere Informationen hierzu finden Sie im Abschnitt "Frankreich nationale d ' Identité (CNI)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8a0b6-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="8a0b6-221">Deutschland</span><span class="sxs-lookup"><span data-stu-id="8a0b6-221">Germany</span></span>

<span data-ttu-id="8a0b6-222">Weitere Informationen hierzu finden Sie im Abschnitt "Deutschland Identität Card-Nummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8a0b6-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="8a0b6-223">Griechenland</span><span class="sxs-lookup"><span data-stu-id="8a0b6-223">Greece</span></span>

<span data-ttu-id="8a0b6-224">Weitere Informationen hierzu finden Sie im Abschnitt "Griechenland nationale d ' Identité" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8a0b6-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="8a0b6-225">Ungarn</span><span class="sxs-lookup"><span data-stu-id="8a0b6-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-226">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-226">Format</span></span>

<span data-ttu-id="8a0b6-227">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8a0b6-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-228">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-228">Pattern</span></span>

<span data-ttu-id="8a0b6-229">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-229">11 digits:</span></span>
  
-  <span data-ttu-id="8a0b6-230">Eine Zahl, die das Geschlecht entspricht (1-Stecker, 2 weiblich, andere Zahlen sind auch für Bürger vor 1900 geboren oder Bürger mit double Bürger möglich)</span><span class="sxs-lookup"><span data-stu-id="8a0b6-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="8a0b6-231">Sechs Ziffern, die Geburtsdatum (JJMMTT) entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="8a0b6-232">Drei Ziffern, die eine fortlaufende Zahl entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="8a0b6-233">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-234">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-234">Checksum</span></span>

<span data-ttu-id="8a0b6-235">Ja</span><span class="sxs-lookup"><span data-stu-id="8a0b6-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-236">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-236">Definition</span></span>

<span data-ttu-id="8a0b6-237">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-238">Die Funktion `Func_hungary_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-239">Ein Schlüsselwort aus `Keywords_hungary_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="8a0b6-240">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-241">Die Funktion `Func_hungary_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-242">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="8a0b6-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-244">Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-244">personal identification number</span></span>
  
<span data-ttu-id="8a0b6-245">identification number
</span><span class="sxs-lookup"><span data-stu-id="8a0b6-245">identification number</span></span>
  
<span data-ttu-id="8a0b6-246">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-246">personal id number</span></span>
  
<span data-ttu-id="8a0b6-247">Személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="8a0b6-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="8a0b6-248">Irland</span><span class="sxs-lookup"><span data-stu-id="8a0b6-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-249">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-249">Format</span></span>

<span data-ttu-id="8a0b6-250">Eine neun Zeichen Kombination von Buchstaben, Zahlen und ein Leerzeichen in dem angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-251">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-251">Pattern</span></span>

<span data-ttu-id="8a0b6-252">Eine neun Zeichen Kombination von Buchstaben, Zahlen und ein Leerzeichen in dem angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="8a0b6-253">Von 01 für Januar 2013 bis jetzt:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="8a0b6-254">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="8a0b6-254">Seven digits</span></span> 
    
- <span data-ttu-id="8a0b6-255">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-255">One check digit</span></span>
    
- <span data-ttu-id="8a0b6-256">Ein Leerzeichen oder der Großbuchstabe "W" (Groß-/Kleinschreibung beachten)</span><span class="sxs-lookup"><span data-stu-id="8a0b6-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="8a0b6-257">Bevor Sie 01 für Januar 2013:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="8a0b6-258">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="8a0b6-258">Seven digits</span></span> 
    
- <span data-ttu-id="8a0b6-259">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-259">One check digit</span></span>
    
- <span data-ttu-id="8a0b6-260">Ein Leerzeichen oder einem großen Buchstaben (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8a0b6-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-261">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-261">Checksum</span></span>

<span data-ttu-id="8a0b6-262">Ja</span><span class="sxs-lookup"><span data-stu-id="8a0b6-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-263">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-263">Definition</span></span>

<span data-ttu-id="8a0b6-264">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-265">Die Funktion sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="8a0b6-266">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-266">A keyword from is found.</span></span>
    
<span data-ttu-id="8a0b6-267">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-268">Die Funktion sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-269">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="8a0b6-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-271">Anzahl der persönlichen öffentliche Dienstleistungen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-271">personal public service number</span></span>
  
<span data-ttu-id="8a0b6-272">PPS keine</span><span class="sxs-lookup"><span data-stu-id="8a0b6-272">pps no</span></span>
  
<span data-ttu-id="8a0b6-273">Umsatz und die Nutzung von sozialen Netzwerken insurance</span><span class="sxs-lookup"><span data-stu-id="8a0b6-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="8a0b6-274">RSI keine</span><span class="sxs-lookup"><span data-stu-id="8a0b6-274">rsi no</span></span>
  
<span data-ttu-id="8a0b6-275">Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-275">personal identification number</span></span>
  
<span data-ttu-id="8a0b6-276">identification number
</span><span class="sxs-lookup"><span data-stu-id="8a0b6-276">identification number</span></span>
  
<span data-ttu-id="8a0b6-277">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-277">personal id number</span></span>
  
<span data-ttu-id="8a0b6-278">Uimhir Phearsanta Seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="8a0b6-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="8a0b6-p103">Uimh. PSP</span><span class="sxs-lookup"><span data-stu-id="8a0b6-p103">uimh. psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="8a0b6-281">Italien</span><span class="sxs-lookup"><span data-stu-id="8a0b6-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-282">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-282">Format</span></span>

<span data-ttu-id="8a0b6-283">Eine 16 Zeichen Kombination von Buchstaben und Ziffern in dem angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-284">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-284">Pattern</span></span>

<span data-ttu-id="8a0b6-285">Eine 16 Zeichen Kombination von Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="8a0b6-286">Drei Buchstaben, die die ersten drei Doppelkonsonanten in der der Name der entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="8a0b6-287">Drei Buchstaben, die die erste, dritte und vierte entsprechen, Doppelkonsonanten in den Vornamen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="8a0b6-288">Zwei Ziffern, die auf die letzte Ziffern des Jahres Geburtsdatum entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="8a0b6-289">Einen Buchstaben, die den Brief, für den Monat Geburtsdatum entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben A bis E, H, L, M, P, R t verwendet werden (also Januar ist eine und Oktober R)</span><span class="sxs-lookup"><span data-stu-id="8a0b6-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="8a0b6-290">Zwei Ziffern, die den Tag des Monats Geburtsdatum entsprechen – 40 wird hinzugefügt, um Männern unterscheiden, auf den Tag des Geburtsdaten von Frau</span><span class="sxs-lookup"><span data-stu-id="8a0b6-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="8a0b6-291">Vier Ziffern, die speziell für die Gemeinde Ortskennzahl entspricht, in die Person geboren wurde (Land geltende Codes für Ausland verwendet werden)</span><span class="sxs-lookup"><span data-stu-id="8a0b6-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="8a0b6-292">Eine Parität Ziffer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-293">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-293">Checksum</span></span>

<span data-ttu-id="8a0b6-294">Ja</span><span class="sxs-lookup"><span data-stu-id="8a0b6-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-295">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-295">Definition</span></span>

<span data-ttu-id="8a0b6-296">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-297">Die Funktion `Func_italy_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-298">Ein Schlüsselwort aus `Keywords_italy_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="8a0b6-299">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-300">Die Funktion `Func_italy_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-301">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="8a0b6-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-303">Persönliche code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-303">personal code</span></span>
  
<span data-ttu-id="8a0b6-304">persönliche Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-304">personal code number</span></span>
  
<span data-ttu-id="8a0b6-305">eigenes Zertifikat Anzahl</span><span class="sxs-lookup"><span data-stu-id="8a0b6-305">personal certificate number</span></span>
  
<span data-ttu-id="8a0b6-306">Fiscal code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-306">fiscal code</span></span>
  
<span data-ttu-id="8a0b6-307">Personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-307">personalcodeno#</span></span>
  
<span data-ttu-id="8a0b6-308">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-308">personal id number</span></span>
  
<span data-ttu-id="8a0b6-309">Persönliche Id-code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-309">personal id code</span></span>
  
<span data-ttu-id="8a0b6-310">Codice personale</span><span class="sxs-lookup"><span data-stu-id="8a0b6-310">codice personale</span></span>
  
<span data-ttu-id="8a0b6-311">Numero Certificato personale</span><span class="sxs-lookup"><span data-stu-id="8a0b6-311">numero certificato personale</span></span>
  
<span data-ttu-id="8a0b6-312">Numero personale</span><span class="sxs-lookup"><span data-stu-id="8a0b6-312">numero personale</span></span>
  
<span data-ttu-id="8a0b6-313">Numero Id personale</span><span class="sxs-lookup"><span data-stu-id="8a0b6-313">numero id personale</span></span>
  
<span data-ttu-id="8a0b6-314">Codice Id personale</span><span class="sxs-lookup"><span data-stu-id="8a0b6-314">codice id personale</span></span>
  
<span data-ttu-id="8a0b6-315">Codice fiscale</span><span class="sxs-lookup"><span data-stu-id="8a0b6-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="8a0b6-316">Italien</span><span class="sxs-lookup"><span data-stu-id="8a0b6-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-317">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-317">Format</span></span>

<span data-ttu-id="8a0b6-318">11 Ziffern und ein Bindestrich im angegebenen format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-319">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-319">Pattern</span></span>

<span data-ttu-id="8a0b6-320">11 Ziffern und ein Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="8a0b6-321">Sechs Ziffern, die das Geburtsdatum (DDMMYY) entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="8a0b6-322">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="8a0b6-322">A hyphen</span></span>
    
- <span data-ttu-id="8a0b6-323">Eine Ziffer aus, die die Century Geburtsdatum ("0" für 19. Century, für allem "1" und "2" für 2015) entspricht</span><span class="sxs-lookup"><span data-stu-id="8a0b6-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="8a0b6-324">Vier Ziffern, zufällig generiert</span><span class="sxs-lookup"><span data-stu-id="8a0b6-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-325">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-325">Checksum</span></span>

<span data-ttu-id="8a0b6-326">Ja</span><span class="sxs-lookup"><span data-stu-id="8a0b6-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-327">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-327">Definition</span></span>

<span data-ttu-id="8a0b6-328">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-329">Die Funktion `Func_latvia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-330">Ein Schlüsselwort aus `Keywords_latvia_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="8a0b6-331">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-332">Die Funktion `Func_latvia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-333">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="8a0b6-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-335">Persönliche code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-335">personal code</span></span>
  
<span data-ttu-id="8a0b6-336">persönliche Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-336">personal code number</span></span>
  
<span data-ttu-id="8a0b6-337">eigenes Zertifikat Anzahl</span><span class="sxs-lookup"><span data-stu-id="8a0b6-337">personal certificate number</span></span>
  
<span data-ttu-id="8a0b6-338">Personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-338">personalcodeno#</span></span>
  
<span data-ttu-id="8a0b6-339">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-339">personal id number</span></span>
  
<span data-ttu-id="8a0b6-340">Persönliche Id-code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-340">personal id code</span></span>
  
<span data-ttu-id="8a0b6-341">Rollen kods</span><span class="sxs-lookup"><span data-stu-id="8a0b6-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="8a0b6-342">Litauen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-343">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-343">Format</span></span>

<span data-ttu-id="8a0b6-344">11 Zahlen ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-345">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-345">Pattern</span></span>

<span data-ttu-id="8a0b6-346">11 Zahlen ohne Leerzeichen und Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="8a0b6-347">Eine Zahl, die das Geschlecht und Century Geburtsdatum der Person entspricht</span><span class="sxs-lookup"><span data-stu-id="8a0b6-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="8a0b6-348">Sechs Ziffern, die Geburtsdatum (JJMMTT) entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="8a0b6-349">Drei Ziffern, die die Seriennummer des das Geburtsdatum entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="8a0b6-350">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-351">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-351">Checksum</span></span>

<span data-ttu-id="8a0b6-352">Ja</span><span class="sxs-lookup"><span data-stu-id="8a0b6-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-353">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-353">Definition</span></span>

<span data-ttu-id="8a0b6-354">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-355">Die Funktion `Func_lithuania_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-356">Ein Schlüsselwort aus `Keywords_lithuania_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="8a0b6-357">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-358">Die Funktion `Func_lithuania_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-359">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="8a0b6-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-361">Persönliche numerischen code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-361">personal numeric code</span></span>
  
<span data-ttu-id="8a0b6-362">eindeutige ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-362">unique identification number</span></span>
  
<span data-ttu-id="8a0b6-363">Anzahl der Bürger-Dienst</span><span class="sxs-lookup"><span data-stu-id="8a0b6-363">citizen service number</span></span>
  
<span data-ttu-id="8a0b6-364">Anzahl der eindeutigen Identität</span><span class="sxs-lookup"><span data-stu-id="8a0b6-364">unique identity number</span></span>
  
<span data-ttu-id="8a0b6-365">Uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="8a0b6-366">Persönliche Code.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-366">personal code.</span></span>
  
<span data-ttu-id="8a0b6-367">Asmeninis Skaitmeninis kodas</span><span class="sxs-lookup"><span data-stu-id="8a0b6-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="8a0b6-368">Unikalus Identifikavimo numeris</span><span class="sxs-lookup"><span data-stu-id="8a0b6-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="8a0b6-369">Piliečio Paslaugos numeris</span><span class="sxs-lookup"><span data-stu-id="8a0b6-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="8a0b6-370">Unikalus Identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="8a0b6-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="8a0b6-371">Asmens Kodas.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="8a0b6-372">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="8a0b6-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-373">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-373">Format</span></span>

<span data-ttu-id="8a0b6-374">11 Zahlen ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-375">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-375">Pattern</span></span>

<span data-ttu-id="8a0b6-376">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8a0b6-376">11 digits</span></span>
  
- <span data-ttu-id="8a0b6-377">Eine Zahl, die das Geschlecht und Century Geburtsdatum der Person entspricht</span><span class="sxs-lookup"><span data-stu-id="8a0b6-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="8a0b6-378">Sechs Ziffern, die Geburtsdatum (JJMMTT) entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="8a0b6-379">Drei Ziffern, die die Seriennummer des das Geburtsdatum entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="8a0b6-380">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-381">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-381">Checksum</span></span>

<span data-ttu-id="8a0b6-382">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8a0b6-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-383">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-383">Definition</span></span>

<span data-ttu-id="8a0b6-384">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-385">Der reguläre Ausdruck `Regex_luxemburg_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-386">Ein Schlüsselwort aus `Keywords_luxemburg_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8a0b6-387">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="8a0b6-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-389">Persönliche id</span><span class="sxs-lookup"><span data-stu-id="8a0b6-389">personal id</span></span>
  
<span data-ttu-id="8a0b6-390">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-390">personal id number</span></span>
  
<span data-ttu-id="8a0b6-391">Personalidno #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-391">personalidno#</span></span>
  
<span data-ttu-id="8a0b6-392">eindeutige Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-392">unique id number</span></span>
  
<span data-ttu-id="8a0b6-393">Personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-393">personalidnumber#</span></span>
  
<span data-ttu-id="8a0b6-394">eindeutige Id-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="8a0b6-394">unique id key</span></span>
  
<span data-ttu-id="8a0b6-395">Persönliche Id-code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-395">personal id code</span></span>
  
<span data-ttu-id="8a0b6-396">Uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-396">uniqueidkey#</span></span>
  
<span data-ttu-id="8a0b6-397">einzelne code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-397">individual code</span></span>
  
<span data-ttu-id="8a0b6-398">einzelne-id</span><span class="sxs-lookup"><span data-stu-id="8a0b6-398">individual id</span></span>
  
<span data-ttu-id="8a0b6-399">Eindeutige Id-nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="8a0b6-400">Eindeutige id</span><span class="sxs-lookup"><span data-stu-id="8a0b6-400">eindeutige id</span></span>
  
<span data-ttu-id="8a0b6-401">ID personnelle</span><span class="sxs-lookup"><span data-stu-id="8a0b6-401">id personnelle</span></span>
  
<span data-ttu-id="8a0b6-402">Numéro d ' Identification Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="8a0b6-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="8a0b6-403">Idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-403">idpersonnelle#</span></span>
  
<span data-ttu-id="8a0b6-404">Persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="8a0b6-405">EINDEUTIGEID #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="8a0b6-406">Malta</span><span class="sxs-lookup"><span data-stu-id="8a0b6-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-407">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-407">Format</span></span>

<span data-ttu-id="8a0b6-408">Sieben Ziffern, gefolgt von einem Buchstaben</span><span class="sxs-lookup"><span data-stu-id="8a0b6-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-409">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-409">Pattern</span></span>

<span data-ttu-id="8a0b6-410">Sieben Ziffern, gefolgt von einem Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="8a0b6-411">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="8a0b6-411">Seven digits</span></span> 
    
- <span data-ttu-id="8a0b6-412">Einen Großbuchstaben (Groß-/Kleinschreibung beachten)</span><span class="sxs-lookup"><span data-stu-id="8a0b6-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-413">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-413">Checksum</span></span>

<span data-ttu-id="8a0b6-414">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8a0b6-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-415">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-415">Definition</span></span>

<span data-ttu-id="8a0b6-416">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-417">Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-418">Ein Schlüsselwort aus `Keywords_malta_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="8a0b6-419">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-420">Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-421">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="8a0b6-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-423">Persönliche numerischen code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-423">personal numeric code</span></span>
  
<span data-ttu-id="8a0b6-424">eindeutige ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-424">unique identification number</span></span>
  
<span data-ttu-id="8a0b6-425">Anzahl der Bürger-Dienst</span><span class="sxs-lookup"><span data-stu-id="8a0b6-425">citizen service number</span></span>
  
<span data-ttu-id="8a0b6-426">Anzahl der eindeutigen Identität</span><span class="sxs-lookup"><span data-stu-id="8a0b6-426">unique identity number</span></span>
  
<span data-ttu-id="8a0b6-427">Uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="8a0b6-428">Kodiċi Numerali personali</span><span class="sxs-lookup"><span data-stu-id="8a0b6-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="8a0b6-429">Numru ta ' Identifikazzjoni Uniku</span><span class="sxs-lookup"><span data-stu-id="8a0b6-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="8a0b6-430">Numru Aufgabe Servizz Taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="8a0b6-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="8a0b6-431">Numru ta' Identità Uniku</span><span class="sxs-lookup"><span data-stu-id="8a0b6-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="8a0b6-432">Niederlande</span><span class="sxs-lookup"><span data-stu-id="8a0b6-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-433">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-433">Format</span></span>

<span data-ttu-id="8a0b6-434">Neun Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-435">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-435">Pattern</span></span>

<span data-ttu-id="8a0b6-436">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="8a0b6-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8a0b6-437">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-437">Checksum</span></span>

<span data-ttu-id="8a0b6-438">Ja</span><span class="sxs-lookup"><span data-stu-id="8a0b6-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-439">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-439">Definition</span></span>

<span data-ttu-id="8a0b6-440">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-441">Die Funktion `Func_netherlands_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-442">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-442">A keyword from is found.</span></span>
    
<span data-ttu-id="8a0b6-443">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-444">Die Funktion `Func_netherlands_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-445">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="8a0b6-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-447">Persönliche numerischen code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-447">personal numeric code</span></span>
  
<span data-ttu-id="8a0b6-448">eindeutige ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-448">unique identification number</span></span>
  
<span data-ttu-id="8a0b6-449">Anzahl der Bürger-Dienst</span><span class="sxs-lookup"><span data-stu-id="8a0b6-449">citizen service number</span></span>
  
<span data-ttu-id="8a0b6-450">Anzahl der eindeutigen Identität</span><span class="sxs-lookup"><span data-stu-id="8a0b6-450">unique identity number</span></span>
  
<span data-ttu-id="8a0b6-451">Uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="8a0b6-452">bsn</span><span class="sxs-lookup"><span data-stu-id="8a0b6-452">bsn</span></span>
  
<span data-ttu-id="8a0b6-453">Bsn #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-453">bsn#</span></span>
  
<span data-ttu-id="8a0b6-454">Persoonlijke Numerieke code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="8a0b6-455">Uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="8a0b6-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-456">burgerservicenummer</span></span>
  
<span data-ttu-id="8a0b6-457">Uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="8a0b6-458">Polen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-458">Poland</span></span>

<span data-ttu-id="8a0b6-459">Weitere Informationen hierzu finden Sie im Abschnitt "Polen National-ID (PESEL)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8a0b6-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="8a0b6-460">Portugal</span><span class="sxs-lookup"><span data-stu-id="8a0b6-460">Portugal</span></span>

<span data-ttu-id="8a0b6-461">Weitere Informationen hierzu finden Sie im Abschnitt "Portugal Bürger Card-Nummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8a0b6-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="8a0b6-462">Rumänien</span><span class="sxs-lookup"><span data-stu-id="8a0b6-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-463">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-463">Format</span></span>

<span data-ttu-id="8a0b6-464">13 Stellen ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-465">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-465">Pattern</span></span>

<span data-ttu-id="8a0b6-466">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="8a0b6-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8a0b6-467">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-467">Checksum</span></span>

<span data-ttu-id="8a0b6-468">Ja</span><span class="sxs-lookup"><span data-stu-id="8a0b6-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-469">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-469">Definition</span></span>

<span data-ttu-id="8a0b6-470">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-471">Die Funktion `Func_romania_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-472">Ein Schlüsselwort aus `Keywords_romania_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="8a0b6-473">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-474">Die Funktion `Func_romania_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-475">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="8a0b6-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-477">Persönliche numerischen code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-477">personal numeric code</span></span>
  
<span data-ttu-id="8a0b6-478">eindeutige ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-478">unique identification number</span></span>
  
<span data-ttu-id="8a0b6-479">CNP</span><span class="sxs-lookup"><span data-stu-id="8a0b6-479">cnp</span></span>
  
<span data-ttu-id="8a0b6-480">CNP #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-480">cnp#</span></span>
  
<span data-ttu-id="8a0b6-481">Anheften</span><span class="sxs-lookup"><span data-stu-id="8a0b6-481">pin</span></span>
  
<span data-ttu-id="8a0b6-482">PIN-</span><span class="sxs-lookup"><span data-stu-id="8a0b6-482">pin#</span></span>
  
<span data-ttu-id="8a0b6-483">Versicherungsvertreter Anzahl</span><span class="sxs-lookup"><span data-stu-id="8a0b6-483">insurance number</span></span>
  
<span data-ttu-id="8a0b6-484">Insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-484">insurancenumber#</span></span>
  
<span data-ttu-id="8a0b6-485">Anzahl der eindeutigen Identität</span><span class="sxs-lookup"><span data-stu-id="8a0b6-485">unique identity number</span></span>
  
<span data-ttu-id="8a0b6-486">Uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="8a0b6-487">COD numerische persönlich</span><span class="sxs-lookup"><span data-stu-id="8a0b6-487">cod numeric personal</span></span>
  
<span data-ttu-id="8a0b6-488">Persönliche Identificare Kabeljau</span><span class="sxs-lookup"><span data-stu-id="8a0b6-488">cod identificare personal</span></span>
  
<span data-ttu-id="8a0b6-489">COD Unic identificare</span><span class="sxs-lookup"><span data-stu-id="8a0b6-489">cod unic identificare</span></span>
  
<span data-ttu-id="8a0b6-490">Persönliche Unic număr</span><span class="sxs-lookup"><span data-stu-id="8a0b6-490">număr personal unic</span></span>
  
<span data-ttu-id="8a0b6-491">Număr identitate</span><span class="sxs-lookup"><span data-stu-id="8a0b6-491">număr identitate</span></span>
  
<span data-ttu-id="8a0b6-492">Număr Identificare persönliche</span><span class="sxs-lookup"><span data-stu-id="8a0b6-492">număr identificare personal</span></span>
  
<span data-ttu-id="8a0b6-493">Număridentitate #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-493">număridentitate#</span></span>
  
<span data-ttu-id="8a0b6-494">Codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="8a0b6-495">Numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="8a0b6-496">Slowakei</span><span class="sxs-lookup"><span data-stu-id="8a0b6-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-497">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-497">Format</span></span>

<span data-ttu-id="8a0b6-498">Mit einem umgekehrten Schrägstrich zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="8a0b6-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-499">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-499">Pattern</span></span>

<span data-ttu-id="8a0b6-500">Zehn Ziffern, die ein umgekehrter Schrägstrich enthält:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8a0b6-501">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-501">Checksum</span></span>

<span data-ttu-id="8a0b6-502">Ja</span><span class="sxs-lookup"><span data-stu-id="8a0b6-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-503">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-503">Definition</span></span>

<span data-ttu-id="8a0b6-504">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-505">Die Funktion `Func_slovakia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-506">Ein Schlüsselwort aus `Keywords_slovakia_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="8a0b6-507">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-508">Die Funktion `Func_slovakia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-509">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="8a0b6-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-511">Geburtsdatum Anzahl</span><span class="sxs-lookup"><span data-stu-id="8a0b6-511">birth number</span></span>
  
<span data-ttu-id="8a0b6-512">National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-512">national identification number</span></span>
  
<span data-ttu-id="8a0b6-513">Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-513">personal identification number</span></span>
  
<span data-ttu-id="8a0b6-514">social security number
</span><span class="sxs-lookup"><span data-stu-id="8a0b6-514">social security number</span></span>
  
<span data-ttu-id="8a0b6-515">Nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-515">nationalnumber#</span></span>
  
<span data-ttu-id="8a0b6-516">ssn #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-516">ssn#</span></span>
  
<span data-ttu-id="8a0b6-517">ssn</span><span class="sxs-lookup"><span data-stu-id="8a0b6-517">ssn</span></span>
  
<span data-ttu-id="8a0b6-518">Vorwahl</span><span class="sxs-lookup"><span data-stu-id="8a0b6-518">national number</span></span>
  
<span data-ttu-id="8a0b6-519">Persönliche Id-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-519">personal id number</span></span>
  
<span data-ttu-id="8a0b6-520">Personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-520">personalidnumber#</span></span>
  
<span data-ttu-id="8a0b6-521">rč</span><span class="sxs-lookup"><span data-stu-id="8a0b6-521">rč</span></span>
  
<span data-ttu-id="8a0b6-522">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="8a0b6-522">rodné číslo</span></span>
  
<span data-ttu-id="8a0b6-523">Rodne cislo</span><span class="sxs-lookup"><span data-stu-id="8a0b6-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="8a0b6-524">Slowenien</span><span class="sxs-lookup"><span data-stu-id="8a0b6-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-525">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-525">Format</span></span>

<span data-ttu-id="8a0b6-526">13 Stellen ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-527">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-527">Pattern</span></span>

<span data-ttu-id="8a0b6-528">13 Stellen in dem angegebenen Muster:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="8a0b6-529">Sieben Ziffern, die das Geburtsdatum (DDMMLLL) entsprechen, wobei "LLL" zur letzten drei Ziffern des Jahres Geburtsdatum entspricht</span><span class="sxs-lookup"><span data-stu-id="8a0b6-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="8a0b6-530">Zwei Ziffern, die den Bereich Geburtsdatum entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="8a0b6-531">Drei Ziffern, die eine Kombination von Geschlecht und Seriennummer für Personen, die am gleichen Tag (000-499 für männlich) und 500-999 für Weiblich geboren entsprechen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="8a0b6-532">Ein Kontrollkästchen Ziffer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-533">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-533">Checksum</span></span>

<span data-ttu-id="8a0b6-534">Ja</span><span class="sxs-lookup"><span data-stu-id="8a0b6-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-535">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-535">Definition</span></span>

<span data-ttu-id="8a0b6-536">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-537">Die Funktion `Func_slovenia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-538">Ein Schlüsselwort aus `Keywords_slovenia_eu_national_id_card` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="8a0b6-539">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-540">Die Funktion `Func_slovenia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="8a0b6-541">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="8a0b6-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-543">Persönliche numerischen code</span><span class="sxs-lookup"><span data-stu-id="8a0b6-543">personal numeric code</span></span>
  
<span data-ttu-id="8a0b6-544">eindeutige ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-544">unique identification number</span></span>
  
<span data-ttu-id="8a0b6-545">eindeutige Nummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-545">unique registration number</span></span>
  
<span data-ttu-id="8a0b6-546">Anzahl der eindeutigen Identität</span><span class="sxs-lookup"><span data-stu-id="8a0b6-546">unique identity number</span></span>
  
<span data-ttu-id="8a0b6-547">Uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="8a0b6-548">Anzahl der eindeutigen master Bürger</span><span class="sxs-lookup"><span data-stu-id="8a0b6-548">unique master citizen number</span></span>
  
<span data-ttu-id="8a0b6-549">Edinstvena Identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="8a0b6-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="8a0b6-550">Uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="8a0b6-551">Edinstvena številka Glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="8a0b6-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="8a0b6-552">emšo</span><span class="sxs-lookup"><span data-stu-id="8a0b6-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="8a0b6-553">Spanien</span><span class="sxs-lookup"><span data-stu-id="8a0b6-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="8a0b6-554">Format</span><span class="sxs-lookup"><span data-stu-id="8a0b6-554">Format</span></span>

<span data-ttu-id="8a0b6-555">Sieben Ziffern, gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8a0b6-556">Muster</span><span class="sxs-lookup"><span data-stu-id="8a0b6-556">Pattern</span></span>

<span data-ttu-id="8a0b6-557">Sieben Ziffern, gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="8a0b6-558">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="8a0b6-558">Seven digits</span></span>
    
- <span data-ttu-id="8a0b6-559">Eine Ziffern oder Buchstaben (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="8a0b6-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8a0b6-560">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="8a0b6-560">Checksum</span></span>

<span data-ttu-id="8a0b6-561">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="8a0b6-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8a0b6-562">Definition</span><span class="sxs-lookup"><span data-stu-id="8a0b6-562">Definition</span></span>

<span data-ttu-id="8a0b6-563">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="8a0b6-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8a0b6-564">Der reguläre Ausdruck `Regex_spain_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8a0b6-565">Ein Schlüsselwort aus `Keywords_spain_eu_national_id_card"` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="8a0b6-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8a0b6-566">Keywords</span><span class="sxs-lookup"><span data-stu-id="8a0b6-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="8a0b6-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="8a0b6-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="8a0b6-568">DNI</span><span class="sxs-lookup"><span data-stu-id="8a0b6-568">dni</span></span>
  
<span data-ttu-id="8a0b6-569">National Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-569">national identification number</span></span>
  
<span data-ttu-id="8a0b6-570">Anzahl der National Identität</span><span class="sxs-lookup"><span data-stu-id="8a0b6-570">national identity number</span></span>
  
<span data-ttu-id="8a0b6-571">Versicherungsvertreter Anzahl</span><span class="sxs-lookup"><span data-stu-id="8a0b6-571">insurance number</span></span>
  
<span data-ttu-id="8a0b6-572">Persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="8a0b6-572">personal identification number</span></span>
  
<span data-ttu-id="8a0b6-573">National Identität</span><span class="sxs-lookup"><span data-stu-id="8a0b6-573">national identity</span></span>
  
<span data-ttu-id="8a0b6-574">Private Identität keine</span><span class="sxs-lookup"><span data-stu-id="8a0b6-574">personal identity no</span></span>
  
<span data-ttu-id="8a0b6-575">Anzahl der eindeutigen Identität</span><span class="sxs-lookup"><span data-stu-id="8a0b6-575">unique identity number</span></span>
  
<span data-ttu-id="8a0b6-576">Nationalidno #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-576">nationalidno#</span></span>
  
<span data-ttu-id="8a0b6-577">UniqueID-</span><span class="sxs-lookup"><span data-stu-id="8a0b6-577">uniqueid#</span></span>
  
<span data-ttu-id="8a0b6-578">DNI #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-578">dni#</span></span>
  
<span data-ttu-id="8a0b6-579">Nationalid #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-579">nationalid#</span></span>
  
<span data-ttu-id="8a0b6-580">Nie #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-580">nie#</span></span>
  
<span data-ttu-id="8a0b6-581">nie</span><span class="sxs-lookup"><span data-stu-id="8a0b6-581">nie</span></span>
  
<span data-ttu-id="8a0b6-582">Nienúmero #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-582">nienúmero#</span></span>
  
<span data-ttu-id="8a0b6-583">Nie número</span><span class="sxs-lookup"><span data-stu-id="8a0b6-583">nie número</span></span>
  
<span data-ttu-id="8a0b6-584">Documento Nacional de identidad</span><span class="sxs-lookup"><span data-stu-id="8a0b6-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="8a0b6-585">Identidad único</span><span class="sxs-lookup"><span data-stu-id="8a0b6-585">identidad único</span></span>
  
<span data-ttu-id="8a0b6-586">Número Nacional identidad</span><span class="sxs-lookup"><span data-stu-id="8a0b6-586">número nacional identidad</span></span>
  
<span data-ttu-id="8a0b6-587">DNI número</span><span class="sxs-lookup"><span data-stu-id="8a0b6-587">dni número</span></span>
  
<span data-ttu-id="8a0b6-588">Dninúmero #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-588">dninúmero#</span></span>
  
<span data-ttu-id="8a0b6-589">Identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="8a0b6-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="8a0b6-590">Schweden</span><span class="sxs-lookup"><span data-stu-id="8a0b6-590">Sweden</span></span>

<span data-ttu-id="8a0b6-591">Weitere Informationen hierzu finden Sie im Abschnitt "Schwedische Ausweisnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8a0b6-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8a0b6-592">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a0b6-592">See also</span></span>

[<span data-ttu-id="8a0b6-593">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="8a0b6-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

