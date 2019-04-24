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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32266917"
---
# <a name="what-the-dlp-functions-look-for"></a>Wonach die DLP-Funktionen suchen

Data Loss Prevention (DLP) enthält vertrauliche Informationstypen wie Kreditkartennummer und EC-Debitkarte, die Sie in ihren DLP-Richtlinien verwenden können. Diese Typen von vertraulichen Informationen suchen nach einem bestimmten Muster und bestätigen es, indem Sie eine korrekte Formatierung sicherstellen, Prüfsummen erzwingen und nach relevanten Stichwörtern oder anderen Informationen suchen. Einige dieser Funktionen werden von internen Funktionen ausgeführt. Beispielsweise verwendet der vertrauliche Informationstyp Kreditkartennummer eine Funktion, um nach Datumsangaben zu suchen, die wie ein Ablaufdatum formatiert sind, um zu bestätigen, dass eine Nummer eine Kreditkartennummer ist.
  
In diesem Thema wird erläutert, wonach diese Funktionen suchen, damit Sie besser verstehen, wie die vordefinierten Typen vertraulicher Informationen funktionieren. Weitere Informationen finden Sie unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
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

Diese Funktion sucht nach einem Datum im allgemeinen Format, das in der EU verwendet wird. (und die meisten Standorte außerhalb der USA). Dazu gehören die Formate "Tag/Monat/Jahr", "Tag-Monat-Jahr" und "Tag Monat Jahr". Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet.
  
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
    
  - Januari, februari, maart, April, Mei, Juni, Juli, Augustus, September, ocktober, Oktober, November, Dezember
    
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
    
  - Janeiro, Fevereiro, Março, Marco, Abril, Maio, Junho, Julho, Agosto, Setembro, Outubro, Novembro, Dezembro
    
  - Jan FEV Mar ABR Mai Jun Jul ago Set out Nov Dez
    
- Spanisch
    
  - enero, Febrero, Marzo, Abril, Mayo, junio, Julio, Agosto, Septiembre, Octubre, Noviembre, Diciembre
    
  - enero Feb. Marzo ABR. Mayo Jun. Juli. Agosto Sept./Set. Okt. Nov. DIC.
    
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
    
  - Janeiro, Fevereiro, Março, Marco, Abril, Maio, Junho, Julho, Agosto, Setembro, Outubro, Novembro, Dezembro
    
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
    
  - Januari, februari, maart, April, Mei, Juni, Juli, Augustus, September, ocktober, Oktober, November, Dezember
    
  - Jan Feb maart Apr Mei Jun Jul Aug Sep Sept Okt Okt Nov Dez
    
## <a name="funcexpirationdate"></a>Func_expiration_date

Diese Funktion sucht nach einem Datum in den Formaten, die häufig von Kredit-und Debitkarten verwendet werden, die Tage für Monate ausschließen. Diese Funktion entspricht Datumsangaben im Format "month/year", "month-year", "[Month Name] Year" und "[month Abkürzung] Year". Bei den Namen oder Abkürzungen von Monaten wird die Groß-/Kleinschreibung nicht beachtet.
  
Beispiele:
  
- MM/JJ--Beispiel: 01/11 oder 1/11
    
- MM/YYYY--zum Beispiel 01/2011 oder 1/2011
    
- MM-YY--zum Beispiel 01-22 oder 1-11
    
- MM-YYYY--zum Beispiel 01-2000 oder 1-2000
    
Die folgenden Formate unterstützen YY oder YYYY:
  
- Month-YYYY--zum Beispiel,. Jan-2010 oder Januar-2010 oder Jan-10 oder Januar-10
    
- Monat YYYY--Beispiel: ' Januar 2010 ' oder ' Jan 2010 ' oder ' Januar 10 ' oder ' Jan 10 '
    
- Monatjjjj--beispielsweise "january2010" oder "Jan2010" oder "january10" oder "Jan10"
    
- Month/YYYY--beispielsweise ' Januar/2010 ' oder ' Jan/2010 ' oder ' Januar/10 ' oder ' Jan/10 '
    
Akzeptierte Monatsnamen:
  
- Englisch
    
  - Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember
    
  - Jan Feb Mär Apr Mai Juni Juli Aug Sep Okt Nov Dez
    
## <a name="funcusaddress"></a>Func_us_address

Diese Funktion sucht nach einem US-Bundesstaat oder einer postalischen Abkürzung gefolgt von einer gültigen Postleitzahl, genau wie Sie in Postanschriften verwendet wird. Bei der Postleitzahl muss es sich um einen der korrekten Postleitzahlen handeln, die dem US-Bundesstaat oder der Abkürzung zugeordnet sind. Der US-Bundesstaat und die Postleitzahl dürfen nicht durch Interpunktion oder Buchstaben getrennt werden.
  
Beispiele:
  
- Washington 98052
    
- Washington 98052-9998
    
- WA 98052
    
- WA 98052-9998
    

