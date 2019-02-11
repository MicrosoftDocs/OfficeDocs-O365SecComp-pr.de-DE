---
title: EU Reisepassnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: In diesem Thema dargestellt was eine Data Loss Prevention (DLP)-Richtlinie für den Typ der EU Reisepassnummer vertrauliche Daten erkannt. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 7a7fc1ff826aab4096c46535686eb0fd68173c6f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "25840324"
---
# <a name="eu-passport-number"></a>EU Reisepassnummer

In diesem Thema dargestellt was eine Data Loss Prevention (DLP)-Richtlinie für den Typ der EU Reisepassnummer vertrauliche Daten erkannt. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
  
## <a name="austria"></a>Österreich

### <a name="format"></a>Format

Einen Buchstaben gefolgt von einem optionalen Leerzeichen und sieben Ziffern
  
### <a name="pattern"></a>Muster

Eine Kombination von einem Buchstaben, sieben Ziffern und ein Leerzeichen:
  
- Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)
    
- Ein Leerzeichen (optional)
    
- Sieben Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_austria_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_austria_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> österreichische Reisepassnummer  <br/> Passport keine  <br/> Reisepass  <br/> Österreichisch reisepass  <br/> |
   
## <a name="belgium"></a>Belgien

### <a name="format"></a>Format

Zwei Buchstaben gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben und gefolgt von sechs Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_belgium_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_belgium_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> belgische Reisepassnummer  <br/> Passport keine  <br/> paspoort  <br/> paspoortnummer  <br/> Kein Reisepass  <br/> Reisepass  <br/> |
   
## <a name="bulgaria"></a>Bulgarien

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

 Neun Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_bulgaria_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_bulgaria_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Bulgarisch Reisepassnummer  <br/> Passport keine  <br/> НОМЕР НА ПАСПОРТА  <br/> |
   
## <a name="croatia"></a>Kroatien

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

 Neun Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_croatia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_croatia_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Kroatisch Reisepassnummer  <br/> Passport keine  <br/> Broj putovnice  <br/> |
   
## <a name="cyprus"></a>Zypern

### <a name="format"></a>Format

Einen Buchstaben gefolgt von 6 bis 8 Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Ein Zeichen, gefolgt von sechs bis acht Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_cyprus_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_cyprus_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Zypern Reisepassnummer  <br/> Passport keine  <br/> ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ  <br/> |
   
## <a name="czech-republic"></a>Tschechien

### <a name="format"></a>Format

Acht Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Acht Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_czech_republic_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_czech_republic_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Tschechische Reisepassnummer  <br/> Passport keine  <br/> Cestovní pas  <br/> PAS  <br/> |
   
## <a name="denmark"></a>Dänemark

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

 Neun Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_denmark_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_denmark_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Dänische Reisepassnummer  <br/> Passport keine  <br/> PAS  <br/> pasnummer  <br/> |
   
## <a name="estonia"></a>Estland

### <a name="format"></a>Format

Einen Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Einen Buchstaben gefolgt von sieben Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_estonia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_estonia_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Estnisch Reisepassnummer  <br/> Passport keine  <br/> übergeben Sie Eesti kodaniku  <br/> |
   
## <a name="finland"></a>Finnland

Weitere Informationen hierzu finden Sie im Abschnitt "Finnland Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>Frankreich

Weitere Informationen hierzu finden Sie im Abschnitt "Französische Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Deutschland

Weitere Informationen hierzu finden Sie im Abschnitt "Deutschland Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Griechenland

### <a name="format"></a>Format

Zwei Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben gefolgt von sieben Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_greece_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_greece_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Griechische Reisepassnummer  <br/> Passport keine  <br/> ΔΙΑΒΑΤΗΡΙΟ  <br/> |
   
## <a name="hungary"></a>Ungarn

### <a name="format"></a>Format

Zwei Buchstaben gefolgt von sechs oder sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben gefolgt von sechs oder sieben Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_hungary_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_hungary_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Ungarisch Reisepassnummer  <br/> Passport keine  <br/> Útlevél száma  <br/> |
   
## <a name="ireland"></a>Irland

### <a name="format"></a>Format

Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:
  
- Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)
    
- Sieben Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_ireland_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_ireland_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Irland Reisepassnummer  <br/> Passport keine  <br/> PAS  <br/> passport  <br/> passeport  <br/> Passeport numero  <br/> |
   
## <a name="italy"></a>Italien

### <a name="format"></a>Format

Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:
  
- Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)
    
- Sieben Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_italy_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_italy_eu_passport_number` gefunden wird. 
    
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
|Italienische Reisepassnummer  <br/> Repubblica Italiana passaporto  <br/> passaporto  <br/> Passaporto italiana  <br/> Reisepassnummer  <br/> Italiana Passaporto numero  <br/> Passaporto numero  <br/> Numéro Passeport italien  <br/> Numéro passeport  <br/> |
   
## <a name="latvia"></a>Lettland

### <a name="format"></a>Format

Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:
  
- Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)
    
- Sieben Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_latvia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_latvia_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Lettisch Reisepassnummer  <br/> Passport keine  <br/> Pase numurs  <br/> |
   
## <a name="lithuania"></a>Litauen

### <a name="format"></a>Format

Acht Ziffern oder Buchstaben ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Acht Ziffern oder Buchstaben (ohne Beachtung von Groß-/Kleinschreibung)
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_lithuania_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_lithuania_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Lithunian Reisepassnummer  <br/> Passport keine  <br/> Paso numeris  <br/> |
   
## <a name="luxemburg"></a>Luxemburg

### <a name="format"></a>Format

Acht Ziffern oder Buchstaben ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Acht Ziffern oder Buchstaben (ohne Beachtung von Groß-/Kleinschreibung)
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_nation_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_nation_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Lettisch Reisepassnummer  <br/> Passport keine  <br/> Passnummer  <br/> |
   
## <a name="malta"></a>Malta

### <a name="format"></a>Format

Sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

 Sieben Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_malta_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_malta_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Maltesisch Reisepassnummer  <br/> Passport keine  <br/> Numru Tal-passaport  <br/> |
   
## <a name="netherlands"></a>Niederlande

### <a name="format"></a>Format

Neun Buchstaben oder Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Neun Buchstaben oder Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_netherlands_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_netherlands_eu_passport_number` gefunden wird. 
    
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
|Niederländische Reisepassnummer  <br/> Reisepassnummer  <br/> Niederlande Reisepassnummer  <br/> Nederlanden Paspoort nummer  <br/> paspoort  <br/> Nederlanden paspoortnummer  <br/> paspoortnummer  <br/> |
   
## <a name="poland"></a>Polen

Weitere Informationen hierzu finden Sie im Abschnitt "Polen Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Portugal

### <a name="format"></a>Format

Ein Zeichen, gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Einen Buchstaben gefolgt von sechs Ziffern:
  
- Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)
    
- Sechs Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_portugal_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_portugal_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Portugiesisch Reisepassnummer  <br/> Passport keine  <br/> Número passaporte  <br/> |
   
## <a name="romania"></a>Rumänien

### <a name="format"></a>Format

Acht oder neun Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Acht oder neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_romania_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_romania_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Rumänisch Reisepassnummer  <br/> Passport keine  <br/> Numărul pașaportului  <br/> |
   
## <a name="slovakia"></a>Slowakei

### <a name="format"></a>Format

Eine Ziffern oder Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Eine Ziffern oder Buchstaben (ohne Beachtung von Groß-/Kleinschreibung) gefolgt von sieben Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_slovakia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_slovakia_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Slowakische Reisepassnummer  <br/> Passport keine  <br/> Číslo pasu  <br/> |
   
## <a name="slovenia"></a>Slowenien

### <a name="format"></a>Format

Zwei Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Zwei Buchstaben gefolgt von sieben Ziffern:
  
- Der Buchstabe "P"
    
- Einen Großbuchstaben
    
- Sieben Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_slovenia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_slovenia_eu_passport_number` gefunden wird. 
    
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
|Reisepassnummer  <br/> Slowenisch Reisepassnummer  <br/> Passport keine  <br/> Številka Potnega lista  <br/> |
   
## <a name="spain"></a>Spanien

### <a name="format"></a>Format

Eine acht oder neun Zeichen Kombination von Buchstaben und Zahlen ohne Leerzeichen oder Trennzeichen
  
### <a name="pattern"></a>Muster

Eine Kombination der acht oder neun Zeichen Buchstaben und Zahlen:
  
-  Zwei Ziffern oder Buchstaben 
    
- Eine Ziffern oder Buchstaben (optional)
    
- Sechs Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nicht zutreffend
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_spain_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_spain_eu_passport_number` gefunden wird. 
    
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
|passport  <br/> Spanien passport  <br/> Passport-Adressbuch  <br/> Reisepassnummer  <br/> Passport keine  <br/> Libreta pasaporte  <br/> Número pasaporte  <br/> España pasaporte  <br/> pasaporte  <br/> |
   
## <a name="sweden"></a>Schweden

Weitere Informationen hierzu finden Sie im Abschnitt "Schwedische Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="uk"></a>GROßBRITANNIEN

Weitere Informationen hierzu finden Sie im Abschnitt "US / Großbritannien Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Siehe auch

[Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)

