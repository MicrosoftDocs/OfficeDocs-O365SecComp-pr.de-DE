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
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Die Typen vertraulicher Informationen suchen nach einem bestimmten Muster und bestätigen es, indem Sie eine korrekte Formatierung sicherstellen, Prüfsummen erzwingen und nach relevanten Stichwörtern oder anderen Informationen suchen. Einige dieser Funktionen werden von internen Funktionen ausgeführt. In diesem Thema wird erläutert, wonach diese Funktionen suchen, damit Sie besser verstehen, wie die vordefinierten Typen vertraulicher Informationen funktionieren.
ms.openlocfilehash: 4cc6f4d27e106aeedb2fa8cae0f3634b9e3d6319
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410550"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="5d7bd-105">Wonach die DLP-Funktionen suchen</span><span class="sxs-lookup"><span data-stu-id="5d7bd-105">What the DLP functions look for</span></span>

<span data-ttu-id="5d7bd-106">Data Loss Prevention (DLP) enthält vertrauliche Informationstypen wie Kreditkartennummer und EC-Debitkarte, die Sie in ihren DLP-Richtlinien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-106">Data loss prevention (DLP) includes sensitive information types, such as Credit Card Number and EU Debit Card Number, which are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="5d7bd-107">Diese Typen von vertraulichen Informationen suchen nach einem bestimmten Muster und bestätigen es, indem Sie eine korrekte Formatierung sicherstellen, Prüfsummen erzwingen und nach relevanten Stichwörtern oder anderen Informationen suchen.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-107">These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information.</span></span> <span data-ttu-id="5d7bd-108">Einige dieser Funktionen werden von internen Funktionen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-108">Some of this functionality is performed by internal functions.</span></span> <span data-ttu-id="5d7bd-109">Beispielsweise verwendet der vertrauliche Informationstyp Kreditkartennummer eine Funktion, um nach Datumsangaben zu suchen, die wie ein Ablaufdatum formatiert sind, um zu bestätigen, dass eine Nummer eine Kreditkartennummer ist.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-109">For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="5d7bd-110">In diesem Thema wird erläutert, wonach diese Funktionen suchen, damit Sie besser verstehen, wie die vordefinierten Typen vertraulicher Informationen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-110">This topic explains what these functions look for, to help you understand how the predefined sensitive information types work.</span></span> <span data-ttu-id="5d7bd-111">Weitere Informationen finden Sie unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="5d7bd-111">For more information, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="funcusdate"></a><span data-ttu-id="5d7bd-112">Func_us_date</span><span class="sxs-lookup"><span data-stu-id="5d7bd-112">Func_us_date</span></span>

<span data-ttu-id="5d7bd-113">Diese Funktion sucht nach einem Datum im allgemeinen Format, das in den USA verwendet wird. Dazu gehören die Formate "Month/Day/Year", "Month-Day-Year" und "Month Day Year".</span><span class="sxs-lookup"><span data-stu-id="5d7bd-113">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ".</span></span> <span data-ttu-id="5d7bd-114">Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-114">The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="5d7bd-115">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-115">Examples:</span></span>
  
- <span data-ttu-id="5d7bd-116">2. Dezember 2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-116">December 2, 2016</span></span>
    
- <span data-ttu-id="5d7bd-117">Dez 2, 2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-117">Dec 2, 2016</span></span>
    
- <span data-ttu-id="5d7bd-118">Dez 02 2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-118">dec 02 2016</span></span>
    
- <span data-ttu-id="5d7bd-119">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-119">12/2/2016</span></span>
    
- <span data-ttu-id="5d7bd-120">12/02/16</span><span class="sxs-lookup"><span data-stu-id="5d7bd-120">12/02/16</span></span>
    
- <span data-ttu-id="5d7bd-121">Dez-2-2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-121">Dec-2-2016</span></span>
    
- <span data-ttu-id="5d7bd-122">12-2-16</span><span class="sxs-lookup"><span data-stu-id="5d7bd-122">12-2-16</span></span>
    
<span data-ttu-id="5d7bd-123">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-123">Accepted month names:</span></span>
  
- <span data-ttu-id="5d7bd-124">Englisch</span><span class="sxs-lookup"><span data-stu-id="5d7bd-124">English</span></span>
    
  - <span data-ttu-id="5d7bd-125">Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="5d7bd-125">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="5d7bd-126">Jan. Feb. Mär. Apr. Mai Juni Juli Aug. Sep. Okt. Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-126">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="funceudate"></a><span data-ttu-id="5d7bd-127">Func_eu_date</span><span class="sxs-lookup"><span data-stu-id="5d7bd-127">Func_eu_date</span></span>

<span data-ttu-id="5d7bd-128">Diese Funktion sucht nach einem Datum im allgemeinen Format, das in der EU verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-128">This function looks for a date in the format commonly used in the E.U.</span></span> <span data-ttu-id="5d7bd-129">(und die meisten Standorte außerhalb der USA).</span><span class="sxs-lookup"><span data-stu-id="5d7bd-129">(and most places outside the U.S.).</span></span> <span data-ttu-id="5d7bd-130">Dazu gehören die Formate "Tag/Monat/Jahr", "Tag-Monat-Jahr" und "Tag Monat Jahr".</span><span class="sxs-lookup"><span data-stu-id="5d7bd-130">This includes the formats "day/month/year", "day-month-year", and "day month year".</span></span> <span data-ttu-id="5d7bd-131">Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-131">The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="5d7bd-132">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-132">Examples:</span></span>
  
- <span data-ttu-id="5d7bd-133">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-133">2 Dec 2016</span></span>
    
- <span data-ttu-id="5d7bd-134">02 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-134">02 dec 2016</span></span>
    
- <span data-ttu-id="5d7bd-135">2 Dez 16</span><span class="sxs-lookup"><span data-stu-id="5d7bd-135">2 Dec 16</span></span>
    
- <span data-ttu-id="5d7bd-136">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-136">2/12/2016</span></span>
    
- <span data-ttu-id="5d7bd-137">02/12/16</span><span class="sxs-lookup"><span data-stu-id="5d7bd-137">02/12/16</span></span>
    
- <span data-ttu-id="5d7bd-138">2-Dez-2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-138">2-Dec-2016</span></span>
    
- <span data-ttu-id="5d7bd-139">2-12-16</span><span class="sxs-lookup"><span data-stu-id="5d7bd-139">2-12-16</span></span>
    
<span data-ttu-id="5d7bd-140">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-140">Accepted month names:</span></span>
  
- <span data-ttu-id="5d7bd-141">Englisch</span><span class="sxs-lookup"><span data-stu-id="5d7bd-141">English</span></span>
    
  - <span data-ttu-id="5d7bd-142">Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="5d7bd-142">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="5d7bd-143">Jan. Feb. Mär. Apr. Mai Juni Juli Aug. Sep. Okt. Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-143">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="5d7bd-144">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="5d7bd-144">Dutch</span></span>
    
  - <span data-ttu-id="5d7bd-145">Januari, februari, maart, April, Mei, Juni, Juli, Augustus, September, ocktober, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="5d7bd-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="5d7bd-146">Jan Feb maart Apr Mei Jun Jul Aug Sep Sept Okt Okt Nov Dez</span><span class="sxs-lookup"><span data-stu-id="5d7bd-146">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="5d7bd-147">Französisch</span><span class="sxs-lookup"><span data-stu-id="5d7bd-147">French</span></span>
    
  - <span data-ttu-id="5d7bd-148">janvier, février, Mars, Avril, Mai, Juni juillet, août, September, Oktober, Novembre, Dezember</span><span class="sxs-lookup"><span data-stu-id="5d7bd-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="5d7bd-149">janv.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-149">janv.</span></span> <span data-ttu-id="5d7bd-150">févr.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-150">févr.</span></span> <span data-ttu-id="5d7bd-151">Mars Avril May juil.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-151">mars avril mai juin juil.</span></span> <span data-ttu-id="5d7bd-152">août Sept.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-152">août sept.</span></span> <span data-ttu-id="5d7bd-153">Okt.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-153">oct.</span></span> <span data-ttu-id="5d7bd-154">Nov.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-154">nov.</span></span> <span data-ttu-id="5d7bd-155">déc.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-155">déc.</span></span>
    
- <span data-ttu-id="5d7bd-156">Deutsch</span><span class="sxs-lookup"><span data-stu-id="5d7bd-156">German</span></span>
    
  - <span data-ttu-id="5d7bd-157">Januar, Februar, März, April, Mai, Juni Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="5d7bd-157">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="5d7bd-158">Jan./Jän.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-158">Jan./Jän.</span></span> <span data-ttu-id="5d7bd-159">Feb. März Apr. Mai Juni Juli Aug. Sept. Okt.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-159">Feb. März Apr. Mai Juni Juli Aug. Sept. Okt.</span></span> <span data-ttu-id="5d7bd-160">Nov. Dez.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-160">Nov. Dez.</span></span>
    
- <span data-ttu-id="5d7bd-161">Italienisch</span><span class="sxs-lookup"><span data-stu-id="5d7bd-161">Italian</span></span>
    
  - <span data-ttu-id="5d7bd-162">gennaio, febbraio, Marzo, Aprile, Maggio, Juni, Juli, Agosto, Settembre, ottobre, Novembre, Dezember</span><span class="sxs-lookup"><span data-stu-id="5d7bd-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="5d7bd-163">Genn.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-163">genn.</span></span> <span data-ttu-id="5d7bd-164">febbr.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-164">febbr.</span></span> <span data-ttu-id="5d7bd-165">Mar.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-165">mar.</span></span> <span data-ttu-id="5d7bd-166">Apr.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-166">apr.</span></span> <span data-ttu-id="5d7bd-167">Magg.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-167">magg.</span></span> <span data-ttu-id="5d7bd-168">Juni Juli AG.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-168">giugno luglio ag.</span></span> <span data-ttu-id="5d7bd-169">Sett.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-169">sett.</span></span> <span data-ttu-id="5d7bd-170">Ott.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-170">ott.</span></span> <span data-ttu-id="5d7bd-171">Nov.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-171">nov.</span></span> <span data-ttu-id="5d7bd-172">DIC.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-172">dic.</span></span>
    
- <span data-ttu-id="5d7bd-173">Portugiesisch</span><span class="sxs-lookup"><span data-stu-id="5d7bd-173">Portuguese</span></span>
    
  - <span data-ttu-id="5d7bd-174">Janeiro, Fevereiro, Março, Marco, Abril, Maio, Junho, Julho, Agosto, Setembro, Outubro, Novembro, Dezembro</span><span class="sxs-lookup"><span data-stu-id="5d7bd-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="5d7bd-175">Jan FEV Mar ABR Mai Jun Jul ago Set out Nov Dez</span><span class="sxs-lookup"><span data-stu-id="5d7bd-175">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="5d7bd-176">Spanisch</span><span class="sxs-lookup"><span data-stu-id="5d7bd-176">Spanish</span></span>
    
  - <span data-ttu-id="5d7bd-177">enero, Febrero, Marzo, Abril, Mayo, junio, Julio, Agosto, Septiembre, Octubre, Noviembre, Diciembre</span><span class="sxs-lookup"><span data-stu-id="5d7bd-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="5d7bd-178">enero Feb.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-178">enero feb.</span></span> <span data-ttu-id="5d7bd-179">Marzo ABR.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-179">marzo abr.</span></span> <span data-ttu-id="5d7bd-180">Mayo Jun.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-180">mayo jun.</span></span> <span data-ttu-id="5d7bd-181">Juli.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-181">jul.</span></span> <span data-ttu-id="5d7bd-182">Agosto Sept./Set.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-182">agosto sept./set.</span></span> <span data-ttu-id="5d7bd-183">Okt.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-183">oct.</span></span> <span data-ttu-id="5d7bd-184">Nov.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-184">nov.</span></span> <span data-ttu-id="5d7bd-185">DIC.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-185">dic.</span></span>
    
## <a name="funceudate1-deprecated"></a><span data-ttu-id="5d7bd-186">Func_eu_date1 (veraltet)</span><span class="sxs-lookup"><span data-stu-id="5d7bd-186">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="5d7bd-187">Diese Funktion ist veraltet, da Sie nur portugiesische Monatsnamen unterstützt, die jetzt in der `Func_eu_date` obigen Funktion enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-187">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="5d7bd-188">Diese Funktion sucht nach einem Datum im Format, das häufig in Portugiesisch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-188">This function looks for a date in the format commonly used in Portuguese.</span></span> <span data-ttu-id="5d7bd-189">Das Format für diese Funktion ist identisch `Func_eu_date`, unterscheidet sich nur in der verwendeten Sprache.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-189">The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="5d7bd-190">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-190">Examples:</span></span>
  
- <span data-ttu-id="5d7bd-191">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-191">2 Dez 2016</span></span>
    
- <span data-ttu-id="5d7bd-192">02 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-192">02 dez 2016</span></span>
    
- <span data-ttu-id="5d7bd-193">2 Dez 16</span><span class="sxs-lookup"><span data-stu-id="5d7bd-193">2 Dez 16</span></span>
    
- <span data-ttu-id="5d7bd-194">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-194">2/12/2016</span></span>
    
- <span data-ttu-id="5d7bd-195">02/12/16</span><span class="sxs-lookup"><span data-stu-id="5d7bd-195">02/12/16</span></span>
    
- <span data-ttu-id="5d7bd-196">2-Dez-2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-196">2-Dez-2016</span></span>
    
- <span data-ttu-id="5d7bd-197">2-12-16</span><span class="sxs-lookup"><span data-stu-id="5d7bd-197">2-12-16</span></span>
    
<span data-ttu-id="5d7bd-198">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-198">Accepted month names:</span></span>
  
- <span data-ttu-id="5d7bd-199">Portugiesisch</span><span class="sxs-lookup"><span data-stu-id="5d7bd-199">Portuguese</span></span>
    
  - <span data-ttu-id="5d7bd-200">Janeiro, Fevereiro, Março, Marco, Abril, Maio, Junho, Julho, Agosto, Setembro, Outubro, Novembro, Dezembro</span><span class="sxs-lookup"><span data-stu-id="5d7bd-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="5d7bd-201">Jan FEV Mar ABR Mai Jun Jul ago Set out Nov Dez</span><span class="sxs-lookup"><span data-stu-id="5d7bd-201">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="funceudate2-deprecated"></a><span data-ttu-id="5d7bd-202">Func_eu_date2 (veraltet)</span><span class="sxs-lookup"><span data-stu-id="5d7bd-202">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="5d7bd-203">Diese Funktion ist veraltet, da Sie nur niederländische Monatsnamen unterstützt, die jetzt in der `Func_eu_date` obigen Funktion enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-203">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="5d7bd-204">Diese Funktion sucht nach einem Datum im Format, das häufig in Niederländisch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-204">This function looks for a date in the format commonly used in Dutch.</span></span> <span data-ttu-id="5d7bd-205">Das Format für diese Funktion ist identisch `Func_eu_date`, unterscheidet sich nur in der verwendeten Sprache.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-205">The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="5d7bd-206">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-206">Examples:</span></span>
  
- <span data-ttu-id="5d7bd-207">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-207">2 Mei 2016</span></span>
    
- <span data-ttu-id="5d7bd-208">02 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-208">02 mei 2016</span></span>
    
- <span data-ttu-id="5d7bd-209">2 Mei 16</span><span class="sxs-lookup"><span data-stu-id="5d7bd-209">2 Mei 16</span></span>
    
- <span data-ttu-id="5d7bd-210">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-210">2/12/2016</span></span>
    
- <span data-ttu-id="5d7bd-211">02/12/16</span><span class="sxs-lookup"><span data-stu-id="5d7bd-211">02/12/16</span></span>
    
- <span data-ttu-id="5d7bd-212">2-Mei-2016</span><span class="sxs-lookup"><span data-stu-id="5d7bd-212">2-Mei-2016</span></span>
    
- <span data-ttu-id="5d7bd-213">2-12-16</span><span class="sxs-lookup"><span data-stu-id="5d7bd-213">2-12-16</span></span>
    
<span data-ttu-id="5d7bd-214">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-214">Accepted month names:</span></span>
  
- <span data-ttu-id="5d7bd-215">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="5d7bd-215">Dutch</span></span>
    
  - <span data-ttu-id="5d7bd-216">Januari, februari, maart, April, Mei, Juni, Juli, Augustus, September, ocktober, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="5d7bd-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="5d7bd-217">Jan Feb maart Apr Mei Jun Jul Aug Sep Sept Okt Okt Nov Dez</span><span class="sxs-lookup"><span data-stu-id="5d7bd-217">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
## <a name="funcexpirationdate"></a><span data-ttu-id="5d7bd-218">Func_expiration_date</span><span class="sxs-lookup"><span data-stu-id="5d7bd-218">Func_expiration_date</span></span>

<span data-ttu-id="5d7bd-219">Diese Funktion sucht nach einem Datum in den Formaten, die häufig von Kredit-und Debitkarten verwendet werden, die Tage für Monate ausschließen.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-219">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months.</span></span> <span data-ttu-id="5d7bd-220">Diese Funktion entspricht Datumsangaben im Format "month/year", "month-year", "[Month Name] Year" und "[month Abkürzung] Year".</span><span class="sxs-lookup"><span data-stu-id="5d7bd-220">This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year".</span></span> <span data-ttu-id="5d7bd-221">Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-221">The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="5d7bd-222">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-222">Examples:</span></span>
  
- <span data-ttu-id="5d7bd-223">MM/JJ--Beispiel: 01/11 oder 1/11</span><span class="sxs-lookup"><span data-stu-id="5d7bd-223">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="5d7bd-224">MM/YYYY--zum Beispiel 01/2011 oder 1/2011</span><span class="sxs-lookup"><span data-stu-id="5d7bd-224">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="5d7bd-225">MM-YY--zum Beispiel 01-22 oder 1-11</span><span class="sxs-lookup"><span data-stu-id="5d7bd-225">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="5d7bd-226">MM-YYYY--zum Beispiel 01-2000 oder 1-2000</span><span class="sxs-lookup"><span data-stu-id="5d7bd-226">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="5d7bd-227">Die folgenden Formate unterstützen YY oder YYYY:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-227">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="5d7bd-228">Month-YYYY--zum Beispiel,. Jan-2010 oder Januar-2010 oder Jan-10 oder Januar-10</span><span class="sxs-lookup"><span data-stu-id="5d7bd-228">Month-YYYY -- for example, .Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="5d7bd-229">Monat YYYY--Beispiel: ' Januar 2010 ' oder ' Jan 2010 ' oder ' Januar 10 ' oder ' Jan 10 '</span><span class="sxs-lookup"><span data-stu-id="5d7bd-229">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="5d7bd-230">Monatjjjj--beispielsweise "january2010" oder "Jan2010" oder "january10" oder "Jan10"</span><span class="sxs-lookup"><span data-stu-id="5d7bd-230">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="5d7bd-231">Month/YYYY--beispielsweise ' Januar/2010 ' oder ' Jan/2010 ' oder ' Januar/10 ' oder ' Jan/10 '</span><span class="sxs-lookup"><span data-stu-id="5d7bd-231">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="5d7bd-232">Akzeptierte Monatsnamen:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-232">Accepted month names:</span></span>
  
- <span data-ttu-id="5d7bd-233">Englisch</span><span class="sxs-lookup"><span data-stu-id="5d7bd-233">English</span></span>
    
  - <span data-ttu-id="5d7bd-234">Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="5d7bd-234">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="5d7bd-235">Jan Feb Mär Apr Mai Juni Juli Aug Sep Okt Nov Dez</span><span class="sxs-lookup"><span data-stu-id="5d7bd-235">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="funcusaddress"></a><span data-ttu-id="5d7bd-236">Func_us_address</span><span class="sxs-lookup"><span data-stu-id="5d7bd-236">Func_us_address</span></span>

<span data-ttu-id="5d7bd-237">Diese Funktion sucht nach einem US-Bundesstaat oder einer postalischen Abkürzung gefolgt von einer gültigen Postleitzahl, genau wie Sie in Postanschriften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-237">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they are used in postal addresses.</span></span> <span data-ttu-id="5d7bd-238">Bei der Postleitzahl muss es sich um einen der korrekten Postleitzahlen handeln, die dem US-Bundesstaat oder der Abkürzung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-238">The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation.</span></span> <span data-ttu-id="5d7bd-239">Der US-Bundesstaat und die Postleitzahl dürfen nicht durch Interpunktion oder Buchstaben getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="5d7bd-239">The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="5d7bd-240">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="5d7bd-240">Examples:</span></span>
  
- <span data-ttu-id="5d7bd-241">Washington 98052</span><span class="sxs-lookup"><span data-stu-id="5d7bd-241">Washington 98052</span></span>
    
- <span data-ttu-id="5d7bd-242">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="5d7bd-242">Washington 98052-9998</span></span>
    
- <span data-ttu-id="5d7bd-243">WA 98052</span><span class="sxs-lookup"><span data-stu-id="5d7bd-243">WA 98052</span></span>
    
- <span data-ttu-id="5d7bd-244">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="5d7bd-244">WA 98052-9998</span></span>
    

