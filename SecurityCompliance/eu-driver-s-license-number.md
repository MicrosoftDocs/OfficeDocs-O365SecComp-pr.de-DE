---
title: EU Führerscheinnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: In diesem Thema wird eine Data Loss Prevention (DLP) Richtlinie sieht für Wenn vertrauliche Informationen vom Typ der EU-Treiber Lizenz Zahl erkannt. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 065684249f9766d567c63e6b8170d36f56692e45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529414"
---
# <a name="eu-drivers-license-number"></a>EU Führerscheinnummer

In diesem Thema wird eine Data Loss Prevention (DLP) Richtlinie sieht für Wenn vertrauliche Informationen vom Typ der EU-Treiber Lizenz Zahl erkannt. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
  
## <a name="austria"></a>Österreich

### <a name="format"></a>Format

Acht Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Acht Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_austria_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_austria_eu_driver's_license_number` gefunden wird. 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_austria_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> des Treibers-Lizenz  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/>  Führerscheinnummer ein  <br/> Dlno #  <br/> fuhrerschein  <br/> Fuhrerschein Republik osterreich  <br/> |
   
## <a name="belgium"></a>Belgien

### <a name="format"></a>Format

10 Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

10 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_belgium_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_belgium_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords__belgium_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Dlno #  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> Führerscheinnummer  <br/> fuhrerscheinnummer  <br/> fuehrerscheinnummer  <br/> Führerschein-Nr.  <br/> Fuehrerschein-Nr.  <br/> Fuehrerschein-Nr.  <br/> |
   
## <a name="bulgaria"></a>Bulgarien

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_bulgaria_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_bulgaria_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_bulgaria_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МПС  <br/> СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МОТОРНО ПРЕВОЗНО СРЕДСТВО  <br/> СУМПС  <br/> ШОФЬОРСКА КНИЖКА  <br/> |
   
## <a name="croatia"></a>Kroatien

### <a name="format"></a>Format

Acht Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Acht Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_croatia_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_croatia_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_croatia_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Vozačka dozvola  <br/> |
   
## <a name="cyprus"></a>Zypern

### <a name="format"></a>Format

12 Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

12 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_cyprus_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_cyprus_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_cyprus_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> ΆΔΕΙΑ ΟΔΉΓΗΣΗΣ  <br/> |
   
## <a name="czech-republic"></a>Tschechische Republik

### <a name="format"></a>Format

Zwei Buchstaben gefolgt von sechs Ziffern
  
### <a name="pattern"></a>Muster

Acht Buchstaben und Ziffern:
  
- Zwei Buchstaben (nicht Groß-/Kleinschreibung)
    
- Ein Leerzeichen (optional) 
    
- Sechs Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_czech_republic_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_czech_republic_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_czech_republic_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Řidičský prúkaz  <br/> |
   
## <a name="denmark"></a>Dänemark

### <a name="format"></a>Format

Acht Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Acht Ziffern
  
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_denmark_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_denmark_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_denmark_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> kørekort  <br/> kørekortnummer  <br/> |
   
## <a name="estonia"></a>Estland

### <a name="format"></a>Format

Zwei Buchstaben gefolgt von sechs Ziffern
  
### <a name="pattern"></a>Muster

Zwei Buchstaben und sechs Ziffern:
  
-  Die Buchstaben "ET" (nicht Groß-/Kleinschreibung) 
    
- Sechs Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_estonia_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_estonia_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_estonia_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> 
permis de conduire  <br/> |
   
## <a name="finland"></a>Finnland

### <a name="format"></a>Format

10 Ziffern, die einen Bindestrich enthalten
  
### <a name="pattern"></a>Muster

10 Ziffern, die einen Bindestrich enthält:
  
-  Sechs Ziffern 
    
- Ein Bindestrich
    
-  Vier Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_finland_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_finland_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_finland_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> ajokortti  <br/> |
   
## <a name="france"></a>Frankreich

Weitere Informationen hierzu finden Sie im Abschnitt "Französische Führerscheinnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Deutschland

Weitere Informationen hierzu finden Sie im Abschnitt "Deutsche Führerscheinnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Griechenland

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

 Neun Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_greece_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_greece_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_greece_eu_driver'S_license_number**|
|:-----|
|DlL-  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> ΔΕΙΑ ΟΔΉΓΗΣΗΣ  <br/> Adeia odigisis  <br/> |
   
## <a name="hungary"></a>Ungarn

### <a name="format"></a>Format

Zwei Buchstaben gefolgt von sechs Ziffern
  
### <a name="pattern"></a>Muster

Zwei Buchstaben und sechs Ziffern:
  
-  Zwei Buchstaben (nicht Groß-/Kleinschreibung) 
    
- Sechs Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_hungary_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_hungary_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_hungary_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Vezetoi engedely  <br/> |
   
## <a name="ireland"></a>Irland

### <a name="format"></a>Format

Sechs Ziffern, gefolgt von vier Buchstaben
  
### <a name="pattern"></a>Muster

Sechs Ziffern und vier Buchstaben:
  
- Sechs Ziffern
    
- Vier Buchstaben (nicht Groß-/Kleinschreibung)
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_ireland_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_ireland_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_ireland_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Ceadúnas tiomána  <br/> |
   
## <a name="italy"></a>Italien

Weitere Informationen hierzu finden Sie im Abschnitt "Italien Führerscheinnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="latvia"></a>Lettland

### <a name="format"></a>Format

Drei Buchstaben, gefolgt von sechs Ziffern
  
### <a name="pattern"></a>Muster

Drei Buchstaben und sechs Ziffern:
  
-  Drei Buchstaben (nicht Groß-/Kleinschreibung) 
    
- Sechs Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_latvia_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_latvia_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_latvia_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Autovadītāja apliecība  <br/> |
   
## <a name="lithuania"></a>Litauen

### <a name="format"></a>Format

Acht Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

 Acht Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_lithuania_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_lithuania_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_lithuania_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Vairuotojo pažymėjimas  <br/> |
   
## <a name="luxemburg"></a>Luxemburg

### <a name="format"></a>Format

Sechs Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

 Sechs Ziffern 
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_luxemburg_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_luxemburg_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_luxemburg_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Fahrerlaubnis  <br/> |
   
## <a name="malta"></a>Malta

### <a name="format"></a>Format

Kombination von zwei Zeichen und sechs Ziffern in dem angegebenen Muster
  
### <a name="pattern"></a>Muster

Kombination von zwei Zeichen und sechs Ziffern:
  
- Zwei Zeichen (Ziffern oder Buchstaben, nicht die Groß-/Kleinschreibung beachtet)
    
- Ein Leerzeichen (optional) 
    
- Drei Ziffern
    
- Ein Leerzeichen (optional) 
    
- Drei Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_malta_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_malta_eu_driver's_license_number` gefunden wird. 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_malta_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Liċenzja Aufgaben-sewqan  <br/> |
   
## <a name="netherlands"></a>Niederlande

### <a name="format"></a>Format

10 Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

10 Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_netherlands_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_netherlands_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_netherlands_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> 
permis de conduire  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> |
   
## <a name="poland"></a>Polen

### <a name="format"></a>Format

14 Stellen mit 2 Schrägstriche
  
### <a name="pattern"></a>Muster

14 Ziffern und 2 Schrägstriche:
  
-  Fünf Ziffern 
    
- Ein Schrägstrich 
    
- Zwei Ziffern
    
- Ein Schrägstrich 
    
- Sieben Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_poland_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_poland_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_poland_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Prawo jazdy  <br/> |
   
## <a name="portugal"></a>Portugal

### <a name="format"></a>Format

Zwei Buchstaben gefolgt von einem sieben Zahlen in dem angegebenen Muster
  
### <a name="pattern"></a>Muster

Zwei Buchstaben gefolgt von sieben Ziffern mit Sonderzeichen:
  
-  Zwei Buchstaben (nicht Groß-/Kleinschreibung) 
    
- Ein Bindestrich 
    
- Sechs Ziffern
    
- Ein Leerzeichen
    
- Eine Ziffer
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_portugal_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_portugal_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_portugal_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Carteira de motorista  <br/> |
   
## <a name="romania"></a>Rumänien

### <a name="format"></a>Format

Ein Zeichen, gefolgt von acht Ziffern
  
### <a name="pattern"></a>Muster

Ein Zeichen, gefolgt von acht Stellen:
  
-  Eine (nicht Groß-/Kleinschreibung) Buchstabe oder Zahl 
    
- Acht Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_romania_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_romania_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_romania_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Permis de conducere  <br/> |
   
## <a name="slovakia"></a>Slowakei

### <a name="format"></a>Format

Ein Zeichen, gefolgt von sieben Ziffern
  
### <a name="pattern"></a>Muster

Ein Zeichen, gefolgt von sieben Ziffern
  
- Eine (nicht Groß-/Kleinschreibung) Buchstabe oder Zahl
    
-  Sieben Ziffern 
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_slovakia_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_slovakia_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_slovakia_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Vodičský preukaz  <br/> |
   
## <a name="slovenia"></a>Slowenien

### <a name="format"></a>Format

Neun Ziffern ohne Leerzeichen und Trennzeichen
  
### <a name="pattern"></a>Muster

Neun Ziffern
  
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_slovenia_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_slovenia_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_slovenia_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> Vozniško dovoljenje  <br/> |
   
## <a name="spain"></a>Spanien

### <a name="format"></a>Format

Acht Ziffern, gefolgt von einem Zeichen
  
### <a name="pattern"></a>Muster

Acht Ziffern, gefolgt von einem Zeichen:
  
-  Acht Ziffern 
    
- Eine Ziffern oder Buchstaben (nicht Groß-/Kleinschreibung)
    
### <a name="checksum"></a>Prüfsumme

Ja
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Die Funktion `Func_spain_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_spain_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_spain_eu_driver'S_license_number**|
|:-----|
|Dlno #  <br/> dl#  <br/> Treiber Lic.  <br/> Treiber-Lizenz  <br/> driver license  <br/> drivers licence  <br/> drivers license  <br/> des Treibers-Lizenz  <br/> driver's license  <br/> driving licence
  <br/> gesteuerte Lizenz  <br/> Anzahl der Treiber-Lizenz  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber Lizenz Anzahl  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer  <br/> Anzahl der lenken-Lizenz  <br/> Führerscheinnummer ein  <br/> gesteuerter zulassen  <br/> Anzahl der steuernde zulassen  <br/> Permiso de conducción  <br/> Permiso conducción  <br/> Número Licencia conducir  <br/> Número de Carnet de conducir  <br/> Número Carnet conducir  <br/> Licencia conducir  <br/> Número de Permiso de conducir  <br/> Número de Permiso conducir  <br/> Número Permiso conducir  <br/> Permiso conducir  <br/> Licencia de sein  <br/> El Carnet de conducir  <br/> Carnet conducir  <br/> |
   
## <a name="sweden"></a>Schweden

### <a name="format"></a>Format

Zehn Ziffern, die einen Bindestrich enthält
  
### <a name="pattern"></a>Muster

Zehn Ziffern, die einen Bindestrich enthält:
  
-  Sechs Ziffern 
    
- Ein Bindestrich
    
- Vier Ziffern
    
### <a name="checksum"></a>Prüfsumme

Nein
  
### <a name="definition"></a>Definition

Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:
  
- Der reguläre Ausdruck `Regex_sweden_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht. 
    
- Ein Schlüsselwort aus `Keywords_sweden_eu_driver's_license_number` gefunden wird. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_sweden_eu_driver'S_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> Anzahl der Treiber-Lizenz  <br/> Treiber-Lizenz  <br/> Treiber Lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> Führerscheinnummer  <br/> Lizenznummer  <br/> Führerscheinnummer ein  <br/> Dlno #  <br/> körkort  <br/> |
   
## <a name="uk"></a>GROßBRITANNIEN

Weitere Informationen hierzu finden Sie im Abschnitt "Großbritannien Führerscheinnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>Siehe auch

[Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)

