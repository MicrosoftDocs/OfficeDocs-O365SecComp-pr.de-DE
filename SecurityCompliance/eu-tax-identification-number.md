---
title: EU-Steuernummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: In diesem Thema wird eine Data Loss Prevention (DLP) Richtlinie sieht für bei der Entdeckung des Typs der EU Steuernummer vertraulichen Informationen. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 5192496b393d15fd6d063e09c9bfe1cb3dd7e2dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529425"
---
# <a name="eu-tax-identification-number"></a>EU-Steuernummer

In diesem Thema dargestellt was eine Data Loss Prevention (DLP)-Richtlinie für den Typ der EU Tax Identification-Nummer (US) vertrauliche Daten erkannt. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
  
## <a name="austria"></a>Österreich

### <a name="format"></a>Format

Neun Ziffern mit bedingter Trennstrich und Schrägstrich
  
### <a name="pattern"></a>Muster

Neun Ziffern mit bedingter Trennstrich und Schrägstrich:
  
-  Zwei Ziffern 
    
- Ein Bindestrich (optional)
    
- Drei Ziffern
    
- Ein Schrägstrich (optional)
    
- Vier Ziffern
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_austria_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
          <Match idRef="Keywords_austria_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsaustriaeutaxfilenumber"></a>Keywords_austria_eu_tax_file_number

Steuernummer
  
Anzahl
  
Steuernummer
  
tax id

  
St.Nr.
  
Steuernummer
  
## <a name="belgium"></a>Belgien

### <a name="format"></a>Format

11 Zahlen ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

11 Ziffern:
  
- Zwei Ziffern
    
- Eine "0" oder "1"
    
- Eine Ziffer
    
- Eine "0" oder "1" oder "2" oder "3" 
    
- Sechs Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_belgium_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_belgium_eu_tax_file_number` gefunden wird. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsbelgiumeutaxfilenumber"></a>Keywords_belgium_eu_tax_file_number

Steuernummer
  
Nummer der Eintragung
  
Steuernummer
  
tax id

  
if
  
if-
  
Numéro de Registre national
  
Numéro d ' Identification fiscale
  
## <a name="bulgaria"></a>Bulgarien

### <a name="format"></a>Format

Zehn Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

10 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_bulgaria_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
          <Match idRef="Keywords_bulgaria_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsbulgariaeutaxfilenumber"></a>Keywords_bulgaria_eu_tax_file_number

bucn
  
Uniform der Anzahl
  
Bucn #
  
Uniformcivilnumber #
  
Uniform der id
  
Uniform der Nr.
  
egn
  
Bulgarisch uniform der Anzahl
  
Uniformcivilno #
  
Egn #
  
УНИФОРМ ГРАЖДАНСКИ НОМЕР
  
Униформ-id
  
Униформ граждански-id
  
УНИФОРМ ГРАЖДАНСКИ НЕ
  
## <a name="croatia"></a>Kroatien

### <a name="format"></a>Format

11 Zahlen ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

11 Ziffern:
  
- Zehn Ziffern, zufällig ausgewählte
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_croatia_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
          <Match idRef="Keywords_croatia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordscroatiaeutaxfilenumber"></a>Keywords_croatia_eu_tax_file_number

Steuernummer
  
tax
  
tax id

  
OID
  
OID-
  
Porezni broj
  
## <a name="cyprus"></a>Zypern

### <a name="format"></a>Format

Acht Ziffern und einem Buchstaben in das angegebene Muster
  
### <a name="pattern"></a>Muster

Acht Ziffern und einem Buchstaben:
  
-  EINE "0" 
    
- Sieben Ziffern 
    
- Ein Buchstabe (nicht Groß-/Kleinschreibung)
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_cyprus_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
          <Match idRef="Keywords_cyprus_eu_tax_file_number" />
        </Pattern>
Pattern confidenceLevel="75">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordscypruseutaxfilenumber"></a>Keywords_cyprus_eu_tax_file_number

Steuernummer
  
tax
  
tax id

  
Tax Kenncode
  
Teilstrichen
  
Teilstrichen #
  
ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
ΦΟΡΟΛΟΓΙΚΉ ΤΑΥΤΌΤΗΤΑ
  
ΚΩΔΙΚΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
## <a name="czech-republic"></a>Tschechische Republik

### <a name="format"></a>Format

Neun oder zehn Ziffern und optional einen umgekehrten Schrägstrich
  
### <a name="pattern"></a>Muster

Neun oder zehn Ziffern mit einem optionalen Backslashl:
  
- Sechs Ziffern 
    
- Einen umgekehrten Schrägstrich (optional)
    
- Drei oder vier Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_czech_republic_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_czech_republic_eu_tax_file_number` gefunden wird. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsczechrepubliceutaxfilenumber"></a>Keywords_czech_republic_eu_tax_file_number

Steuernummer
  
tax
  
tax id

  
persönliche Nummer
  
Daňové číslo
  
Osobní číslo
  
## <a name="denmark"></a>Dänemark

### <a name="format"></a>Format

Zehn Ziffern, die einen Bindestrich enthält
  
### <a name="pattern"></a>Muster

Zehn Ziffern, die ein Hyphenl enthält:
  
-  Sechs Ziffern, die das Geburtsdatum (DDMMYY) entsprechen 
    
- Ein Bindestrich 
    
- Vier Ziffern, die ein, wobei die erste Ziffer der Century Geburtsdatum entspricht, Sequenznummer entsprechen und die letzte Ziffer entspricht der betroffenen Person Geschlecht (ungerade für Männlich und sogar weiblich)
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_denmark_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
          <Match idRef="Keywords_denmark_eu_tax_file_number" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsdenmarkeutaxfilenumber"></a>Keywords_denmark_eu_tax_file_number

Steuernummer
  
tax
  
tax id

  
CPR Anzahl
  
CPR-
  
Skat nummer
  
Skat-id
  
## <a name="estonia"></a>Estland

### <a name="format"></a>Format

11 Zahlen ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

11 Ziffern:
  
-  Eine Zahl, die Geschlecht und Century Geburtsdatum, in dem eine ungerade Anzahl gibt Männlich und die gerade Zahl Weiblich wie folgt, entspricht: 1, 2 für die 19. Century; 3, 4 für die allem; 5 und 6 für 2015 
    
- Sechs Ziffern, die Geburtsdatum (JJMMTT) entsprechen
    
- Drei Ziffern, die eine fortlaufende Zahl, die Personen, die an demselben Tag geboren trennt entsprechen
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_estonia_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
          <Match idRef="Keywords_estonia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsestoniaeutaxfilenumber"></a>Keywords_estonia_eu_tax_file_number

Steuernummer
  
tax
  
tax id

  
Persönliche code
  
maksunumber
  
Maksu-id
  
isikukood
  
## <a name="finland"></a>Finnland

### <a name="format"></a>Format

Eine Kombination aus 11 Zeichen Ziffern, Buchstaben, und Plus- und Minuszeichen
  
### <a name="pattern"></a>Muster

Eine Kombination aus 11 Zeichen Ziffern, Buchstaben, und Plus- und Minuszeichen:
  
- Sechs Ziffern
    
- Einer der folgenden: ein Pluszeichen (+), ein Minuszeichen oder dem Buchstaben "A" (nicht Groß-/Kleinschreibung), in dem das Pluszeichen (+) bedeutet, dass, zwischen 1800-1899 geboren, Signieren das Minuszeichen bedeutet, dass zwischen geboren 1900-1999, und "A" bedeutet, dass geboren 2000 und nach
    
- Drei Ziffern
    
- Einen Buchstaben oder eine Zahl
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_finland_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
          <Match idRef="Keywords_finland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsfinlandeutaxfilenumber"></a>Keywords_finland_eu_tax_file_number

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
  
## <a name="france"></a>Frankreich

### <a name="format"></a>Format

13 Stellen für einzelne Benutzer und neun Ziffern für Entitäten
  
### <a name="pattern"></a>Muster

13 Stellen für einzelne Benutzer:
  
- Eine Zahl, die 0, 1, 2 oder 3 sein müssen
    
- 12 Ziffern
    
Neun Ziffern für Entitäten
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_france_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
          <Match idRef="Keywords_france_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsfranceeutaxfilenumber"></a>Keywords_france_eu_tax_file_number

Steuernummer
  
Steuernummer
  
tax id

  
Numéro d ' Identification fiscale
  
## <a name="germany"></a>Deutschland

### <a name="format"></a>Format

11 Zahlen ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

11 Stellen:
  
-  Zehn Ziffern 
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_germany_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
          <Match idRef="Keywords_germany_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsgermanyeutaxfilenumber"></a>Keywords_germany_eu_tax_file_number

Steuernummer
  
Steuern Sie Nein.
  
Taxno #
  
Taxnumber #
  
taxnumber
  
tax id

  
Taxid #
  
Steuernummer
  
Steuernummer nicht.
  
Steuernummer
  
Steuer-id
  
steueridentifikationsnummer
  
## <a name="greece"></a>Griechenland

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_greece_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_greece_eu_tax_file_number` gefunden wird. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsgreeceeutaxfilenumber"></a>Keywords_greece_eu_tax_file_number

AFM
  
tin

  
Steuernummer nicht.
  
keine Steuernummer
  
Steuernummer
  
Registrierung Steuernummer
  
Steuern Sie Registrierung nicht.
  
AFM #
  
Steuernummer #
  
Taxidno #
  
Taxregistryno #
  
ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
aφμ
  
Aφμ αριθμός
  
ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ ΝΟ.
  
ΤΟΝ ΑΡΙΘΜΌ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
## <a name="hungary"></a>Ungarn

### <a name="format"></a>Format

Zehn Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zehn Ziffern:
  
-  Eine Zahl, die "8" sein müssen 
    
- Fünf Ziffern, die die Anzahl der Tage zwischen dem Datum entsprechen, 01/01/1867 und das Geburtsdatum der Person
    
- Drei Ziffern, die die Anzahl an Personen, die an demselben Tag geboren unterscheiden zufällig generiert entsprechen
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_hungary_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
          <Match idRef="Keywords_hungary_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordshungaryeutaxfilenumber"></a>Keywords_hungary_eu_tax_file_number

Ungarisch Steuernummer
  
Ungarisch Steuernummer
  
Steuernummer
  
Anzahl der Mehrwertsteuer
  
Behörde nicht steuern
  
Tax Identität Steuernummer
  
Taxidnumber #
  
Steuernummer #
  
Hungatiantin #
  
keine Steuernummer
  
Taxidno #
  
Adóazonosító szám
  
adószám
  
Adóhatóság szám
  
## <a name="ireland"></a>Irland

### <a name="format"></a>Format

Sieben Ziffern, gefolgt von einem Buchstaben ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Sieben Ziffern, gefolgt von einem Buchstaben:
  
-  Sieben Ziffern  
    
- Ein Buchstabe (nicht Groß-/Kleinschreibung)
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_ireland_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
          <Match idRef="Keywords_ireland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsirelandeutaxfilenumber"></a>Keywords_ireland_eu_tax_file_number

öffentliche Dienstleistungen keine
  
Persönliche öffentliche Dienstleistungen keine
  
PPS keine
  
Persönliche Nein service
  
PPS-service Nein
  
Ppsno #
  
Irland Pps keine
  
Publicserviceno #
  
Anzahl der persönlichen öffentliche Dienstleistungen
  
Uimhir Phearsanta Seirbhíse poiblí
  
PPS-uimh
  
Uimhir Aitheantais phearsanta
  
## <a name="italy"></a>Italien

### <a name="format"></a>Format

16 Buchstaben und Ziffern in dem angegebenen Muster
  
### <a name="pattern"></a>Muster

16 Buchstaben und Ziffern:
  
-  Drei Buchstaben, die die ersten drei Doppelkonsonanten in der der Name der entsprechen 
    
- Drei Buchstaben, die die erste, dritte und vierte entsprechen, Doppelkonsonanten in den Vornamen
    
- Zwei Ziffern, die auf die letzte Ziffern des Jahres Geburtsdatum entsprechen
    
- Eine Ziffer, die den Monat Geburtsdatum entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben A bis E, H, L, M, P, R t verwendet werden (also Januar ist eine und Oktober R)
    
- Zwei Ziffern, die den Tag des Monats Geburtsdatum entsprechen, in dem der Tag Geburtsdaten von bestimmten zur Unterscheidung von Männlich 40 hinzugefügt wird
    
- Vier Ziffern, die speziell für die Gemeinde Ortskennzahl entsprechen, in die Person geboren wurde – Land geltende Codes für Ausland verwendet werden
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_italy_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
          <Match idRef="Keywords_italy_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsitalyeutaxfilenumber"></a>Keywords_italy_eu_tax_file_number

Steuernummer
  
Steuern Sie Nein.
  
Taxno #
  
Taxnumber #
  
taxnumber
  
tax id

  
Taxid #
  
Fiscal code
  
Codice fiscale
  
## <a name="latvia"></a>Lettland

### <a name="format"></a>Format

11 Zahlen ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

11 Stellen in dem angegebenen Muster
  
-  Sechs Ziffern, die das Geburtsdatum (DDMMYY) entsprechen 
    
- Eine Zahl, die die Century Geburtsdatum entspricht, in dem 19. Century entspricht "0", "1" entspricht allem und 2015 "2" entspricht
    
- Vier Ziffern
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_latvia_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
          <Match idRef="Keywords_latvia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordslatviaeutaxfilenumber"></a>Keywords_latvia_eu_tax_file_number

Steuernummer
  
Steuern Sie Nein.
  
Taxno #
  
Taxnumber #
  
taxnumber
  
tax id

  
Taxid #
  
Steuernummer
  
Steuernummer nicht.
  
Nodokļa numurs
  
Nodokļu Identifikācijas numurs
  
Nodokļu Identifikācija numurs
  
## <a name="lithuania"></a>Litauen

### <a name="format"></a>Format

11 Zahlen ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

11 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_lithuania_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
          <Match idRef="Keywords_lithuania_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordslithuaniaeutaxfilenumber"></a>Keywords_lithuania_eu_tax_file_number

Steuernummer
  
Steuern Sie Nein.
  
Steuerinformationen Nein #
  
Taxnumber #
  
taxnumber
  
tax id

  
Taxid #
  
Steuernummer
  
Steuernummer nicht.
  
Mokesčių-id
  
Mokesčių numeris
  
Mokesčių Identifikavimas numeris
  
## <a name="luxemburg"></a>Luxemburg

### <a name="format"></a>Format

13 Stellen ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

13 Ziffern:
  
-  11 Ziffern 
    
- Zwei Prüfziffern
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_luxemburg_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
          <Match idRef="Keywords_luxemburg_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsluxemburgeutaxfilenumber"></a>Keywords_luxemburg_eu_tax_file_number

Steuernummer
  
Steuern Sie Nein.
  
Taxno #
  
Taxnumber #
  
taxnumber
  
tax id

  
Taxid #
  
Steuernummer
  
Steuernummer nicht.
  
Steuernummer
  
Steuer-id
  
steueridentifikationsnummer
  
## <a name="malta"></a>Malta

### <a name="format"></a>Format

Maltesisch Staatsangehörigen: 7 Ziffern und einem Buchstaben in das angegebene Muster
  
Nicht-Maltesisch Staatsangehörigen und Maltesisch Entitäten: 9 Ziffern
  
### <a name="pattern"></a>Muster

Maltesisch Staatsangehörigen: 7 Ziffern und einem Buchstaben
  
-  Sieben Ziffern  
    
- Ein Buchstabe (nicht Groß-/Kleinschreibung)
    
Nicht-Maltesisch Staatsangehörigen und Maltesisch Entitäten: 9 Ziffern
  
-  Neun Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_malta_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_malta_eu_tax_file_number" />
          <Match idRef="Keywords_malta_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsmaltaeutaxfilenumber"></a>Keywords_malta_eu_tax_file_number

Steuernummer
  
Steuern Sie Nein.
  
Taxno #
  
Taxnumber #
  
taxnumber
  
tax id

  
Taxid #
  
Steuernummer
  
Steuernummer nicht.
  
Numru Tat-taxxa
  
ID Tat-taxxa
  
Numru ta ' Identifikazzjoni Tat-Taxxa
  
## <a name="netherlands"></a>Niederlande

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Neun Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_netherlands_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
          <Match idRef="Keywords_netherlands_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsnetherlandseutaxfilenumber"></a>Keywords_netherlands_eu_tax_file_number

Niederlande Steuernummer
  
Niederlande Steuernummer
  
der niederländische Steuernummer
  
der niederländische Steuernummer
  
Steuernummer
  
Niederländische Steuernummer
  
Niederländische Steuernummer
  
tax id

  
Nr.
  
Steuernummer
  
Steuerinformationen Nein #
  
Tax #
  
tin

  
Steuernummer #
  
Niederlande Steuernummer
  
der niederländische Steuernummer
  
Niederlande Belasting identificatienummer
  
Identificatienummer van belasting
  
Identificatienummer belasting
  
Niederlande Belasting identificatie
  
Niederlande Belasting-Id-nummer
  
Niederlande belastingnummer
  
btw Nummer
  
Nederlandse Belasting identificatie
  
## <a name="poland"></a>Polen

### <a name="format"></a>Format

Elf Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Elf Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_poland_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
          <Match idRef="Keywords_poland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordspolandeutaxfilenumber"></a>Keywords_poland_eu_tax_file_number

Steuernummer
  
Steuern Sie Nein.
  
Taxno #
  
Taxnumber #
  
taxnumber
  
Aktivieren der
  
Aktivieren der #
  
tax id

  
Nr.
  
Aktivieren der id
  
Aktivieren der ID-Nummer
  
Steuernummer
  
Steuernummer nicht.
  
Anzahl der Mehrwertsteuer
  
Umsatzsteuer.
  
Vatno #
  
ber
  
Mehrwertsteuer-ID-Nummer
  
Anzahl Identyfikacji podatkowej
  
Polski Anzahl Identyfikacji podatkowej
  
Numeridentyfikacjipodatkowej #
  
## <a name="portugal"></a>Portugal

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_portugal_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
          <Match idRef="Keywords_portugal_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsportugaleutaxfilenumber"></a>Keywords_portugal_eu_tax_file_number

Steuernummer
  
Steuern Sie Nein.
  
Taxno #
  
Taxnumber #
  
taxnumber
  
if
  
if-
  
Numero Geschäftsjahr
  
Número de Identificação Geschäftszeiträume
  
## <a name="romania"></a>Rumänien

### <a name="format"></a>Format

13 Stellen ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

13 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_romania_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_romania_eu_tax_file_number` gefunden wird. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsromaniaeutaxfilenumber"></a>Keywords_romania_eu_tax_file_number

tax id

  
Steuernummer
  
Datei nicht steuern
  


tax file number
  
Nein Steuerinformationen
  
Steuernummer
  
Taxid #
  
Taxno #
  
ID-Ul taxei
  
Numărul de Identificare fiscală
  
## <a name="slovakia"></a>Slowakei

### <a name="format"></a>Format

10 Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

10 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_slovakia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_slovakia_eu_tax_file_number` gefunden wird. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsslovakiaeutaxfilenumber"></a>Keywords_slovakia_eu_tax_file_number

tax id

  
Steuernummer
  
Steuernummer-id
  
Steuernummer Nr.
  
Slowakische Steuernummer-id
  
tin

  
Datei nicht steuern
  


tax file number
  
Nein Steuerinformationen
  
Steuernummer
  
Taxid #
  
Taxno #
  
Daňové Identifikačné číslo
  
Daňové číslo
  
Daňové číslo súboru
  
## <a name="slovenia"></a>Slowenien

### <a name="format"></a>Format

Acht Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Acht Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_slovenia_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_nation_eu_tax_file_number" />
          <Match idRef="Keywords_nation_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordssloveniaeutaxfilenumber"></a>Keywords_slovenia_eu_tax_file_number

tax id

  
Steuernummer
  
Steuernummer-id
  
Steuernummer Nr.
  
Slowenisch Steuernummer-id
  
tin

  
Datei nicht steuern
  


tax file number
  
Nein Steuerinformationen
  
Steuernummer
  
Taxid #
  
Taxno #
  
Identifikacijska številka davka
  
Davčna številka
  
Številka Davčne datoteke
  
## <a name="spain"></a>Spanien

### <a name="format"></a>Format

Sieben oder acht Ziffern und ein oder zwei Buchstaben in das angegebene Muster
  
### <a name="pattern"></a>Muster

Spanische natürliche Personen mit einer Spanien National Identität Karte:
  
-  Acht Ziffern 
    
- Einen Großbuchstaben (Groß-/Kleinschreibung) 
    
Nicht Spaniards ohne eine Spanien National-Personalausweis
  
- Einen Großbuchstaben "L" (Groß-/Kleinschreibung)
    
- Sieben Ziffern 
    
- Einen Großbuchstaben (Groß-/Kleinschreibung) 
    
Berater Spaniards unter 14 Jahre ohne eine Spanien National Personalausweis:
  
- Ein Großbuchstabe "K" (Groß-/Kleinschreibung)
    
-  Sieben Ziffern  
    
- Einen Großbuchstaben (Groß-/Kleinschreibung)
    
Foreigners mit einer Foreigner-ID
  
- Einen Großbuchstaben Buchstabe d. h., "X", "Y" oder "Z" (Groß-/Kleinschreibung) 
    
- Sieben Ziffern 
    
- Einen Großbuchstaben (Groß-/Kleinschreibung) 
    
Foreigners ohne eine Foreigner-ID-Nummer
  
- Einen Großbuchstaben, das "M" (Groß-/Kleinschreibung) ist. 
    
- Sieben Ziffern 
    
- Einen Großbuchstaben (Groß-/Kleinschreibung) 
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_spain_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
          <Match idRef="Keywords_spain_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsspaineutaxfilenumber"></a>Keywords_spain_eu_tax_file_number

tax id

  
Steuernummer
  
Cif-id
  
Cif keine
  
Spanische Cif-id
  
cif
  
Datei nicht steuern
  
Spanische Cif-Anzahl
  


tax file number
  
Spanische Cif keine
  
Nein Steuerinformationen
  
Steuernummer
  
Taxid #
  
Taxno #
  
CIFID #
  
Spanishcifid #
  
Spanishcifno #
  
Número de contribuyente
  
Número de Impuesto corporativo
  
Número de Identificación Geschäftszeiträume
  
Cif-número
  
Cifnúmero #
  
## <a name="sweden"></a>Schweden

### <a name="format"></a>Format

Zehn Ziffern und ein Symbol in das angegebene Muster
  
### <a name="pattern"></a>Muster

Zehn Ziffern und ein Symbol:
  
-  Sechs Ziffern, die das Geburtsdatum (JJMMTT) entsprechen 
    
- Ein Pluszeichen (+), Minuszeichen oder umgekehrter Schrägstrich
    
- Drei Ziffern, aus die die Kennung zusammensetzt Nummer eindeutige Where wählen: 
    
  - Zahlen, die vor dem 1990 ausgestellt wurden identifizieren Sie die siebte und die achte Ziffer den Kanton des Geburtsdatum oder foreign-born Personen
    
  - Die Ziffer in der neunten Position gibt Geschlecht nach entweder ungerade für männlich oder sogar Weiblich
    
- Ein Kontrollkästchen Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_sweden_eu_tax_file_number` gefunden wird. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
          <Match idRef="Keywords_sweden_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsswedeneutaxfilenumber"></a>Keywords_sweden_eu_tax_file_number

tax id

  
Steuernummer nicht.
  
Steuernummer
  
tax identification

  
Tax Identification #
  
Steuern Sie Nein.
  
Tax #
  
Taxid #
  
Tax-Datei
  
Steuern Sie Datei nicht.
  
Persönliche Id-Nummer
  
Skatt-Id-nummer
  
Skatt identifikation
  
personnummer
  
## <a name="uk"></a>GROßBRITANNIEN

### <a name="format"></a>Format

Eindeutige Steuernummer-Referenz (UTR): 10 Ziffern ohne Leerzeichen und Trennzeichen
  
Sozialversicherungsnummer (NINO): Weitere Informationen hierzu finden Sie im Abschnitt "Großbritannien National Insurance Anzahl (NINO)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
### <a name="pattern"></a>Muster

Eindeutige Steuernummer-Referenz (UTR): 10 Ziffern
  
Sozialversicherungsnummer (NINO): Weitere Informationen hierzu finden Sie im Abschnitt "Großbritannien National Insurance Anzahl (NINO)" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_uk_eu_tax_file_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_uk_eu_tax_file_number` gefunden wird. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsukeutaxfilenumber"></a>Keywords_uk_eu_tax_file_number

tax id

  
Steuernummer nicht.
  
Steuernummer
  
tax identification

  
Tax Identification #
  
Steuern Sie Nein.
  
Tax #
  
Taxid #
  
Tax-Datei
  
Steuern Sie Datei nicht.
  
## <a name="see-also"></a>Siehe auch

[Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)

