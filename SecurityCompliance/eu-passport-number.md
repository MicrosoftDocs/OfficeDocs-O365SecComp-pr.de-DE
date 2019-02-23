---
title: EU-Passport-Nummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Passport-Nummer erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: c46f683bd1baf651bcf13c1766dfff3cb953b341
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218265"
---
# <a name="eu-passport-number"></a>EU-Passport-Nummer

In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Passport-Nummer erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
  
## <a name="austria"></a>Österreich

### <a name="format"></a>Format

Ein Buchstabe gefolgt von einem optionalen Leerzeichen und sieben Ziffern
  
### <a name="pattern"></a>Muster

Eine Kombination aus einem Buchstaben, sieben Ziffern und einem Leerzeichen:
  
- Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)
    
- Ein Leerzeichen (optional)
    
- Sieben Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_austria_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_austria_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_austria_eu_passport_number**|
|:-----|
|Passnummer  <br/> Österreichische Passnummer  <br/> Passport-Nr.  <br/> Reisepass  <br/> österreichisch Reisepass  <br/> |
   
## <a name="belgium"></a>Belgien

### <a name="format"></a>Format

Zwei Buchstaben, gefolgt von sechs Ziffern, ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben, gefolgt von sechs Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_belgium_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_belgium_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_belgium_eu_passport_number**|
|:-----|
|Passnummer  <br/> belgische Passnummer  <br/> Passport-Nr.  <br/> paspoort  <br/> paspoortnummer  <br/> Reisepass kein  <br/> Reisepass  <br/> |
   
## <a name="bulgaria"></a>Bulgarien

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

 Neun Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_bulgaria_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_bulgaria_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_bulgaria_eu_passport_number**|
|:-----|
|Passnummer  <br/> Bulgarische Passnummer  <br/> Passport-Nr.  <br/> номер на паспорта  <br/> |
   
## <a name="croatia"></a>Kroatien

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

 Neun Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_croatia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_croatia_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_croatia_eu_passport_number**|
|:-----|
|Passnummer  <br/> Kroatische Passnummer  <br/> Passport-Nr.  <br/> Broj putovnice  <br/> |
   
## <a name="cyprus"></a>Zypern

### <a name="format"></a>Format

Ein Buchstabe, gefolgt von 6-8 Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

Ein Buchstabe gefolgt von sechs bis acht Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_cyprus_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_cyprus_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_cyprus_eu_passport_number**|
|:-----|
|Passnummer  <br/> Zypern-Passnummer  <br/> Passport-Nr.  <br/> αριθμό διαβατηρίου  <br/> |
   
## <a name="czech-republic"></a>Tschechien

### <a name="format"></a>Format

Acht Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

Acht Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_czech_republic_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_czech_republic_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_czech_republic_eu_passport_number**|
|:-----|
|Passnummer  <br/> Tschechische Passnummer  <br/> Passport-Nr.  <br/> Cestovní Pas  <br/> Pas  <br/> |
   
## <a name="denmark"></a>Dänemark

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

 Neun Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_denmark_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_denmark_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_denmark_eu_passport_number**|
|:-----|
|Passnummer  <br/> dänische Passnummer  <br/> Passport-Nr.  <br/> Pas  <br/> pasnummer  <br/> |
   
## <a name="estonia"></a>Estland

### <a name="format"></a>Format

Ein Buchstaben, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Ein Buchstabe gefolgt von sieben Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_estonia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_estonia_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_estonia_eu_passport_number**|
|:-----|
|Passnummer  <br/> Estnische Passnummer  <br/> Passport-Nr.  <br/> Eesti kodaniku-Durchlauf  <br/> |
   
## <a name="finland"></a>Finnland

Weitere Informationen finden Sie im Abschnitt "Finland Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>Frankreich

Weitere Informationen finden Sie im Abschnitt "Frankreich Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Deutschland

Weitere Informationen finden Sie im Abschnitt "Deutschland Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Griechenland

### <a name="format"></a>Format

Zwei Buchstaben, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben gefolgt von sieben Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_greece_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_greece_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_greece_eu_passport_number**|
|:-----|
|Passnummer  <br/> griechische Passnummer  <br/> Passport-Nr.  <br/> διαβατηριο  <br/> |
   
## <a name="hungary"></a>Ungarn

### <a name="format"></a>Format

Zwei Buchstaben, gefolgt von sechs oder sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben, gefolgt von sechs oder sieben Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_hungary_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_hungary_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_hungary_eu_passport_number**|
|:-----|
|Passnummer  <br/> ungarische Passnummer  <br/> Passport-Nr.  <br/> útlevél száma  <br/> |
   
## <a name="ireland"></a>Irland

### <a name="format"></a>Format

Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:
  
- Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)
    
- Sieben Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_ireland_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_ireland_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_ireland_eu_passport_number**|
|:-----|
|Passnummer  <br/> irische Passnummer  <br/> Passport-Nr.  <br/> Pas  <br/> passport  <br/> Passeport  <br/> Passeport numero  <br/> |
   
## <a name="italy"></a>Italien

### <a name="format"></a>Format

Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:
  
- Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)
    
- Sieben Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_italy_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_italy_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_italy_eu_passport_number**|
|:-----|
|italienische Passnummer  <br/> Repubblica Italiana Passa Porto  <br/> Passa Porto  <br/> Passa Porto Italiana  <br/> Passnummer  <br/> Italiana Passa Porto numero  <br/> Passa Porto numero  <br/> Numéro Passeport Italien  <br/> Numéro Passeport  <br/> |
   
## <a name="latvia"></a>Lettland

### <a name="format"></a>Format

Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:
  
- Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)
    
- Sieben Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_latvia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_latvia_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_latvia_eu_passport_number**|
|:-----|
|Passnummer  <br/> Lettische Passnummer  <br/> Passport-Nr.  <br/> Pase numurs  <br/> |
   
## <a name="lithuania"></a>Litauen

### <a name="format"></a>Format

Acht Ziffern oder Buchstaben ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Acht Ziffern oder Buchstaben (Groß-/Kleinschreibung nicht beachtet)
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_lithuania_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_lithuania_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_lithuania_eu_passport_number**|
|:-----|
|Passnummer  <br/> lithunian-Passport-Nummer  <br/> Passport-Nr.  <br/> Paso Numeris  <br/> |
   
## <a name="luxemburg"></a>Luxemburg

### <a name="format"></a>Format

Acht Ziffern oder Buchstaben ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Acht Ziffern oder Buchstaben (Groß-/Kleinschreibung nicht beachtet)
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_nation_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_nation_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_nation_eu_passport_number**|
|:-----|
|Passnummer  <br/> Lettische Passnummer  <br/> Passport-Nr.  <br/> Passnummer  <br/> |
   
## <a name="malta"></a>Malta

### <a name="format"></a>Format

Sieben Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

 Sieben Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_malta_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_malta_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_malta_eu_passport_number**|
|:-----|
|Passnummer  <br/> Maltesische Passnummer  <br/> Passport-Nr.  <br/> numru Tal-Passaport  <br/> |
   
## <a name="netherlands"></a>Niederlande

### <a name="format"></a>Format

Neun Buchstaben oder Ziffern ohne Leerzeichen oder Abgrenzungen
  
### <a name="pattern"></a>Muster

Neun Buchstaben oder Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_netherlands_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_netherlands_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_netherlands_eu_passport_number**|
|:-----|
|niederländische Passnummer  <br/> Passnummer  <br/> niederländische Passnummer  <br/> Nederlanden paspoort Nummer  <br/> paspoort  <br/> Nederlanden paspoortnummer  <br/> paspoortnummer  <br/> |
   
## <a name="poland"></a>Polen

Weitere Informationen finden Sie im Abschnitt "polnische Passnummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Portugal

### <a name="format"></a>Format

Ein Buchstaben, gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Ein Buchstabe gefolgt von sechs Ziffern:
  
- Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)
    
- Sechs Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_portugal_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_portugal_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_portugal_eu_passport_number**|
|:-----|
|Passnummer  <br/> portugiesische Passnummer  <br/> Passport-Nr.  <br/> número do passaporte  <br/> |
   
## <a name="romania"></a>Rumänien

### <a name="format"></a>Format

Acht oder neun Ziffern ohne Leerzeichen und Abgrenzungen
  
### <a name="pattern"></a>Muster

Acht oder neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_romania_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_romania_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_romania_eu_passport_number**|
|:-----|
|Passnummer  <br/> rumänische Passnummer  <br/> Passport-Nr.  <br/> numărul pașaportului  <br/> |
   
## <a name="slovakia"></a>Slowakei

### <a name="format"></a>Format

Eine Ziffer oder ein Buchstaben, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Eine Ziffer oder ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung), gefolgt von sieben Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_slovakia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_slovakia_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_slovakia_eu_passport_number**|
|:-----|
|Passnummer  <br/> Slowakische Passnummer  <br/> Passport-Nr.  <br/> číslo Pasu  <br/> |
   
## <a name="slovenia"></a>Slowenien

### <a name="format"></a>Format

Zwei Buchstaben, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben, gefolgt von sieben Ziffern:
  
- Der Buchstabe "P"
    
- Ein Großbuchstabe
    
- Sieben Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_slovenia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_slovenia_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_slovenia_eu_passport_number**|
|:-----|
|Passnummer  <br/> slowenische Passnummer  <br/> Passport-Nr.  <br/> številka potnega lista  <br/> |
   
## <a name="spain"></a>Spanien

### <a name="format"></a>Format

Eine acht-oder neunstellige Kombination aus Buchstaben und Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Eine Kombination aus Buchstaben und Zahlen mit acht oder neun Zeichen:
  
-  Zwei Ziffern oder Buchstaben 
    
- Eine Ziffer oder ein Buchstabe (optional)
    
- Sechs Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_spain_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen. 
    
- Ein Schlüsselwort `Keywords_spain_eu_passport_number` aus wurde gefunden. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Schlüsselwörter

| |
|**Keywords_spain_eu_passport_number**|
|:-----|
|passport  <br/> Spanien Passport  <br/> Passport-Buch  <br/> Passnummer  <br/> Passport-Nr.  <br/> Libreta Pasaporte  <br/> número Pasaporte  <br/> ESPAÑA PASAPORTE  <br/> Pasaporte  <br/> |
   
## <a name="sweden"></a>Schweden

Weitere Informationen finden Sie im Abschnitt "schwedische Passport-Nummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="uk"></a>UK

Weitere Informationen finden Sie im Abschnitt "U.S./UK Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Siehe auch

[Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)

