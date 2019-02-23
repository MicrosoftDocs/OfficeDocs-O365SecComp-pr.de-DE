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
# <a name="what-the-dlp-functions-look-for"></a>Wonach die DLP-Funktionen suchen

Schutz vor Datenverlust (Data Loss Prevention, DLP) umfasst Typen vertraulicher Informationen, wie z. B. Kreditkartennummern und EC-Kartennummern, die in Ihren DLP-Richtlinien verwendet werden können. Diese Typen vertraulicher Informationen suchen nach einem bestimmten Muster und bestätigen sie durch Sicherstellen der ordnungsgemäßen Formatierung, durch Erzwingen von Prüfsummen und durch Suchen nach relevanten Schüsselwörtern oder anderen Informationen. Einige dieser Funktionen werden durch interne Funktionen ausgeführt. Der Typ vertraulicher Informationen für die Kreditkartennummer verwendet beispielsweise eine Funktion für die Suche nach Datumsangaben, die wie ein Ablaufdatum formatiert sind, um zu bestätigen, dass es sich bei einer Nummer um eine Kreditkartennummer handelt.
  
In diesem Thema wird erläutert, wie diese Funktionen vorgehen, um die Funktionsweise der vordefinierten Typen vertraulicher Informationen besser zu verstehen. Weitere Informationen finden Sie unter [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).
  
## <a name="funcusdate"></a>Func_us_date

Diese Funktion sucht nach einem Datum im allgemeinen Format, das in den USA verwendet wird. Dazu gehören die Formate "Month/Day/Year", "Month-Day-Year" und "Month Day Year". Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet. 
  
Beispiele:
  
- 2. Dezember 2016
    
- Dez 2, 2016
    
- Dez 02 2016
    
- 12/2/2016
    
- 12/02/16
    
- Dez-2-2016
    
- 12-2-16
    
Akzeptierte Monatsnamen:
  
- Englisch
    
  - Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember
    
  - Jan. Feb. Mär. Apr. Mai Juni Juli Aug. Sep. Okt. Nov. Dez.
    
## <a name="funceudate"></a>Func_eu_date

Diese Funktion sucht nach einem Datum im häufig in der EU (und in den meisten Ländern außerhalb der USA) verwendeten Format. Dies umfasst die Formate „Tag/Monat/Jahr“, „Tag-Monat-Jahr“ und „Tag Monat Jahr“. Die Namen oder Abkürzungen der Monate unterscheiden nicht nach Groß- und Kleinschreibung.
  
Beispiele:
  
- 2 Dez 2016
    
- 02 Dez 2016
    
- 2 Dez 16
    
- 2/12/2016
    
- 02/12/16
    
- 2-Dez-2016
    
- 2-12-16
    
Akzeptierte Monatsnamen:
  
- Englisch
    
  - Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember
    
  - Jan. Feb. Mär. Apr. Mai Juni Juli Aug. Sep. Okt. Nov. Dez.
    
- Niederländisch
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - Jan Feb maart Apr Mei Jun Jul Aug Sep Sept Okt Okt Nov Dez
    
- Französisch
    
  - janvier, février, Mars, Avril, Mai, Juni juillet, août, September, Oktober, Novembre, Dezember
    
  - janv. févr. Mars Avril May juil. août Sept. Okt. Nov. déc.
    
- Deutsch
    
  - Januar, Februar, März, April, Mai, Juni Juli, August, September, Oktober, November, Dezember
    
  - Jan./Jän. Feb. März Apr. Mai Juni Juli Aug. Sept. Okt. Nov. Dez.
    
- Italienisch
    
  - gennaio, febbraio, Marzo, Aprile, Maggio, Juni, Juli, Agosto, Settembre, ottobre, Novembre, Dezember
    
  - Genn. febbr. Mar. Apr. Magg. Juni Juli AG. Sett. Ott. Nov. DIC.
    
- Portugiesisch
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan FEV Mar ABR Mai Jun Jul ago Set out Nov Dez
    
- Spanisch
    
  - enero, Febrero, Marzo, Abril, Mayo, junio, Julio, Agosto, Septiembre, Octubre, Noviembre, Diciembre
    
  - enero Feb. Marzo ABR. Mayo Jun. Jul. Agosto Sept./Set. Okt. Nov. DIC.
    
## <a name="funceudate1-deprecated"></a>Func_eu_date1 (veraltet)

> [!NOTE]
> Diese Funktion ist veraltet, da Sie nur portugiesische Monatsnamen unterstützt, die jetzt in der `Func_eu_date` obigen Funktion enthalten sind. 
  
Diese Funktion sucht nach einem Datum im Format, das häufig in Portugiesisch verwendet wird. Das Format für diese Funktion ist identisch `Func_eu_date`, unterscheidet sich nur in der verwendeten Sprache.
  
Beispiele:
  
- 2 Dez 2016
    
- 02 Dez 2016
    
- 2 Dez 16
    
- 2/12/2016
    
- 02/12/16
    
- 2-Dez-2016
    
- 2-12-16
    
Akzeptierte Monatsnamen:
  
- Portugiesisch
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan FEV Mar ABR Mai Jun Jul ago Set out Nov Dez
    
## <a name="funceudate2-deprecated"></a>Func_eu_date2 (veraltet)

> [!NOTE]
> Diese Funktion ist veraltet, da Sie nur niederländische Monatsnamen unterstützt, die jetzt in der `Func_eu_date` obigen Funktion enthalten sind. 
  
Diese Funktion sucht nach einem Datum im Format, das häufig in Niederländisch verwendet wird. Das Format für diese Funktion ist identisch `Func_eu_date`, unterscheidet sich nur in der verwendeten Sprache.
  
Beispiele:
  
- 2 Mei 2016
    
- 02 Mei 2016
    
- 2 Mei 16
    
- 2/12/2016
    
- 02/12/16
    
- 2-Mei-2016
    
- 2-12-16
    
Akzeptierte Monatsnamen:
  
- Niederländisch
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - Jan Feb maart Apr Mei Jun Jul Aug Sep Sept Okt Okt Nov Dez
    
## <a name="funcexpirationdate"></a>Func_expiration_date

Diese Funktion sucht nach einem Datum in den Formaten, die häufig von Kredit-und Debitkarten verwendet werden, die Tage für Monate ausschließen. Diese Funktion entspricht Datumsangaben im Format "month/year", "month-year", "[Month Name] Year" und "[month Abkürzung] Year". Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet.
  
Beispiele
  
- MM/JJ – z. B. 01/11 oder 1/11
    
- MM/JJJJ – z. B. 01/2011 oder 1/2011
    
- MM-JJ – z. B. 01-22 oder 1-11
    
- MM-JJJJ – z. B. 01-2000 oder 1-2000
    
Die folgenden Formate unterstützen JJ oder JJJJ:
  
- Monat-JJJJ – z. B. Jan-2010 oder Januar-2010 Jan-10 oder Januar-10
    
- Monat JJJJ – z. B. 'Januar 2010' oder 'Jan 2010' oder '10 Januar' oder 'Jan 10'
    
- MonatJJJJ – zum Beispiel, 'Januar2010' oder 'Jan2010' oder 'Januar10' oder 'Jan10'
    
- Month/YYYY--beispielsweise ' Januar/2010 ' oder ' Jan/2010 ' oder ' Januar/10 ' oder ' Jan/10 '
    
Akzeptierte Monatsnamen:
  
- Englisch
    
  - Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember
    
  - Jan Feb Mär Apr Mai Juni Juli Aug Sep Okt Nov Dez
    
## <a name="funcusaddress"></a>Func_us_address

Diese Funktion sucht nach dem Namen eines Bundesstaats in den USA oder nach einer postalischen Abkürzung, gefolgt von einer gültigen Postleitzahl, wie sie in Postanschriften verwendet werden. Die Postleitzahl muss eine der richtigen Postleitzahlen sein, die dem Namen des Bundesstaats in den USA oder der Abkürzung zugeordnet ist. Der Name des Bundesstaats in den USA und die Postleitzahl können nicht durch Zeichensetzung oder Buchstaben getrennt werden.
  
Beispiele:
  
- 	Washington 98052
    
- Washington 98052-9998
    
- 	WA 98052
    
- WA 98052-9998
    

