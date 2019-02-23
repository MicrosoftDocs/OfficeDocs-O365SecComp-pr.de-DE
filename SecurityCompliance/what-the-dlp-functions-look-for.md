---
title: Wonach die DLP-Funktionen suchen
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: Die Typen vertraulicher Informationen suchen nach einem bestimmten Muster und bestätigen es, indem Sie eine korrekte Formatierung sicherstellen, Prüfsummen erzwingen und nach relevanten Stichwörtern oder anderen Informationen suchen. Einige dieser Funktionen werden von internen Funktionen ausgeführt. In diesem Thema wird erläutert, wonach diese Funktionen suchen, damit Sie besser verstehen, wie die vordefinierten Typen vertraulicher Informationen funktionieren.
ms.openlocfilehash: 55c740e892e92902b368b2dcf7b0999cbc60f3ed
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219355"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="bf39c-105">Wonach die DLP-Funktionen suchen</span><span class="sxs-lookup"><span data-stu-id="bf39c-105">What the DLP functions look for</span></span>

<span data-ttu-id="bf39c-p102">Schutz vor Datenverlust (Data Loss Prevention, DLP) umfasst Typen vertraulicher Informationen, wie z. B. Kreditkartennummern und EC-Kartennummern, die in Ihren DLP-Richtlinien verwendet werden können. Diese Typen vertraulicher Informationen suchen nach einem bestimmten Muster und bestätigen sie durch Sicherstellen der ordnungsgemäßen Formatierung, durch Erzwingen von Prüfsummen und durch Suchen nach relevanten Schüsselwörtern oder anderen Informationen. Einige dieser Funktionen werden durch interne Funktionen ausgeführt. Der Typ vertraulicher Informationen für die Kreditkartennummer verwendet beispielsweise eine Funktion für die Suche nach Datumsangaben, die wie ein Ablaufdatum formatiert sind, um zu bestätigen, dass es sich bei einer Nummer um eine Kreditkartennummer handelt.</span><span class="sxs-lookup"><span data-stu-id="bf39c-p102">Data loss prevention (DLP) includes sensitive information types, such as Credit Card Number and EU Debit Card Number, which are ready for you to use in your DLP policies. These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information. Some of this functionality is performed by internal functions. For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="bf39c-p103">In diesem Thema wird erläutert, wie diese Funktionen vorgehen, um die Funktionsweise der vordefinierten Typen vertraulicher Informationen besser zu verstehen. Weitere Informationen finden Sie unter [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="bf39c-p103">This topic explains what these functions look for, to help you understand how the predefined sensitive information types work. For more information, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="funcusdate"></a><span data-ttu-id="bf39c-112">Func_us_date</span><span class="sxs-lookup"><span data-stu-id="bf39c-112">Func_us_date</span></span>

<span data-ttu-id="bf39c-p104">Diese Funktion sucht nach einem Datum im allgemeinen Format, das in den USA verwendet wird. Dazu gehören die Formate "Month/Day/Year", "Month-Day-Year" und "Month Day Year". Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="bf39c-p104">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ". The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="bf39c-115">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="bf39c-115">Examples:</span></span>
  
- <span data-ttu-id="bf39c-116">2. Dezember 2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-116">December 2, 2016</span></span>
    
- <span data-ttu-id="bf39c-117">Dez 2, 2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-117">Dec 2, 2016</span></span>
    
- <span data-ttu-id="bf39c-118">Dez 02 2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-118">dec 02 2016</span></span>
    
- <span data-ttu-id="bf39c-119">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-119">12/2/2016</span></span>
    
- <span data-ttu-id="bf39c-120">12/02/16</span><span class="sxs-lookup"><span data-stu-id="bf39c-120">12/02/16</span></span>
    
- <span data-ttu-id="bf39c-121">Dez-2-2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-121">Dec-2-2016</span></span>
    
- <span data-ttu-id="bf39c-122">12-2-16</span><span class="sxs-lookup"><span data-stu-id="bf39c-122">12-2-16</span></span>
    
<span data-ttu-id="bf39c-123">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="bf39c-123">Accepted month names:</span></span>
  
- <span data-ttu-id="bf39c-124">Englisch</span><span class="sxs-lookup"><span data-stu-id="bf39c-124">English</span></span>
    
  - <span data-ttu-id="bf39c-125">Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="bf39c-125">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="bf39c-126">Jan. Feb. Mär. Apr. Mai Juni Juli Aug. Sep. Okt. Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="bf39c-126">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="funceudate"></a><span data-ttu-id="bf39c-127">Func_eu_date</span><span class="sxs-lookup"><span data-stu-id="bf39c-127">Func_eu_date</span></span>

<span data-ttu-id="bf39c-p105">Diese Funktion sucht nach einem Datum im häufig in der EU (und in den meisten Ländern außerhalb der USA) verwendeten Format. Dies umfasst die Formate „Tag/Monat/Jahr“, „Tag-Monat-Jahr“ und „Tag Monat Jahr“. Die Namen oder Abkürzungen der Monate unterscheiden nicht nach Groß- und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="bf39c-p105">This function looks for a date in the format commonly used in the E.U. (and most places outside the U.S.). This includes the formats "day/month/year", "day-month-year", and "day month year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="bf39c-132">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="bf39c-132">Examples:</span></span>
  
- <span data-ttu-id="bf39c-133">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-133">2 Dec 2016</span></span>
    
- <span data-ttu-id="bf39c-134">02 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-134">02 dec 2016</span></span>
    
- <span data-ttu-id="bf39c-135">2 Dez 16</span><span class="sxs-lookup"><span data-stu-id="bf39c-135">2 Dec 16</span></span>
    
- <span data-ttu-id="bf39c-136">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-136">2/12/2016</span></span>
    
- <span data-ttu-id="bf39c-137">02/12/16</span><span class="sxs-lookup"><span data-stu-id="bf39c-137">02/12/16</span></span>
    
- <span data-ttu-id="bf39c-138">2-Dez-2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-138">2-Dec-2016</span></span>
    
- <span data-ttu-id="bf39c-139">2-12-16</span><span class="sxs-lookup"><span data-stu-id="bf39c-139">2-12-16</span></span>
    
<span data-ttu-id="bf39c-140">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="bf39c-140">Accepted month names:</span></span>
  
- <span data-ttu-id="bf39c-141">Englisch</span><span class="sxs-lookup"><span data-stu-id="bf39c-141">English</span></span>
    
  - <span data-ttu-id="bf39c-142">Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="bf39c-142">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="bf39c-143">Jan. Feb. Mär. Apr. Mai Juni Juli Aug. Sep. Okt. Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="bf39c-143">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="bf39c-144">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="bf39c-144">Dutch</span></span>
    
  - <span data-ttu-id="bf39c-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="bf39c-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="bf39c-146">Jan Feb maart Apr Mei Jun Jul Aug Sep Sept Okt Okt Nov Dez</span><span class="sxs-lookup"><span data-stu-id="bf39c-146">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="bf39c-147">Französisch</span><span class="sxs-lookup"><span data-stu-id="bf39c-147">French</span></span>
    
  - <span data-ttu-id="bf39c-148">janvier, février, Mars, Avril, Mai, Juni juillet, août, September, Oktober, Novembre, Dezember</span><span class="sxs-lookup"><span data-stu-id="bf39c-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="bf39c-p106">janv. févr. Mars Avril May juil. août Sept. Okt. Nov. déc.</span><span class="sxs-lookup"><span data-stu-id="bf39c-p106">janv. févr. mars avril mai juin juil. août sept. oct. nov. déc.</span></span>
    
- <span data-ttu-id="bf39c-156">Deutsch</span><span class="sxs-lookup"><span data-stu-id="bf39c-156">German</span></span>
    
  - <span data-ttu-id="bf39c-157">Januar, Februar, März, April, Mai, Juni Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="bf39c-157">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="bf39c-p107">Jan./Jän. Feb. März Apr. Mai Juni Juli Aug. Sept. Okt. Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="bf39c-p107">Jan./Jän. Feb. März Apr. Mai Juni Juli Aug. Sept. Okt. Nov. Dez.</span></span>
    
- <span data-ttu-id="bf39c-161">Italienisch</span><span class="sxs-lookup"><span data-stu-id="bf39c-161">Italian</span></span>
    
  - <span data-ttu-id="bf39c-162">gennaio, febbraio, Marzo, Aprile, Maggio, Juni, Juli, Agosto, Settembre, ottobre, Novembre, Dezember</span><span class="sxs-lookup"><span data-stu-id="bf39c-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="bf39c-p108">Genn. febbr. Mar. Apr. Magg. Juni Juli AG. Sett. Ott. Nov. DIC.</span><span class="sxs-lookup"><span data-stu-id="bf39c-p108">genn. febbr. mar. apr. magg. giugno luglio ag. sett. ott. nov. dic.</span></span>
    
- <span data-ttu-id="bf39c-173">Portugiesisch</span><span class="sxs-lookup"><span data-stu-id="bf39c-173">Portuguese</span></span>
    
  - <span data-ttu-id="bf39c-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="bf39c-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="bf39c-175">Jan FEV Mar ABR Mai Jun Jul ago Set out Nov Dez</span><span class="sxs-lookup"><span data-stu-id="bf39c-175">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="bf39c-176">Spanisch</span><span class="sxs-lookup"><span data-stu-id="bf39c-176">Spanish</span></span>
    
  - <span data-ttu-id="bf39c-177">enero, Febrero, Marzo, Abril, Mayo, junio, Julio, Agosto, Septiembre, Octubre, Noviembre, Diciembre</span><span class="sxs-lookup"><span data-stu-id="bf39c-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="bf39c-p109">enero Feb. Marzo ABR. Mayo Jun. Jul. Agosto Sept./Set. Okt. Nov. DIC.</span><span class="sxs-lookup"><span data-stu-id="bf39c-p109">enero feb. marzo abr. mayo jun. jul. agosto sept./set. oct. nov. dic.</span></span>
    
## <a name="funceudate1-deprecated"></a><span data-ttu-id="bf39c-186">Func_eu_date1 (veraltet)</span><span class="sxs-lookup"><span data-stu-id="bf39c-186">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="bf39c-187">Diese Funktion ist veraltet, da Sie nur portugiesische Monatsnamen unterstützt, die jetzt in der `Func_eu_date` obigen Funktion enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bf39c-187">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="bf39c-p110">Diese Funktion sucht nach einem Datum im Format, das häufig in Portugiesisch verwendet wird. Das Format für diese Funktion ist identisch `Func_eu_date`, unterscheidet sich nur in der verwendeten Sprache.</span><span class="sxs-lookup"><span data-stu-id="bf39c-p110">This function looks for a date in the format commonly used in Portuguese. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="bf39c-190">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="bf39c-190">Examples:</span></span>
  
- <span data-ttu-id="bf39c-191">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-191">2 Dez 2016</span></span>
    
- <span data-ttu-id="bf39c-192">02 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-192">02 dez 2016</span></span>
    
- <span data-ttu-id="bf39c-193">2 Dez 16</span><span class="sxs-lookup"><span data-stu-id="bf39c-193">2 Dez 16</span></span>
    
- <span data-ttu-id="bf39c-194">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-194">2/12/2016</span></span>
    
- <span data-ttu-id="bf39c-195">02/12/16</span><span class="sxs-lookup"><span data-stu-id="bf39c-195">02/12/16</span></span>
    
- <span data-ttu-id="bf39c-196">2-Dez-2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-196">2-Dez-2016</span></span>
    
- <span data-ttu-id="bf39c-197">2-12-16</span><span class="sxs-lookup"><span data-stu-id="bf39c-197">2-12-16</span></span>
    
<span data-ttu-id="bf39c-198">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="bf39c-198">Accepted month names:</span></span>
  
- <span data-ttu-id="bf39c-199">Portugiesisch</span><span class="sxs-lookup"><span data-stu-id="bf39c-199">Portuguese</span></span>
    
  - <span data-ttu-id="bf39c-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="bf39c-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="bf39c-201">Jan FEV Mar ABR Mai Jun Jul ago Set out Nov Dez</span><span class="sxs-lookup"><span data-stu-id="bf39c-201">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="funceudate2-deprecated"></a><span data-ttu-id="bf39c-202">Func_eu_date2 (veraltet)</span><span class="sxs-lookup"><span data-stu-id="bf39c-202">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="bf39c-203">Diese Funktion ist veraltet, da Sie nur niederländische Monatsnamen unterstützt, die jetzt in der `Func_eu_date` obigen Funktion enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bf39c-203">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="bf39c-p111">Diese Funktion sucht nach einem Datum im Format, das häufig in Niederländisch verwendet wird. Das Format für diese Funktion ist identisch `Func_eu_date`, unterscheidet sich nur in der verwendeten Sprache.</span><span class="sxs-lookup"><span data-stu-id="bf39c-p111">This function looks for a date in the format commonly used in Dutch. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="bf39c-206">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="bf39c-206">Examples:</span></span>
  
- <span data-ttu-id="bf39c-207">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-207">2 Mei 2016</span></span>
    
- <span data-ttu-id="bf39c-208">02 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-208">02 mei 2016</span></span>
    
- <span data-ttu-id="bf39c-209">2 Mei 16</span><span class="sxs-lookup"><span data-stu-id="bf39c-209">2 Mei 16</span></span>
    
- <span data-ttu-id="bf39c-210">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-210">2/12/2016</span></span>
    
- <span data-ttu-id="bf39c-211">02/12/16</span><span class="sxs-lookup"><span data-stu-id="bf39c-211">02/12/16</span></span>
    
- <span data-ttu-id="bf39c-212">2-Mei-2016</span><span class="sxs-lookup"><span data-stu-id="bf39c-212">2-Mei-2016</span></span>
    
- <span data-ttu-id="bf39c-213">2-12-16</span><span class="sxs-lookup"><span data-stu-id="bf39c-213">2-12-16</span></span>
    
<span data-ttu-id="bf39c-214">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="bf39c-214">Accepted month names:</span></span>
  
- <span data-ttu-id="bf39c-215">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="bf39c-215">Dutch</span></span>
    
  - <span data-ttu-id="bf39c-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="bf39c-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="bf39c-217">Jan Feb maart Apr Mei Jun Jul Aug Sep Sept Okt Okt Nov Dez</span><span class="sxs-lookup"><span data-stu-id="bf39c-217">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
## <a name="funcexpirationdate"></a><span data-ttu-id="bf39c-218">Func_expiration_date</span><span class="sxs-lookup"><span data-stu-id="bf39c-218">Func_expiration_date</span></span>

<span data-ttu-id="bf39c-p112">Diese Funktion sucht nach einem Datum in den Formaten, die häufig von Kredit-und Debitkarten verwendet werden, die Tage für Monate ausschließen. Diese Funktion entspricht Datumsangaben im Format "month/year", "month-year", "[Month Name] Year" und "[month Abkürzung] Year". Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="bf39c-p112">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months. This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="bf39c-222">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf39c-222">Examples:</span></span>
  
- <span data-ttu-id="bf39c-223">MM/JJ – z. B. 01/11 oder 1/11</span><span class="sxs-lookup"><span data-stu-id="bf39c-223">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="bf39c-224">MM/JJJJ – z. B. 01/2011 oder 1/2011</span><span class="sxs-lookup"><span data-stu-id="bf39c-224">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="bf39c-225">MM-JJ – z. B. 01-22 oder 1-11</span><span class="sxs-lookup"><span data-stu-id="bf39c-225">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="bf39c-226">MM-JJJJ – z. B. 01-2000 oder 1-2000</span><span class="sxs-lookup"><span data-stu-id="bf39c-226">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="bf39c-227">Die folgenden Formate unterstützen JJ oder JJJJ:</span><span class="sxs-lookup"><span data-stu-id="bf39c-227">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="bf39c-228">Monat-JJJJ – z. B. Jan-2010 oder Januar-2010 Jan-10 oder Januar-10</span><span class="sxs-lookup"><span data-stu-id="bf39c-228">Month-YYYY -- for example, .Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="bf39c-229">Monat JJJJ – z. B. 'Januar 2010' oder 'Jan 2010' oder '10 Januar' oder 'Jan 10'</span><span class="sxs-lookup"><span data-stu-id="bf39c-229">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="bf39c-230">MonatJJJJ – zum Beispiel, 'Januar2010' oder 'Jan2010' oder 'Januar10' oder 'Jan10'</span><span class="sxs-lookup"><span data-stu-id="bf39c-230">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="bf39c-231">Month/YYYY--beispielsweise ' Januar/2010 ' oder ' Jan/2010 ' oder ' Januar/10 ' oder ' Jan/10 '</span><span class="sxs-lookup"><span data-stu-id="bf39c-231">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="bf39c-232">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="bf39c-232">Accepted month names:</span></span>
  
- <span data-ttu-id="bf39c-233">Englisch</span><span class="sxs-lookup"><span data-stu-id="bf39c-233">English</span></span>
    
  - <span data-ttu-id="bf39c-234">Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="bf39c-234">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="bf39c-235">Jan Feb Mär Apr Mai Juni Juli Aug Sep Okt Nov Dez</span><span class="sxs-lookup"><span data-stu-id="bf39c-235">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="funcusaddress"></a><span data-ttu-id="bf39c-236">Func_us_address</span><span class="sxs-lookup"><span data-stu-id="bf39c-236">Func_us_address</span></span>

<span data-ttu-id="bf39c-p113">Diese Funktion sucht nach dem Namen eines Bundesstaats in den USA oder nach einer postalischen Abkürzung, gefolgt von einer gültigen Postleitzahl, wie sie in Postanschriften verwendet werden. Die Postleitzahl muss eine der richtigen Postleitzahlen sein, die dem Namen des Bundesstaats in den USA oder der Abkürzung zugeordnet ist. Der Name des Bundesstaats in den USA und die Postleitzahl können nicht durch Zeichensetzung oder Buchstaben getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="bf39c-p113">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they are used in postal addresses. The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation. The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="bf39c-240">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="bf39c-240">Examples:</span></span>
  
- <span data-ttu-id="bf39c-241">	Washington 98052</span><span class="sxs-lookup"><span data-stu-id="bf39c-241">Washington 98052</span></span>
    
- <span data-ttu-id="bf39c-242">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="bf39c-242">Washington 98052-9998</span></span>
    
- <span data-ttu-id="bf39c-243">	WA 98052</span><span class="sxs-lookup"><span data-stu-id="bf39c-243">WA 98052</span></span>
    
- <span data-ttu-id="bf39c-244">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="bf39c-244">WA 98052-9998</span></span>
    

