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
# <a name="eu-national-identification-number"></a>EU National Identifikationsnummer

In diesem Thema wird eine Data Loss Prevention (DLP) Richtlinie sieht für beim Erkennen des EU National Identifikationsnummer vertrauliche Informationen-Typs. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
  
## <a name="austria"></a>Österreich

### <a name="format"></a>Format

Eine 24 Zeichen Kombination von Buchstaben, Zahlen und Sonderzeichen
  
### <a name="pattern"></a>Muster

24 Zeichen:
  
-  22 Buchstaben (nicht Groß-/Kleinschreibung), Ziffern, umgekehrte Schrägstriche, Schrägstriche oder Pluszeichen 
    
- Zwei Buchstaben (nicht Groß-/Kleinschreibung), Ziffern, umgekehrte Schrägstriche, Schrägstriche, Pluszeichen oder Gleichheitszeichen
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_austria_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_austria_eu_national_id_card` gefunden wird. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsaustriaeunationalidcard"></a>Keywords_austria_eu_national_id_card

österreichische Identität Anzahl
  
Anzahl der National Identität
  
Anzahl der Identität
  

national id
  
Personalausweis Republik österreich
  
## <a name="belgium"></a>Belgien

Weitere Informationen hierzu finden Sie im Abschnitt "Belgien Vorwahl" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="bulgaria"></a>Bulgarien

### <a name="format"></a>Format

Zehn Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Zehn Ziffern ohne Leerzeichen und Trennzeichen
  
-  Sechs Ziffern, die das Geburtsdatum (JJMMTT) entsprechen 
    
- Zwei Ziffern, die die Reihenfolge Geburtsdatum entsprechen
    
- Eine Zahl, die das Geschlecht entspricht: eine gerade Zahl für Männlich und eine ungerade Ziffer für Weiblich
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_bulgaria_national_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_bulgaria_national_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_bulgaria_national_number` sucht nach Inhalten, die dem Muster entspricht. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsbulgarianationalnumber"></a>Keywords_bulgaria_national_number

egn
  
Egn #
  
Bulgarisch Vorwahl
  
Vorwahl
  
social security number

  
Nationalnumber #
  
ssn #
  
ssn
  
nationalnumber
  
Bnn #
  
bnn
  
Persönliche Id-Nummer
  
Personalidnumber #
  
ЕДИНЕН ГРАЖДАНСКИ НОМЕР
  
Edinen Grazhdanski nomer
  
ЕГН
  
ЕГН #
  
## <a name="croatia"></a>Kroatien

Weitere Informationen hierzu finden Sie im Abschnitt "Kroatien Identity Number" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="cyprus"></a>Zypern

### <a name="format"></a>Format

Zehn Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

 Zehn Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_cyprus_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_cyprus_eu_national_id_card` gefunden wird. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordscypruseunationalidcard"></a>Keywords_cyprus_eu_national_id_card

Ausweisnummer
  
National Identifikationsnummer
  
Persönliche Id-Nummer
  
Identität Card-Nummer
  
ΤΑΥΤΟΤΗΤΑΣ
  
## <a name="czech-republic"></a>Tschechische Republik

Weitere Informationen hierzu finden Sie im Abschnitt "Tschechisch National Identity Number" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="denmark"></a>Dänemark

Weitere Informationen hierzu finden Sie im Abschnitt "Dänemark persönliche Identifikationsnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="estonia"></a>Estland

### <a name="format"></a>Format

11 Zahlen ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

11 Ziffern:
  
- Eine Zahl, die das Geschlecht und Century Geburtsdatum entspricht (ungerade Anzahl Männlich, gerade Anzahl Weiblich; 1 – 2: 19. Century; 3-4: 20. Century; 5-6: 2015)
    
- Sechs Ziffern, die das Geburtsdatum (JJMMTT) entsprechen
    
- Drei Ziffern, die eine fortlaufende Zahl, die Personen, die an demselben Tag geboren trennt entsprechen
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_estonia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_estonia_eu_national_id_card` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_estonia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsestoniaeunationalidcard"></a>Keywords_estonia_eu_national_id_card

PIN-code
  
Persönliche Identifikationsnummer
  
National Identifikationsnummer
  
Vorwahl
  
Persönliche Id-Nummer
  
Personalidnumber #
  
IK
  
isikukood
  
ID-kaart
  
## <a name="finland"></a>Finnland

Weitere Informationen hierzu finden Sie im Abschnitt "Finnland Personalausweis" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>Frankreich

Weitere Informationen hierzu finden Sie im Abschnitt "Frankreich nationale d ' Identité (CNI)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Deutschland

Weitere Informationen hierzu finden Sie im Abschnitt "Deutschland Identität Card-Nummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Griechenland

Weitere Informationen hierzu finden Sie im Abschnitt "Griechenland nationale d ' Identité" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Ungarn

### <a name="format"></a>Format

11 Ziffern
  
### <a name="pattern"></a>Muster

11 Ziffern:
  
-  Eine Zahl, die das Geschlecht entspricht (1-Stecker, 2 weiblich, andere Zahlen sind auch für Bürger vor 1900 geboren oder Bürger mit double Bürger möglich) 
    
- Sechs Ziffern, die Geburtsdatum (JJMMTT) entsprechen
    
- Drei Ziffern, die eine fortlaufende Zahl entsprechen
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_hungary_eu_national_id_card` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordshungaryeunationalidcard"></a>Keywords_hungary_eu_national_id_card

Persönliche Identifikationsnummer
  
identification number

  
Persönliche Id-Nummer
  
Személyazonosító igazolvány
  
## <a name="ireland"></a>Irland

### <a name="format"></a>Format

Eine neun Zeichen Kombination von Buchstaben, Zahlen und ein Leerzeichen in dem angegebenen Muster
  
### <a name="pattern"></a>Muster

Eine neun Zeichen Kombination von Buchstaben, Zahlen und ein Leerzeichen in dem angegebenen Muster
  
Von 01 für Januar 2013 bis jetzt:
  
-  Sieben Ziffern  
    
- Ein Kontrollkästchen Ziffer
    
- Ein Leerzeichen oder der Großbuchstabe "W" (Groß-/Kleinschreibung beachten)
    
Bevor Sie 01 für Januar 2013:
  
-  Sieben Ziffern  
    
- Ein Kontrollkästchen Ziffer
    
- Ein Leerzeichen oder einem großen Buchstaben (Groß-/Kleinschreibung)
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion sucht nach Inhalten, die dem Muster entspricht.
    
- Ein Schlüsselwort gefunden wird.
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion sucht nach Inhalten, die dem Muster entspricht.
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsirelandeunationalidcard"></a>Keywords_ireland_eu_national_id_card

Anzahl der persönlichen öffentliche Dienstleistungen
  
PPS keine
  
Umsatz und die Nutzung von sozialen Netzwerken insurance
  
RSI keine
  
Persönliche Identifikationsnummer
  
identification number

  
Persönliche Id-Nummer
  
Uimhir Phearsanta Seirbhíse poiblí
  
Uimh. PSP
  
## <a name="italy"></a>Italien

### <a name="format"></a>Format

Eine 16 Zeichen Kombination von Buchstaben und Ziffern in dem angegebenen Muster
  
### <a name="pattern"></a>Muster

Eine 16 Zeichen Kombination von Buchstaben und Ziffern:
  
- Drei Buchstaben, die die ersten drei Doppelkonsonanten in der der Name der entsprechen
    
- Drei Buchstaben, die die erste, dritte und vierte entsprechen, Doppelkonsonanten in den Vornamen
    
- Zwei Ziffern, die auf die letzte Ziffern des Jahres Geburtsdatum entsprechen
    
- Einen Buchstaben, die den Brief, für den Monat Geburtsdatum entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben A bis E, H, L, M, P, R t verwendet werden (also Januar ist eine und Oktober R)
    
- Zwei Ziffern, die den Tag des Monats Geburtsdatum entsprechen – 40 wird hinzugefügt, um Männern unterscheiden, auf den Tag des Geburtsdaten von Frau
    
- Vier Ziffern, die speziell für die Gemeinde Ortskennzahl entspricht, in die Person geboren wurde (Land geltende Codes für Ausland verwendet werden)
    
- Eine Parität Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_italy_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_italy_eu_national_id_card` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_italy_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsitalyeunationalidcard"></a>Keywords_italy_eu_national_id_card

Persönliche code
  
persönliche Nummer
  
eigenes Zertifikat Anzahl
  
Fiscal code
  
Personalcodeno #
  
Persönliche Id-Nummer
  
Persönliche Id-code
  
Codice personale
  
Numero Certificato personale
  
Numero personale
  
Numero Id personale
  
Codice Id personale
  
Codice fiscale
  
## <a name="italy"></a>Italien

### <a name="format"></a>Format

11 Ziffern und ein Bindestrich im angegebenen format
  
### <a name="pattern"></a>Muster

11 Ziffern und ein Bindestrich:
  
-  Sechs Ziffern, die das Geburtsdatum (DDMMYY) entsprechen 
    
- Ein Bindestrich 
    
- Eine Ziffer aus, die die Century Geburtsdatum ("0" für 19. Century, für allem "1" und "2" für 2015) entspricht
    
- Vier Ziffern, zufällig generiert
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_latvia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_latvia_eu_national_id_card` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_latvia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordslatviaeunationalidcard"></a>Keywords_latvia_eu_national_id_card

Persönliche code
  
persönliche Nummer
  
eigenes Zertifikat Anzahl
  
Personalcodeno #
  
Persönliche Id-Nummer
  
Persönliche Id-code
  
Rollen kods
  
## <a name="lithuania"></a>Litauen

### <a name="format"></a>Format

11 Zahlen ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

11 Zahlen ohne Leerzeichen und Trennzeichen:
  
- Eine Zahl, die das Geschlecht und Century Geburtsdatum der Person entspricht
    
-  Sechs Ziffern, die Geburtsdatum (JJMMTT) entsprechen 
    
- Drei Ziffern, die die Seriennummer des das Geburtsdatum entsprechen
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_lithuania_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_lithuania_eu_national_id_card` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_lithuania_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordslithuaniaeunationalidcard"></a>Keywords_lithuania_eu_national_id_card

Persönliche numerischen code
  
eindeutige ID-Nummer
  
Anzahl der Bürger-Dienst
  
Anzahl der eindeutigen Identität
  
Uniqueidentityno #
  
Persönliche Code.
  
Asmeninis Skaitmeninis kodas
  
Unikalus Identifikavimo numeris
  
Piliečio Paslaugos numeris
  
Unikalus Identifikavimo kodas
  
Asmens Kodas.
  
## <a name="luxemburg"></a>Luxemburg

### <a name="format"></a>Format

11 Zahlen ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

11 Ziffern
  
- Eine Zahl, die das Geschlecht und Century Geburtsdatum der Person entspricht
    
-  Sechs Ziffern, die Geburtsdatum (JJMMTT) entsprechen 
    
- Drei Ziffern, die die Seriennummer des das Geburtsdatum entsprechen
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_luxemburg_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_luxemburg_eu_national_id_card` gefunden wird. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsluxemburgeunationalidcard"></a>Keywords_luxemburg_eu_national_id_card

Persönliche id
  
Persönliche Id-Nummer
  
Personalidno #
  
eindeutige Id-Nummer
  
Personalidnumber #
  
eindeutige Id-Schlüssel
  
Persönliche Id-code
  
Uniqueidkey #
  
einzelne code
  
einzelne-id
  
Eindeutige Id-nummer
  
Eindeutige id
  
ID personnelle
  
Numéro d ' Identification Mitarbeiter
  
Idpersonnelle #
  
Persönliche identifikationsnummer
  
EINDEUTIGEID #
  
## <a name="malta"></a>Malta

### <a name="format"></a>Format

Sieben Ziffern, gefolgt von einem Buchstaben
  
### <a name="pattern"></a>Muster

Sieben Ziffern, gefolgt von einem Buchstaben:
  
-  Sieben Ziffern  
    
- Einen Großbuchstaben (Groß-/Kleinschreibung beachten)
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_malta_eu_national_id_card` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsmaltaeunationalidcard"></a>Keywords_malta_eu_national_id_card

Persönliche numerischen code
  
eindeutige ID-Nummer
  
Anzahl der Bürger-Dienst
  
Anzahl der eindeutigen Identität
  
Uniqueidentityno #
  
Kodiċi Numerali personali
  
Numru ta ' Identifikazzjoni Uniku
  
Numru Aufgabe Servizz Taċ-ċittadin
  
Numru ta' Identità Uniku
  
## <a name="netherlands"></a>Niederlande

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_netherlands_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort gefunden wird.
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_netherlands_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsnetherlandseunationalidcard"></a>Keywords_netherlands_eu_national_id_card

Persönliche numerischen code
  
eindeutige ID-Nummer
  
Anzahl der Bürger-Dienst
  
Anzahl der eindeutigen Identität
  
Uniqueidentityno #
  
bsn
  
Bsn #
  
Persoonlijke Numerieke code
  
Uniek identificatienummer
  
burgerservicenummer
  
Uniek identiteitsnummer
  
## <a name="poland"></a>Polen

Weitere Informationen hierzu finden Sie im Abschnitt "Polen National-ID (PESEL)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Portugal

Weitere Informationen hierzu finden Sie im Abschnitt "Portugal Bürger Card-Nummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="romania"></a>Rumänien

### <a name="format"></a>Format

13 Stellen ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

13 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_romania_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_romania_eu_national_id_card` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_romania_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsromaniaeunationalidcard"></a>Keywords_romania_eu_national_id_card

Persönliche numerischen code
  
eindeutige ID-Nummer
  
CNP
  
CNP #
  
Anheften
  
PIN-
  
Versicherungsvertreter Anzahl
  
Insurancenumber #
  
Anzahl der eindeutigen Identität
  
Uniqueidentityno #
  
COD numerische persönlich
  
Persönliche Identificare Kabeljau
  
COD Unic identificare
  
Persönliche Unic număr
  
Număr identitate
  
Număr Identificare persönliche
  
Număridentitate #
  
Codnumericpersonal #
  
Numărpersonalunic #
  
## <a name="slovakia"></a>Slowakei

### <a name="format"></a>Format

Mit einem umgekehrten Schrägstrich zehn Ziffern
  
### <a name="pattern"></a>Muster

Zehn Ziffern, die ein umgekehrter Schrägstrich enthält:
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovakia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_slovakia_eu_national_id_card` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovakia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordsslovakiaeunationalidcard"></a>Keywords_slovakia_eu_national_id_card

Geburtsdatum Anzahl
  
National Identifikationsnummer
  
Persönliche Identifikationsnummer
  
social security number

  
Nationalnumber #
  
ssn #
  
ssn
  
Vorwahl
  
Persönliche Id-Nummer
  
Personalidnumber #
  
rč
  
Rodné číslo
  
Rodne cislo
  
## <a name="slovenia"></a>Slowenien

### <a name="format"></a>Format

13 Stellen ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

13 Stellen in dem angegebenen Muster:
  
-  Sieben Ziffern, die das Geburtsdatum (DDMMLLL) entsprechen, wobei "LLL" zur letzten drei Ziffern des Jahres Geburtsdatum entspricht 
    
- Zwei Ziffern, die den Bereich Geburtsdatum entsprechen
    
- Drei Ziffern, die eine Kombination von Geschlecht und Seriennummer für Personen, die am gleichen Tag (000-499 für männlich) und 500-999 für Weiblich geboren entsprechen
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovenia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_slovenia_eu_national_id_card` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovenia_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
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

### <a name="keywords"></a>Keywords

#### <a name="keywordssloveniaeunationalidcard"></a>Keywords_slovenia_eu_national_id_card

Persönliche numerischen code
  
eindeutige ID-Nummer
  
eindeutige Nummer
  
Anzahl der eindeutigen Identität
  
Uniqueidentityno #
  
Anzahl der eindeutigen master Bürger
  
Edinstvena Identifikacijska številka
  
Uniqueidentityno #
  
Edinstvena številka Glavnega državljana
  
emšo
  
## <a name="spain"></a>Spanien

### <a name="format"></a>Format

Sieben Ziffern, gefolgt von einem Zeichen
  
### <a name="pattern"></a>Muster

Sieben Ziffern, gefolgt von einem Zeichen
  
- Sieben Ziffern 
    
- Eine Ziffern oder Buchstaben (nicht Groß-/Kleinschreibung)
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_spain_eu_national_id_card` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_spain_eu_national_id_card"` gefunden wird. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsspaineunationalidcard"></a>Keywords_spain_eu_national_id_card

DNI
  
National Identifikationsnummer
  
Anzahl der National Identität
  
Versicherungsvertreter Anzahl
  
Persönliche Identifikationsnummer
  
National Identität
  
Private Identität keine
  
Anzahl der eindeutigen Identität
  
Nationalidno #
  
UniqueID-
  
DNI #
  
Nationalid #
  
Nie #
  
nie
  
Nienúmero #
  
Nie número
  
Documento Nacional de identidad
  
Identidad único
  
Número Nacional identidad
  
DNI número
  
Dninúmero #
  
Identidadúnico #
  
## <a name="sweden"></a>Schweden

Weitere Informationen hierzu finden Sie im Abschnitt "Schwedische Ausweisnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Siehe auch

[Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)

