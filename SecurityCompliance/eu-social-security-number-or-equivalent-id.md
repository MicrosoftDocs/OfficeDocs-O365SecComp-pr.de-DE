---
title: EU Sozialversicherungsnummer oder einer ähnlichen-ID
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: In diesem Thema wird eine Data Loss Prevention (DLP) Richtlinie sieht für beim Erkennen des EU Sozialversicherungsnummer oder gleichwertige ID vertrauliche Informationen-Typs. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 6f1027dcfb648ed937b8180d74d4bc6348dab650
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529332"
---
# <a name="eu-social-security-number-or-equivalent-id"></a>EU Sozialversicherungsnummer oder einer ähnlichen-ID

In diesem Thema wird, wonach eine Data Loss Prevention (DLP) Richtlinie sucht bei der Entdeckung des EU Sozialversicherungsnummer (SSN) oder die entsprechende ID vertrauliche Informationen Typs. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
  
## <a name="austria"></a>Österreich

### <a name="format"></a>Format

10 Ziffern im angegebenen format
  
### <a name="pattern"></a>Muster

10 Ziffern:
  
-  Drei Ziffern, die eine fortlaufende Zahl entsprechen 
    
- Ein Kontrollkästchen Ziffer
    
- Sechs Ziffern, die das Geburtsdatum (DDMMYY) entsprechen
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_austria_eu_ssn_or_equivalent` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_austria_eu_ssn_or_equivalent" />
        </Pattern>
<Pattern confidenceLevel="75">
            <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsaustriaeussnorequivalent"></a>Keywords_austria_eu_ssn_or_equivalent

soziale Sicherheit keine
  
social security number

  

social security code
  
Versicherungsvertreter Anzahl
  
österreichische ssn
  
ssn #
  
ssn
  
Versicherungsvertreter code
  
Versicherungsvertreter Code #
  
Socialsecurityno #
  
Sozialversicherungsnummer
  
Soziale Sicherheit kein
  
Versicherungsnummer
  
## <a name="belgium"></a>Belgien

### <a name="format"></a>Format

11 Zahlen ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

11 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_belgium_eu_ssn_or_equivalent` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_belgium_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsbelgiumeussnorequivalent"></a>Keywords_belgium_eu_ssn_or_equivalent

belgische Vorwahl
  
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
  
national numéro
  
numéro de sécurité

  
Numéro d'Assuré
  
national identifiant
  
Identifiantnational #
  
Numéronational #
  
## <a name="croatia"></a>Kroatien

### <a name="format"></a>Format

11 Zahlen ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

 11 Ziffern: 
  
-  Zehn Ziffern 
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_croatia_eu_ssn_or_equivalent` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_croatia_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordscroatiaeussnorequivalent"></a>Keywords_croatia_eu_ssn_or_equivalent

Persönliche Identifikationsnummer
  
Anzahl der Master Bürger
  
National Identifikationsnummer
  
social security number

  
Nationalnumber #
  
ssn #
  
ssn
  
nationalnumber
  
Bnn #
  
bnn
  
Persönliche Id-Nummer
  
Personalidnumber #
  
oib
  
Osobni Identifikacijski broj
  
## <a name="czech-republic"></a>Tschechische Republik

### <a name="format"></a>Format

Zehn Ziffern und einem umgekehrten Schrägstrich in dem angegebenen Muster
  
### <a name="pattern"></a>Muster

Zehn Ziffern und einem umgekehrten Schrägstrich:
  
- Sechs Ziffern, die das Geburtsdatum (JJMMTT) entsprechen: 
    
- Ein umgekehrter Schrägstrich
    
- Drei Ziffern, die eine fortlaufende Zahl entsprechen, die Personen, die an demselben Tag geboren trennt
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_czech_republic_eu_ssn_or_equivalent` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_czech_republic_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsczechrepubliceussnorequivalent"></a>Keywords_czech_republic_eu_ssn_or_equivalent

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
  
## <a name="denmark"></a>Dänemark

### <a name="format"></a>Format

Zehn Ziffern und ein Bindestrich in dem angegebenen Muster
  
### <a name="pattern"></a>Muster

Zehn Ziffern und ein Bindestrich:
  
- Sechs Ziffern, die das Geburtsdatum (DDMMYY) entsprechen 
    
- Ein Bindestrich 
    
- Vier Ziffern, die eine Sequenznummer entsprechen
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_denmark_eu_ssn_or_equivalent` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_denmark_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsdenmarkeussnorequivalent"></a>Keywords_denmark_eu_ssn_or_equivalent

Persönliche Identifikationsnummer
  
National Identifikationsnummer
  
social security number

  
Nationalnumber #
  
ssn #
  
ssn
  
Vorwahl
  
Persönliche Id-Nummer
  
Personalidnumber #
  
CPR-nummer
  
personnummer
  
## <a name="finland"></a>Finnland

### <a name="format"></a>Format

Eine Kombination 11 Zeichen im angegebenen format
  
### <a name="pattern"></a>Muster

Eine Kombination der 11 Zeichen im angegebenen Format:
  
-  Sechs Ziffern 
    
- Eine Instanz einer der folgenden:
    
  - Plus -symbol
    
  - Minuszeichen
    
  - Die Buchstaben "A" (nicht Groß-/Kleinschreibung)
    
- Drei Ziffern
    
- Einen Buchstaben oder eine Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_finland_eu_ssn_or_equivalent` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_finland_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsfinlandeussnorequivalent"></a>Keywords_finland_eu_ssn_or_equivalent

identification number

  
Persönliche id
  
Anzahl der Identität
  
Anzahl der Finnland Personalausweis
  
Personalidnumber #
  
National Identifikationsnummer
  
ID-Nummer
  
Personalausweis keine.
  
Ausweis-Id-Nummer
  
ID keine
  
tunnistenumero
  
henkilötunnus
  
Yksilöllinen Henkilökohtainen tunnistenumero
  
Ainutlaatuinen Henkilökohtainen tunnus
  
Identiteetti numero
  
Suomen Kansallinen henkilötunnus
  
Henkilötunnusnumero #
  
Kansallisen tunnistenumero
  
tunnusnumero
  
Kansallinen Tunnus numero
  
hetu
  
## <a name="france"></a>Frankreich

Weitere Informationen hierzu finden Sie im Abschnitt "französische Sozialversicherungsnummer (INSEE)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Deutschland

Weitere Informationen hierzu finden Sie im Abschnitt "Deutschland Identität Card-Nummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Griechenland

Weitere Informationen hierzu finden Sie im Abschnitt "Griechenland nationale d ' Identité" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Ungarn

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_hungary_eu_ssn_or_equivalent` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_hungary_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordshungaryeussnorequivalent"></a>Keywords_hungary_eu_ssn_or_equivalent

Ungarisch Sozialversicherungsnummer
  
social security number

  
Socialsecuritynumber #
  
Hssn #
  
socialsecuritynno
  
hssn
  
taj
  
Taj #
  
ssn
  
ssn #
  
soziale Sicherheit keine
  
áfa
  
Közösségi adószám
  
Általános Forgalmi Adó szám
  
Hozzáadottérték adó
  
Áfa szám
  
Magyar Áfa szám
  
## <a name="portugal"></a>Portugal

Weitere Informationen hierzu finden Sie im Abschnitt "Portugal Bürger Card-Nummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="spain"></a>Spanien

Weitere Informationen hierzu finden Sie im Abschnitt "Spanien Sozialversicherungsnummer (SSN)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="sweden"></a>Schweden

### <a name="format"></a>Format

12 Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

12 Ziffern:
  
-  Acht Ziffern, die das Geburtsdatum (JJJJMMTT) entsprechen 
    
- Drei Ziffern, die eine fortlaufende Zahl entsprechen, in dem: 
    
  - Die letzte Ziffer in der Seriennummer gibt Geschlecht an, durch die Zuweisung von eine ungerade Anzahl für Männlich und eine gerade Anzahl für Weiblich
    
  - Bis zu 1990 entsprach die Zuordnung der Seriennummer auf den Kanton Geburtsbetriebs der Anzahl der Bearer oder (wenn vor 1947 geboren), in dem er hatte wurde Leben, gemäß Tax-Datensätze auf Januar 1, 1947 mit einen speziellen Code (in der Regel 9 als 7. Ziffer) für Einwanderer 
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_sweden_eu_ssn_or_equivalent` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_sweden_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsswedeneussnorequivalent"></a>Keywords_sweden_eu_ssn_or_equivalent

Persönliche Id-Nummer
  
identification number

  
Persönliche Id keine
  
Identität keine
  
Kennung keine
  
Persönliche Identifikationsnummer keine
  
Personnummer-id
  
Personligt-Id-nummer
  
Unikt-Id-nummer
  
personnummer
  
identifikationsnumret
  
Personnummer #
  
Identifikationsnumret #
  
## <a name="see-also"></a>Siehe auch

[Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)

