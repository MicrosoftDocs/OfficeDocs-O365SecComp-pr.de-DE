---
title: EU-nationale Identifikationsnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine DLP-Richtlinie (Data Loss Prevention) sucht, wenn der vertrauliche Informationstyp "EU-nationale Identifikationsnummer" erkannt wird. Dieser Typ vertraulicher Informationen definiert unterschiedliche Muster, Stichwörter und andere Beweise für jedes Land.
ms.openlocfilehash: b784b7509eed899f9f03db96ee5e827b9bf70d2e
ms.sourcegitcommit: ff370e93b792204547694139ef99bc0848304570
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/11/2019
ms.locfileid: "36852747"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="9b48b-104">EU-nationale Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-104">EU National Identification Number</span></span>

<span data-ttu-id="9b48b-105">In diesem Thema wird gezeigt, was eine DLP-Richtlinie (Data Loss Prevention) sucht, wenn der vertrauliche Informationstyp "EU-nationale Identifikationsnummer" erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="9b48b-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type.</span></span> <span data-ttu-id="9b48b-106">Dieser Typ vertraulicher Informationen definiert unterschiedliche Muster, Stichwörter und andere Beweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="9b48b-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="9b48b-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="9b48b-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-108">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-108">Format</span></span>

<span data-ttu-id="9b48b-109">Eine Kombination aus Buchstaben, Ziffern und Sonderzeichen mit einer 24 Zeichen Länge</span><span class="sxs-lookup"><span data-stu-id="9b48b-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-110">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-110">Pattern</span></span>

<span data-ttu-id="9b48b-111">24 Zeichen:</span><span class="sxs-lookup"><span data-stu-id="9b48b-111">24 characters:</span></span>
  
-  <span data-ttu-id="9b48b-112">22 Buchstaben (Unterscheidung nach Groß-/Kleinschreibung), Ziffern, umgekehrte Schrägstriche oder Pluszeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="9b48b-113">Zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet), Ziffern, Backslashes, Schrägstriche, Pluszeichen oder gleich Zeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-114">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-114">Checksum</span></span>

<span data-ttu-id="9b48b-115">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9b48b-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-116">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-116">Definition</span></span>

<span data-ttu-id="9b48b-117">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-118">Der reguläre Ausdruck `Regex_austria_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-119">Ein Schlüsselwort `Keywords_austria_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b48b-120">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-120">Keywords</span></span>

#### <a name="keywords_austria_eu_national_id_card"></a><span data-ttu-id="9b48b-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-122">Österreichische Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-122">austrian identity number</span></span>
  
<span data-ttu-id="9b48b-123">nationale Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-123">national identity number</span></span>
  
<span data-ttu-id="9b48b-124">Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-124">identity number</span></span>
  
<span data-ttu-id="9b48b-125">national id</span><span class="sxs-lookup"><span data-stu-id="9b48b-125">national id</span></span>
  
<span data-ttu-id="9b48b-126">Personalausweis Republik Österreich</span><span class="sxs-lookup"><span data-stu-id="9b48b-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="9b48b-127">Belgien</span><span class="sxs-lookup"><span data-stu-id="9b48b-127">Belgium</span></span>

<span data-ttu-id="9b48b-128">Ausführliche Informationen finden Sie im Abschnitt "belgische nationale Nummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9b48b-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="9b48b-129">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="9b48b-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-130">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-130">Format</span></span>

<span data-ttu-id="9b48b-131">Zehn Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-132">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-132">Pattern</span></span>

<span data-ttu-id="9b48b-133">Zehn Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="9b48b-134">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="9b48b-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="9b48b-135">Zwei Ziffern, die der Geburts Reihenfolge entsprechen</span><span class="sxs-lookup"><span data-stu-id="9b48b-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="9b48b-136">Eine Ziffer, die dem Geschlecht entspricht: eine gerade Ziffer für "männlich" und eine ungerade Ziffer für "weiblich".</span><span class="sxs-lookup"><span data-stu-id="9b48b-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="9b48b-137">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9b48b-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-138">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-138">Checksum</span></span>

<span data-ttu-id="9b48b-139">Ja</span><span class="sxs-lookup"><span data-stu-id="9b48b-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-140">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-140">Definition</span></span>

<span data-ttu-id="9b48b-141">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-142">Die- `Func_bulgaria_national_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-143">Ein Schlüsselwort `Keywords_bulgaria_national_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="9b48b-144">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-145">Die- `Func_bulgaria_national_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-146">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-146">Keywords</span></span>

#### <a name="keywords_bulgaria_national_number"></a><span data-ttu-id="9b48b-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="9b48b-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="9b48b-148">EGN</span><span class="sxs-lookup"><span data-stu-id="9b48b-148">egn</span></span>
  
<span data-ttu-id="9b48b-149">EGN #</span><span class="sxs-lookup"><span data-stu-id="9b48b-149">egn#</span></span>
  
<span data-ttu-id="9b48b-150">Bulgarische Nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-150">bulgarian national number</span></span>
  
<span data-ttu-id="9b48b-151">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-151">national number</span></span>
  
<span data-ttu-id="9b48b-152">social security number</span><span class="sxs-lookup"><span data-stu-id="9b48b-152">social security number</span></span>
  
<span data-ttu-id="9b48b-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="9b48b-153">nationalnumber#</span></span>
  
<span data-ttu-id="9b48b-154">SSN #</span><span class="sxs-lookup"><span data-stu-id="9b48b-154">ssn#</span></span>
  
<span data-ttu-id="9b48b-155">SSN</span><span class="sxs-lookup"><span data-stu-id="9b48b-155">ssn</span></span>
  
<span data-ttu-id="9b48b-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="9b48b-156">nationalnumber</span></span>
  
<span data-ttu-id="9b48b-157">BNN #</span><span class="sxs-lookup"><span data-stu-id="9b48b-157">bnn#</span></span>
  
<span data-ttu-id="9b48b-158">BNN</span><span class="sxs-lookup"><span data-stu-id="9b48b-158">bnn</span></span>
  
<span data-ttu-id="9b48b-159">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-159">personal id number</span></span>
  
<span data-ttu-id="9b48b-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="9b48b-160">personalidnumber#</span></span>
  
<span data-ttu-id="9b48b-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="9b48b-161">единен граждански номер</span></span>
  
<span data-ttu-id="9b48b-162">edinen grazhdanski Nomen</span><span class="sxs-lookup"><span data-stu-id="9b48b-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="9b48b-163">егн</span><span class="sxs-lookup"><span data-stu-id="9b48b-163">егн</span></span>
  
<span data-ttu-id="9b48b-164">егн #</span><span class="sxs-lookup"><span data-stu-id="9b48b-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="9b48b-165">Kroatien</span><span class="sxs-lookup"><span data-stu-id="9b48b-165">Croatia</span></span>

<span data-ttu-id="9b48b-166">Ausführliche Informationen finden Sie im Abschnitt "kroatische Identitätsnummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9b48b-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="9b48b-167">Zypern</span><span class="sxs-lookup"><span data-stu-id="9b48b-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-168">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-168">Format</span></span>

<span data-ttu-id="9b48b-169">Zehn Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-170">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-170">Pattern</span></span>

 <span data-ttu-id="9b48b-171">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="9b48b-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="9b48b-172">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-172">Checksum</span></span>

<span data-ttu-id="9b48b-173">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9b48b-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-174">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-174">Definition</span></span>

<span data-ttu-id="9b48b-175">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-176">Der reguläre Ausdruck `Regex_cyprus_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-177">Ein Schlüsselwort `Keywords_cyprus_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b48b-178">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-178">Keywords</span></span>

#### <a name="keywords_cyprus_eu_national_id_card"></a><span data-ttu-id="9b48b-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-180">ID-Kartennummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-180">id card number</span></span>
  
<span data-ttu-id="9b48b-181">national identification number</span><span class="sxs-lookup"><span data-stu-id="9b48b-181">national identification number</span></span>
  
<span data-ttu-id="9b48b-182">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-182">personal id number</span></span>
  
<span data-ttu-id="9b48b-183">Personalausweisnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-183">identity card number</span></span>
  
<span data-ttu-id="9b48b-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="9b48b-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="9b48b-185">Tschechien</span><span class="sxs-lookup"><span data-stu-id="9b48b-185">Czech Republic</span></span>

<span data-ttu-id="9b48b-186">Ausführliche Informationen finden Sie im Abschnitt "Tschechische Nationale Identitätsnummer" unter [was die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9b48b-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="9b48b-187">Dänemark</span><span class="sxs-lookup"><span data-stu-id="9b48b-187">Denmark</span></span>

<span data-ttu-id="9b48b-188">Ausführliche Informationen finden Sie im Abschnitt "dänische persönliche Identifikationsnummer" unter [was die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9b48b-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="9b48b-189">Estland</span><span class="sxs-lookup"><span data-stu-id="9b48b-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-190">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-190">Format</span></span>

<span data-ttu-id="9b48b-191">11 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-192">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-192">Pattern</span></span>

<span data-ttu-id="9b48b-193">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="9b48b-193">11 digits:</span></span>
  
- <span data-ttu-id="9b48b-194">Eine Ziffer, die Geschlecht und Jahrhundert der Geburt entspricht (ungerade Zahl männlich, gerade Zahl weiblich; 1-2:19. Jahrhundert; 3-4:20th Century; 5-6:21st Century)</span><span class="sxs-lookup"><span data-stu-id="9b48b-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="9b48b-195">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="9b48b-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="9b48b-196">Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am gleichen Datum geboren wurden</span><span class="sxs-lookup"><span data-stu-id="9b48b-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="9b48b-197">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9b48b-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-198">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-198">Checksum</span></span>

<span data-ttu-id="9b48b-199">Ja</span><span class="sxs-lookup"><span data-stu-id="9b48b-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-200">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-200">Definition</span></span>

<span data-ttu-id="9b48b-201">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-202">Die- `Func_estonia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-203">Ein Schlüsselwort `Keywords_estonia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9b48b-204">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-205">Die- `Func_estonia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-206">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-206">Keywords</span></span>

#### <a name="keywords_estonia_eu_national_id_card"></a><span data-ttu-id="9b48b-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-208">persönlicher Identifikationscode</span><span class="sxs-lookup"><span data-stu-id="9b48b-208">personal identification code</span></span>
  
<span data-ttu-id="9b48b-209">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-209">personal identification number</span></span>
  
<span data-ttu-id="9b48b-210">national identification number</span><span class="sxs-lookup"><span data-stu-id="9b48b-210">national identification number</span></span>
  
<span data-ttu-id="9b48b-211">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-211">national number</span></span>
  
<span data-ttu-id="9b48b-212">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-212">personal id number</span></span>
  
<span data-ttu-id="9b48b-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="9b48b-213">personalidnumber#</span></span>
  
<span data-ttu-id="9b48b-214">IK</span><span class="sxs-lookup"><span data-stu-id="9b48b-214">ik</span></span>
  
<span data-ttu-id="9b48b-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="9b48b-215">isikukood</span></span>
  
<span data-ttu-id="9b48b-216">ID-Kaart</span><span class="sxs-lookup"><span data-stu-id="9b48b-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="9b48b-217">Finnland</span><span class="sxs-lookup"><span data-stu-id="9b48b-217">Finland</span></span>

<span data-ttu-id="9b48b-218">Ausführliche Informationen finden Sie im Abschnitt "finnische nationale ID" unter [was die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9b48b-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="9b48b-219">Frankreich</span><span class="sxs-lookup"><span data-stu-id="9b48b-219">France</span></span>

<span data-ttu-id="9b48b-220">Ausführliche Informationen finden Sie im Abschnitt "France National ID Card (CNI)" in [What the sensitive Information Types Look for](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9b48b-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="9b48b-221">Deutschland</span><span class="sxs-lookup"><span data-stu-id="9b48b-221">Germany</span></span>

<span data-ttu-id="9b48b-222">Ausführliche Informationen finden Sie im Abschnitt "Deutsche Identitätskartennummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9b48b-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="9b48b-223">Griechenland</span><span class="sxs-lookup"><span data-stu-id="9b48b-223">Greece</span></span>

<span data-ttu-id="9b48b-224">Ausführliche Informationen finden Sie im Abschnitt "Griechenland-National Ausweis" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9b48b-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="9b48b-225">Ungarn</span><span class="sxs-lookup"><span data-stu-id="9b48b-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-226">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-226">Format</span></span>

<span data-ttu-id="9b48b-227">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="9b48b-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-228">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-228">Pattern</span></span>

<span data-ttu-id="9b48b-229">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="9b48b-229">11 digits:</span></span>
  
-  <span data-ttu-id="9b48b-230">Eine Ziffer, die dem Geschlecht entspricht (1-männlich, 2-weiblich, andere Zahlen sind auch für Bürger möglich, die vor 1900 oder Bürgern mit doppelter Staatsbürgerschaft geboren wurden)</span><span class="sxs-lookup"><span data-stu-id="9b48b-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="9b48b-231">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="9b48b-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="9b48b-232">Drei Ziffern, die einer Seriennummer entsprechen</span><span class="sxs-lookup"><span data-stu-id="9b48b-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="9b48b-233">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9b48b-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-234">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-234">Checksum</span></span>

<span data-ttu-id="9b48b-235">Ja</span><span class="sxs-lookup"><span data-stu-id="9b48b-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-236">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-236">Definition</span></span>

<span data-ttu-id="9b48b-237">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-238">Die- `Func_hungary_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-239">Ein Schlüsselwort `Keywords_hungary_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9b48b-240">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-241">Die- `Func_hungary_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-242">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-242">Keywords</span></span>

#### <a name="keywords_hungary_eu_national_id_card"></a><span data-ttu-id="9b48b-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-244">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-244">personal identification number</span></span>
  
<span data-ttu-id="9b48b-245">identification number</span><span class="sxs-lookup"><span data-stu-id="9b48b-245">identification number</span></span>
  
<span data-ttu-id="9b48b-246">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-246">personal id number</span></span>
  
<span data-ttu-id="9b48b-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="9b48b-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="9b48b-248">Irland</span><span class="sxs-lookup"><span data-stu-id="9b48b-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-249">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-249">Format</span></span>

<span data-ttu-id="9b48b-250">Eine neunstellige Kombination aus Buchstaben, Ziffern und einem Leerzeichen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-251">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-251">Pattern</span></span>

<span data-ttu-id="9b48b-252">Eine neunstellige Kombination aus Buchstaben, Ziffern und einem Leerzeichen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="9b48b-253">Vom 01 Januar 2013 bis jetzt:</span><span class="sxs-lookup"><span data-stu-id="9b48b-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="9b48b-254">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="9b48b-254">Seven digits</span></span> 
    
- <span data-ttu-id="9b48b-255">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9b48b-255">One check digit</span></span>
    
- <span data-ttu-id="9b48b-256">Ein Leerzeichen oder der Großbuchstabe "W" (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="9b48b-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="9b48b-257">Vor dem 01. Januar 2013:</span><span class="sxs-lookup"><span data-stu-id="9b48b-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="9b48b-258">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="9b48b-258">Seven digits</span></span> 
    
- <span data-ttu-id="9b48b-259">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9b48b-259">One check digit</span></span>
    
- <span data-ttu-id="9b48b-260">Ein Leerzeichen oder ein Großbuchstabe (Groß-/Kleinschreibung beachten)</span><span class="sxs-lookup"><span data-stu-id="9b48b-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-261">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-261">Checksum</span></span>

<span data-ttu-id="9b48b-262">Ja</span><span class="sxs-lookup"><span data-stu-id="9b48b-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-263">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-263">Definition</span></span>

<span data-ttu-id="9b48b-264">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-265">Die-Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="9b48b-266">Ein Schlüsselwort aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-266">A keyword from is found.</span></span>
    
<span data-ttu-id="9b48b-267">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-268">Die-Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-269">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-269">Keywords</span></span>

#### <a name="keywords_ireland_eu_national_id_card"></a><span data-ttu-id="9b48b-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-271">persönliche öffentliche Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-271">personal public service number</span></span>
  
<span data-ttu-id="9b48b-272">PPS Nein</span><span class="sxs-lookup"><span data-stu-id="9b48b-272">pps no</span></span>
  
<span data-ttu-id="9b48b-273">Umsatz-und Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="9b48b-274">RSI-Nr.</span><span class="sxs-lookup"><span data-stu-id="9b48b-274">rsi no</span></span>
  
<span data-ttu-id="9b48b-275">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-275">personal identification number</span></span>
  
<span data-ttu-id="9b48b-276">identification number</span><span class="sxs-lookup"><span data-stu-id="9b48b-276">identification number</span></span>
  
<span data-ttu-id="9b48b-277">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-277">personal id number</span></span>
  
<span data-ttu-id="9b48b-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="9b48b-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="9b48b-279">uimh.</span><span class="sxs-lookup"><span data-stu-id="9b48b-279">uimh.</span></span> <span data-ttu-id="9b48b-280">PSP</span><span class="sxs-lookup"><span data-stu-id="9b48b-280">psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="9b48b-281">Italien</span><span class="sxs-lookup"><span data-stu-id="9b48b-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-282">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-282">Format</span></span>

<span data-ttu-id="9b48b-283">Eine Kombination aus Buchstaben und Ziffern aus 16 Zeichen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-284">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-284">Pattern</span></span>

<span data-ttu-id="9b48b-285">Eine Kombination aus Buchstaben und Ziffern aus 16 Zeichen:</span><span class="sxs-lookup"><span data-stu-id="9b48b-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="9b48b-286">Drei Buchstaben, die den ersten drei Konsonanten im Familiennamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="9b48b-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="9b48b-287">Drei Buchstaben, die den ersten, dritten und vierten Konsonanten im Vornamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="9b48b-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="9b48b-288">Zwei Ziffern, die den letzten Ziffern des Geburtsjahres entsprechen</span><span class="sxs-lookup"><span data-stu-id="9b48b-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="9b48b-289">Ein Buchstabe, der dem Brief für den Monat der Geburt entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben a bis E, H, L, M, P, R bis T werden verwendet (der Januar ist also a und Oktober ist r).</span><span class="sxs-lookup"><span data-stu-id="9b48b-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="9b48b-290">Zwei Ziffern, die dem Tag des Geburtsmonats entsprechen – um zwischen den Geschlechtern zu unterscheiden, wird 40 am Tag der Geburt für Frauen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9b48b-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="9b48b-291">Vier Ziffern, die der Ortskennzahl für die Gemeinde entsprechen, in der die Person geboren wurde (landesweite Codes werden für fremde Länder verwendet)</span><span class="sxs-lookup"><span data-stu-id="9b48b-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="9b48b-292">Eine Paritäts Ziffer</span><span class="sxs-lookup"><span data-stu-id="9b48b-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-293">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-293">Checksum</span></span>

<span data-ttu-id="9b48b-294">Ja</span><span class="sxs-lookup"><span data-stu-id="9b48b-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-295">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-295">Definition</span></span>

<span data-ttu-id="9b48b-296">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-297">Die- `Func_italy_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-298">Ein Schlüsselwort `Keywords_italy_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9b48b-299">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-300">Die- `Func_italy_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-301">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-301">Keywords</span></span>

#### <a name="keywords_italy_eu_national_id_card"></a><span data-ttu-id="9b48b-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-303">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-303">personal code</span></span>
  
<span data-ttu-id="9b48b-304">persönliche Codenummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-304">personal code number</span></span>
  
<span data-ttu-id="9b48b-305">persönliche Zertifikat Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-305">personal certificate number</span></span>
  
<span data-ttu-id="9b48b-306">Geschäftscode</span><span class="sxs-lookup"><span data-stu-id="9b48b-306">fiscal code</span></span>
  
<span data-ttu-id="9b48b-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="9b48b-307">personalcodeno#</span></span>
  
<span data-ttu-id="9b48b-308">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-308">personal id number</span></span>
  
<span data-ttu-id="9b48b-309">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-309">personal id code</span></span>
  
<span data-ttu-id="9b48b-310">Dice personale</span><span class="sxs-lookup"><span data-stu-id="9b48b-310">codice personale</span></span>
  
<span data-ttu-id="9b48b-311">Numero Bescheinigung personale</span><span class="sxs-lookup"><span data-stu-id="9b48b-311">numero certificato personale</span></span>
  
<span data-ttu-id="9b48b-312">Numero personale</span><span class="sxs-lookup"><span data-stu-id="9b48b-312">numero personale</span></span>
  
<span data-ttu-id="9b48b-313">Numero-ID personale</span><span class="sxs-lookup"><span data-stu-id="9b48b-313">numero id personale</span></span>
  
<span data-ttu-id="9b48b-314">Dice ID personale</span><span class="sxs-lookup"><span data-stu-id="9b48b-314">codice id personale</span></span>
  
<span data-ttu-id="9b48b-315">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="9b48b-315">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="9b48b-316">Lettland</span><span class="sxs-lookup"><span data-stu-id="9b48b-316">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-317">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-317">Format</span></span>

<span data-ttu-id="9b48b-318">11 Ziffern und ein Bindestrich im angegebenen Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-319">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-319">Pattern</span></span>

<span data-ttu-id="9b48b-320">11 Ziffern und Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="9b48b-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="9b48b-321">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="9b48b-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="9b48b-322">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="9b48b-322">A hyphen</span></span>
    
- <span data-ttu-id="9b48b-323">Eine Ziffer, die dem Jahrhundert der Geburt entspricht ("0" für das 19. Jahrhundert, "1" für das 20. Jahrhundert und "2" für das 21. Jahrhundert)</span><span class="sxs-lookup"><span data-stu-id="9b48b-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="9b48b-324">Vier Ziffern, nach dem Zufallsprinzip generiert</span><span class="sxs-lookup"><span data-stu-id="9b48b-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-325">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-325">Checksum</span></span>

<span data-ttu-id="9b48b-326">Ja</span><span class="sxs-lookup"><span data-stu-id="9b48b-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-327">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-327">Definition</span></span>

<span data-ttu-id="9b48b-328">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-329">Die- `Func_latvia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-330">Ein Schlüsselwort `Keywords_latvia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9b48b-331">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-332">Die- `Func_latvia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-333">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-333">Keywords</span></span>

#### <a name="keywords_latvia_eu_national_id_card"></a><span data-ttu-id="9b48b-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-335">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-335">personal code</span></span>
  
<span data-ttu-id="9b48b-336">persönliche Codenummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-336">personal code number</span></span>
  
<span data-ttu-id="9b48b-337">persönliche Zertifikat Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-337">personal certificate number</span></span>
  
<span data-ttu-id="9b48b-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="9b48b-338">personalcodeno#</span></span>
  
<span data-ttu-id="9b48b-339">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-339">personal id number</span></span>
  
<span data-ttu-id="9b48b-340">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-340">personal id code</span></span>
  
<span data-ttu-id="9b48b-341">Personas KODS</span><span class="sxs-lookup"><span data-stu-id="9b48b-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="9b48b-342">Litauen</span><span class="sxs-lookup"><span data-stu-id="9b48b-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-343">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-343">Format</span></span>

<span data-ttu-id="9b48b-344">11 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-345">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-345">Pattern</span></span>

<span data-ttu-id="9b48b-346">11 Ziffern ohne Leerzeichen und Trennzeichen:</span><span class="sxs-lookup"><span data-stu-id="9b48b-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="9b48b-347">Eine Ziffer, die dem Geschlecht der Person und dem Jahrhundert der Geburt entspricht</span><span class="sxs-lookup"><span data-stu-id="9b48b-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="9b48b-348">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="9b48b-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="9b48b-349">Drei Ziffern, die der Seriennummer des Geburtsdatums entsprechen</span><span class="sxs-lookup"><span data-stu-id="9b48b-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="9b48b-350">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9b48b-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-351">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-351">Checksum</span></span>

<span data-ttu-id="9b48b-352">Ja</span><span class="sxs-lookup"><span data-stu-id="9b48b-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-353">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-353">Definition</span></span>

<span data-ttu-id="9b48b-354">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-355">Die- `Func_lithuania_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-356">Ein Schlüsselwort `Keywords_lithuania_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9b48b-357">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-358">Die- `Func_lithuania_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-359">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-359">Keywords</span></span>

#### <a name="keywords_lithuania_eu_national_id_card"></a><span data-ttu-id="9b48b-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-361">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-361">personal numeric code</span></span>
  
<span data-ttu-id="9b48b-362">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-362">unique identification number</span></span>
  
<span data-ttu-id="9b48b-363">Bürgerdienst Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-363">citizen service number</span></span>
  
<span data-ttu-id="9b48b-364">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-364">unique identity number</span></span>
  
<span data-ttu-id="9b48b-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9b48b-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="9b48b-366">persönlicher Code.</span><span class="sxs-lookup"><span data-stu-id="9b48b-366">personal code.</span></span>
  
<span data-ttu-id="9b48b-367">asmeninis skaitmeninis KODAS</span><span class="sxs-lookup"><span data-stu-id="9b48b-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="9b48b-368">unikalus identifikavimo Numeris</span><span class="sxs-lookup"><span data-stu-id="9b48b-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="9b48b-369">piliečio paslaugos Numeris</span><span class="sxs-lookup"><span data-stu-id="9b48b-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="9b48b-370">unikalus identifikavimo KODAS</span><span class="sxs-lookup"><span data-stu-id="9b48b-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="9b48b-371">Mens KODAS.</span><span class="sxs-lookup"><span data-stu-id="9b48b-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="9b48b-372">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="9b48b-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-373">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-373">Format</span></span>

<span data-ttu-id="9b48b-374">11 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-375">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-375">Pattern</span></span>

<span data-ttu-id="9b48b-376">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="9b48b-376">11 digits</span></span>
  
- <span data-ttu-id="9b48b-377">Eine Ziffer, die dem Geschlecht der Person und dem Jahrhundert der Geburt entspricht</span><span class="sxs-lookup"><span data-stu-id="9b48b-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="9b48b-378">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="9b48b-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="9b48b-379">Drei Ziffern, die der Seriennummer des Geburtsdatums entsprechen</span><span class="sxs-lookup"><span data-stu-id="9b48b-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="9b48b-380">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9b48b-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-381">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-381">Checksum</span></span>

<span data-ttu-id="9b48b-382">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9b48b-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-383">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-383">Definition</span></span>

<span data-ttu-id="9b48b-384">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-385">Der reguläre Ausdruck `Regex_luxemburg_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-386">Ein Schlüsselwort `Keywords_luxemburg_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b48b-387">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-387">Keywords</span></span>

#### <a name="keywords_luxemburg_eu_national_id_card"></a><span data-ttu-id="9b48b-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-389">persönliche ID</span><span class="sxs-lookup"><span data-stu-id="9b48b-389">personal id</span></span>
  
<span data-ttu-id="9b48b-390">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-390">personal id number</span></span>
  
<span data-ttu-id="9b48b-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="9b48b-391">personalidno#</span></span>
  
<span data-ttu-id="9b48b-392">eindeutige ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-392">unique id number</span></span>
  
<span data-ttu-id="9b48b-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="9b48b-393">personalidnumber#</span></span>
  
<span data-ttu-id="9b48b-394">eindeutiger ID-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="9b48b-394">unique id key</span></span>
  
<span data-ttu-id="9b48b-395">persönlicher ID-Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-395">personal id code</span></span>
  
<span data-ttu-id="9b48b-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="9b48b-396">uniqueidkey#</span></span>
  
<span data-ttu-id="9b48b-397">einzelner Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-397">individual code</span></span>
  
<span data-ttu-id="9b48b-398">individuelle ID</span><span class="sxs-lookup"><span data-stu-id="9b48b-398">individual id</span></span>
  
<span data-ttu-id="9b48b-399">eindeutige-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="9b48b-400">eindeutige-ID</span><span class="sxs-lookup"><span data-stu-id="9b48b-400">eindeutige id</span></span>
  
<span data-ttu-id="9b48b-401">ID personnelle</span><span class="sxs-lookup"><span data-stu-id="9b48b-401">id personnelle</span></span>
  
<span data-ttu-id="9b48b-402">Numéro-d'identification-Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="9b48b-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="9b48b-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="9b48b-403">idpersonnelle#</span></span>
  
<span data-ttu-id="9b48b-404">persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="9b48b-405">eindeutigeid #</span><span class="sxs-lookup"><span data-stu-id="9b48b-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="9b48b-406">Malta</span><span class="sxs-lookup"><span data-stu-id="9b48b-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-407">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-407">Format</span></span>

<span data-ttu-id="9b48b-408">Sieben Ziffern, gefolgt von einem Buchstaben</span><span class="sxs-lookup"><span data-stu-id="9b48b-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-409">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-409">Pattern</span></span>

<span data-ttu-id="9b48b-410">Sieben Ziffern, gefolgt von einem Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="9b48b-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="9b48b-411">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="9b48b-411">Seven digits</span></span> 
    
- <span data-ttu-id="9b48b-412">Ein Großbuchstabe (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="9b48b-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-413">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-413">Checksum</span></span>

<span data-ttu-id="9b48b-414">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9b48b-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-415">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-415">Definition</span></span>

<span data-ttu-id="9b48b-416">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-417">Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-418">Ein Schlüsselwort `Keywords_malta_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9b48b-419">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-420">Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-421">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-421">Keywords</span></span>

#### <a name="keywords_malta_eu_national_id_card"></a><span data-ttu-id="9b48b-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-423">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-423">personal numeric code</span></span>
  
<span data-ttu-id="9b48b-424">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-424">unique identification number</span></span>
  
<span data-ttu-id="9b48b-425">Bürgerdienst Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-425">citizen service number</span></span>
  
<span data-ttu-id="9b48b-426">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-426">unique identity number</span></span>
  
<span data-ttu-id="9b48b-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9b48b-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="9b48b-428">Kodiċi Numeri personali</span><span class="sxs-lookup"><span data-stu-id="9b48b-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="9b48b-429">numru ta ' identifikazzjoni uniku</span><span class="sxs-lookup"><span data-stu-id="9b48b-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="9b48b-430">numru TAS-servizz taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="9b48b-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="9b48b-431">numru ta ' identità uniku</span><span class="sxs-lookup"><span data-stu-id="9b48b-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="9b48b-432">Niederlande</span><span class="sxs-lookup"><span data-stu-id="9b48b-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-433">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-433">Format</span></span>

<span data-ttu-id="9b48b-434">Neun Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-435">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-435">Pattern</span></span>

<span data-ttu-id="9b48b-436">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="9b48b-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b48b-437">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-437">Checksum</span></span>

<span data-ttu-id="9b48b-438">Ja</span><span class="sxs-lookup"><span data-stu-id="9b48b-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-439">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-439">Definition</span></span>

<span data-ttu-id="9b48b-440">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-441">Die- `Func_netherlands_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-442">Ein Schlüsselwort aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-442">A keyword from is found.</span></span>
    
<span data-ttu-id="9b48b-443">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-444">Die- `Func_netherlands_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-445">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-445">Keywords</span></span>

#### <a name="keywords_netherlands_eu_national_id_card"></a><span data-ttu-id="9b48b-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-447">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-447">personal numeric code</span></span>
  
<span data-ttu-id="9b48b-448">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-448">unique identification number</span></span>
  
<span data-ttu-id="9b48b-449">Bürgerdienst Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-449">citizen service number</span></span>
  
<span data-ttu-id="9b48b-450">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-450">unique identity number</span></span>
  
<span data-ttu-id="9b48b-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9b48b-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="9b48b-452">BSN</span><span class="sxs-lookup"><span data-stu-id="9b48b-452">bsn</span></span>
  
<span data-ttu-id="9b48b-453">BSN #</span><span class="sxs-lookup"><span data-stu-id="9b48b-453">bsn#</span></span>
  
<span data-ttu-id="9b48b-454">Persoonlijke-numerieke-Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="9b48b-455">uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="9b48b-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-456">burgerservicenummer</span></span>
  
<span data-ttu-id="9b48b-457">uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="9b48b-458">Polen</span><span class="sxs-lookup"><span data-stu-id="9b48b-458">Poland</span></span>

<span data-ttu-id="9b48b-459">Ausführliche Informationen finden Sie im Abschnitt "Poland National ID (PESEL)" in [What the sensitive Information Types Look for](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9b48b-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="9b48b-460">Portugal</span><span class="sxs-lookup"><span data-stu-id="9b48b-460">Portugal</span></span>

<span data-ttu-id="9b48b-461">Ausführliche Informationen finden Sie im Abschnitt "Portugal-Bürgerkarten Nummer" unter [was die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9b48b-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="9b48b-462">Rumänien</span><span class="sxs-lookup"><span data-stu-id="9b48b-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-463">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-463">Format</span></span>

<span data-ttu-id="9b48b-464">13 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-465">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-465">Pattern</span></span>

<span data-ttu-id="9b48b-466">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="9b48b-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b48b-467">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-467">Checksum</span></span>

<span data-ttu-id="9b48b-468">Ja</span><span class="sxs-lookup"><span data-stu-id="9b48b-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-469">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-469">Definition</span></span>

<span data-ttu-id="9b48b-470">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-471">Die- `Func_romania_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-472">Ein Schlüsselwort `Keywords_romania_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9b48b-473">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-474">Die- `Func_romania_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-475">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-475">Keywords</span></span>

#### <a name="keywords_romania_eu_national_id_card"></a><span data-ttu-id="9b48b-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-477">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-477">personal numeric code</span></span>
  
<span data-ttu-id="9b48b-478">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-478">unique identification number</span></span>
  
<span data-ttu-id="9b48b-479">CNP</span><span class="sxs-lookup"><span data-stu-id="9b48b-479">cnp</span></span>
  
<span data-ttu-id="9b48b-480">CNP #</span><span class="sxs-lookup"><span data-stu-id="9b48b-480">cnp#</span></span>
  
<span data-ttu-id="9b48b-481">PIN</span><span class="sxs-lookup"><span data-stu-id="9b48b-481">pin</span></span>
  
<span data-ttu-id="9b48b-482">PIN #</span><span class="sxs-lookup"><span data-stu-id="9b48b-482">pin#</span></span>
  
<span data-ttu-id="9b48b-483">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-483">insurance number</span></span>
  
<span data-ttu-id="9b48b-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="9b48b-484">insurancenumber#</span></span>
  
<span data-ttu-id="9b48b-485">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-485">unique identity number</span></span>
  
<span data-ttu-id="9b48b-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9b48b-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="9b48b-487">COD numerisch persönlich</span><span class="sxs-lookup"><span data-stu-id="9b48b-487">cod numeric personal</span></span>
  
<span data-ttu-id="9b48b-488">COD identificare Personal</span><span class="sxs-lookup"><span data-stu-id="9b48b-488">cod identificare personal</span></span>
  
<span data-ttu-id="9b48b-489">COD Unic identificare</span><span class="sxs-lookup"><span data-stu-id="9b48b-489">cod unic identificare</span></span>
  
<span data-ttu-id="9b48b-490">număr Personal Unic</span><span class="sxs-lookup"><span data-stu-id="9b48b-490">număr personal unic</span></span>
  
<span data-ttu-id="9b48b-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="9b48b-491">număr identitate</span></span>
  
<span data-ttu-id="9b48b-492">număr identificare Personal</span><span class="sxs-lookup"><span data-stu-id="9b48b-492">număr identificare personal</span></span>
  
<span data-ttu-id="9b48b-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="9b48b-493">număridentitate#</span></span>
  
<span data-ttu-id="9b48b-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="9b48b-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="9b48b-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="9b48b-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="9b48b-496">Slowakei</span><span class="sxs-lookup"><span data-stu-id="9b48b-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-497">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-497">Format</span></span>

<span data-ttu-id="9b48b-498">Zehn Ziffern mit einem Backslash</span><span class="sxs-lookup"><span data-stu-id="9b48b-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-499">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-499">Pattern</span></span>

<span data-ttu-id="9b48b-500">Zehn Ziffern mit einem Backslash:</span><span class="sxs-lookup"><span data-stu-id="9b48b-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="9b48b-501">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-501">Checksum</span></span>

<span data-ttu-id="9b48b-502">Ja</span><span class="sxs-lookup"><span data-stu-id="9b48b-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-503">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-503">Definition</span></span>

<span data-ttu-id="9b48b-504">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-505">Die- `Func_slovakia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-506">Ein Schlüsselwort `Keywords_slovakia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9b48b-507">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-508">Die- `Func_slovakia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-509">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-509">Keywords</span></span>

#### <a name="keywords_slovakia_eu_national_id_card"></a><span data-ttu-id="9b48b-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-511">Geburtsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-511">birth number</span></span>
  
<span data-ttu-id="9b48b-512">national identification number</span><span class="sxs-lookup"><span data-stu-id="9b48b-512">national identification number</span></span>
  
<span data-ttu-id="9b48b-513">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-513">personal identification number</span></span>
  
<span data-ttu-id="9b48b-514">social security number</span><span class="sxs-lookup"><span data-stu-id="9b48b-514">social security number</span></span>
  
<span data-ttu-id="9b48b-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="9b48b-515">nationalnumber#</span></span>
  
<span data-ttu-id="9b48b-516">SSN #</span><span class="sxs-lookup"><span data-stu-id="9b48b-516">ssn#</span></span>
  
<span data-ttu-id="9b48b-517">SSN</span><span class="sxs-lookup"><span data-stu-id="9b48b-517">ssn</span></span>
  
<span data-ttu-id="9b48b-518">nationale Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-518">national number</span></span>
  
<span data-ttu-id="9b48b-519">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-519">personal id number</span></span>
  
<span data-ttu-id="9b48b-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="9b48b-520">personalidnumber#</span></span>
  
<span data-ttu-id="9b48b-521">rč</span><span class="sxs-lookup"><span data-stu-id="9b48b-521">rč</span></span>
  
<span data-ttu-id="9b48b-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="9b48b-522">rodné číslo</span></span>
  
<span data-ttu-id="9b48b-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="9b48b-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="9b48b-524">Slowenien</span><span class="sxs-lookup"><span data-stu-id="9b48b-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-525">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-525">Format</span></span>

<span data-ttu-id="9b48b-526">13 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-527">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-527">Pattern</span></span>

<span data-ttu-id="9b48b-528">13 Ziffern im angegebenen Muster:</span><span class="sxs-lookup"><span data-stu-id="9b48b-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="9b48b-529">Sieben Ziffern, die dem Geburtsdatum (DDMMLLL) entsprechen, wobei "LLL" den letzten drei Ziffern des Geburtsjahres entspricht.</span><span class="sxs-lookup"><span data-stu-id="9b48b-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="9b48b-530">Zwei Ziffern, die dem Geburts Bereich entsprechen</span><span class="sxs-lookup"><span data-stu-id="9b48b-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="9b48b-531">Drei Ziffern, die einer Kombination aus Geschlecht und Seriennummer für Personen entsprechen, die am selben Tag geboren wurden (000-499 für männliche und 500-999 für weiblich)</span><span class="sxs-lookup"><span data-stu-id="9b48b-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="9b48b-532">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="9b48b-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-533">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-533">Checksum</span></span>

<span data-ttu-id="9b48b-534">Ja</span><span class="sxs-lookup"><span data-stu-id="9b48b-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-535">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-535">Definition</span></span>

<span data-ttu-id="9b48b-536">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-537">Die- `Func_slovenia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-538">Ein Schlüsselwort `Keywords_slovenia_eu_national_id_card` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="9b48b-539">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-540">Die- `Func_slovenia_eu_national_id_card` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="9b48b-541">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-541">Keywords</span></span>

#### <a name="keywords_slovenia_eu_national_id_card"></a><span data-ttu-id="9b48b-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-543">persönlicher numerischer Code</span><span class="sxs-lookup"><span data-stu-id="9b48b-543">personal numeric code</span></span>
  
<span data-ttu-id="9b48b-544">eindeutige Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-544">unique identification number</span></span>
  
<span data-ttu-id="9b48b-545">eindeutige Registrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-545">unique registration number</span></span>
  
<span data-ttu-id="9b48b-546">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-546">unique identity number</span></span>
  
<span data-ttu-id="9b48b-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9b48b-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="9b48b-548">eindeutige Master Bürgerzahl</span><span class="sxs-lookup"><span data-stu-id="9b48b-548">unique master citizen number</span></span>
  
<span data-ttu-id="9b48b-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="9b48b-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="9b48b-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="9b48b-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="9b48b-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="9b48b-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="9b48b-552">EMŠO</span><span class="sxs-lookup"><span data-stu-id="9b48b-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="9b48b-553">Spanien</span><span class="sxs-lookup"><span data-stu-id="9b48b-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="9b48b-554">Format</span><span class="sxs-lookup"><span data-stu-id="9b48b-554">Format</span></span>

<span data-ttu-id="9b48b-555">Acht Ziffern, gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-555">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="9b48b-556">Muster</span><span class="sxs-lookup"><span data-stu-id="9b48b-556">Pattern</span></span>

<span data-ttu-id="9b48b-557">Acht Ziffern, gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="9b48b-557">Eight digits followed by one character</span></span>
  
- <span data-ttu-id="9b48b-558">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="9b48b-558">Eight digits</span></span>
    
- <span data-ttu-id="9b48b-559">Eine Ziffer oder ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="9b48b-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="9b48b-560">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="9b48b-560">Checksum</span></span>

<span data-ttu-id="9b48b-561">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9b48b-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="9b48b-562">Definition</span><span class="sxs-lookup"><span data-stu-id="9b48b-562">Definition</span></span>

<span data-ttu-id="9b48b-563">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="9b48b-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="9b48b-564">Der reguläre Ausdruck `Regex_spain_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b48b-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="9b48b-565">Ein Schlüsselwort `Keywords_spain_eu_national_id_card"` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="9b48b-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="9b48b-566">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="9b48b-566">Keywords</span></span>

#### <a name="keywords_spain_eu_national_id_card"></a><span data-ttu-id="9b48b-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="9b48b-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="9b48b-568">DNI</span><span class="sxs-lookup"><span data-stu-id="9b48b-568">dni</span></span>
  
<span data-ttu-id="9b48b-569">national identification number</span><span class="sxs-lookup"><span data-stu-id="9b48b-569">national identification number</span></span>
  
<span data-ttu-id="9b48b-570">nationale Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-570">national identity number</span></span>
  
<span data-ttu-id="9b48b-571">Versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-571">insurance number</span></span>
  
<span data-ttu-id="9b48b-572">persönliche Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-572">personal identification number</span></span>
  
<span data-ttu-id="9b48b-573">nationale Identität</span><span class="sxs-lookup"><span data-stu-id="9b48b-573">national identity</span></span>
  
<span data-ttu-id="9b48b-574">persönliche Identität Nein</span><span class="sxs-lookup"><span data-stu-id="9b48b-574">personal identity no</span></span>
  
<span data-ttu-id="9b48b-575">eindeutige Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="9b48b-575">unique identity number</span></span>
  
<span data-ttu-id="9b48b-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="9b48b-576">nationalidno#</span></span>
  
<span data-ttu-id="9b48b-577">UniqueId #</span><span class="sxs-lookup"><span data-stu-id="9b48b-577">uniqueid#</span></span>
  
<span data-ttu-id="9b48b-578">DNI #</span><span class="sxs-lookup"><span data-stu-id="9b48b-578">dni#</span></span>
  
<span data-ttu-id="9b48b-579">National-Nr. #</span><span class="sxs-lookup"><span data-stu-id="9b48b-579">nationalid#</span></span>
  
<span data-ttu-id="9b48b-580">nie #</span><span class="sxs-lookup"><span data-stu-id="9b48b-580">nie#</span></span>
  
<span data-ttu-id="9b48b-581">nie</span><span class="sxs-lookup"><span data-stu-id="9b48b-581">nie</span></span>
  
<span data-ttu-id="9b48b-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="9b48b-582">nienúmero#</span></span>
  
<span data-ttu-id="9b48b-583">nie número</span><span class="sxs-lookup"><span data-stu-id="9b48b-583">nie número</span></span>
  
<span data-ttu-id="9b48b-584">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="9b48b-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="9b48b-585">Identidad Único</span><span class="sxs-lookup"><span data-stu-id="9b48b-585">identidad único</span></span>
  
<span data-ttu-id="9b48b-586">número Nacional Identidad</span><span class="sxs-lookup"><span data-stu-id="9b48b-586">número nacional identidad</span></span>
  
<span data-ttu-id="9b48b-587">DNI número</span><span class="sxs-lookup"><span data-stu-id="9b48b-587">dni número</span></span>
  
<span data-ttu-id="9b48b-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="9b48b-588">dninúmero#</span></span>
  
<span data-ttu-id="9b48b-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="9b48b-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="9b48b-590">Schweden</span><span class="sxs-lookup"><span data-stu-id="9b48b-590">Sweden</span></span>

<span data-ttu-id="9b48b-591">Ausführliche Informationen finden Sie im Abschnitt "Sweden National ID" unter [What the sensitive Information Types Look](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="9b48b-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b48b-592">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b48b-592">See also</span></span>

[<span data-ttu-id="9b48b-593">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="9b48b-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

