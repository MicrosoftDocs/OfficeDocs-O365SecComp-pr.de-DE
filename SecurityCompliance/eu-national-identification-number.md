---
title: Nationale IdentifikationsNummer der EU
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp EU National Identification Number erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: afae2c3fa54fe5fcd93990cdf5797f5517c46202
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410970"
---
# <a name="eu-national-identification-number"></a>Nationale IdentifikationsNummer der EU

In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp EU National Identification Number erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
  
## <a name="austria"></a>Österreich

### <a name="format"></a>Format

Eine 24-Zeichen-Kombination aus Buchstaben, Ziffern und Sonderzeichen
  
### <a name="pattern"></a>Muster

24 Zeichen:
  
-  22 Buchstaben (Groß-/Kleinschreibung nicht beachtet), Ziffern, Schrägstriche, Schrägstriche oder Pluszeichen 
    
- Zwei Buchstaben (ohne Unterscheidung nach Groß-/Kleinschreibung), Ziffern, Schrägstriche, Schrägstriche, Pluszeichen oder Gleichheitszeichen
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_austria_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_austria_eu_national_id_card` aus wurde gefunden. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsaustriaeunationalidcard"></a>Keywords_austria_eu_national_id_card

Österreichische Identitätsnummer
  
nationale Identitätsnummer
  
Identitätsnummer
  
national id
  
Personalausweis Republik Österreich
  
## <a name="belgium"></a>Belgien

Weitere Informationen finden Sie im Abschnitt "belgische nationale Rufnummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="bulgaria"></a>Bulgarien

### <a name="format"></a>Format

Zehn Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

Zehn Ziffern ohne Leerzeichen und Abgrenzungen
  
-  Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT) 
    
- Zwei Ziffern, die der Geburts Reihenfolge entsprechen
    
- Eine Ziffer, die dem Geschlecht entspricht: eine gerade Ziffer für männliche und eine ungerade Ziffer für weiblich
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_bulgaria_national_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_bulgaria_national_number` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_bulgaria_national_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsbulgarianationalnumber"></a>Keywords_bulgaria_national_number

EGN
  
EGN
  
Bulgarische Nationale Nummer
  
nationale Nummer
  
social security number
  
nationalnumber #
  
SSN
  
SSN
  
nationalnumber
  
BNN
  
BNN
  
persönliche ID-Nummer
  
personalidnumber #
  
единен граждански номер
  
edinn grazhdanski Nomer
  
егн
  
егн #
  
## <a name="croatia"></a>Kroatien

Weitere Informationen finden Sie im Abschnitt "Croatia Identity Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="cyprus"></a>Zypern

### <a name="format"></a>Format

Zehn Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

 Zehn Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_cyprus_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_cyprus_eu_national_id_card` aus wurde gefunden. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordscypruseunationalidcard"></a>Keywords_cyprus_eu_national_id_card

ID-Kartennummer
  
national identification number
  
persönliche ID-Nummer
  
Personalausweisnummer
  
ταυτοτητασ
  
## <a name="czech-republic"></a>Tschechien

Weitere Informationen finden Sie im Abschnitt "Czech National Identity Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="denmark"></a>Dänemark

Weitere Informationen finden Sie im Abschnitt "Denmark Personal Identification Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="estonia"></a>Estland

### <a name="format"></a>Format

11 Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

11 Ziffern:
  
- Eine Ziffer, die dem Geschlecht und dem Jahrhundert der Geburt entspricht (ungerade Zahl, gerade Zahl weiblich; 1-2:19. Jahrhundert; 3-4:20. Jahrhundert; 5-6:21st Century)
    
- Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)
    
- Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am selben Datum geboren wurden
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_estonia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_estonia_eu_national_id_card` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_estonia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsestoniaeunationalidcard"></a>Keywords_estonia_eu_national_id_card

persönlicher Identifizierungscode
  
persönliche Identifikationsnummer
  
national identification number
  
nationale Nummer
  
persönliche ID-Nummer
  
personalidnumber #
  
IK
  
Isikukood
  
ID-Kaart
  
## <a name="finland"></a>Finnland

Weitere Informationen finden Sie im Abschnitt "Finland National ID" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>Frankreich

Weitere Informationen finden Sie im Abschnitt "France National ID Card (CNI)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Deutschland

Weitere Informationen finden Sie im Abschnitt "Deutschland PersonalausweisNummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Griechenland

Weitere Informationen finden Sie im Abschnitt "GriechenLand National ID Card" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Ungarn

### <a name="format"></a>Format

11 Ziffern
  
### <a name="pattern"></a>Muster

11 Ziffern:
  
-  Eine Ziffer, die dem Geschlecht entspricht (1-männlich, 2-weiblich, andere Zahlen sind auch für Bürger möglich, die vor 1900 oder Bürger mit doppelter Staatsbürgerschaft geboren wurden) 
    
- Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)
    
- Drei Ziffern, die einer Seriennummer entsprechen
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_hungary_eu_national_id_card` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordshungaryeunationalidcard"></a>Keywords_hungary_eu_national_id_card

persönliche Identifikationsnummer
  
identification number
  
persönliche ID-Nummer
  
személyazonosító igazolvány
  
## <a name="ireland"></a>Irland

### <a name="format"></a>Format

Eine neunstellige Kombination aus Buchstaben, Ziffern und einem Leerzeichen im angegebenen Muster
  
### <a name="pattern"></a>Muster

Eine neunstellige Kombination aus Buchstaben, Ziffern und einem Leerzeichen im angegebenen Muster
  
Vom 01. Januar 2013 bis jetzt:
  
-  Sieben Ziffern  
    
- Eine Prüfziffer
    
- Ein Leerzeichen oder der Großbuchstabe "W" (Groß-/Kleinschreibung)
    
Vor 01. Januar 2013:
  
-  Sieben Ziffern  
    
- Eine Prüfziffer
    
- Ein Leerzeichen oder ein Großbuchstabe (Groß-/Kleinschreibung beachtet)
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.
    
- Ein Schlüsselwort aus wurde gefunden.
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsirelandeunationalidcard"></a>Keywords_ireland_eu_national_id_card

persönliche öffentliche Dienstnummer
  
PPS Nein
  
Umsatz-und Sozialversicherungsnummer
  
RSI-No
  
persönliche Identifikationsnummer
  
identification number
  
persönliche ID-Nummer
  
uimhir phearsanta seirbhíse poiblí
  
uimh. PSP
  
## <a name="italy"></a>Italien

### <a name="format"></a>Format

Eine 16-stellige Kombination aus Buchstaben und Ziffern im angegebenen Muster
  
### <a name="pattern"></a>Muster

Eine 16-stellige Kombination aus Buchstaben und Ziffern:
  
- Drei Buchstaben, die den ersten drei Konsonanten im Familiennamen entsprechen
    
- Drei Buchstaben, die dem ersten, dritten und vierten Konsonanten im Vornamen entsprechen
    
- Zwei Ziffern, die den letzten Ziffern des Geburtsjahrs entsprechen
    
- Ein Buchstabe, der dem Buchstaben für den Geburtsmonat entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben A bis E, H, L, M, P, R bis T werden verwendet (also Januar ist A und Oktober ist R)
    
- Zwei Ziffern, die dem Tag des Geburtsmonats entsprechen – zur Unterscheidung zwischen den Geschlechtern wird 40 zum Geburtstag für Frauen hinzugefügt.
    
- Vier Ziffern, die der Ortskennzahl für die Gemeinde entsprechen, in der die Person geboren wurde (landesweite Codes werden für fremde Länder verwendet)
    
- Eine Paritäts Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_italy_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_italy_eu_national_id_card` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_italy_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsitalyeunationalidcard"></a>Keywords_italy_eu_national_id_card

persönlicher Code
  
persönliche Codenummer
  
persönliche Zertifikatsnummer
  
Fiskal Code
  
personalcodeno #
  
persönliche ID-Nummer
  
persönlicher ID-Code
  
codedice personale
  
Numero Bescheinigung personale
  
Numero personale
  
Numero-ID personale
  
codedice-ID personale
  
Geschäftsjahr
  
## <a name="italy"></a>Italien

### <a name="format"></a>Format

11 Ziffern und ein Bindestrich im angegebenen Format
  
### <a name="pattern"></a>Muster

11 Ziffern und ein Bindestrich:
  
-  Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ) 
    
- Ein Bindestrich 
    
- Eine Ziffer, die dem Jahrhundert der Geburt entspricht ("0" für das 19. Jahrhundert, "1" für das 20. Jahrhundert und "2" für das 21. Jahrhundert)
    
- Vier Ziffern, nach dem Zufallsprinzip generiert
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_latvia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_latvia_eu_national_id_card` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_latvia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordslatviaeunationalidcard"></a>Keywords_latvia_eu_national_id_card

persönlicher Code
  
persönliche Codenummer
  
persönliche Zertifikatsnummer
  
personalcodeno #
  
persönliche ID-Nummer
  
persönlicher ID-Code
  
Personas KODS
  
## <a name="lithuania"></a>Litauen

### <a name="format"></a>Format

11 Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

11 Ziffern ohne Leerzeichen und Abgrenzungen:
  
- Eine Ziffer, die dem Geschlecht der Person und dem Jahrhundert der Geburt entspricht
    
-  Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT) 
    
- Drei Ziffern, die der Seriennummer des Geburtsdatums entsprechen
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_lithuania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_lithuania_eu_national_id_card` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_lithuania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordslithuaniaeunationalidcard"></a>Keywords_lithuania_eu_national_id_card

persönlicher numerischer Code
  
eindeutige Identifikationsnummer
  
Citizen-Dienstnummer
  
eindeutige Identitätsnummer
  
uniqueidentityno #
  
persönlicher Code.
  
asmeninis skaitmeninis koda
  
unikalus identifikavimo Numeris
  
piliečio paslaugos Numeris
  
unikalus identifikavimo koda
  
Mens koda.
  
## <a name="luxemburg"></a>Luxemburg

### <a name="format"></a>Format

11 Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

11 Ziffern
  
- Eine Ziffer, die dem Geschlecht der Person und dem Jahrhundert der Geburt entspricht
    
-  Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT) 
    
- Drei Ziffern, die der Seriennummer des Geburtsdatums entsprechen
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_luxemburg_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_luxemburg_eu_national_id_card` aus wurde gefunden. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsluxemburgeunationalidcard"></a>Keywords_luxemburg_eu_national_id_card

persönliche ID
  
persönliche ID-Nummer
  
personalidno #
  
eindeutige ID-Nummer
  
personalidnumber #
  
eindeutiger ID-Schlüssel
  
persönlicher ID-Code
  
uniqueidkey #
  
individueller Code
  
einzelne ID
  
eindeutige-ID-Nummer
  
eindeutige-ID
  
ID personnelle
  
Numéro d'identification Personal
  
idpersonnelle #
  
persönliche Identifikationsnummer
  
EINDEUTIGEID #
  
## <a name="malta"></a>Malta

### <a name="format"></a>Format

Sieben Ziffern gefolgt von einem Buchstaben
  
### <a name="pattern"></a>Muster

Sieben Ziffern gefolgt von einem Buchstaben:
  
-  Sieben Ziffern  
    
- Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_malta_eu_national_id_card` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_malta_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsmaltaeunationalidcard"></a>Keywords_malta_eu_national_id_card

persönlicher numerischer Code
  
eindeutige Identifikationsnummer
  
Citizen-Dienstnummer
  
eindeutige Identitätsnummer
  
uniqueidentityno #
  
Kodiċi personali
  
numru ta ' identifikazzjoni uniku
  
numru TAS-servizz taċ-ċittadin
  
numru ta ' identità uniku
  
## <a name="netherlands"></a>Niederlande

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

Neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_netherlands_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort aus wurde gefunden.
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_netherlands_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsnetherlandseunationalidcard"></a>Keywords_netherlands_eu_national_id_card

persönlicher numerischer Code
  
eindeutige Identifikationsnummer
  
Citizen-Dienstnummer
  
eindeutige Identitätsnummer
  
uniqueidentityno #
  
BSN
  
BSN
  
Persoonlijke-numerieke-Code
  
uniek identificatienummer
  
burgerservicenummer
  
uniek identiteitsnummer
  
## <a name="poland"></a>Polen

Weitere Informationen finden Sie im Abschnitt "polnische National ID (PESEL)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Portugal

Weitere Informationen finden Sie im Abschnitt "portugiesische Bürgerkarten Nummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="romania"></a>Rumänien

### <a name="format"></a>Format

13 Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

13 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_romania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_romania_eu_national_id_card` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_romania_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsromaniaeunationalidcard"></a>Keywords_romania_eu_national_id_card

persönlicher numerischer Code
  
eindeutige Identifikationsnummer
  
CNP
  
CNP
  
PIN
  
PIN
  
Versicherungsnummer
  
insurancenumber #
  
eindeutige Identitätsnummer
  
uniqueidentityno #
  
COD numerische Personal
  
COD identificare Personal
  
COD Unic identificare
  
număr Personal Unic
  
număr identitate
  
număr identificare Personal
  
număridentitate #
  
codnumericpersonal #
  
numărpersonalunic #
  
## <a name="slovakia"></a>Slowakei

### <a name="format"></a>Format

Zehn Ziffern mit einem umgekehrten Schrägstrich
  
### <a name="pattern"></a>Muster

Zehn Ziffern mit einem umgekehrten Schrägstrich:
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovakia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_slovakia_eu_national_id_card` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovakia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsslovakiaeunationalidcard"></a>Keywords_slovakia_eu_national_id_card

Geburtsnummer
  
national identification number
  
persönliche Identifikationsnummer
  
social security number
  
nationalnumber #
  
SSN
  
SSN
  
nationale Nummer
  
persönliche ID-Nummer
  
personalidnumber #
  
rč
  
rodné číslo
  
rodne cislo
  
## <a name="slovenia"></a>Slowenien

### <a name="format"></a>Format

13 Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

13 Ziffern im angegebenen Muster:
  
-  Sieben Ziffern, die dem Geburtsdatum (DDMMLLL) entsprechen, wobei "LLL" den letzten drei Ziffern des Geburtsjahrs entspricht. 
    
- Zwei Ziffern, die dem Bereich der Geburt entsprechen
    
- Drei Ziffern, die einer Kombination aus Geschlecht und Seriennummer für Personen entsprechen, die am selben Tag geboren wurden (000-499 für männlich und 500-999 für weiblich)
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovenia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_slovenia_eu_national_id_card` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_slovenia_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordssloveniaeunationalidcard"></a>Keywords_slovenia_eu_national_id_card

persönlicher numerischer Code
  
eindeutige Identifikationsnummer
  
eindeutige Registrierungsnummer
  
eindeutige Identitätsnummer
  
uniqueidentityno #
  
eindeutige Master Bürger-Nummer
  
edinstvena identifikacijska številka
  
uniqueidentityno #
  
edinstvena številka glavnega državljana
  
EMŠO
  
## <a name="spain"></a>Spanien

### <a name="format"></a>Format

Sieben Ziffern gefolgt von einem Zeichen
  
### <a name="pattern"></a>Muster

Sieben Ziffern gefolgt von einem Zeichen
  
- Sieben Ziffern 
    
- Eine Ziffer oder ein Buchstaben (Groß-/Kleinschreibung nicht beachtet)
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_spain_eu_national_id_card` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_spain_eu_national_id_card"` aus wurde gefunden. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsspaineunationalidcard"></a>Keywords_spain_eu_national_id_card

DNI
  
national identification number
  
nationale Identitätsnummer
  
Versicherungsnummer
  
persönliche Identifikationsnummer
  
nationale Identität
  
persönliche Identität Nein
  
eindeutige Identitätsnummer
  
nationalidno #
  
UniqueId
  
DNI
  
National-Nr.
  
nie
  
nie
  
nienúmero #
  
nie número
  
Documento Nacional de Identidad
  
Identidad Único
  
número Nacional Identidad
  
DNI número
  
dninúmero #
  
identidadúnico #
  
## <a name="sweden"></a>Schweden

Weitere Informationen finden Sie im Abschnitt "schwedische National ID" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Siehe auch

[Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)

