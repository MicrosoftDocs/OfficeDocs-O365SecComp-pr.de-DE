---
title: EU-nationale Identifikationsnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine DLP-Richtlinie (Data Loss Prevention) sucht, wenn der vertrauliche Informationstyp "EU-nationale Identifikationsnummer" erkannt wird. Dieser Typ vertraulicher Informationen definiert unterschiedliche Muster, Stichwörter und andere Beweise für jedes Land.
ms.openlocfilehash: 205019d040648f0600f3dbf4403063edf9f31c41
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154458"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="59a99-104">EU-nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-104">EU National Identification Number</span></span>

<span data-ttu-id="59a99-105">In diesem Thema wird gezeigt, was eine DLP-Richtlinie (Data Loss Prevention) sucht, wenn der vertrauliche Informationstyp "EU-nationale Identifikationsnummer" erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="59a99-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type.</span></span> <span data-ttu-id="59a99-106">Dieser Typ vertraulicher Informationen definiert unterschiedliche Muster, Stichwörter und andere Beweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="59a99-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="59a99-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="59a99-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="59a99-108">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-108">Format</span></span>

<span data-ttu-id="59a99-109">Eine Kombination aus Buchstaben, Ziffern und Sonderzeichen mit einer 24 Zeichen Länge</span><span class="sxs-lookup"><span data-stu-id="59a99-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-110">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-110">Pattern</span></span>

<span data-ttu-id="59a99-111">24 Zeichen:</span><span class="sxs-lookup"><span data-stu-id="59a99-111">24 characters:</span></span>
  
-  <span data-ttu-id="59a99-112">22 Buchstaben (Unterscheidung nach Groß-/Kleinschreibung), Ziffern, umgekehrte Schrägstriche oder Pluszeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="59a99-113">Zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet), Ziffern, Backslashes, Schrägstriche, Pluszeichen oder gleich Zeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-114">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-114">Checksum</span></span>

<span data-ttu-id="59a99-115">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="59a99-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-116">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-116">Definition</span></span>

<span data-ttu-id="59a99-117">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-118">Der reguläre Ausdruck `Regex_austria_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-119">Ein Schlüsselwort `Keywords_austria_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="59a99-120">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="59a99-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="59a99-122">Österreichische Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-122">austrian identity number</span></span>
  
<span data-ttu-id="59a99-123">nationale Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-123">national identity number</span></span>
  
<span data-ttu-id="59a99-124">Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-124">identity number</span></span>
  
<span data-ttu-id="59a99-125">national id</span><span class="sxs-lookup"><span data-stu-id="59a99-125">national id</span></span>
  
<span data-ttu-id="59a99-126">Personalausweis Republik Österreich</span><span class="sxs-lookup"><span data-stu-id="59a99-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="59a99-127">Belgien</span><span class="sxs-lookup"><span data-stu-id="59a99-127">Belgium</span></span>

<span data-ttu-id="59a99-128">Ausführliche Informationen finden Sie im Abschnitt "belgische nationale Nummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="59a99-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="59a99-129">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="59a99-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="59a99-130">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-130">Format</span></span>

<span data-ttu-id="59a99-131">Zehn Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-132">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-132">Pattern</span></span>

<span data-ttu-id="59a99-133">Zehn Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="59a99-134">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="59a99-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="59a99-135">Zwei Ziffern, die der Geburts Reihenfolge entsprechen</span><span class="sxs-lookup"><span data-stu-id="59a99-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="59a99-136">Eine Ziffer, die dem Geschlecht entspricht: eine gerade Ziffer für "männlich" und eine ungerade Ziffer für "weiblich".</span><span class="sxs-lookup"><span data-stu-id="59a99-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="59a99-137">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="59a99-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-138">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-138">Checksum</span></span>

<span data-ttu-id="59a99-139">Ja</span><span class="sxs-lookup"><span data-stu-id="59a99-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-140">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-140">Definition</span></span>

<span data-ttu-id="59a99-141">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-142">Die- `Func_bulgaria_national_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-143">Ein Schlüsselwort `Keywords_bulgaria_national_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="59a99-144">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-145">Die- `Func_bulgaria_national_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-146">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="59a99-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="59a99-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="59a99-148">EGN</span><span class="sxs-lookup"><span data-stu-id="59a99-148">egn</span></span>
  
<span data-ttu-id="59a99-149">EGN</span><span class="sxs-lookup"><span data-stu-id="59a99-149">egn#</span></span>
  
<span data-ttu-id="59a99-150">Bulgarische Nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-150">bulgarian national number</span></span>
  
<span data-ttu-id="59a99-151">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-151">national number</span></span>
  
<span data-ttu-id="59a99-152">social security number</span><span class="sxs-lookup"><span data-stu-id="59a99-152">social security number</span></span>
  
<span data-ttu-id="59a99-153">nationalnumber#</span><span class="sxs-lookup"><span data-stu-id="59a99-153">nationalnumber#</span></span>
  
<span data-ttu-id="59a99-154">SSN</span><span class="sxs-lookup"><span data-stu-id="59a99-154">ssn#</span></span>
  
<span data-ttu-id="59a99-155">SSN</span><span class="sxs-lookup"><span data-stu-id="59a99-155">ssn</span></span>
  
<span data-ttu-id="59a99-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="59a99-156">nationalnumber</span></span>
  
<span data-ttu-id="59a99-157">BNN</span><span class="sxs-lookup"><span data-stu-id="59a99-157">bnn#</span></span>
  
<span data-ttu-id="59a99-158">BNN</span><span class="sxs-lookup"><span data-stu-id="59a99-158">bnn</span></span>
  
<span data-ttu-id="59a99-159">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-159">personal id number</span></span>
  
<span data-ttu-id="59a99-160">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="59a99-160">personalidnumber#</span></span>
  
<span data-ttu-id="59a99-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="59a99-161">единен граждански номер</span></span>
  
<span data-ttu-id="59a99-162">edinen grazhdanski Nomen</span><span class="sxs-lookup"><span data-stu-id="59a99-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="59a99-163">егн</span><span class="sxs-lookup"><span data-stu-id="59a99-163">егн</span></span>
  
<span data-ttu-id="59a99-164">егн#</span><span class="sxs-lookup"><span data-stu-id="59a99-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="59a99-165">Kroatien</span><span class="sxs-lookup"><span data-stu-id="59a99-165">Croatia</span></span>

<span data-ttu-id="59a99-166">Ausführliche Informationen finden Sie im Abschnitt "kroatische Identitätsnummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="59a99-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="59a99-167">Zypern</span><span class="sxs-lookup"><span data-stu-id="59a99-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="59a99-168">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-168">Format</span></span>

<span data-ttu-id="59a99-169">Zehn Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-170">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-170">Pattern</span></span>

 <span data-ttu-id="59a99-171">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="59a99-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="59a99-172">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-172">Checksum</span></span>

<span data-ttu-id="59a99-173">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="59a99-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-174">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-174">Definition</span></span>

<span data-ttu-id="59a99-175">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-176">Der reguläre Ausdruck `Regex_cyprus_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-177">Ein Schlüsselwort `Keywords_cyprus_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="59a99-178">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="59a99-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="59a99-180">ID-Kartennummer</span><span class="sxs-lookup"><span data-stu-id="59a99-180">id card number</span></span>
  
<span data-ttu-id="59a99-181">national identification number</span><span class="sxs-lookup"><span data-stu-id="59a99-181">national identification number</span></span>
  
<span data-ttu-id="59a99-182">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-182">personal id number</span></span>
  
<span data-ttu-id="59a99-183">Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-183">identity card number</span></span>
  
<span data-ttu-id="59a99-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="59a99-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="59a99-185">Tschechien</span><span class="sxs-lookup"><span data-stu-id="59a99-185">Czech Republic</span></span>

<span data-ttu-id="59a99-186">Ausführliche Informationen finden Sie im Abschnitt "Tschechische Nationale Identitätsnummer" unter [was die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="59a99-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="59a99-187">Dänemark</span><span class="sxs-lookup"><span data-stu-id="59a99-187">Denmark</span></span>

<span data-ttu-id="59a99-188">Ausführliche Informationen finden Sie im Abschnitt "dänische persönliche Identifikationsnummer" unter [was die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="59a99-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="59a99-189">Estland</span><span class="sxs-lookup"><span data-stu-id="59a99-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="59a99-190">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-190">Format</span></span>

<span data-ttu-id="59a99-191">11 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-192">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-192">Pattern</span></span>

<span data-ttu-id="59a99-193">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="59a99-193">11 digits:</span></span>
  
- <span data-ttu-id="59a99-194">Eine Ziffer, die Geschlecht und Jahrhundert der Geburt entspricht (ungerade Zahl männlich, gerade Zahl weiblich; 1-2:19. Jahrhundert; 3-4:20th Century; 5-6:21st Century)</span><span class="sxs-lookup"><span data-stu-id="59a99-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="59a99-195">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="59a99-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="59a99-196">Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am gleichen Datum geboren wurden</span><span class="sxs-lookup"><span data-stu-id="59a99-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="59a99-197">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="59a99-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-198">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-198">Checksum</span></span>

<span data-ttu-id="59a99-199">Ja</span><span class="sxs-lookup"><span data-stu-id="59a99-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-200">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-200">Definition</span></span>

<span data-ttu-id="59a99-201">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-202">Die- `Func_estonia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-203">Ein Schlüsselwort `Keywords_estonia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="59a99-204">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-205">Die- `Func_estonia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-206">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="59a99-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="59a99-208">persönlicher Identifikationscode</span><span class="sxs-lookup"><span data-stu-id="59a99-208">personal identification code</span></span>
  
<span data-ttu-id="59a99-209">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-209">personal identification number</span></span>
  
<span data-ttu-id="59a99-210">national identification number</span><span class="sxs-lookup"><span data-stu-id="59a99-210">national identification number</span></span>
  
<span data-ttu-id="59a99-211">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-211">national number</span></span>
  
<span data-ttu-id="59a99-212">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-212">personal id number</span></span>
  
<span data-ttu-id="59a99-213">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="59a99-213">personalidnumber#</span></span>
  
<span data-ttu-id="59a99-214">IK</span><span class="sxs-lookup"><span data-stu-id="59a99-214">ik</span></span>
  
<span data-ttu-id="59a99-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="59a99-215">isikukood</span></span>
  
<span data-ttu-id="59a99-216">ID-Kaart</span><span class="sxs-lookup"><span data-stu-id="59a99-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="59a99-217">Finnland</span><span class="sxs-lookup"><span data-stu-id="59a99-217">Finland</span></span>

<span data-ttu-id="59a99-218">Ausführliche Informationen finden Sie im Abschnitt "finnische nationale ID" unter [was die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="59a99-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="59a99-219">Frankreich</span><span class="sxs-lookup"><span data-stu-id="59a99-219">France</span></span>

<span data-ttu-id="59a99-220">Ausführliche Informationen finden Sie im Abschnitt "France National ID Card (CNI)" in [What the sensitive Information Types Look for](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="59a99-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="59a99-221">Deutschland</span><span class="sxs-lookup"><span data-stu-id="59a99-221">Germany</span></span>

<span data-ttu-id="59a99-222">Ausführliche Informationen finden Sie im Abschnitt "Deutsche Identitätskartennummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="59a99-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="59a99-223">Griechenland</span><span class="sxs-lookup"><span data-stu-id="59a99-223">Greece</span></span>

<span data-ttu-id="59a99-224">Ausführliche Informationen finden Sie im Abschnitt "Griechenland-National Ausweis" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="59a99-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="59a99-225">Ungarn</span><span class="sxs-lookup"><span data-stu-id="59a99-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="59a99-226">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-226">Format</span></span>

<span data-ttu-id="59a99-227">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="59a99-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-228">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-228">Pattern</span></span>

<span data-ttu-id="59a99-229">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="59a99-229">11 digits:</span></span>
  
-  <span data-ttu-id="59a99-230">Eine Ziffer, die dem Geschlecht entspricht (1-männlich, 2-weiblich, andere Zahlen sind auch für Bürger möglich, die vor 1900 oder Bürgern mit doppelter Staatsbürgerschaft geboren wurden)</span><span class="sxs-lookup"><span data-stu-id="59a99-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="59a99-231">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="59a99-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="59a99-232">Drei Ziffern, die einer Seriennummer entsprechen</span><span class="sxs-lookup"><span data-stu-id="59a99-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="59a99-233">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="59a99-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-234">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-234">Checksum</span></span>

<span data-ttu-id="59a99-235">Ja</span><span class="sxs-lookup"><span data-stu-id="59a99-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-236">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-236">Definition</span></span>

<span data-ttu-id="59a99-237">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-238">Die- `Func_hungary_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-239">Ein Schlüsselwort `Keywords_hungary_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="59a99-240">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-241">Die- `Func_hungary_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-242">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="59a99-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="59a99-244">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-244">personal identification number</span></span>
  
<span data-ttu-id="59a99-245">identification number</span><span class="sxs-lookup"><span data-stu-id="59a99-245">identification number</span></span>
  
<span data-ttu-id="59a99-246">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-246">personal id number</span></span>
  
<span data-ttu-id="59a99-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="59a99-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="59a99-248">Irland</span><span class="sxs-lookup"><span data-stu-id="59a99-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="59a99-249">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-249">Format</span></span>

<span data-ttu-id="59a99-250">Eine neunstellige Kombination aus Buchstaben, Ziffern und einem Leerzeichen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-251">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-251">Pattern</span></span>

<span data-ttu-id="59a99-252">Eine neunstellige Kombination aus Buchstaben, Ziffern und einem Leerzeichen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="59a99-253">Vom 01 Januar 2013 bis jetzt:</span><span class="sxs-lookup"><span data-stu-id="59a99-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="59a99-254">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="59a99-254">Seven digits</span></span> 
    
- <span data-ttu-id="59a99-255">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="59a99-255">One check digit</span></span>
    
- <span data-ttu-id="59a99-256">Ein Leerzeichen oder der Großbuchstabe "W" (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="59a99-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="59a99-257">Vor dem 01. Januar 2013:</span><span class="sxs-lookup"><span data-stu-id="59a99-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="59a99-258">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="59a99-258">Seven digits</span></span> 
    
- <span data-ttu-id="59a99-259">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="59a99-259">One check digit</span></span>
    
- <span data-ttu-id="59a99-260">Ein Leerzeichen oder ein Großbuchstabe (Groß-/Kleinschreibung beachten)</span><span class="sxs-lookup"><span data-stu-id="59a99-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-261">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-261">Checksum</span></span>

<span data-ttu-id="59a99-262">Ja</span><span class="sxs-lookup"><span data-stu-id="59a99-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-263">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-263">Definition</span></span>

<span data-ttu-id="59a99-264">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-265">Die-Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="59a99-266">Ein Schlüsselwort aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-266">A keyword from is found.</span></span>
    
<span data-ttu-id="59a99-267">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-268">Die-Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-269">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="59a99-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="59a99-271">persönliche öffentliche Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-271">personal public service number</span></span>
  
<span data-ttu-id="59a99-272">PPS Nein</span><span class="sxs-lookup"><span data-stu-id="59a99-272">pps no</span></span>
  
<span data-ttu-id="59a99-273">Umsatz-und Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="59a99-274">RSI-Nr.</span><span class="sxs-lookup"><span data-stu-id="59a99-274">rsi no</span></span>
  
<span data-ttu-id="59a99-275">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-275">personal identification number</span></span>
  
<span data-ttu-id="59a99-276">identification number</span><span class="sxs-lookup"><span data-stu-id="59a99-276">identification number</span></span>
  
<span data-ttu-id="59a99-277">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-277">personal id number</span></span>
  
<span data-ttu-id="59a99-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="59a99-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="59a99-279">uimh.</span><span class="sxs-lookup"><span data-stu-id="59a99-279">uimh.</span></span> <span data-ttu-id="59a99-280">PSP</span><span class="sxs-lookup"><span data-stu-id="59a99-280">psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="59a99-281">Italien</span><span class="sxs-lookup"><span data-stu-id="59a99-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="59a99-282">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-282">Format</span></span>

<span data-ttu-id="59a99-283">Eine Kombination aus Buchstaben und Ziffern aus 16 Zeichen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-284">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-284">Pattern</span></span>

<span data-ttu-id="59a99-285">Eine Kombination aus Buchstaben und Ziffern aus 16 Zeichen:</span><span class="sxs-lookup"><span data-stu-id="59a99-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="59a99-286">Drei Buchstaben, die den ersten drei Konsonanten im Familiennamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="59a99-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="59a99-287">Drei Buchstaben, die den ersten, dritten und vierten Konsonanten im Vornamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="59a99-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="59a99-288">Zwei Ziffern, die den letzten Ziffern des Geburtsjahres entsprechen</span><span class="sxs-lookup"><span data-stu-id="59a99-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="59a99-289">Ein Buchstabe, der dem Brief für den Monat der Geburt entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben a bis E, H, L, M, P, R bis T werden verwendet (der Januar ist also a und Oktober ist r).</span><span class="sxs-lookup"><span data-stu-id="59a99-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="59a99-290">Zwei Ziffern, die dem Tag des Geburtsmonats entsprechen – um zwischen den Geschlechtern zu unterscheiden, wird 40 am Tag der Geburt für Frauen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="59a99-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="59a99-291">Vier Ziffern, die der Ortskennzahl für die Gemeinde entsprechen, in der die Person geboren wurde (landesweite Codes werden für fremde Länder verwendet)</span><span class="sxs-lookup"><span data-stu-id="59a99-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="59a99-292">Eine Paritäts Ziffer</span><span class="sxs-lookup"><span data-stu-id="59a99-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-293">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-293">Checksum</span></span>

<span data-ttu-id="59a99-294">Ja</span><span class="sxs-lookup"><span data-stu-id="59a99-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-295">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-295">Definition</span></span>

<span data-ttu-id="59a99-296">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-297">Die- `Func_italy_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-298">Ein Schlüsselwort `Keywords_italy_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="59a99-299">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-300">Die- `Func_italy_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-301">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="59a99-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="59a99-303">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="59a99-303">personal code</span></span>
  
<span data-ttu-id="59a99-304">persönliche Codenummer</span><span class="sxs-lookup"><span data-stu-id="59a99-304">personal code number</span></span>
  
<span data-ttu-id="59a99-305">persönliche Zertifikat Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-305">personal certificate number</span></span>
  
<span data-ttu-id="59a99-306">Geschäftscode</span><span class="sxs-lookup"><span data-stu-id="59a99-306">fiscal code</span></span>
  
<span data-ttu-id="59a99-307">personalcodeno#</span><span class="sxs-lookup"><span data-stu-id="59a99-307">personalcodeno#</span></span>
  
<span data-ttu-id="59a99-308">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-308">personal id number</span></span>
  
<span data-ttu-id="59a99-309">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="59a99-309">personal id code</span></span>
  
<span data-ttu-id="59a99-310">Dice personale</span><span class="sxs-lookup"><span data-stu-id="59a99-310">codice personale</span></span>
  
<span data-ttu-id="59a99-311">Numero Bescheinigung personale</span><span class="sxs-lookup"><span data-stu-id="59a99-311">numero certificato personale</span></span>
  
<span data-ttu-id="59a99-312">Numero personale</span><span class="sxs-lookup"><span data-stu-id="59a99-312">numero personale</span></span>
  
<span data-ttu-id="59a99-313">Numero-ID personale</span><span class="sxs-lookup"><span data-stu-id="59a99-313">numero id personale</span></span>
  
<span data-ttu-id="59a99-314">Dice ID personale</span><span class="sxs-lookup"><span data-stu-id="59a99-314">codice id personale</span></span>
  
<span data-ttu-id="59a99-315">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="59a99-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="59a99-316">Italien</span><span class="sxs-lookup"><span data-stu-id="59a99-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="59a99-317">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-317">Format</span></span>

<span data-ttu-id="59a99-318">11 Ziffern und ein Bindestrich im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="59a99-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-319">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-319">Pattern</span></span>

<span data-ttu-id="59a99-320">11 Ziffern und Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="59a99-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="59a99-321">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="59a99-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="59a99-322">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="59a99-322">A hyphen</span></span>
    
- <span data-ttu-id="59a99-323">Eine Ziffer, die dem Jahrhundert der Geburt entspricht ("0" für das 19. Jahrhundert, "1" für das 20. Jahrhundert und "2" für das 21. Jahrhundert)</span><span class="sxs-lookup"><span data-stu-id="59a99-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="59a99-324">Vier Ziffern, nach dem Zufallsprinzip generiert</span><span class="sxs-lookup"><span data-stu-id="59a99-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-325">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-325">Checksum</span></span>

<span data-ttu-id="59a99-326">Ja</span><span class="sxs-lookup"><span data-stu-id="59a99-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-327">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-327">Definition</span></span>

<span data-ttu-id="59a99-328">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-329">Die- `Func_latvia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-330">Ein Schlüsselwort `Keywords_latvia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="59a99-331">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-332">Die- `Func_latvia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-333">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="59a99-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="59a99-335">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="59a99-335">personal code</span></span>
  
<span data-ttu-id="59a99-336">persönliche Codenummer</span><span class="sxs-lookup"><span data-stu-id="59a99-336">personal code number</span></span>
  
<span data-ttu-id="59a99-337">persönliche Zertifikat Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-337">personal certificate number</span></span>
  
<span data-ttu-id="59a99-338">personalcodeno#</span><span class="sxs-lookup"><span data-stu-id="59a99-338">personalcodeno#</span></span>
  
<span data-ttu-id="59a99-339">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-339">personal id number</span></span>
  
<span data-ttu-id="59a99-340">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="59a99-340">personal id code</span></span>
  
<span data-ttu-id="59a99-341">Personas KODS</span><span class="sxs-lookup"><span data-stu-id="59a99-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="59a99-342">Litauen</span><span class="sxs-lookup"><span data-stu-id="59a99-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="59a99-343">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-343">Format</span></span>

<span data-ttu-id="59a99-344">11 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-345">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-345">Pattern</span></span>

<span data-ttu-id="59a99-346">11 Ziffern ohne Leerzeichen und Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="59a99-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="59a99-347">Eine Ziffer, die dem Geschlecht der Person und dem Jahrhundert der Geburt entspricht</span><span class="sxs-lookup"><span data-stu-id="59a99-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="59a99-348">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="59a99-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="59a99-349">Drei Ziffern, die der Seriennummer des Geburtsdatums entsprechen</span><span class="sxs-lookup"><span data-stu-id="59a99-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="59a99-350">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="59a99-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-351">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-351">Checksum</span></span>

<span data-ttu-id="59a99-352">Ja</span><span class="sxs-lookup"><span data-stu-id="59a99-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-353">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-353">Definition</span></span>

<span data-ttu-id="59a99-354">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-355">Die- `Func_lithuania_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-356">Ein Schlüsselwort `Keywords_lithuania_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="59a99-357">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-358">Die- `Func_lithuania_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-359">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="59a99-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="59a99-361">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="59a99-361">personal numeric code</span></span>
  
<span data-ttu-id="59a99-362">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-362">unique identification number</span></span>
  
<span data-ttu-id="59a99-363">Bürgerdienst Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-363">citizen service number</span></span>
  
<span data-ttu-id="59a99-364">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-364">unique identity number</span></span>
  
<span data-ttu-id="59a99-365">uniqueidentityno#</span><span class="sxs-lookup"><span data-stu-id="59a99-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="59a99-366">persönlicher Code.</span><span class="sxs-lookup"><span data-stu-id="59a99-366">personal code.</span></span>
  
<span data-ttu-id="59a99-367">asmeninis skaitmeninis KODAS</span><span class="sxs-lookup"><span data-stu-id="59a99-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="59a99-368">unikalus identifikavimo Numeris</span><span class="sxs-lookup"><span data-stu-id="59a99-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="59a99-369">piliečio paslaugos Numeris</span><span class="sxs-lookup"><span data-stu-id="59a99-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="59a99-370">unikalus identifikavimo KODAS</span><span class="sxs-lookup"><span data-stu-id="59a99-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="59a99-371">Mens KODAS.</span><span class="sxs-lookup"><span data-stu-id="59a99-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="59a99-372">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="59a99-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="59a99-373">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-373">Format</span></span>

<span data-ttu-id="59a99-374">11 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-375">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-375">Pattern</span></span>

<span data-ttu-id="59a99-376">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="59a99-376">11 digits</span></span>
  
- <span data-ttu-id="59a99-377">Eine Ziffer, die dem Geschlecht der Person und dem Jahrhundert der Geburt entspricht</span><span class="sxs-lookup"><span data-stu-id="59a99-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="59a99-378">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="59a99-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="59a99-379">Drei Ziffern, die der Seriennummer des Geburtsdatums entsprechen</span><span class="sxs-lookup"><span data-stu-id="59a99-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="59a99-380">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="59a99-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-381">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-381">Checksum</span></span>

<span data-ttu-id="59a99-382">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="59a99-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-383">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-383">Definition</span></span>

<span data-ttu-id="59a99-384">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-385">Der reguläre Ausdruck `Regex_luxemburg_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-386">Ein Schlüsselwort `Keywords_luxemburg_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="59a99-387">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="59a99-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="59a99-389">persönliche ID</span><span class="sxs-lookup"><span data-stu-id="59a99-389">personal id</span></span>
  
<span data-ttu-id="59a99-390">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-390">personal id number</span></span>
  
<span data-ttu-id="59a99-391">personalidno#</span><span class="sxs-lookup"><span data-stu-id="59a99-391">personalidno#</span></span>
  
<span data-ttu-id="59a99-392">eindeutige ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-392">unique id number</span></span>
  
<span data-ttu-id="59a99-393">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="59a99-393">personalidnumber#</span></span>
  
<span data-ttu-id="59a99-394">eindeutiger ID-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="59a99-394">unique id key</span></span>
  
<span data-ttu-id="59a99-395">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="59a99-395">personal id code</span></span>
  
<span data-ttu-id="59a99-396">uniqueidkey#</span><span class="sxs-lookup"><span data-stu-id="59a99-396">uniqueidkey#</span></span>
  
<span data-ttu-id="59a99-397">einzelner Code</span><span class="sxs-lookup"><span data-stu-id="59a99-397">individual code</span></span>
  
<span data-ttu-id="59a99-398">individuelle ID</span><span class="sxs-lookup"><span data-stu-id="59a99-398">individual id</span></span>
  
<span data-ttu-id="59a99-399">eindeutige-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="59a99-400">eindeutige-ID</span><span class="sxs-lookup"><span data-stu-id="59a99-400">eindeutige id</span></span>
  
<span data-ttu-id="59a99-401">ID personnelle</span><span class="sxs-lookup"><span data-stu-id="59a99-401">id personnelle</span></span>
  
<span data-ttu-id="59a99-402">Numéro-d'identification-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="59a99-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="59a99-403">idpersonnelle#</span><span class="sxs-lookup"><span data-stu-id="59a99-403">idpersonnelle#</span></span>
  
<span data-ttu-id="59a99-404">persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="59a99-405">eindeutigeid#</span><span class="sxs-lookup"><span data-stu-id="59a99-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="59a99-406">Malta</span><span class="sxs-lookup"><span data-stu-id="59a99-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="59a99-407">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-407">Format</span></span>

<span data-ttu-id="59a99-408">Sieben Ziffern, gefolgt von einem Buchstaben</span><span class="sxs-lookup"><span data-stu-id="59a99-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-409">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-409">Pattern</span></span>

<span data-ttu-id="59a99-410">Sieben Ziffern, gefolgt von einem Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="59a99-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="59a99-411">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="59a99-411">Seven digits</span></span> 
    
- <span data-ttu-id="59a99-412">Ein Großbuchstabe (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="59a99-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-413">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-413">Checksum</span></span>

<span data-ttu-id="59a99-414">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="59a99-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-415">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-415">Definition</span></span>

<span data-ttu-id="59a99-416">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-417">Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-418">Ein Schlüsselwort `Keywords_malta_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="59a99-419">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-420">Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-421">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="59a99-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="59a99-423">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="59a99-423">personal numeric code</span></span>
  
<span data-ttu-id="59a99-424">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-424">unique identification number</span></span>
  
<span data-ttu-id="59a99-425">Bürgerdienst Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-425">citizen service number</span></span>
  
<span data-ttu-id="59a99-426">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-426">unique identity number</span></span>
  
<span data-ttu-id="59a99-427">uniqueidentityno#</span><span class="sxs-lookup"><span data-stu-id="59a99-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="59a99-428">Kodiċi Numeri personali</span><span class="sxs-lookup"><span data-stu-id="59a99-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="59a99-429">numru ta ' identifikazzjoni uniku</span><span class="sxs-lookup"><span data-stu-id="59a99-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="59a99-430">numru TAS-servizz taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="59a99-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="59a99-431">numru ta ' identità uniku</span><span class="sxs-lookup"><span data-stu-id="59a99-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="59a99-432">Niederlande</span><span class="sxs-lookup"><span data-stu-id="59a99-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="59a99-433">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-433">Format</span></span>

<span data-ttu-id="59a99-434">Neun Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-435">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-435">Pattern</span></span>

<span data-ttu-id="59a99-436">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="59a99-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="59a99-437">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-437">Checksum</span></span>

<span data-ttu-id="59a99-438">Ja</span><span class="sxs-lookup"><span data-stu-id="59a99-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-439">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-439">Definition</span></span>

<span data-ttu-id="59a99-440">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-441">Die- `Func_netherlands_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-442">Ein Schlüsselwort aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-442">A keyword from is found.</span></span>
    
<span data-ttu-id="59a99-443">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-444">Die- `Func_netherlands_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-445">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="59a99-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="59a99-447">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="59a99-447">personal numeric code</span></span>
  
<span data-ttu-id="59a99-448">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-448">unique identification number</span></span>
  
<span data-ttu-id="59a99-449">Bürgerdienst Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-449">citizen service number</span></span>
  
<span data-ttu-id="59a99-450">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-450">unique identity number</span></span>
  
<span data-ttu-id="59a99-451">uniqueidentityno#</span><span class="sxs-lookup"><span data-stu-id="59a99-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="59a99-452">BSN</span><span class="sxs-lookup"><span data-stu-id="59a99-452">bsn</span></span>
  
<span data-ttu-id="59a99-453">BSN</span><span class="sxs-lookup"><span data-stu-id="59a99-453">bsn#</span></span>
  
<span data-ttu-id="59a99-454">Persoonlijke-numerieke-Code</span><span class="sxs-lookup"><span data-stu-id="59a99-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="59a99-455">uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="59a99-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="59a99-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="59a99-456">burgerservicenummer</span></span>
  
<span data-ttu-id="59a99-457">uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="59a99-458">Polen</span><span class="sxs-lookup"><span data-stu-id="59a99-458">Poland</span></span>

<span data-ttu-id="59a99-459">Ausführliche Informationen finden Sie im Abschnitt "Poland National ID (PESEL)" in [What the sensitive Information Types Look for](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="59a99-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="59a99-460">Portugal</span><span class="sxs-lookup"><span data-stu-id="59a99-460">Portugal</span></span>

<span data-ttu-id="59a99-461">Ausführliche Informationen finden Sie im Abschnitt "Portugal-Bürgerkarten Nummer" unter [was die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="59a99-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="59a99-462">Rumänien</span><span class="sxs-lookup"><span data-stu-id="59a99-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="59a99-463">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-463">Format</span></span>

<span data-ttu-id="59a99-464">13 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-465">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-465">Pattern</span></span>

<span data-ttu-id="59a99-466">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="59a99-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="59a99-467">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-467">Checksum</span></span>

<span data-ttu-id="59a99-468">Ja</span><span class="sxs-lookup"><span data-stu-id="59a99-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-469">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-469">Definition</span></span>

<span data-ttu-id="59a99-470">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-471">Die- `Func_romania_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-472">Ein Schlüsselwort `Keywords_romania_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="59a99-473">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-474">Die- `Func_romania_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-475">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="59a99-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="59a99-477">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="59a99-477">personal numeric code</span></span>
  
<span data-ttu-id="59a99-478">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-478">unique identification number</span></span>
  
<span data-ttu-id="59a99-479">CNP</span><span class="sxs-lookup"><span data-stu-id="59a99-479">cnp</span></span>
  
<span data-ttu-id="59a99-480">CNP</span><span class="sxs-lookup"><span data-stu-id="59a99-480">cnp#</span></span>
  
<span data-ttu-id="59a99-481">PIN</span><span class="sxs-lookup"><span data-stu-id="59a99-481">pin</span></span>
  
<span data-ttu-id="59a99-482">PIN</span><span class="sxs-lookup"><span data-stu-id="59a99-482">pin#</span></span>
  
<span data-ttu-id="59a99-483">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-483">insurance number</span></span>
  
<span data-ttu-id="59a99-484">insurancenumber#</span><span class="sxs-lookup"><span data-stu-id="59a99-484">insurancenumber#</span></span>
  
<span data-ttu-id="59a99-485">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-485">unique identity number</span></span>
  
<span data-ttu-id="59a99-486">uniqueidentityno#</span><span class="sxs-lookup"><span data-stu-id="59a99-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="59a99-487">COD numerisch persönlich</span><span class="sxs-lookup"><span data-stu-id="59a99-487">cod numeric personal</span></span>
  
<span data-ttu-id="59a99-488">COD identificare Personal</span><span class="sxs-lookup"><span data-stu-id="59a99-488">cod identificare personal</span></span>
  
<span data-ttu-id="59a99-489">COD Unic identificare</span><span class="sxs-lookup"><span data-stu-id="59a99-489">cod unic identificare</span></span>
  
<span data-ttu-id="59a99-490">număr Personal Unic</span><span class="sxs-lookup"><span data-stu-id="59a99-490">număr personal unic</span></span>
  
<span data-ttu-id="59a99-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="59a99-491">număr identitate</span></span>
  
<span data-ttu-id="59a99-492">număr identificare Personal</span><span class="sxs-lookup"><span data-stu-id="59a99-492">număr identificare personal</span></span>
  
<span data-ttu-id="59a99-493">număridentitate#</span><span class="sxs-lookup"><span data-stu-id="59a99-493">număridentitate#</span></span>
  
<span data-ttu-id="59a99-494">codnumericpersonal#</span><span class="sxs-lookup"><span data-stu-id="59a99-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="59a99-495">numărpersonalunic#</span><span class="sxs-lookup"><span data-stu-id="59a99-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="59a99-496">Slowakei</span><span class="sxs-lookup"><span data-stu-id="59a99-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="59a99-497">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-497">Format</span></span>

<span data-ttu-id="59a99-498">Zehn Ziffern mit einem Backslash</span><span class="sxs-lookup"><span data-stu-id="59a99-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-499">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-499">Pattern</span></span>

<span data-ttu-id="59a99-500">Zehn Ziffern mit einem Backslash:</span><span class="sxs-lookup"><span data-stu-id="59a99-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="59a99-501">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-501">Checksum</span></span>

<span data-ttu-id="59a99-502">Ja</span><span class="sxs-lookup"><span data-stu-id="59a99-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-503">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-503">Definition</span></span>

<span data-ttu-id="59a99-504">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-505">Die- `Func_slovakia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-506">Ein Schlüsselwort `Keywords_slovakia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="59a99-507">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-508">Die- `Func_slovakia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-509">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="59a99-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="59a99-511">Geburtsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-511">birth number</span></span>
  
<span data-ttu-id="59a99-512">national identification number</span><span class="sxs-lookup"><span data-stu-id="59a99-512">national identification number</span></span>
  
<span data-ttu-id="59a99-513">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-513">personal identification number</span></span>
  
<span data-ttu-id="59a99-514">social security number</span><span class="sxs-lookup"><span data-stu-id="59a99-514">social security number</span></span>
  
<span data-ttu-id="59a99-515">nationalnumber#</span><span class="sxs-lookup"><span data-stu-id="59a99-515">nationalnumber#</span></span>
  
<span data-ttu-id="59a99-516">SSN</span><span class="sxs-lookup"><span data-stu-id="59a99-516">ssn#</span></span>
  
<span data-ttu-id="59a99-517">SSN</span><span class="sxs-lookup"><span data-stu-id="59a99-517">ssn</span></span>
  
<span data-ttu-id="59a99-518">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-518">national number</span></span>
  
<span data-ttu-id="59a99-519">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="59a99-519">personal id number</span></span>
  
<span data-ttu-id="59a99-520">personalidnumber#</span><span class="sxs-lookup"><span data-stu-id="59a99-520">personalidnumber#</span></span>
  
<span data-ttu-id="59a99-521">rč</span><span class="sxs-lookup"><span data-stu-id="59a99-521">rč</span></span>
  
<span data-ttu-id="59a99-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="59a99-522">rodné číslo</span></span>
  
<span data-ttu-id="59a99-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="59a99-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="59a99-524">Slowenien</span><span class="sxs-lookup"><span data-stu-id="59a99-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="59a99-525">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-525">Format</span></span>

<span data-ttu-id="59a99-526">13 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-527">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-527">Pattern</span></span>

<span data-ttu-id="59a99-528">13 Ziffern im angegebenen Muster:</span><span class="sxs-lookup"><span data-stu-id="59a99-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="59a99-529">Sieben Ziffern, die dem Geburtsdatum (DDMMLLL) entsprechen, wobei "LLL" den letzten drei Ziffern des Geburtsjahres entspricht.</span><span class="sxs-lookup"><span data-stu-id="59a99-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="59a99-530">Zwei Ziffern, die dem Geburts Bereich entsprechen</span><span class="sxs-lookup"><span data-stu-id="59a99-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="59a99-531">Drei Ziffern, die einer Kombination aus Geschlecht und Seriennummer für Personen entsprechen, die am selben Tag geboren wurden (000-499 für männliche und 500-999 für weiblich)</span><span class="sxs-lookup"><span data-stu-id="59a99-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="59a99-532">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="59a99-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-533">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-533">Checksum</span></span>

<span data-ttu-id="59a99-534">Ja</span><span class="sxs-lookup"><span data-stu-id="59a99-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-535">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-535">Definition</span></span>

<span data-ttu-id="59a99-536">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-537">Die- `Func_slovenia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-538">Ein Schlüsselwort `Keywords_slovenia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="59a99-539">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-540">Die- `Func_slovenia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="59a99-541">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="59a99-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="59a99-543">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="59a99-543">personal numeric code</span></span>
  
<span data-ttu-id="59a99-544">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-544">unique identification number</span></span>
  
<span data-ttu-id="59a99-545">eindeutige Registrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-545">unique registration number</span></span>
  
<span data-ttu-id="59a99-546">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-546">unique identity number</span></span>
  
<span data-ttu-id="59a99-547">uniqueidentityno#</span><span class="sxs-lookup"><span data-stu-id="59a99-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="59a99-548">eindeutige Master Bürgerzahl</span><span class="sxs-lookup"><span data-stu-id="59a99-548">unique master citizen number</span></span>
  
<span data-ttu-id="59a99-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="59a99-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="59a99-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="59a99-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="59a99-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="59a99-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="59a99-552">EMŠO</span><span class="sxs-lookup"><span data-stu-id="59a99-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="59a99-553">Spanien</span><span class="sxs-lookup"><span data-stu-id="59a99-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="59a99-554">Format</span><span class="sxs-lookup"><span data-stu-id="59a99-554">Format</span></span>

<span data-ttu-id="59a99-555">Sieben Ziffern, gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="59a99-556">Muster</span><span class="sxs-lookup"><span data-stu-id="59a99-556">Pattern</span></span>

<span data-ttu-id="59a99-557">Sieben Ziffern, gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="59a99-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="59a99-558">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="59a99-558">Seven digits</span></span>
    
- <span data-ttu-id="59a99-559">Eine Ziffer oder ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="59a99-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="59a99-560">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="59a99-560">Checksum</span></span>

<span data-ttu-id="59a99-561">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="59a99-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="59a99-562">Definition</span><span class="sxs-lookup"><span data-stu-id="59a99-562">Definition</span></span>

<span data-ttu-id="59a99-563">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="59a99-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="59a99-564">Der reguläre Ausdruck `Regex_spain_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="59a99-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="59a99-565">Ein Schlüsselwort `Keywords_spain_eu_national_id_card"` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="59a99-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="59a99-566">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="59a99-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="59a99-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="59a99-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="59a99-568">DNI</span><span class="sxs-lookup"><span data-stu-id="59a99-568">dni</span></span>
  
<span data-ttu-id="59a99-569">national identification number</span><span class="sxs-lookup"><span data-stu-id="59a99-569">national identification number</span></span>
  
<span data-ttu-id="59a99-570">nationale Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-570">national identity number</span></span>
  
<span data-ttu-id="59a99-571">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-571">insurance number</span></span>
  
<span data-ttu-id="59a99-572">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-572">personal identification number</span></span>
  
<span data-ttu-id="59a99-573">nationale Identität</span><span class="sxs-lookup"><span data-stu-id="59a99-573">national identity</span></span>
  
<span data-ttu-id="59a99-574">persönliche Identität Nein</span><span class="sxs-lookup"><span data-stu-id="59a99-574">personal identity no</span></span>
  
<span data-ttu-id="59a99-575">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="59a99-575">unique identity number</span></span>
  
<span data-ttu-id="59a99-576">nationalidno#</span><span class="sxs-lookup"><span data-stu-id="59a99-576">nationalidno#</span></span>
  
<span data-ttu-id="59a99-577">UniqueId</span><span class="sxs-lookup"><span data-stu-id="59a99-577">uniqueid#</span></span>
  
<span data-ttu-id="59a99-578">DNI</span><span class="sxs-lookup"><span data-stu-id="59a99-578">dni#</span></span>
  
<span data-ttu-id="59a99-579">National-Nr.</span><span class="sxs-lookup"><span data-stu-id="59a99-579">nationalid#</span></span>
  
<span data-ttu-id="59a99-580">nie</span><span class="sxs-lookup"><span data-stu-id="59a99-580">nie#</span></span>
  
<span data-ttu-id="59a99-581">nie</span><span class="sxs-lookup"><span data-stu-id="59a99-581">nie</span></span>
  
<span data-ttu-id="59a99-582">nienúmero#</span><span class="sxs-lookup"><span data-stu-id="59a99-582">nienúmero#</span></span>
  
<span data-ttu-id="59a99-583">nie número</span><span class="sxs-lookup"><span data-stu-id="59a99-583">nie número</span></span>
  
<span data-ttu-id="59a99-584">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="59a99-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="59a99-585">Identidad Único</span><span class="sxs-lookup"><span data-stu-id="59a99-585">identidad único</span></span>
  
<span data-ttu-id="59a99-586">número Nacional Identidad</span><span class="sxs-lookup"><span data-stu-id="59a99-586">número nacional identidad</span></span>
  
<span data-ttu-id="59a99-587">DNI número</span><span class="sxs-lookup"><span data-stu-id="59a99-587">dni número</span></span>
  
<span data-ttu-id="59a99-588">dninúmero#</span><span class="sxs-lookup"><span data-stu-id="59a99-588">dninúmero#</span></span>
  
<span data-ttu-id="59a99-589">identidadúnico#</span><span class="sxs-lookup"><span data-stu-id="59a99-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="59a99-590">Schweden</span><span class="sxs-lookup"><span data-stu-id="59a99-590">Sweden</span></span>

<span data-ttu-id="59a99-591">Ausführliche Informationen finden Sie im Abschnitt "Sweden National ID" unter [What the sensitive Information Types Look](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="59a99-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="59a99-592">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59a99-592">See also</span></span>

[<span data-ttu-id="59a99-593">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="59a99-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

