---
title: EU-sozialVersicherungsNummer oder entsprechende ID
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn die EU-sozialVersicherungsNummer oder der entsprechende ID-vertrauliche Informationstyp erkannt wird. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: c0c808eafa52209c79f3b4e8a2113f587fd8a771
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410800"
---
# <a name="eu-social-security-number-or-equivalent-id"></a>EU-sozialVersicherungsNummer oder entsprechende ID

In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn die EU-sozialVersicherungsNummer (SSN) oder der entsprechende ID-vertrauliche Informationstyp erkannt wird. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
  
## <a name="austria"></a>Österreich

### <a name="format"></a>Format

10 Ziffern im angegebenen Format
  
### <a name="pattern"></a>Muster

10 Ziffern:
  
-  Drei Ziffern, die einer Seriennummer entsprechen 
    
- Eine Prüfziffer
    
- Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_austria_eu_ssn_or_equivalent` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_austria_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsaustriaeussnorequivalent"></a>Keywords_austria_eu_ssn_or_equivalent

Sozialversicherungsnummer
  
social security number
  
social security code
  
Versicherungsnummer
  
Austrian SSN
  
SSN
  
SSN
  
versicherungscode
  
versicherungscode #
  
socialsecurityno #
  
Sozialversicherungsnummer
  
soziale Sicherheit kein
  
Versicherungsnummer
  
## <a name="belgium"></a>Belgien

### <a name="format"></a>Format

11 Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

11 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_belgium_eu_ssn_or_equivalent` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_belgium_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsbelgiumeussnorequivalent"></a>Keywords_belgium_eu_ssn_or_equivalent

belgische nationale Nummer
  
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
  
Numéro National
  
numéro de sécurité
  
Numéro d'assuré
  
identifizierbare nationale
  
identifiantnational #
  
numéronational #
  
## <a name="croatia"></a>Kroatien

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
  
- Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_croatia_eu_ssn_or_equivalent` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_croatia_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordscroatiaeussnorequivalent"></a>Keywords_croatia_eu_ssn_or_equivalent

persönliche Identifikationsnummer
  
Master-Bürgerzahl
  
national identification number
  
social security number
  
nationalnumber #
  
SSN
  
SSN
  
nationalnumber
  
BNN
  
BNN
  
persönliche ID-Nummer
  
personalidnumber #
  
OIB
  
Osobni identifikacijski Broj
  
## <a name="czech-republic"></a>Tschechien

### <a name="format"></a>Format

Zehn Ziffern und ein umgekehrter Schrägstrich im angegebenen Muster
  
### <a name="pattern"></a>Muster

Zehn Ziffern und ein umgekehrter Schrägstrich:
  
- Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT): 
    
- Einen umgekehrten Schrägstrich
    
- Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am selben Datum geboren wurden
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_czech_republic_eu_ssn_or_equivalent` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_czech_republic_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsczechrepubliceussnorequivalent"></a>Keywords_czech_republic_eu_ssn_or_equivalent

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
  
## <a name="denmark"></a>Dänemark

### <a name="format"></a>Format

Zehn Ziffern und ein Bindestrich im angegebenen Muster
  
### <a name="pattern"></a>Muster

Zehn Ziffern und ein Bindestrich:
  
- Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ) 
    
- Ein Bindestrich 
    
- Vier Ziffern, die einer Sequenznummer entsprechen
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_denmark_eu_ssn_or_equivalent` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_denmark_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsdenmarkeussnorequivalent"></a>Keywords_denmark_eu_ssn_or_equivalent

persönliche Identifikationsnummer
  
national identification number
  
social security number
  
nationalnumber #
  
SSN
  
SSN
  
nationale Nummer
  
persönliche ID-Nummer
  
personalidnumber #
  
CPR-Nummer
  
PERSONNUMMER
  
## <a name="finland"></a>Finnland

### <a name="format"></a>Format

Eine Kombination aus 11 Zeichen im angegebenen Format
  
### <a name="pattern"></a>Muster

Eine Kombination aus 11 Zeichen im angegebenen Format:
  
-  Sechs Ziffern 
    
- Eine der folgenden Instanzen:
    
  - Plus-Symbol
    
  - Minus Zeichen
    
  - Der Buchstabe "A" (Groß-/Kleinschreibung wird nicht beachtet)
    
- Drei Ziffern
    
- Ein Buchstabe oder eine Ziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_finland_eu_ssn_or_equivalent` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_finland_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsfinlandeussnorequivalent"></a>Keywords_finland_eu_ssn_or_equivalent

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
  
Hetu
  
## <a name="france"></a>Frankreich

Weitere Informationen finden Sie im Abschnitt "französische sozialVersicherungsNummer (INSEE)" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Deutschland

Weitere Informationen finden Sie im Abschnitt "Deutschland PersonalausweisNummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Griechenland

Weitere Informationen finden Sie im Abschnitt "GriechenLand National ID Card" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Ungarn

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

Neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_hungary_eu_ssn_or_equivalent` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_hungary_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordshungaryeussnorequivalent"></a>Keywords_hungary_eu_ssn_or_equivalent

Sozialversicherungsnummer (ungarisch)
  
social security number
  
socialsecuritynumber #
  
hssn #
  
socialsecuritynno
  
hssn
  
Taj
  
Taj
  
SSN
  
SSN
  
Sozialversicherungsnummer
  
ÁFA
  
közösségi adószám
  
Általános forgalmi adó szám
  
hozzáadottérték adó
  
ÁFA szám
  
Magyar ÁFA szám
  
## <a name="portugal"></a>Portugal

Weitere Informationen finden Sie im Abschnitt "portugiesische Bürgerkarten Nummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="spain"></a>Spanien

Weitere Informationen finden Sie im Abschnitt "sozialVersicherungsNummer (SSN) in Spanien" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="sweden"></a>Schweden

### <a name="format"></a>Format

12 Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

12 Ziffern:
  
-  Acht Ziffern, die dem Geburtsdatum entsprechen (JJJJMMTT) 
    
- Drei Ziffern, die einer Seriennummer entsprechen, wobei: 
    
  - Die letzte Ziffer in der Seriennummer kennzeichnet das Geschlecht durch die Zuweisung einer ungerade Zahl für männliche und eine gerade Zahl für weibliche
    
  - Bis zu 1990 entspricht die Zuordnung der Seriennummer der Grafschaft, in der der Träger der Nummer geboren wurde, oder (wenn er vor 1947 geboren wurde), in dem er nach Steuerdaten Sätzen am 1. Januar 1947 lebte, mit einem speziellen Code (in der Regel 9 als 7. Ziffer) für Einwanderer 
    
- Eine Prüfziffer
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_sweden_eu_ssn_or_equivalent` aus wurde gefunden. 
    
Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_sweden_eu_ssn_or_equivalent` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
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

### <a name="keywords"></a>Schlüsselwörter

#### <a name="keywordsswedeneussnorequivalent"></a>Keywords_sweden_eu_ssn_or_equivalent

persönliche ID-Nummer
  
identification number
  
persönliche ID Nein
  
Identität Nein
  
Identifikationsnummer
  
persönliche Identifikationsnummer
  
PERSONNUMMER-ID
  
personligt-ID-Nummer
  
unikt-ID-Nummer
  
PERSONNUMMER
  
identifikationsnumret
  
PERSONNUMMER #
  
identifikationsnumret #
  
## <a name="see-also"></a>Siehe auch

[Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)

