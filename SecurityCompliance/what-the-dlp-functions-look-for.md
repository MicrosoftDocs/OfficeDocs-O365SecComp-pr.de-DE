---
title: Wonach die DLP-Funktionen suchen
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: Arten der vertraulichen Informationen, suchen Sie nach einem bestimmten Muster und vorgetragenen bestätigen sie durch Sicherstellen der ordnungsgemäßen Formatierung, durchsetzen Prüfsumme und relevante Schlüsselwörter oder sonstigen Informationen gesucht. Einige dieser Funktionen erfolgt über interne Funktionen. In diesem Thema wird erläutert, was diese Funktionen für, aussehen, um Ihnen zu verdeutlichen, wie die Arten vordefinierter vertrauliche Informationen funktionieren.
ms.openlocfilehash: 510f98e2b4e1d2480550f11026cf445be6ffc931
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013759"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="90116-105">Wonach die DLP-Funktionen suchen</span><span class="sxs-lookup"><span data-stu-id="90116-105">What the DLP functions look for</span></span>

<span data-ttu-id="90116-p102">Schutz vor Datenverlust (Data Loss Prevention, DLP) umfasst Typen vertraulicher Informationen, wie z. B. Kreditkartennummern und EC-Kartennummern, die in Ihren DLP-Richtlinien verwendet werden können. Diese Typen vertraulicher Informationen suchen nach einem bestimmten Muster und bestätigen sie durch Sicherstellen der ordnungsgemäßen Formatierung, durch Erzwingen von Prüfsummen und durch Suchen nach relevanten Schüsselwörtern oder anderen Informationen. Einige dieser Funktionen werden durch interne Funktionen ausgeführt. Der Typ vertraulicher Informationen für die Kreditkartennummer verwendet beispielsweise eine Funktion für die Suche nach Datumsangaben, die wie ein Ablaufdatum formatiert sind, um zu bestätigen, dass es sich bei einer Nummer um eine Kreditkartennummer handelt.</span><span class="sxs-lookup"><span data-stu-id="90116-p102">Data loss prevention (DLP) includes sensitive information types, such as Credit Card Number and EU Debit Card Number, which are ready for you to use in your DLP policies. These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information. Some of this functionality is performed by internal functions. For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="90116-p103">In diesem Thema wird erläutert, wie diese Funktionen vorgehen, um die Funktionsweise der vordefinierten Typen vertraulicher Informationen besser zu verstehen. Weitere Informationen finden Sie unter [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="90116-p103">This topic explains what these functions look for, to help you understand how the predefined sensitive information types work. For more information, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="funcusdate"></a><span data-ttu-id="90116-112">Func_us_date</span><span class="sxs-lookup"><span data-stu-id="90116-112">Func_us_date</span></span>

<span data-ttu-id="90116-p104">Diese Funktion sucht nach einem Datum im Format in den USA häufig verwendet Dazu gehören die Formate "Tag/Monat/Jahr", "Monat-Tag-Jahr" und "Monat-Tag-Jahr". Die Namen oder Abkürzungen Monate sind nicht zwischen Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="90116-p104">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ". The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="90116-115">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="90116-115">Examples:</span></span>
  
- <span data-ttu-id="90116-116">2 Dezember 2016</span><span class="sxs-lookup"><span data-stu-id="90116-116">December 2, 2016</span></span>
    
- <span data-ttu-id="90116-117">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="90116-117">Dec 2, 2016</span></span>
    
- <span data-ttu-id="90116-118">Dez 02 2016</span><span class="sxs-lookup"><span data-stu-id="90116-118">dec 02 2016</span></span>
    
- <span data-ttu-id="90116-119">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="90116-119">12/2/2016</span></span>
    
- <span data-ttu-id="90116-120">12/02/16</span><span class="sxs-lookup"><span data-stu-id="90116-120">12/02/16</span></span>
    
- <span data-ttu-id="90116-121">Dez-2-2016</span><span class="sxs-lookup"><span data-stu-id="90116-121">Dec-2-2016</span></span>
    
- <span data-ttu-id="90116-122">12-2-16</span><span class="sxs-lookup"><span data-stu-id="90116-122">12-2-16</span></span>
    
<span data-ttu-id="90116-123">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="90116-123">Accepted month names:</span></span>
  
- <span data-ttu-id="90116-124">Englisch</span><span class="sxs-lookup"><span data-stu-id="90116-124">English</span></span>
    
  - <span data-ttu-id="90116-125">Januar, Februar, Mai März, April, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="90116-125">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="90116-126">Januar Februar März April Mai Juni Juli August September Oktober November Dezember.</span><span class="sxs-lookup"><span data-stu-id="90116-126">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="funceudate"></a><span data-ttu-id="90116-127">Func_eu_date</span><span class="sxs-lookup"><span data-stu-id="90116-127">Func_eu_date</span></span>

<span data-ttu-id="90116-p105">Diese Funktion sucht nach einem Datum im häufig in der EU (und in den meisten Ländern außerhalb der USA) verwendeten Format. Dies umfasst die Formate „Tag/Monat/Jahr“, „Tag-Monat-Jahr“ und „Tag Monat Jahr“. Die Namen oder Abkürzungen der Monate unterscheiden nicht nach Groß- und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="90116-p105">This function looks for a date in the format commonly used in the E.U. (and most places outside the U.S.). This includes the formats "day/month/year", "day-month-year", and "day month year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="90116-132">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="90116-132">Examples:</span></span>
  
- <span data-ttu-id="90116-133">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="90116-133">2 Dec 2016</span></span>
    
- <span data-ttu-id="90116-134">02 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="90116-134">02 dec 2016</span></span>
    
- <span data-ttu-id="90116-135">2 Dez 16</span><span class="sxs-lookup"><span data-stu-id="90116-135">2 Dec 16</span></span>
    
- <span data-ttu-id="90116-136">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="90116-136">2/12/2016</span></span>
    
- <span data-ttu-id="90116-137">02/12/16</span><span class="sxs-lookup"><span data-stu-id="90116-137">02/12/16</span></span>
    
- <span data-ttu-id="90116-138">2 – Dez-2016</span><span class="sxs-lookup"><span data-stu-id="90116-138">2-Dec-2016</span></span>
    
- <span data-ttu-id="90116-139">2-12-16</span><span class="sxs-lookup"><span data-stu-id="90116-139">2-12-16</span></span>
    
<span data-ttu-id="90116-140">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="90116-140">Accepted month names:</span></span>
  
- <span data-ttu-id="90116-141">Englisch</span><span class="sxs-lookup"><span data-stu-id="90116-141">English</span></span>
    
  - <span data-ttu-id="90116-142">Januar, Februar, Mai März, April, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="90116-142">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="90116-143">Januar Februar März April Mai Juni Juli August September Oktober November Dezember.</span><span class="sxs-lookup"><span data-stu-id="90116-143">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="90116-144">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="90116-144">Dutch</span></span>
    
  - <span data-ttu-id="90116-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="90116-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="90116-146">Jan Februar Maart Apr Mei Juni, Juli August Sep September OAT Okt November (dezimal)</span><span class="sxs-lookup"><span data-stu-id="90116-146">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="90116-147">Französisch</span><span class="sxs-lookup"><span data-stu-id="90116-147">French</span></span>
    
  - <span data-ttu-id="90116-148">Uhrzeitanzeige, Février, Mars, Avril, Mai, Juin Juillet, Août, Septembre, Octobre, Novembre, Dezember</span><span class="sxs-lookup"><span data-stu-id="90116-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="90116-p106">Janv. Févr. MAR Avril Mai Juin Juil. Août September. Oktober November. Déc.</span><span class="sxs-lookup"><span data-stu-id="90116-p106">janv. févr. mars avril mai juin juil. août sept. oct. nov. déc.</span></span>
    
- <span data-ttu-id="90116-156">Deutsch</span><span class="sxs-lookup"><span data-stu-id="90116-156">German</span></span>
    
  - <span data-ttu-id="90116-157">Jänuar deutscher, März, April, Mai, Juni Juli, August, September, h., November, Dezember</span><span class="sxs-lookup"><span data-stu-id="90116-157">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="90116-p107">Jan. / Jän. Februar März April Mai Juni Juli August September Okt. Dez November.</span><span class="sxs-lookup"><span data-stu-id="90116-p107">Jan./Jän. Feb. März Apr. Mai Juni Juli Aug. Sept. Okt. Nov. Dez.</span></span>
    
- <span data-ttu-id="90116-161">Italienisch</span><span class="sxs-lookup"><span data-stu-id="90116-161">Italian</span></span>
    
  - <span data-ttu-id="90116-162">Gennaio, Febbraio, Marzo, Aprile, Maggio, Giugno, Luglio, Agosto, Settembre, Ottobre, Novembre, dicembre</span><span class="sxs-lookup"><span data-stu-id="90116-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="90116-p108">Dänemarks. Febbr. Mrz. APR. Magg. Giugno Luglio ag. festlegen. Ott. November. DIC.</span><span class="sxs-lookup"><span data-stu-id="90116-p108">genn. febbr. mar. apr. magg. giugno luglio ag. sett. ott. nov. dic.</span></span>
    
- <span data-ttu-id="90116-173">Portugiesisch</span><span class="sxs-lookup"><span data-stu-id="90116-173">Portuguese</span></span>
    
  - <span data-ttu-id="90116-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="90116-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="90116-175">Jan Fev Mrz Abr Mai Juni, Juli vor November Dez dargelegten</span><span class="sxs-lookup"><span data-stu-id="90116-175">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="90116-176">Spanisch</span><span class="sxs-lookup"><span data-stu-id="90116-176">Spanish</span></span>
    
  - <span data-ttu-id="90116-177">Enero, Febrero, Marzo, Abril, Mayo, Junio, Julio, Agosto, Septiembre, Octubre, Noviembre, diciembre</span><span class="sxs-lookup"><span data-stu-id="90116-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="90116-p109">Enero Februar. Marzo abr. Mayo Uhr angezeigt Juli. Agosto September/festlegen. Oktober November. DIC.</span><span class="sxs-lookup"><span data-stu-id="90116-p109">enero feb. marzo abr. mayo jun. jul. agosto sept./set. oct. nov. dic.</span></span>
    
## <a name="funceudate1-deprecated"></a><span data-ttu-id="90116-186">Func_eu_date1 (veraltet)</span><span class="sxs-lookup"><span data-stu-id="90116-186">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="90116-187">Diese Funktion ist veraltet, da es nur Portugiesisch Monatsnamen unterstützt, die nun in enthalten sind die `Func_eu_date` Funktion oben.</span><span class="sxs-lookup"><span data-stu-id="90116-187">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="90116-p110">Diese Funktion sucht nach einem Datum im Format häufig verwendet für Portugiesisch. Das Format für diese Funktion ist identisch mit `Func_eu_date`, unterschiedliche nur in der Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="90116-p110">This function looks for a date in the format commonly used in Portuguese. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="90116-190">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="90116-190">Examples:</span></span>
  
- <span data-ttu-id="90116-191">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="90116-191">2 Dez 2016</span></span>
    
- <span data-ttu-id="90116-192">02 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="90116-192">02 dez 2016</span></span>
    
- <span data-ttu-id="90116-193">2 Dez 16</span><span class="sxs-lookup"><span data-stu-id="90116-193">2 Dez 16</span></span>
    
- <span data-ttu-id="90116-194">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="90116-194">2/12/2016</span></span>
    
- <span data-ttu-id="90116-195">02/12/16</span><span class="sxs-lookup"><span data-stu-id="90116-195">02/12/16</span></span>
    
- <span data-ttu-id="90116-196">2 – Dez-2016</span><span class="sxs-lookup"><span data-stu-id="90116-196">2-Dez-2016</span></span>
    
- <span data-ttu-id="90116-197">2-12-16</span><span class="sxs-lookup"><span data-stu-id="90116-197">2-12-16</span></span>
    
<span data-ttu-id="90116-198">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="90116-198">Accepted month names:</span></span>
  
- <span data-ttu-id="90116-199">Portugiesisch</span><span class="sxs-lookup"><span data-stu-id="90116-199">Portuguese</span></span>
    
  - <span data-ttu-id="90116-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="90116-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="90116-201">Jan Fev Mrz Abr Mai Juni, Juli vor November Dez dargelegten</span><span class="sxs-lookup"><span data-stu-id="90116-201">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="funceudate2-deprecated"></a><span data-ttu-id="90116-202">Func_eu_date2 (veraltet)</span><span class="sxs-lookup"><span data-stu-id="90116-202">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="90116-203">Diese Funktion ist veraltet, da es nur niederländische Monatsnamen unterstützt, die nun in enthalten sind die `Func_eu_date` Funktion oben.</span><span class="sxs-lookup"><span data-stu-id="90116-203">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="90116-p111">Diese Funktion sucht nach einem Datum im Format häufig verwendet für Niederländisch. Das Format für diese Funktion ist identisch mit `Func_eu_date`, unterschiedliche nur in der Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="90116-p111">This function looks for a date in the format commonly used in Dutch. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="90116-206">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="90116-206">Examples:</span></span>
  
- <span data-ttu-id="90116-207">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="90116-207">2 Mei 2016</span></span>
    
- <span data-ttu-id="90116-208">02 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="90116-208">02 mei 2016</span></span>
    
- <span data-ttu-id="90116-209">2 Mei 16</span><span class="sxs-lookup"><span data-stu-id="90116-209">2 Mei 16</span></span>
    
- <span data-ttu-id="90116-210">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="90116-210">2/12/2016</span></span>
    
- <span data-ttu-id="90116-211">02/12/16</span><span class="sxs-lookup"><span data-stu-id="90116-211">02/12/16</span></span>
    
- <span data-ttu-id="90116-212">2-Mei-2016</span><span class="sxs-lookup"><span data-stu-id="90116-212">2-Mei-2016</span></span>
    
- <span data-ttu-id="90116-213">2-12-16</span><span class="sxs-lookup"><span data-stu-id="90116-213">2-12-16</span></span>
    
<span data-ttu-id="90116-214">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="90116-214">Accepted month names:</span></span>
  
- <span data-ttu-id="90116-215">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="90116-215">Dutch</span></span>
    
  - <span data-ttu-id="90116-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="90116-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="90116-217">Jan Februar Maart Apr Mei Juni, Juli August Sep September OAT Okt November (dezimal)</span><span class="sxs-lookup"><span data-stu-id="90116-217">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
## <a name="funcexpirationdate"></a><span data-ttu-id="90116-218">Func_expiration_date</span><span class="sxs-lookup"><span data-stu-id="90116-218">Func_expiration_date</span></span>

<span data-ttu-id="90116-p112">Diese Funktion sucht nach einem Datum in den Formaten von Kredit und soll-Karten, die was die Tage zugunsten Monate ausschließen häufig verwendet. Diese Funktion entspricht Datumsangaben im Format "Monat/Jahr", "Monat-Jahr", "[Monatsname]", und "[Abkürzung für den Monat] Jahr". Die Namen oder Abkürzungen Monate sind nicht zwischen Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="90116-p112">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months. This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="90116-222">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90116-222">Examples:</span></span>
  
- <span data-ttu-id="90116-223">MM/JJ – z. B. 01/11 oder 1/11</span><span class="sxs-lookup"><span data-stu-id="90116-223">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="90116-224">MM/JJJJ – z. B. 01/2011 oder 1/2011</span><span class="sxs-lookup"><span data-stu-id="90116-224">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="90116-225">MM-JJ – z. B. 01-22 oder 1-11</span><span class="sxs-lookup"><span data-stu-id="90116-225">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="90116-226">MM-JJJJ – z. B. 01-2000 oder 1-2000</span><span class="sxs-lookup"><span data-stu-id="90116-226">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="90116-227">Die folgenden Formate unterstützen JJ oder JJJJ:</span><span class="sxs-lookup"><span data-stu-id="90116-227">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="90116-228">Monat-JJJJ – z. B. Jan-2010 oder Januar-2010 Jan-10 oder Januar-10</span><span class="sxs-lookup"><span data-stu-id="90116-228">Month-YYYY -- for example, .Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="90116-229">Monat JJJJ – z. B. 'Januar 2010' oder 'Jan 2010' oder '10 Januar' oder 'Jan 10'</span><span class="sxs-lookup"><span data-stu-id="90116-229">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="90116-230">MonatJJJJ – zum Beispiel, 'Januar2010' oder 'Jan2010' oder 'Januar10' oder 'Jan10'</span><span class="sxs-lookup"><span data-stu-id="90116-230">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="90116-231">Monat/JJJJ – beispielsweise "Januar/2010" oder "Jan/2010" oder "Januar/10" oder "Jan/10"</span><span class="sxs-lookup"><span data-stu-id="90116-231">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="90116-232">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="90116-232">Accepted month names:</span></span>
  
- <span data-ttu-id="90116-233">Englisch</span><span class="sxs-lookup"><span data-stu-id="90116-233">English</span></span>
    
  - <span data-ttu-id="90116-234">Januar, Februar, Mai März, April, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="90116-234">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="90116-235">Jan Februar Mrz Apr Mai Juni Juli August September OAT November (dezimal)</span><span class="sxs-lookup"><span data-stu-id="90116-235">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="funcusaddress"></a><span data-ttu-id="90116-236">Func_us_address</span><span class="sxs-lookup"><span data-stu-id="90116-236">Func_us_address</span></span>

<span data-ttu-id="90116-p113">Diese Funktion sucht nach dem Namen eines Bundesstaats in den USA oder nach einer postalischen Abkürzung, gefolgt von einer gültigen Postleitzahl, wie sie in Postanschriften verwendet werden. Die Postleitzahl muss eine der richtigen Postleitzahlen sein, die dem Namen des Bundesstaats in den USA oder der Abkürzung zugeordnet ist. Der Name des Bundesstaats in den USA und die Postleitzahl können nicht durch Zeichensetzung oder Buchstaben getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="90116-p113">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they are used in postal addresses. The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation. The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="90116-240">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="90116-240">Examples:</span></span>
  
- <span data-ttu-id="90116-241">	Washington 98052</span><span class="sxs-lookup"><span data-stu-id="90116-241">Washington 98052</span></span>
    
- <span data-ttu-id="90116-242">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="90116-242">Washington 98052-9998</span></span>
    
- <span data-ttu-id="90116-243">	WA 98052</span><span class="sxs-lookup"><span data-stu-id="90116-243">WA 98052</span></span>
    
- <span data-ttu-id="90116-244">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="90116-244">WA 98052-9998</span></span>
    

