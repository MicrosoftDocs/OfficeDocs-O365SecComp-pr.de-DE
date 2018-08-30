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
# <a name="what-the-dlp-functions-look-for"></a>Wonach die DLP-Funktionen suchen

Schutz vor Datenverlust (Data Loss Prevention, DLP) umfasst Typen vertraulicher Informationen, wie z. B. Kreditkartennummern und EC-Kartennummern, die in Ihren DLP-Richtlinien verwendet werden können. Diese Typen vertraulicher Informationen suchen nach einem bestimmten Muster und bestätigen sie durch Sicherstellen der ordnungsgemäßen Formatierung, durch Erzwingen von Prüfsummen und durch Suchen nach relevanten Schüsselwörtern oder anderen Informationen. Einige dieser Funktionen werden durch interne Funktionen ausgeführt. Der Typ vertraulicher Informationen für die Kreditkartennummer verwendet beispielsweise eine Funktion für die Suche nach Datumsangaben, die wie ein Ablaufdatum formatiert sind, um zu bestätigen, dass es sich bei einer Nummer um eine Kreditkartennummer handelt.
  
In diesem Thema wird erläutert, wie diese Funktionen vorgehen, um die Funktionsweise der vordefinierten Typen vertraulicher Informationen besser zu verstehen. Weitere Informationen finden Sie unter [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).
  
## <a name="funcusdate"></a>Func_us_date

Diese Funktion sucht nach einem Datum im Format in den USA häufig verwendet Dazu gehören die Formate "Tag/Monat/Jahr", "Monat-Tag-Jahr" und "Monat-Tag-Jahr". Die Namen oder Abkürzungen Monate sind nicht zwischen Groß-und Kleinschreibung. 
  
Beispiele:
  
- 2 Dezember 2016
    
- 2 Dez 2016
    
- Dez 02 2016
    
- 12/2/2016
    
- 12/02/16
    
- Dez-2-2016
    
- 12-2-16
    
Akzeptierte Monatsnamen:
  
- Englisch
    
  - Januar, Februar, Mai März, April, Juni, Juli, August, September, Oktober, November, Dezember
    
  - Januar Februar März April Mai Juni Juli August September Oktober November Dezember.
    
## <a name="funceudate"></a>Func_eu_date

Diese Funktion sucht nach einem Datum im häufig in der EU (und in den meisten Ländern außerhalb der USA) verwendeten Format. Dies umfasst die Formate „Tag/Monat/Jahr“, „Tag-Monat-Jahr“ und „Tag Monat Jahr“. Die Namen oder Abkürzungen der Monate unterscheiden nicht nach Groß- und Kleinschreibung.
  
Beispiele:
  
- 2 Dez 2016
    
- 02 Dez 2016
    
- 2 Dez 16
    
- 2/12/2016
    
- 02/12/16
    
- 2 – Dez-2016
    
- 2-12-16
    
Akzeptierte Monatsnamen:
  
- Englisch
    
  - Januar, Februar, Mai März, April, Juni, Juli, August, September, Oktober, November, Dezember
    
  - Januar Februar März April Mai Juni Juli August September Oktober November Dezember.
    
- Niederländisch
    
  - januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December
    
  - Jan Februar Maart Apr Mei Juni, Juli August Sep September OAT Okt November (dezimal)
    
- Französisch
    
  - Uhrzeitanzeige, Février, Mars, Avril, Mai, Juin Juillet, Août, Septembre, Octobre, Novembre, Dezember
    
  - Janv. Févr. MAR Avril Mai Juin Juil. Août September. Oktober November. Déc.
    
- Deutsch
    
  - Jänuar deutscher, März, April, Mai, Juni Juli, August, September, h., November, Dezember
    
  - Jan. / Jän. Februar März April Mai Juni Juli August September Okt. Dez November.
    
- Italienisch
    
  - Gennaio, Febbraio, Marzo, Aprile, Maggio, Giugno, Luglio, Agosto, Settembre, Ottobre, Novembre, dicembre
    
  - Dänemarks. Febbr. Mrz. APR. Magg. Giugno Luglio ag. festlegen. Ott. November. DIC.
    
- Portugiesisch
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan Fev Mrz Abr Mai Juni, Juli vor November Dez dargelegten
    
- Spanisch
    
  - Enero, Febrero, Marzo, Abril, Mayo, Junio, Julio, Agosto, Septiembre, Octubre, Noviembre, diciembre
    
  - Enero Februar. Marzo abr. Mayo Uhr angezeigt Juli. Agosto September/festlegen. Oktober November. DIC.
    
## <a name="funceudate1-deprecated"></a>Func_eu_date1 (veraltet)

> [!NOTE]
> Diese Funktion ist veraltet, da es nur Portugiesisch Monatsnamen unterstützt, die nun in enthalten sind die `Func_eu_date` Funktion oben. 
  
Diese Funktion sucht nach einem Datum im Format häufig verwendet für Portugiesisch. Das Format für diese Funktion ist identisch mit `Func_eu_date`, unterschiedliche nur in der Sprache verwendet.
  
Beispiele:
  
- 2 Dez 2016
    
- 02 Dez 2016
    
- 2 Dez 16
    
- 2/12/2016
    
- 02/12/16
    
- 2 – Dez-2016
    
- 2-12-16
    
Akzeptierte Monatsnamen:
  
- Portugiesisch
    
  - janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro
    
  - Jan Fev Mrz Abr Mai Juni, Juli vor November Dez dargelegten
    
## <a name="funceudate2-deprecated"></a>Func_eu_date2 (veraltet)

> [!NOTE]
> Diese Funktion ist veraltet, da es nur niederländische Monatsnamen unterstützt, die nun in enthalten sind die `Func_eu_date` Funktion oben. 
  
Diese Funktion sucht nach einem Datum im Format häufig verwendet für Niederländisch. Das Format für diese Funktion ist identisch mit `Func_eu_date`, unterschiedliche nur in der Sprache verwendet.
  
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
    
  - Jan Februar Maart Apr Mei Juni, Juli August Sep September OAT Okt November (dezimal)
    
## <a name="funcexpirationdate"></a>Func_expiration_date

Diese Funktion sucht nach einem Datum in den Formaten von Kredit und soll-Karten, die was die Tage zugunsten Monate ausschließen häufig verwendet. Diese Funktion entspricht Datumsangaben im Format "Monat/Jahr", "Monat-Jahr", "[Monatsname]", und "[Abkürzung für den Monat] Jahr". Die Namen oder Abkürzungen Monate sind nicht zwischen Groß-und Kleinschreibung.
  
Beispiele
  
- MM/JJ – z. B. 01/11 oder 1/11
    
- MM/JJJJ – z. B. 01/2011 oder 1/2011
    
- MM-JJ – z. B. 01-22 oder 1-11
    
- MM-JJJJ – z. B. 01-2000 oder 1-2000
    
Die folgenden Formate unterstützen JJ oder JJJJ:
  
- Monat-JJJJ – z. B. Jan-2010 oder Januar-2010 Jan-10 oder Januar-10
    
- Monat JJJJ – z. B. 'Januar 2010' oder 'Jan 2010' oder '10 Januar' oder 'Jan 10'
    
- MonatJJJJ – zum Beispiel, 'Januar2010' oder 'Jan2010' oder 'Januar10' oder 'Jan10'
    
- Monat/JJJJ – beispielsweise "Januar/2010" oder "Jan/2010" oder "Januar/10" oder "Jan/10"
    
Akzeptierte Monatsnamen:
  
- Englisch
    
  - Januar, Februar, Mai März, April, Juni, Juli, August, September, Oktober, November, Dezember
    
  - Jan Februar Mrz Apr Mai Juni Juli August September OAT November (dezimal)
    
## <a name="funcusaddress"></a>Func_us_address

Diese Funktion sucht nach dem Namen eines Bundesstaats in den USA oder nach einer postalischen Abkürzung, gefolgt von einer gültigen Postleitzahl, wie sie in Postanschriften verwendet werden. Die Postleitzahl muss eine der richtigen Postleitzahlen sein, die dem Namen des Bundesstaats in den USA oder der Abkürzung zugeordnet ist. Der Name des Bundesstaats in den USA und die Postleitzahl können nicht durch Zeichensetzung oder Buchstaben getrennt werden.
  
Beispiele:
  
- 	Washington 98052
    
- Washington 98052-9998
    
- 	WA 98052
    
- WA 98052-9998
    

