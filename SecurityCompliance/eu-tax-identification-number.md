---
title: USt-ID-Nummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Steuernummer erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 4914ff078695519c2a298190d82c86a6abebceb9
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410910"
---
# <a name="eu-tax-identification-number"></a>USt-ID-Nummer

In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie bei der Erkennung des vertraulichen Informationstyps "TIN" (EU Tax Identification Number) sucht. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
  
## <a name="austria"></a>Österreich

### <a name="format"></a>Format

Neun Ziffern mit optionalem Bindestrich und Schrägstrich
  
### <a name="pattern"></a>Muster

Neun Ziffern mit optionalem Bindestrich und Schrägstrich:
  
-  Zwei Ziffern 
    
- Ein Bindestrich (optional)
    
- Drei Ziffern
    
- Ein Schrägstrich (optional)
    
- Vier Ziffern
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_austria_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsaustriaeutaxfilenumber"></a>Keywords_austria_eu_tax_file_number

Steuernummer
  
number
  
Steuernummer
  
tax id
  
St.Nr.
  
Steuernummer
  
## <a name="belgium"></a>Belgien

### <a name="format"></a>Format

11 Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

11 Ziffern:
  
- Zwei Ziffern
    
- "0" oder "1"
    
- Eine Ziffer
    
- "0" oder "1" oder "2" oder "3" 
    
- Sechs Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_belgium_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_belgium_eu_tax_file_number` aus wurde gefunden. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsbelgiumeutaxfilenumber"></a>Keywords_belgium_eu_tax_file_number

Steuernummer
  
nationale Registrierungsnummer
  
Steuernummer
  
tax id
  
NIF
  
NIF
  
Numéro de Registre National
  
Numéro d'identification Fiscale
  
## <a name="bulgaria"></a>Bulgarien

### <a name="format"></a>Format

Zehn Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

10 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_bulgaria_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsbulgariaeutaxfilenumber"></a>Keywords_bulgaria_eu_tax_file_number

BUCN
  
einheitliche Zivil Nummer
  
BUCN
  
uniformcivilnumber #
  
einheitliche Civil ID
  
einheitliches ziviles Nein
  
EGN
  
Bulgarische einheitliche Zivil Nummer
  
uniformcivilno #
  
EGN
  
униформ граждански номер
  
униформ-ID
  
униформ-граждански-ID
  
униформ граждански не
  
## <a name="croatia"></a>Kroatien

### <a name="format"></a>Format

11 Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

11 Ziffern:
  
- Zehn Ziffern, zufällig gewählt
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_croatia_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordscroatiaeutaxfilenumber"></a>Keywords_croatia_eu_tax_file_number

Steuernummer
  
Steuer
  
tax id
  
oid
  
OID
  
porezni Broj
  
## <a name="cyprus"></a>Zypern

### <a name="format"></a>Format

Acht Ziffern und ein Buchstabe im angegebenen Muster
  
### <a name="pattern"></a>Muster

Acht Ziffern und ein Buchstabe:
  
-  Ein "0" 
    
- Sieben Ziffern 
    
- Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_cyprus_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordscypruseutaxfilenumber"></a>Keywords_cyprus_eu_tax_file_number

Steuernummer
  
Steuer
  
tax id
  
USt-ID-Code
  
TIC
  
TIC
  
αριθμός φορολογικού μητρώου
  
φορολογική ταυτότητα
  
κωδικός φορολογικού μητρώου
  
## <a name="czech-republic"></a>Tschechien

### <a name="format"></a>Format

Neun oder zehn Ziffern mit optionalem Backslash
  
### <a name="pattern"></a>Muster

Neun oder zehn Ziffern mit einem optionalen umgekehrten Schrägstrich:
  
- Sechs Ziffern 
    
- Ein umgekehrter Schrägstrich (optional)
    
- Drei oder vier Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_czech_republic_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_czech_republic_eu_tax_file_number` aus wurde gefunden. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsczechrepubliceutaxfilenumber"></a>Keywords_czech_republic_eu_tax_file_number

Steuernummer
  
Steuer
  
tax id
  
persönliche Nummer
  
Daňové číslo
  
Osobní číslo
  
## <a name="denmark"></a>Dänemark

### <a name="format"></a>Format

Zehn Ziffern mit einem Bindestrich
  
### <a name="pattern"></a>Muster

Zehn Ziffern, die einen Bindestrich enthalten:
  
-  Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ) 
    
- Ein Bindestrich 
    
- Vier Ziffern, die einer Sequenznummer entsprechen, wobei die erste Ziffer dem Jahrhundert der Geburt entspricht und die letzte Ziffer dem Geschlecht des einzelnen entspricht (ungerade für männlich und sogar für weiblich)
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_denmark_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsdenmarkeutaxfilenumber"></a>Keywords_denmark_eu_tax_file_number

Steuernummer
  
Steuer
  
tax id
  
CPR-Nummer
  
CPR
  
Skate Nummer
  
Skat-ID
  
## <a name="estonia"></a>Estland

### <a name="format"></a>Format

11 Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

11 Ziffern:
  
-  Eine Ziffer, die dem Geschlecht und dem Jahrhundert der Geburt entspricht, wobei eine ungerade Zahl männliche und die gerade Zahl angibt, wie folgt: 1,2 für das 19. Jahrhundert; 3, 4 für das 20. Jahrhundert; und 5, 6 für das 21. Jahrhundert 
    
- Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)
    
- Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am selben Datum geboren wurden
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_estonia_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsestoniaeutaxfilenumber"></a>Keywords_estonia_eu_tax_file_number

Steuernummer
  
Steuer
  
tax id
  
persönlicher Code
  
maksunumber
  
maksu-ID
  
Isikukood
  
## <a name="finland"></a>Finnland

### <a name="format"></a>Format

Eine 11-stellige Kombination aus Ziffern, Buchstaben und Plus-und Minuszeichen
  
### <a name="pattern"></a>Muster

Eine 11-stellige Kombination aus Ziffern, Buchstaben und Plus-und Minuszeichen:
  
- Sechs Ziffern
    
- Eine der folgenden Optionen: ein Pluszeichen, ein Minuszeichen oder der Buchstabe "A" (ohne Beachtung der Groß-/Kleinschreibung), wobei das Pluszeichen zwischen 1800-1899, das Minuszeichen zwischen 1900-1999 und "A" als geboren 2000 und nach
    
- Drei Ziffern
    
- Ein Buchstaben oder eine Zahl
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_finland_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsfinlandeutaxfilenumber"></a>Keywords_finland_eu_tax_file_number

identification number
  
persönliche ID
  
Identitätsnummer
  
nationale finnische ID-Nummer
  
personalidnumber #
  
national identification number
  
ID-Nummer
  
nationale ID-Nr.
  
nationale ID-Nummer
  
ID Nein
  
tunnistenumero
  
henkilötunnus
  
yksilöllinen henkilökohtainen tunnistenumero
  
ainutlaatuinen henkilökohtainen tunnus
  
identiteetti numero
  
Suomen der Kok henkilötunnus
  
henkilötunnusnumero #
  
kansallisen tunnistenumero
  
tunnusnumero
  
der Kok tunnus numero
  
## <a name="france"></a>Frankreich

### <a name="format"></a>Format

13 Ziffern für Einzelpersonen und neun Ziffern für Entitäten
  
### <a name="pattern"></a>Muster

13 Ziffern für Einzelpersonen:
  
- Eine Ziffer, die 0, 1, 2 oder 3 sein muss
    
- 12 Ziffern
    
Neun Ziffern für Entitäten
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_france_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsfranceeutaxfilenumber"></a>Keywords_france_eu_tax_file_number

USt-ID-Nummer
  
Steuernummer
  
tax id
  
Numéro d'identification Fiscale
  
## <a name="germany"></a>Deutschland

### <a name="format"></a>Format

11 Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

11 Ziffern:
  
-  Zehn Ziffern 
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_germany_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsgermanyeutaxfilenumber"></a>Keywords_germany_eu_tax_file_number

Steuernummer
  
Steuernummer
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id
  
getaxit #
  
USt-ID-Nummer
  
USt-ID-Nr.
  
Steuernummer
  
Ingo-ID
  
Steueridentifikationsnummer
  
## <a name="greece"></a>Griechenland

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

Neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_greece_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_greece_eu_tax_file_number` aus wurde gefunden. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsgreeceeutaxfilenumber"></a>Keywords_greece_eu_tax_file_number

AFM
  
Zinn
  
USt-ID-Nr.
  
USt-ID-Nr.
  
USt-ID-Nummer
  
Steuerregistrierungsnummer
  
Steuerregistrierungsnummer
  
AFM
  
Zinn
  
taxidno #
  
taxregistryno #
  
αριθμός φορολογικού μητρώου
  
aφμ
  
aφμ αριθμός
  
φορολογικού μητρώου νο.
  
τον αριθμό φορολογικού μητρώου
  
## <a name="hungary"></a>Ungarn

### <a name="format"></a>Format

Zehn Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

Zehn Ziffern:
  
-  Eine Ziffer, die "8" sein muss 
    
- Fünf Ziffern, die der Anzahl von Tagen zwischen dem Datum 01/01/1867 und dem Geburtsdatum des einzelnen entsprechen
    
- Drei Ziffern, die der Zahl entsprechen, die von Wahrscheinlichkeit zur Unterscheidung von Individuen generiert wurde, die am selben Tag geboren wurden
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_hungary_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordshungaryeutaxfilenumber"></a>Keywords_hungary_eu_tax_file_number

ungarische Steuernummer
  
ungarische Dose
  
USt-ID-Nummer
  
USt-IdNr.
  
Finanzamt Nein
  
USt-ID-Steuernummer
  
taxidnumber #
  
Zinn
  
hungatiantin #
  
USt-ID-Nr.
  
taxidno #
  
adóazonosító szám
  
adószám
  
adóhatóság szám
  
## <a name="ireland"></a>Irland

### <a name="format"></a>Format

Sieben Ziffern, gefolgt von einem Buchstaben ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Sieben Ziffern gefolgt von einem Buchstaben:
  
-  Sieben Ziffern  
    
- Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_ireland_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsirelandeutaxfilenumber"></a>Keywords_ireland_eu_tax_file_number

öffentlicher Dienst Nein
  
persönlicher öffentlicher Dienst Nein
  
PPS Nein
  
persönlicher Dienst Nein
  
PPS-Dienst Nein
  
ppsno #
  
Irisch PPS Nein
  
publicserviceno #
  
persönliche öffentliche Dienstnummer
  
uimhir phearsanta seirbhíse poiblí
  
PPS-uimh
  
uimhir aitheantais phearsanta
  
## <a name="italy"></a>Italien

### <a name="format"></a>Format

16 Buchstaben und Ziffern im angegebenen Muster
  
### <a name="pattern"></a>Muster

16 Buchstaben und Ziffern:
  
-  Drei Buchstaben, die den ersten drei Konsonanten im Familiennamen entsprechen 
    
- Drei Buchstaben, die dem ersten, dritten und vierten Konsonanten im Vornamen entsprechen
    
- Zwei Ziffern, die den letzten Ziffern des Geburtsjahrs entsprechen
    
- Eine Ziffer, die dem Geburtsmonat entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben A bis E, H, L, M, P, R bis T werden verwendet (also Januar ist A und Oktober ist R)
    
- Zwei Ziffern, die dem Tag des Geburtsmonats entsprechen, wobei 40 zum Geburtstag hinzugefügt wird, damit Frauen von Männern unterschieden werden.
    
- Vier Ziffern, die einer Ortskennzahl für die Gemeinde entsprechen, in der die Person geboren wurde – landesweite Codes werden für fremde Länder verwendet
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_italy_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsitalyeutaxfilenumber"></a>Keywords_italy_eu_tax_file_number

Steuernummer
  
Steuernummer
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id
  
getaxit #
  
Fiskal Code
  
Geschäftsjahr
  
## <a name="latvia"></a>Lettland

### <a name="format"></a>Format

11 Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

11 Ziffern im angegebenen Muster
  
-  Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ) 
    
- Eine Ziffer, die dem Jahrhundert der Geburt entspricht, wobei "0" dem 19. Jahrhundert entspricht, "1" entspricht dem 20. Jahrhundert, und "2" entspricht dem 21. Jahrhundert
    
- Vier Ziffern
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_latvia_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordslatviaeutaxfilenumber"></a>Keywords_latvia_eu_tax_file_number

Steuernummer
  
Steuernummer
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id
  
getaxit #
  
USt-ID-Nummer
  
USt-ID-Nr.
  
nodokļa numurs
  
nodokļu identifikācijas numurs
  
nodokļu identifikācija numurs
  
## <a name="lithuania"></a>Litauen

### <a name="format"></a>Format

11 Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

11 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_lithuania_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordslithuaniaeutaxfilenumber"></a>Keywords_lithuania_eu_tax_file_number

Steuernummer
  
Steuernummer
  
Steuernummer
  
taxnumber #
  
taxnumber
  
tax id
  
getaxit #
  
USt-ID-Nummer
  
USt-ID-Nr.
  
mokesčių-ID
  
mokesčių Numeris
  
mokesčių identifikavimas Numeris
  
## <a name="luxemburg"></a>Luxemburg

### <a name="format"></a>Format

13 Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

13 Ziffern:
  
-  11 Ziffern 
    
- Zwei Prüfziffern
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_luxemburg_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsluxemburgeutaxfilenumber"></a>Keywords_luxemburg_eu_tax_file_number

Steuernummer
  
Steuernummer
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id
  
getaxit #
  
USt-ID-Nummer
  
USt-ID-Nr.
  
Steuernummer
  
Ingo-ID
  
Steueridentifikationsnummer
  
## <a name="malta"></a>Malta

### <a name="format"></a>Format

Für maltesische Staatsangehörige: 7 Ziffern und ein Buchstabe im angegebenen Muster
  
Nicht maltesische Staatsangehörige und maltesische Entitäten: 9 Ziffern
  
### <a name="pattern"></a>Muster

Maltesische Staatsangehörige: 7 Ziffern und ein Buchstabe
  
-  Sieben Ziffern  
    
- Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)
    
Nicht maltesische Staatsangehörige und maltesische Entitäten: 9 Ziffern
  
-  Neun Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_malta_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsmaltaeutaxfilenumber"></a>Keywords_malta_eu_tax_file_number

Steuernummer
  
Steuernummer
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id
  
getaxit #
  
USt-ID-Nummer
  
USt-ID-Nr.
  
numru tat-Taxxa
  
ID tat-Taxxa
  
numru ta ' identifikazzjoni tat-Taxxa
  
## <a name="netherlands"></a>Niederlande

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

Neun Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_netherlands_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsnetherlandseutaxfilenumber"></a>Keywords_netherlands_eu_tax_file_number

niederländische Steuernummer
  
niederländische Steueridentifikation
  
USt-ID-Nummer Niederlande
  
niederländische Steueridentifikation
  
USt-ID-Nummer
  
niederländische Steuernummer
  
niederländische Steuernummer
  
tax id
  
USt-ID-Nummer
  
Steuernummer
  
Steuernummer
  
Steuer
  
Zinn
  
Zinn
  
Niederlande Zinn
  
Zinn der Niederlande
  
Nederlands identificatienummer
  
identificatienummer van belastend
  
identificatienummer-Belastungen
  
Nederlands identificatie
  
Nederlands-Nummer-ID
  
Nederlands belastingnummer
  
BTW Nummer
  
Nederlandse identificatie
  
## <a name="poland"></a>Polen

### <a name="format"></a>Format

Elf Ziffern ohne Leerzeichen
  
### <a name="pattern"></a>Muster

Elf Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_poland_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordspolandeutaxfilenumber"></a>Keywords_poland_eu_tax_file_number

Steuernummer
  
Steuernummer
  
taxno #
  
taxnumber #
  
taxnumber
  
NIP
  
NIP
  
tax id
  
USt-ID-Nummer
  
NIP-ID
  
NIP-ID #
  
USt-ID-Nummer
  
USt-ID-Nr.
  
USt-IdNr.
  
USt-IdNr.
  
vatno #
  
USt-ID
  
USt-ID #
  
Numer identyfikacji podatkowej
  
Polski Numer identyfikacji podatkowej
  
numeridentyfikacjipodatkowej #
  
## <a name="portugal"></a>Portugal

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

Neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_portugal_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsportugaleutaxfilenumber"></a>Keywords_portugal_eu_tax_file_number

Steuernummer
  
Steuernummer
  
taxno #
  
taxnumber #
  
taxnumber
  
NIF
  
NIF
  
Numero Fiscal
  
número de identificação Fiscal
  
## <a name="romania"></a>Rumänien

### <a name="format"></a>Format

13 Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

13 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_romania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_romania_eu_tax_file_number` aus wurde gefunden. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsromaniaeutaxfilenumber"></a>Keywords_romania_eu_tax_file_number

tax id
  
USt-ID-Nummer
  
Steuerdatei Nein
  
tax file number
  
Steuernummer
  
Steuernummer
  
getaxit #
  
taxno #
  
ID – UL-taxei
  
numărul de identificare fiscală
  
## <a name="slovakia"></a>Slowakei

### <a name="format"></a>Format

10 Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

10 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_slovakia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_slovakia_eu_tax_file_number` aus wurde gefunden. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsslovakiaeutaxfilenumber"></a>Keywords_slovakia_eu_tax_file_number

tax id
  
USt-ID-Nummer
  
Tin-ID
  
Tin Nein
  
Slowakische Tin-ID
  
Zinn
  
Steuerdatei Nein
  
tax file number
  
Steuernummer
  
Steuernummer
  
getaxit #
  
taxno #
  
Daňové identifikačné číslo
  
Daňové číslo
  
Daňové číslo SÚBORU
  
## <a name="slovenia"></a>Slowenien

### <a name="format"></a>Format

Acht Ziffern ohne Leerzeichen oder Begrenzungen
  
### <a name="pattern"></a>Muster

Acht Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_slovenia_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordssloveniaeutaxfilenumber"></a>Keywords_slovenia_eu_tax_file_number

tax id
  
USt-ID-Nummer
  
Tin-ID
  
Tin Nein
  
slowenische Tin-ID
  
Zinn
  
Steuerdatei Nein
  
tax file number
  
Steuernummer
  
Steuernummer
  
getaxit #
  
taxno #
  
identifikacijska številka beim Davka
  
davčna številka
  
številka davčne datoteke
  
## <a name="spain"></a>Spanien

### <a name="format"></a>Format

Sieben oder acht Ziffern und ein oder zwei Buchstaben im angegebenen Muster
  
### <a name="pattern"></a>Muster

Spanische natürliche Personen mit einem nationalen spanischen Identitätsausweis:
  
-  Acht Ziffern 
    
- Ein Großbuchstabe (Groß-/Kleinschreibung beachtet) 
    
Nicht residente Spanier ohne nationalen Personalausweis
  
- Ein Großbuchstabe "L" (Groß-/Kleinschreibung)
    
- Sieben Ziffern 
    
- Ein Großbuchstabe (Groß-/Kleinschreibung beachtet) 
    
Residente Spanier unter 14 Jahren ohne National Ausweis für Spanien:
  
- Ein Großbuchstabe "K" (Groß-/Kleinschreibung beachten)
    
-  Sieben Ziffern  
    
- Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)
    
Ausländer mit der IdentifikationsNummer eines ausLänders
  
- Ein Großbuchstabe, der "X", "Y" oder "Z" ist (Groß-/Kleinschreibung) 
    
- Sieben Ziffern 
    
- Ein Großbuchstabe (Groß-/Kleinschreibung beachtet) 
    
Ausländer ohne IdentifikationsNummer eines ausLänders
  
- Ein Großbuchstabe, der "M" (Groß-/Kleinschreibung beachtet) ist 
    
- Sieben Ziffern 
    
- Ein Großbuchstabe (Groß-/Kleinschreibung beachtet) 
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_spain_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsspaineutaxfilenumber"></a>Keywords_spain_eu_tax_file_number

tax id
  
USt-ID-Nummer
  
CIF-ID
  
CIF Nein
  
spanische CIF-ID
  
CIF
  
Steuerdatei Nein
  
spanische CIF-Nummer
  
tax file number
  
Spanisch (CIF) Nein
  
Steuernummer
  
Steuernummer
  
getaxit #
  
taxno #
  
CIFID #
  
spanishcifid #
  
spanishcifno #
  
número de contribuyente
  
número de Impuesto Corporativo
  
número de Identificación Fiscal
  
CIF-número
  
cifnúmero #
  
## <a name="sweden"></a>Schweden

### <a name="format"></a>Format

Zehn Ziffern und ein Symbol im angegebenen Muster
  
### <a name="pattern"></a>Muster

Zehn Ziffern und ein Symbol:
  
-  Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT) 
    
- Ein Pluszeichen, Minuszeichen oder umgekehrter Schrägstrich
    
- Drei Ziffern, die die Identifizierungsnummer eindeutig machen, wobei: 
    
  - Für Zahlen, die vor 1990 ausgegeben wurden, kennzeichnen die siebte und die achte Ziffer den Geburtsort oder die im Ausland geborenen Personen.
    
  - Die Ziffer in der neunten Position gibt an, dass Geschlecht entweder ungerade für männlich oder sogar für weiblich ist.
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_sweden_eu_tax_file_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsswedeneutaxfilenumber"></a>Keywords_sweden_eu_tax_file_number

tax id
  
USt-ID-Nr.
  
USt-ID-Nummer
  
tax identification
  
USt-Identifikationsnummer
  
Steuernummer
  
Steuer
  
getaxit #
  
Steuerdatei
  
Steuerdatei Nr.
  
persönliche ID-Nummer
  
Skate ID Nummer
  
Skate Identifikation
  
PERSONNUMMER
  
## <a name="uk"></a>UK

### <a name="format"></a>Format

Eindeutige Steuerzahler-Referenz (UTR): 10 Ziffern ohne Leerzeichen und Abgrenzungen
  
Nationale Versicherungsnummer (NINO): Weitere Informationen finden Sie im Abschnitt "U.K. National Insurance Number (NINO) "in [dem, wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
### <a name="pattern"></a>Muster

Eindeutige Steuerzahler-Referenz (UTR): 10 Ziffern
  
Nationale Versicherungsnummer (NINO): Weitere Informationen finden Sie im Abschnitt "U.K. National Insurance Number (NINO) "in [dem, wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_uk_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_uk_eu_tax_file_number` aus wurde gefunden. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsukeutaxfilenumber"></a>Keywords_uk_eu_tax_file_number

tax id
  
USt-ID-Nr.
  
USt-ID-Nummer
  
tax identification
  
USt-Identifikationsnummer
  
Steuernummer
  
Steuer
  
getaxit #
  
Steuerdatei
  
Steuerdatei Nr.
  
## <a name="see-also"></a>Siehe auch

[Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)

