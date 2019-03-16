---
title: Wonach die DLP-Funktionen suchen
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Die Typen vertraulicher Informationen suchen nach einem bestimmten Muster und bestätigen es, indem Sie eine korrekte Formatierung sicherstellen, Prüfsummen erzwingen und nach relevanten Stichwörtern oder anderen Informationen suchen. Einige dieser Funktionen werden von internen Funktionen ausgeführt. In diesem Thema wird erläutert, wonach diese Funktionen suchen, damit Sie besser verstehen, wie die vordefinierten Typen vertraulicher Informationen funktionieren.
ms.openlocfilehash: d0aeb38001f42d9db2b124466b02746ee106b078
ms.sourcegitcommit: 8657e003ab1ff49113f222d1ee8400eff174cb54
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2019
ms.locfileid: "30638932"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="deed0-105">Wonach die DLP-Funktionen suchen</span><span class="sxs-lookup"><span data-stu-id="deed0-105">What the DLP functions look for</span></span>

<span data-ttu-id="deed0-106">Data Loss Prevention (DLP) enthält vertrauliche Informationstypen wie Kreditkartennummer und EC-Debitkarte, die Sie in ihren DLP-Richtlinien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="deed0-106">Data loss prevention (DLP) includes sensitive information types, such as Credit Card Number and EU Debit Card Number, which are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="deed0-107">Diese Typen von vertraulichen Informationen suchen nach einem bestimmten Muster und bestätigen es, indem Sie eine korrekte Formatierung sicherstellen, Prüfsummen erzwingen und nach relevanten Stichwörtern oder anderen Informationen suchen.</span><span class="sxs-lookup"><span data-stu-id="deed0-107">These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information.</span></span> <span data-ttu-id="deed0-108">Einige dieser Funktionen werden von internen Funktionen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="deed0-108">Some of this functionality is performed by internal functions.</span></span> <span data-ttu-id="deed0-109">Beispielsweise verwendet der vertrauliche Informationstyp Kreditkartennummer eine Funktion, um nach Datumsangaben zu suchen, die wie ein Ablaufdatum formatiert sind, um zu bestätigen, dass eine Nummer eine Kreditkartennummer ist.</span><span class="sxs-lookup"><span data-stu-id="deed0-109">For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="deed0-110">In diesem Thema wird erläutert, wonach diese Funktionen suchen, damit Sie besser verstehen, wie die vordefinierten Typen vertraulicher Informationen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="deed0-110">This topic explains what these functions look for, to help you understand how the predefined sensitive information types work.</span></span> <span data-ttu-id="deed0-111">Weitere Informationen finden Sie unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="deed0-111">For more information, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="funcusdate"></a><span data-ttu-id="deed0-112">Func_us_date</span><span class="sxs-lookup"><span data-stu-id="deed0-112">Func_us_date</span></span>

<span data-ttu-id="deed0-113">Diese Funktion sucht nach einem Datum im allgemeinen Format, das in den USA verwendet wird. Dazu gehören die Formate "Month/Day/Year", "Month-Day-Year" und "Month Day Year".</span><span class="sxs-lookup"><span data-stu-id="deed0-113">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ".</span></span> <span data-ttu-id="deed0-114">Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="deed0-114">The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="deed0-115">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="deed0-115">Examples:</span></span>
  
- <span data-ttu-id="deed0-116">2. Dezember 2016</span><span class="sxs-lookup"><span data-stu-id="deed0-116">December 2, 2016</span></span>
    
- <span data-ttu-id="deed0-117">Dez 2, 2016</span><span class="sxs-lookup"><span data-stu-id="deed0-117">Dec 2, 2016</span></span>
    
- <span data-ttu-id="deed0-118">Dez 02 2016</span><span class="sxs-lookup"><span data-stu-id="deed0-118">dec 02 2016</span></span>
    
- <span data-ttu-id="deed0-119">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="deed0-119">12/2/2016</span></span>
    
- <span data-ttu-id="deed0-120">12/02/16</span><span class="sxs-lookup"><span data-stu-id="deed0-120">12/02/16</span></span>
    
- <span data-ttu-id="deed0-121">Dez-2-2016</span><span class="sxs-lookup"><span data-stu-id="deed0-121">Dec-2-2016</span></span>
    
- <span data-ttu-id="deed0-122">12-2-16</span><span class="sxs-lookup"><span data-stu-id="deed0-122">12-2-16</span></span>
    
<span data-ttu-id="deed0-123">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="deed0-123">Accepted month names:</span></span>
  
- <span data-ttu-id="deed0-124">Englisch</span><span class="sxs-lookup"><span data-stu-id="deed0-124">English</span></span>
    
  - <span data-ttu-id="deed0-125">Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="deed0-125">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="deed0-126">Jan. Feb. Mär. Apr. Mai Juni Juli Aug. Sep. Okt. Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="deed0-126">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="funceudate"></a><span data-ttu-id="deed0-127">Func_eu_date</span><span class="sxs-lookup"><span data-stu-id="deed0-127">Func_eu_date</span></span>

<span data-ttu-id="deed0-128">Diese Funktion sucht nach einem Datum im allgemeinen Format, das in der EU verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="deed0-128">This function looks for a date in the format commonly used in the E.U.</span></span> <span data-ttu-id="deed0-129">(und die meisten Standorte außerhalb der USA).</span><span class="sxs-lookup"><span data-stu-id="deed0-129">(and most places outside the U.S.).</span></span> <span data-ttu-id="deed0-130">Dazu gehören die Formate "Tag/Monat/Jahr", "Tag-Monat-Jahr" und "Tag Monat Jahr".</span><span class="sxs-lookup"><span data-stu-id="deed0-130">This includes the formats "day/month/year", "day-month-year", and "day month year".</span></span> <span data-ttu-id="deed0-131">Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="deed0-131">The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="deed0-132">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="deed0-132">Examples:</span></span>
  
- <span data-ttu-id="deed0-133">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="deed0-133">2 Dec 2016</span></span>
    
- <span data-ttu-id="deed0-134">02 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="deed0-134">02 dec 2016</span></span>
    
- <span data-ttu-id="deed0-135">2 Dez 16</span><span class="sxs-lookup"><span data-stu-id="deed0-135">2 Dec 16</span></span>
    
- <span data-ttu-id="deed0-136">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="deed0-136">2/12/2016</span></span>
    
- <span data-ttu-id="deed0-137">02/12/16</span><span class="sxs-lookup"><span data-stu-id="deed0-137">02/12/16</span></span>
    
- <span data-ttu-id="deed0-138">2-Dez-2016</span><span class="sxs-lookup"><span data-stu-id="deed0-138">2-Dec-2016</span></span>
    
- <span data-ttu-id="deed0-139">2-12-16</span><span class="sxs-lookup"><span data-stu-id="deed0-139">2-12-16</span></span>
    
<span data-ttu-id="deed0-140">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="deed0-140">Accepted month names:</span></span>
  
- <span data-ttu-id="deed0-141">Englisch</span><span class="sxs-lookup"><span data-stu-id="deed0-141">English</span></span>
    
  - <span data-ttu-id="deed0-142">Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="deed0-142">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="deed0-143">Jan. Feb. Mär. Apr. Mai Juni Juli Aug. Sep. Okt. Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="deed0-143">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="deed0-144">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="deed0-144">Dutch</span></span>
    
  - <span data-ttu-id="deed0-145">Januari, februari, maart, April, Mei, Juni, Juli, Augustus, September, ocktober, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="deed0-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="deed0-146">Jan Feb maart Apr Mei Jun Jul Aug Sep Sept Okt Okt Nov Dez</span><span class="sxs-lookup"><span data-stu-id="deed0-146">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="deed0-147">Französisch</span><span class="sxs-lookup"><span data-stu-id="deed0-147">French</span></span>
    
  - <span data-ttu-id="deed0-148">janvier, février, Mars, Avril, Mai, Juni juillet, août, September, Oktober, Novembre, Dezember</span><span class="sxs-lookup"><span data-stu-id="deed0-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="deed0-149">janv.</span><span class="sxs-lookup"><span data-stu-id="deed0-149">janv.</span></span> <span data-ttu-id="deed0-150">févr.</span><span class="sxs-lookup"><span data-stu-id="deed0-150">févr.</span></span> <span data-ttu-id="deed0-151">Mars Avril May juil.</span><span class="sxs-lookup"><span data-stu-id="deed0-151">mars avril mai juin juil.</span></span> <span data-ttu-id="deed0-152">août Sept.</span><span class="sxs-lookup"><span data-stu-id="deed0-152">août sept.</span></span> <span data-ttu-id="deed0-153">Okt.</span><span class="sxs-lookup"><span data-stu-id="deed0-153">oct.</span></span> <span data-ttu-id="deed0-154">Nov.</span><span class="sxs-lookup"><span data-stu-id="deed0-154">nov.</span></span> <span data-ttu-id="deed0-155">déc.</span><span class="sxs-lookup"><span data-stu-id="deed0-155">déc.</span></span>
    
- <span data-ttu-id="deed0-156">Deutsch</span><span class="sxs-lookup"><span data-stu-id="deed0-156">German</span></span>
    
  - <span data-ttu-id="deed0-157">Januar, Februar, März, April, Mai, Juni Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="deed0-157">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="deed0-158">Jan./Jän.</span><span class="sxs-lookup"><span data-stu-id="deed0-158">Jan./Jän.</span></span> <span data-ttu-id="deed0-159">Feb. März Apr. Mai Juni Juli Aug. Sept. Okt.</span><span class="sxs-lookup"><span data-stu-id="deed0-159">Feb. März Apr. Mai Juni Juli Aug. Sept. Okt.</span></span> <span data-ttu-id="deed0-160">Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="deed0-160">Nov. Dez.</span></span>
    
- <span data-ttu-id="deed0-161">Italienisch</span><span class="sxs-lookup"><span data-stu-id="deed0-161">Italian</span></span>
    
  - <span data-ttu-id="deed0-162">gennaio, febbraio, Marzo, Aprile, Maggio, Juni, Juli, Agosto, Settembre, ottobre, Novembre, Dezember</span><span class="sxs-lookup"><span data-stu-id="deed0-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="deed0-163">Genn.</span><span class="sxs-lookup"><span data-stu-id="deed0-163">genn.</span></span> <span data-ttu-id="deed0-164">febbr.</span><span class="sxs-lookup"><span data-stu-id="deed0-164">febbr.</span></span> <span data-ttu-id="deed0-165">Mar.</span><span class="sxs-lookup"><span data-stu-id="deed0-165">mar.</span></span> <span data-ttu-id="deed0-166">Apr.</span><span class="sxs-lookup"><span data-stu-id="deed0-166">apr.</span></span> <span data-ttu-id="deed0-167">Magg.</span><span class="sxs-lookup"><span data-stu-id="deed0-167">magg.</span></span> <span data-ttu-id="deed0-168">Juni Juli AG.</span><span class="sxs-lookup"><span data-stu-id="deed0-168">giugno luglio ag.</span></span> <span data-ttu-id="deed0-169">Sett.</span><span class="sxs-lookup"><span data-stu-id="deed0-169">sett.</span></span> <span data-ttu-id="deed0-170">Ott.</span><span class="sxs-lookup"><span data-stu-id="deed0-170">ott.</span></span> <span data-ttu-id="deed0-171">Nov.</span><span class="sxs-lookup"><span data-stu-id="deed0-171">nov.</span></span> <span data-ttu-id="deed0-172">DIC.</span><span class="sxs-lookup"><span data-stu-id="deed0-172">dic.</span></span>
    
- <span data-ttu-id="deed0-173">Portugiesisch</span><span class="sxs-lookup"><span data-stu-id="deed0-173">Portuguese</span></span>
    
  - <span data-ttu-id="deed0-174">Janeiro, Fevereiro, Março, Marco, Abril, Maio, Junho, Julho, Agosto, Setembro, Outubro, Novembro, Dezembro</span><span class="sxs-lookup"><span data-stu-id="deed0-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="deed0-175">Jan FEV Mar ABR Mai Jun Jul ago Set out Nov Dez</span><span class="sxs-lookup"><span data-stu-id="deed0-175">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="deed0-176">Spanisch</span><span class="sxs-lookup"><span data-stu-id="deed0-176">Spanish</span></span>
    
  - <span data-ttu-id="deed0-177">enero, Febrero, Marzo, Abril, Mayo, junio, Julio, Agosto, Septiembre, Octubre, Noviembre, Diciembre</span><span class="sxs-lookup"><span data-stu-id="deed0-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="deed0-178">enero Feb.</span><span class="sxs-lookup"><span data-stu-id="deed0-178">enero feb.</span></span> <span data-ttu-id="deed0-179">Marzo ABR.</span><span class="sxs-lookup"><span data-stu-id="deed0-179">marzo abr.</span></span> <span data-ttu-id="deed0-180">Mayo Jun.</span><span class="sxs-lookup"><span data-stu-id="deed0-180">mayo jun.</span></span> <span data-ttu-id="deed0-181">Juli.</span><span class="sxs-lookup"><span data-stu-id="deed0-181">jul.</span></span> <span data-ttu-id="deed0-182">Agosto Sept./Set.</span><span class="sxs-lookup"><span data-stu-id="deed0-182">agosto sept./set.</span></span> <span data-ttu-id="deed0-183">Okt.</span><span class="sxs-lookup"><span data-stu-id="deed0-183">oct.</span></span> <span data-ttu-id="deed0-184">Nov.</span><span class="sxs-lookup"><span data-stu-id="deed0-184">nov.</span></span> <span data-ttu-id="deed0-185">DIC.</span><span class="sxs-lookup"><span data-stu-id="deed0-185">dic.</span></span>
    
## <a name="funceudate1-deprecated"></a><span data-ttu-id="deed0-186">Func_eu_date1 (veraltet)</span><span class="sxs-lookup"><span data-stu-id="deed0-186">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="deed0-187">Diese Funktion ist veraltet, da Sie nur portugiesische Monatsnamen unterstützt, die jetzt in der `Func_eu_date` obigen Funktion enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="deed0-187">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="deed0-188">Diese Funktion sucht nach einem Datum im Format, das häufig in Portugiesisch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="deed0-188">This function looks for a date in the format commonly used in Portuguese.</span></span> <span data-ttu-id="deed0-189">Das Format für diese Funktion ist identisch `Func_eu_date`, unterscheidet sich nur in der verwendeten Sprache.</span><span class="sxs-lookup"><span data-stu-id="deed0-189">The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="deed0-190">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="deed0-190">Examples:</span></span>
  
- <span data-ttu-id="deed0-191">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="deed0-191">2 Dez 2016</span></span>
    
- <span data-ttu-id="deed0-192">02 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="deed0-192">02 dez 2016</span></span>
    
- <span data-ttu-id="deed0-193">2 Dez 16</span><span class="sxs-lookup"><span data-stu-id="deed0-193">2 Dez 16</span></span>
    
- <span data-ttu-id="deed0-194">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="deed0-194">2/12/2016</span></span>
    
- <span data-ttu-id="deed0-195">02/12/16</span><span class="sxs-lookup"><span data-stu-id="deed0-195">02/12/16</span></span>
    
- <span data-ttu-id="deed0-196">2-Dez-2016</span><span class="sxs-lookup"><span data-stu-id="deed0-196">2-Dez-2016</span></span>
    
- <span data-ttu-id="deed0-197">2-12-16</span><span class="sxs-lookup"><span data-stu-id="deed0-197">2-12-16</span></span>
    
<span data-ttu-id="deed0-198">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="deed0-198">Accepted month names:</span></span>
  
- <span data-ttu-id="deed0-199">Portugiesisch</span><span class="sxs-lookup"><span data-stu-id="deed0-199">Portuguese</span></span>
    
  - <span data-ttu-id="deed0-200">Janeiro, Fevereiro, Março, Marco, Abril, Maio, Junho, Julho, Agosto, Setembro, Outubro, Novembro, Dezembro</span><span class="sxs-lookup"><span data-stu-id="deed0-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="deed0-201">Jan FEV Mar ABR Mai Jun Jul ago Set out Nov Dez</span><span class="sxs-lookup"><span data-stu-id="deed0-201">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="funceudate2-deprecated"></a><span data-ttu-id="deed0-202">Func_eu_date2 (veraltet)</span><span class="sxs-lookup"><span data-stu-id="deed0-202">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="deed0-203">Diese Funktion ist veraltet, da Sie nur niederländische Monatsnamen unterstützt, die jetzt in der `Func_eu_date` obigen Funktion enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="deed0-203">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="deed0-204">Diese Funktion sucht nach einem Datum im Format, das häufig in Niederländisch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="deed0-204">This function looks for a date in the format commonly used in Dutch.</span></span> <span data-ttu-id="deed0-205">Das Format für diese Funktion ist identisch `Func_eu_date`, unterscheidet sich nur in der verwendeten Sprache.</span><span class="sxs-lookup"><span data-stu-id="deed0-205">The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="deed0-206">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="deed0-206">Examples:</span></span>
  
- <span data-ttu-id="deed0-207">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="deed0-207">2 Mei 2016</span></span>
    
- <span data-ttu-id="deed0-208">02 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="deed0-208">02 mei 2016</span></span>
    
- <span data-ttu-id="deed0-209">2 Mei 16</span><span class="sxs-lookup"><span data-stu-id="deed0-209">2 Mei 16</span></span>
    
- <span data-ttu-id="deed0-210">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="deed0-210">2/12/2016</span></span>
    
- <span data-ttu-id="deed0-211">02/12/16</span><span class="sxs-lookup"><span data-stu-id="deed0-211">02/12/16</span></span>
    
- <span data-ttu-id="deed0-212">2-Mei-2016</span><span class="sxs-lookup"><span data-stu-id="deed0-212">2-Mei-2016</span></span>
    
- <span data-ttu-id="deed0-213">2-12-16</span><span class="sxs-lookup"><span data-stu-id="deed0-213">2-12-16</span></span>
    
<span data-ttu-id="deed0-214">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="deed0-214">Accepted month names:</span></span>
  
- <span data-ttu-id="deed0-215">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="deed0-215">Dutch</span></span>
    
  - <span data-ttu-id="deed0-216">Januari, februari, maart, April, Mei, Juni, Juli, Augustus, September, ocktober, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="deed0-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="deed0-217">Jan Feb maart Apr Mei Jun Jul Aug Sep Sept Okt Okt Nov Dez</span><span class="sxs-lookup"><span data-stu-id="deed0-217">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
## <a name="funcexpirationdate"></a><span data-ttu-id="deed0-218">Func_expiration_date</span><span class="sxs-lookup"><span data-stu-id="deed0-218">Func_expiration_date</span></span>

<span data-ttu-id="deed0-219">Diese Funktion sucht nach einem Datum in den Formaten, die häufig von Kredit-und Debitkarten verwendet werden, die Tage für Monate ausschließen.</span><span class="sxs-lookup"><span data-stu-id="deed0-219">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months.</span></span> <span data-ttu-id="deed0-220">Diese Funktion entspricht Datumsangaben im Format "month/year", "month-year", "[Month Name] Year" und "[month Abkürzung] Year".</span><span class="sxs-lookup"><span data-stu-id="deed0-220">This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year".</span></span> <span data-ttu-id="deed0-221">Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="deed0-221">The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="deed0-222">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="deed0-222">Examples:</span></span>
  
- <span data-ttu-id="deed0-223">MM/JJ--Beispiel: 01/11 oder 1/11</span><span class="sxs-lookup"><span data-stu-id="deed0-223">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="deed0-224">MM/YYYY--zum Beispiel 01/2011 oder 1/2011</span><span class="sxs-lookup"><span data-stu-id="deed0-224">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="deed0-225">MM-YY--zum Beispiel 01-22 oder 1-11</span><span class="sxs-lookup"><span data-stu-id="deed0-225">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="deed0-226">MM-YYYY--zum Beispiel 01-2000 oder 1-2000</span><span class="sxs-lookup"><span data-stu-id="deed0-226">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="deed0-227">Die folgenden Formate unterstützen YY oder YYYY:</span><span class="sxs-lookup"><span data-stu-id="deed0-227">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="deed0-228">Month-YYYY--zum Beispiel,. Jan-2010 oder Januar-2010 oder Jan-10 oder Januar-10</span><span class="sxs-lookup"><span data-stu-id="deed0-228">Month-YYYY -- for example, .Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="deed0-229">Monat YYYY--Beispiel: ' Januar 2010 ' oder ' Jan 2010 ' oder ' Januar 10 ' oder ' Jan 10 '</span><span class="sxs-lookup"><span data-stu-id="deed0-229">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="deed0-230">Monatjjjj--beispielsweise "january2010" oder "Jan2010" oder "january10" oder "Jan10"</span><span class="sxs-lookup"><span data-stu-id="deed0-230">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="deed0-231">Month/YYYY--beispielsweise ' Januar/2010 ' oder ' Jan/2010 ' oder ' Januar/10 ' oder ' Jan/10 '</span><span class="sxs-lookup"><span data-stu-id="deed0-231">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="deed0-232">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="deed0-232">Accepted month names:</span></span>
  
- <span data-ttu-id="deed0-233">Englisch</span><span class="sxs-lookup"><span data-stu-id="deed0-233">English</span></span>
    
  - <span data-ttu-id="deed0-234">Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="deed0-234">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="deed0-235">Jan Feb Mär Apr Mai Juni Juli Aug Sep Okt Nov Dez</span><span class="sxs-lookup"><span data-stu-id="deed0-235">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="funcusaddress"></a><span data-ttu-id="deed0-236">Func_us_address</span><span class="sxs-lookup"><span data-stu-id="deed0-236">Func_us_address</span></span>

<span data-ttu-id="deed0-237">Diese Funktion sucht nach einem US-Bundesstaat oder einer postalischen Abkürzung gefolgt von einer gültigen Postleitzahl, genau wie Sie in Postanschriften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="deed0-237">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they are used in postal addresses.</span></span> <span data-ttu-id="deed0-238">Bei der Postleitzahl muss es sich um einen der korrekten Postleitzahlen handeln, die dem US-Bundesstaat oder der Abkürzung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="deed0-238">The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation.</span></span> <span data-ttu-id="deed0-239">Der US-Bundesstaat und die Postleitzahl dürfen nicht durch Interpunktion oder Buchstaben getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="deed0-239">The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="deed0-240">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="deed0-240">Examples:</span></span>
  
- <span data-ttu-id="deed0-241">Washington 98052</span><span class="sxs-lookup"><span data-stu-id="deed0-241">Washington 98052</span></span>
    
- <span data-ttu-id="deed0-242">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="deed0-242">Washington 98052-9998</span></span>
    
- <span data-ttu-id="deed0-243">WA 98052</span><span class="sxs-lookup"><span data-stu-id="deed0-243">WA 98052</span></span>
    
- <span data-ttu-id="deed0-244">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="deed0-244">WA 98052-9998</span></span>
    

